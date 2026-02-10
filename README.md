# Pluvel Documentation

This repository contains the documentation for [Pluvel](https://pluvel.com) — the all-in-one platform for forming, running, and managing your business.

**Live docs:** [docs.pluvel.com](https://docs.pluvel.com)

## Development

### Prerequisites

- Node.js 18+
- npm or yarn

### Local preview

```bash
# Install Mintlify CLI
npm install -g mintlify

# Start local development server
npx mintlify dev
```

Open [http://localhost:3000](http://localhost:3000) to view the docs.

### Project structure

```
├── mint.json              # Mintlify configuration
├── styles.css             # Custom CSS
├── introduction.mdx       # Home page
├── guides/                # How-to guides
│   ├── getting-started/   # Onboarding guides
│   ├── formation/         # Business formation
│   ├── money/             # Banking and transactions
│   ├── payroll/           # Payroll guides
│   └── taxes/             # Tax and reporting
├── features/              # Feature documentation
│   ├── company/           # Company management
│   ├── formation/         # Formation features
│   ├── banking/           # Banking features
│   ├── invoicing/         # Invoicing features
│   ├── payroll/           # Payroll features
│   └── ...
├── integrations/          # Integration docs
├── accountants/           # Firm Mode docs
├── changelog/             # Release notes
├── images/                # Screenshots and assets
└── logo/                  # Pluvel logos
```

### Writing guidelines

- Use direct, active voice
- Second person ("you" not "users")
- Be specific with numbers and examples
- Keep sentences and paragraphs short
- Be honest about limitations

**Avoid:**
- "Dive into" / "Unlock" / "Leverage"
- "Seamlessly" / "Robust" / "Cutting-edge"
- Starting with "So," or "Well,"
- Ending with "Happy [doing thing]!"

## Contributing

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/improve-payroll-docs`)
3. Make your changes
4. Test locally with `npx mintlify dev`
5. Submit a pull request

For major changes, open an issue first to discuss what you'd like to change.

## Deployment

Docs are automatically deployed when changes are pushed to the `main` branch. Mintlify handles the build and deployment.

## License

MIT License - see [LICENSE](LICENSE) for details.

## Support

- **Documentation issues:** Open an issue in this repository
- **Pluvel product support:** [support@pluvel.com](mailto:support@pluvel.com)
- **General questions:** [pluvel.com](https://pluvel.com)
