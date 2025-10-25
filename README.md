# Professor AI - Assets Repository

This repository contains all downloadable assets for the Professor AI application, including question databases, AI models, images, and resources.

## Asset Types

- **Questions**: ENEM, FUVEST, OAB question databases
- **AI Models**: Quantized Gemma 3 4B model for offline inference
- **Images**: Question illustrations and diagrams
- **Resources**: Study materials and PDFs
- **Fonts**: Custom typography
- **Translations**: Language packs (PT-BR, EN)

## Download

All assets are available as GitHub Releases. Download the latest assets from the [Releases](../../releases) page.

### Direct Download Links

Assets are automatically built and released. Use these direct links in the Professor AI app:

```
https://github.com/mouracleiton/professor-ai-assets/releases/download/{release-tag}/{asset-name}
```

## Asset Management

This repository is automatically updated with new assets through GitHub Actions. Assets are compressed and hosted as GitHub Releases for easy distribution.

## Checksum Verification

Each asset release includes a `checksums.sha256` file for integrity verification. Always verify downloads:

```bash
sha256sum -c checksums.sha256
```

## Usage in Professor AI

The Professor AI app automatically downloads these assets on first run. Users can manage assets through the Assets Download screen.

## Directory Structure

```
assets/
├── questions/         # Question databases (CSV, JSON)
├── models/           # TFLite and ML models
├── images/           # Question illustrations
├── resources/        # PDFs and study materials
├── fonts/            # Custom font files
└── translations/     # Language packs (JSON, ARB)
```

## Development

For development or custom asset creation:

1. Prepare your assets in the appropriate folder
2. Create a pull request with your changes
3. Assets will be automatically compressed and released

## License

Assets are part of the Professor AI project and follow the same license terms.
