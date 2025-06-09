# VS Code Development Guide

This guide helps you get the most out of the Angular Example App development environment in VS Code.

## Quick Start Checklist

- [ ] Install recommended extensions when prompted
- [ ] Run `npm install` to install dependencies
- [ ] Use `Ctrl+Shift+P` → "Tasks: Run Task" → "ng-serve" to start development server
- [ ] Press `F5` to start debugging

## Development Workflow

### 1. Starting Development

```bash
# Method 1: Using VS Code tasks (recommended)
Ctrl+Shift+P → Tasks: Run Task → ng-serve

# Method 2: Using terminal
npm start
```

### 2. Running Tests

```bash
# Method 1: Using VS Code tasks
Ctrl+Shift+P → Tasks: Run Task → ng-test

# Method 2: Using terminal  
npm test
```

### 3. Linting and Formatting

The project is configured to:
- Auto-format on save (Prettier)
- Auto-fix ESLint issues on save
- Auto-fix Stylelint issues on save
- Organize imports on save

### 4. Debugging

1. Start the development server (Task: ng-serve)
2. Set breakpoints in your TypeScript files
3. Press `F5` or use Run and Debug panel
4. Select "Launch Chrome (Development)"

## File Structure

```
src/
├── app/
│   ├── modules/          # Feature modules
│   │   ├── auth/         # Authentication module
│   │   ├── shared/       # Shared components
│   │   └── user/         # User management module
│   ├── styles/           # Global styles (SCSS)
│   └── environments/     # Environment configurations
├── assets/               # Static assets
└── locale/              # i18n translation files
```

## Available Scripts

| Script | Description |
|--------|-------------|
| `npm start` | Start development server (English) |
| `npm run start:es` | Start development server (Spanish) |
| `npm run build` | Build for production |
| `npm test` | Run unit tests |
| `npm run test:watch` | Run tests in watch mode |
| `npm run lint` | Run linting |
| `npm run e2e` | Run end-to-end tests |
| `npm run extract` | Extract i18n messages |

## Code Generation

Use Angular CLI to generate new components:

```bash
# Method 1: Using VS Code tasks
Ctrl+Shift+P → Tasks: Run Task → ng-generate-component

# Method 2: Using terminal
npx ng generate component modules/shared/components/my-component
npx ng generate service modules/shared/services/my-service
```

## Architecture Notes

- **Angular 17** with standalone components
- **ESBuild** for fast builds
- **i18n support** (English/Spanish)
- **Apollo GraphQL** for API communication
- **Elf** for state management
- **Bootstrap 5** for styling
- **SCSS** with custom variables
- **Karma/Jasmine** for unit testing
- **Playwright** for e2e testing

## Troubleshooting

### Common Issues

1. **Development server won't start**
   - Check if port 4200 is available
   - Run `npm install` to ensure dependencies are installed

2. **Linting errors**
   - Many errors are auto-fixable on save
   - Run `npm run lint` to see all issues

3. **Build failures**
   - Check network connectivity for external resources (Google Fonts)
   - Review console output for specific errors

### Getting Help

- Check the project's README.md for general setup instructions
- Review Angular documentation: https://angular.io/docs
- Check the issue tracker for known problems

## Tips for Productivity

1. **Use snippets**: Type `ng-` for Angular-specific snippets
2. **IntelliSense**: Leverage TypeScript auto-completion
3. **File navigation**: Use `Ctrl+P` to quickly open files
4. **Symbol search**: Use `Ctrl+Shift+O` to navigate to symbols
5. **Multi-cursor editing**: Use `Ctrl+D` to select multiple occurrences
6. **Integrated terminal**: Use `Ctrl+`` to open terminal