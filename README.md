# Flaticon Quick Search - Chrome Extension

A Chrome extension that lets you search Flaticon icons instantly from any website with a beautiful popup interface.

## Features

- 🔍 **Instant Search**: Search thousands of Flaticon icons without leaving your current page
- 🎨 **Beautiful UI**: Modern, responsive design with smooth animations
- ⚡ **Fast Performance**: Debounced search with smart caching
- 📱 **Keyboard Support**: Full keyboard navigation support
- ⌨️ **Quick Access**: Open search with Ctrl+Shift+I (Cmd+Shift+I on Mac)
- 🔄 **Fallback Options**: Multiple API endpoints and graceful error handling
- 📋 **Copy Support**: Right-click to copy image URLs
- 🌐 **Direct Links**: Click icons to open them on Flaticon

## Setup Instructions

### 1. Add Extension Icons

You need to add icon files for the extension. Create PNG files with these exact names and sizes:

- `icon16.png` (16x16 pixels)
- `icon32.png` (32x32 pixels)  
- `icon48.png` (48x48 pixels)
- `icon128.png` (128x128 pixels)

**Recommended**: Use a simple, recognizable icon related to search or icons (like a magnifying glass with a small icon symbol).

### 2. Install the Extension

1. Open Chrome and go to `chrome://extensions/`
2. Enable "Developer mode" (toggle in top-right corner)
3. Click "Load unpacked"
4. Select the folder containing these extension files
5. The extension should appear in your extensions list

### 3. Using the Extension

1. Click the extension icon in your Chrome toolbar
2. Type your search query in the search bar
3. Browse through the icon results with the scrollbar
4. Click any icon to open it on Flaticon
5. Right-click any icon to copy its image URL
6. Press Enter in the search bar to open Flaticon search

### 4. Keyboard Shortcuts

**Quick Access Shortcut:**
- **Windows/Linux**: `Ctrl+Shift+I`
- **Mac**: `Cmd+Shift+I`

This will instantly open the search popup and automatically focus on the search input, allowing you to start typing immediately.

**Customizing the Shortcut:**
1. Go to `chrome://extensions/shortcuts` in your browser
2. Find "Flaticon Quick Search" in the list
3. Click in the shortcut field and press your preferred key combination
4. The new shortcut will be saved automatically

## Technical Details

### Files Structure

```
Flaticon extension/
├── manifest.json       # Extension configuration
├── popup.html         # Popup interface
├── popup.css          # Styling
├── popup.js           # Main functionality
├── README.md          # This file
└── icons/             # Extension icons (you need to add these)
    ├── icon16.png
    ├── icon32.png
    ├── icon48.png
    └── icon128.png
```

### API Approach

The extension tries multiple methods to fetch icons:

1. **Primary**: Official/unofficial Flaticon API endpoints
2. **Fallback**: Web scraping of search results
3. **Ultimate Fallback**: Direct link to Flaticon search

### Privacy & Usage

- The extension only accesses Flaticon.com
- No data is stored or transmitted to third parties
- Respects Flaticon's terms of service
- For personal/educational use only

## Troubleshooting

### Extension Won't Load
- Make sure all files are in the same folder
- Check that manifest.json is valid JSON
- Add the required icon files

### Search Not Working
- Check your internet connection
- Try different search terms
- Use the "search on Flaticon" fallback option

### No Icons Displayed
- Flaticon may have changed their API
- The extension will fallback to opening Flaticon directly
- Clear your browser cache and try again

## Customization

### Modify Search Behavior
Edit `popup.js` to:
- Change the number of results (`MAX_RESULTS`)
- Adjust search delay (`SEARCH_DELAY`)
- Add new API endpoints

### Styling Changes
Edit `popup.css` to:
- Change colors and themes
- Modify popup size
- Adjust grid layout

## Limitations

- Uses unofficial Flaticon APIs that may change
- Limited to free icons (premium icons require authentication)
- No offline functionality
- Search quality depends on Flaticon's API

## Development

To enhance this extension:

1. **Add Authentication**: Support for Flaticon premium accounts
2. **Local Storage**: Cache recent searches and favorites  
3. **Multiple Providers**: Add IconScout, Material Icons, etc.
4. **Better Parsing**: Improve icon extraction from different sources
5. **Download Support**: Direct icon download functionality

## License

This is a personal/educational project. Respect Flaticon's terms of service when using their icons and API.

## Disclaimer

This extension is not affiliated with or endorsed by Flaticon. It's a third-party tool for educational and personal use. The extension may stop working if Flaticon changes their API or terms of service.