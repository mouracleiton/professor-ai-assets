# Contributing to Professor AI Assets

Thank you for helping us build the Professor AI asset library!

## Overview

This repository contains downloadable assets for the Professor AI educational platform, including:
- Question databases (ENEM, FUVEST, OAB)
- AI models (Gemma 3 4B quantized)
- Question images and illustrations
- Study materials and PDFs
- Custom fonts
- Language packs

## Getting Started

### Prerequisites
- Git
- Basic understanding of the asset types
- GitHub account

### Fork and Clone
```bash
# Fork the repository on GitHub
# Then clone your fork
git clone https://github.com/YOUR_USERNAME/professor-ai-assets.git
cd professor-ai-assets
```

## Adding Assets

### 1. Question Databases

Questions should be in CSV or JSON format:

**CSV Format:**
```csv
id,exam_type,subject,difficulty,year,question_text,image_url,options,answer,explanation
1,ENEM,Mathematics,Easy,2023,"What is 2+2?","","A|B|C|D","A","Because 2+2 equals 4"
```

**JSON Format:**
```json
{
  "id": 1,
  "exam_type": "ENEM",
  "subject": "Mathematics",
  "difficulty": "Easy",
  "year": 2023,
  "question_text": "What is 2+2?",
  "image_url": "image_url_or_path",
  "options": ["A", "B", "C", "D"],
  "answer": "A",
  "explanation": "Because 2+2 equals 4"
}
```

**Location:** `assets/questions/{exam_type}/{subject}/`

### 2. AI Models

TensorFlow Lite models (.tflite files):
- Must be quantized to reduce size
- Should include metadata documentation
- Include checksum in metadata

**Location:** `assets/models/{model_name}/`

### 3. Images

PNG/JPG images for question illustrations:
- Optimize for mobile (max 1MB per image)
- Use descriptive names
- Include alt text in metadata

**Location:** `assets/images/{category}/`

### 4. Study Materials

PDFs and educational resources:
- Maximum 10MB per file
- Include description in README
- Ensure proper copyright/licensing

**Location:** `assets/resources/{subject}/`

### 5. Fonts

TrueType or OpenType font files:
- Include font family name
- Document supported scripts

**Location:** `assets/fonts/`

### 6. Translations

JSON or ARB format language files:
- Key-value pairs for strings
- Support for pluralization
- Include language code (pt_BR, en_US, etc.)

**Location:** `assets/translations/{language}/`

## Contribution Process

### Step 1: Create a Branch
```bash
git checkout -b feature/add-new-questions
```

### Step 2: Add Your Assets
```bash
# Copy files to appropriate directories
cp my_questions.csv assets/questions/ENEM/Mathematics/
```

### Step 3: Create Asset List
Update `assets/README.md` with:
- Asset name
- File size
- Description
- Date added

### Step 4: Commit Changes
```bash
git add .
git commit -m "Add ENEM mathematics questions 2023-2024"
```

### Step 5: Push and Create PR
```bash
git push origin feature/add-new-questions
```

Then create a Pull Request on GitHub.

## Quality Standards

### Before Submitting

- [ ] Files are in correct directories
- [ ] File names are descriptive
- [ ] No sensitive information included
- [ ] Files are optimized (images compressed, etc.)
- [ ] Checksums match for verification
- [ ] Documentation is complete

### Asset Requirements

**Questions:**
- [ ] Complete metadata (exam, subject, difficulty, year)
- [ ] Clear question text
- [ ] Correct answer marked
- [ ] Explanation provided
- [ ] References included if applicable

**Models:**
- [ ] Quantized (not full precision)
- [ ] Tested on target devices
- [ ] Documentation included
- [ ] Performance benchmarks

**Images:**
- [ ] Optimized for mobile
- [ ] Clear and readable
- [ ] Properly named
- [ ] License documented

## Review Process

1. **Automated Checks**
   - File size validation
   - Format checking
   - Duplicate detection

2. **Manual Review**
   - Content quality
   - Accuracy verification
   - Asset organization

3. **Approval**
   - Merges to main branch
   - Triggers automatic release
   - Assets available within 5 minutes

## Release Cycle

When your PR is merged:
1. GitHub Actions automatically packages assets
2. Creates a new release (v${RUN_NUMBER})
3. Generates SHA256 checksums
4. Makes files available for download

Users can then access new assets:
- Automatically in the app
- Manually from releases page

## Licensing

By contributing assets, you agree:
- Assets are original or properly licensed
- You have the right to distribute
- Assets follow the project license
- Copyright is properly attributed

## Questions?

- Check [README.md](README.md) for overview
- Review existing assets for examples
- Open an issue with questions
- Reach out to project maintainers

## Code of Conduct

- Be respectful and professional
- Provide constructive feedback
- Focus on asset quality
- Help other contributors

Thank you for contributing to Professor AI! 🎓

---

**Last Updated:** October 25, 2024
**Maintained by:** Professor AI Team
