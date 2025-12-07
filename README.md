# Package Dependency Version Checker

A lightweight, single-file web application for checking if your npm dependencies are up to date. Simply drag and drop your `package.json` file to see which packages have newer versions available.

## Features

- **Single File Application** - Everything contained in one `index.html` file
- **Drag & Drop Interface** - Easy file upload by dragging your `package.json`
- **Real-time Version Checking** - Fetches latest versions from npm registry via unpkg.com
- **Progress Tracking** - Visual progress bar shows checking status
- **Version Comparison** - Highlights outdated packages for easy identification
- **Local Storage** - Persists your data between sessions
- **Zero Dependencies** - Pure vanilla HTML/CSS/JavaScript, no frameworks required
- **Portable** - Works offline after initial load, no build step needed

## Usage

1. Open `index.html` in any modern web browser
2. Drag and drop your `package.json` file onto the drop zone (or click to browse)
3. Wait for the version check to complete
4. Review the tables showing:
   - Current versions from your package.json
   - Latest available versions from npm
   - Status indicators (up to date / outdated)
5. Click "Check for Updates" anytime to refresh the latest versions

## What Gets Checked

The app checks both:
- **dependencies** - Production dependencies
- **devDependencies** - Development dependencies

## How It Works

- Uses the [unpkg.com](https://unpkg.com) CDN API to fetch package information
- Compares semantic versions to determine if updates are available
- Stores results in browser localStorage for persistence
- Fetches all packages in parallel for fast performance

## Requirements

- Modern web browser with JavaScript enabled
- Internet connection (to fetch package versions)

## Security & Privacy

- All processing happens in your browser
- No data is sent to any server except npm package lookups
- No tracking or analytics
- Your package.json is never uploaded anywhere

## Browser Compatibility

Works in all modern browsers that support:
- ES6+ JavaScript (async/await, spread operator)
- FileReader API
- localStorage
- HTML5 `<progress>` element

## Use Cases

- Quick security audit of project dependencies
- Checking for updates before starting work
- Comparing multiple projects' dependency versions
- Educational tool for understanding semantic versioning

## Contributing

This is a single-file application by design for maximum portability. When contributing:
- Keep everything in `index.html`
- Use vanilla JavaScript (no frameworks)
- Maintain semantic HTML structure
- Avoid external dependencies

## License

MIT
