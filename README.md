# IMS Desktop App

A standalone desktop application that wraps the IMS web interface in an Electron app.

## Features

- Clean desktop interface for IMS system
- Native window controls and menus
- Secure web wrapper with external link handling
- Single executable distribution ready
- Cross-platform compatible

## Target URL

The app loads: `https://ug2002019.cse.pstu.ac.bd/ims-web/public/admin`

## Quick Start

### Running the Development Version
```bash
npm start
```

### Building the Desktop App
```bash
npm run package
```

This creates a complete desktop application in the `dist/IMS Desktop-win32-x64/` folder.

**The main executable is: `dist/IMS Desktop-win32-x64/IMS Desktop.exe`**

## Project Structure

```
ims-desktop-electron/
├── main.js          # Main Electron process
├── renderer.js      # Renderer process script
├── index.html       # Fallback loading page
├── package.json     # Project configuration
├── assets/          # Icons and images
│   ├── bookshop-logo.ico   # Application icon
│   ├── bookshop-logo.png   # PNG version of logo
│   ├── bookshop-logo.jpg   # JPG version of logo
│   └── bookshop-logo.svg   # SVG version of logo
├── dist/            # Built application
│   └── IMS Desktop-win32-x64/  # Packaged app folder
│       └── IMS Desktop.exe     # Main executable
└── node_modules/    # Dependencies
```

## How to Use

1. **Development**: Run `npm start` to test the app
2. **Build**: Run `npm run package` to create the desktop app
3. **Distribute**: Copy the entire `dist/IMS Desktop-win32-x64/` folder to share the app

## Application Features

- **Desktop Integration**: Native window with proper menu bar and custom bookshop logo
- **Security**: Context isolation enabled, external links open in browser
- **Auto-Navigation**: Direct loading of the IMS admin interface
- **Error Handling**: Graceful handling of network issues
- **Responsive**: Adapts to different window sizes
- **Custom Branding**: Uses bookshop logo as application icon and favicon

## Technical Details

- Built with Electron 28.x
- Packaged using electron-packager
- Windows 64-bit compatible
- No installation required (portable)

## Distribution

To distribute the app:
1. Copy the entire `dist/IMS Desktop-win32-x64/` folder
2. Users can run `IMS Desktop.exe` directly
3. No installation or admin rights required

## Requirements

**For Development:**
- Node.js 16 or higher
- npm

**For End Users:**
- Windows 10 or higher (64-bit)
- No additional software required

## Security Features

- Context isolation enabled
- Node integration disabled
- External links open in default browser
- Certificate validation for production use
- CSP headers for enhanced security

## Customization

You can modify the following in `main.js`:
- Window size and properties
- Application menu
- Target URL (change the TARGET_URL constant)
- Icon paths

### Logo Customization
The application uses the bookshop logo files located in the `assets/` directory:
- `bookshop-logo.ico` - Used as the main application icon
- `bookshop-logo.png` - Used as favicon and window icon
- Multiple formats available (SVG, JPG, PNG, ICO) for different use cases

To change the logo:
1. Replace the files in the `assets/` directory
2. Update the icon path in `main.js` if using a different filename
3. Rebuild with `npm run package`

