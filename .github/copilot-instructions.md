# Radisson Beach Larnaca Website

Radisson Beach Larnaca is a simple static HTML/CSS website for a Hebrew hotel. The website displays hotel information in Hebrew (RTL language) with a gallery section and uses modern CSS styling.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Quick Start
- **No installation required** - This is a pure HTML/CSS static website with no dependencies
- **No build process** - Files are served directly without compilation
- **No testing framework** - Manual validation only

### Running the Website
- Start a local HTTP server to serve the website:
  ```bash
  python3 -m http.server 8000
  ```
- **Timing**: Server starts in under 3 seconds
- **NEVER CANCEL**: No long-running commands in this project
- Access the website at: `http://localhost:8000/`
- Stop the server with: `Ctrl+C` or `pkill -f "python3 -m http.server"`

### Alternative Server Options
- Using Node.js: `npx http-server .` (if available)
- Using PHP: `php -S localhost:8000` (if available)
- Any static file server will work

## Validation

### Manual Validation Requirements
- **ALWAYS** start the HTTP server and access `http://localhost:8000/` after making changes
- **Expected behavior**: 
  - Hebrew text displays correctly (RTL layout)
  - Blue header with hotel name "רדיסון ביץ' לרנקה"
  - Gallery section with broken image placeholders (this is EXPECTED)
  - Dark footer with copyright text
- **Expected console errors**: 5 404 errors for missing gallery images (normal behavior)
  - `images/hotel-front.jpg`, `images/room.jpg`, `images/pool.jpg`, `images/chef.jpg`, `images/food.jpg`
- **Screenshot validation**: The working website should look similar to the reference screenshot

### Testing Scenarios
- Load the website and verify Hebrew text renders correctly
- Check that CSS styling is applied (blue header, centered gallery, dark footer)
- Verify responsive layout works on different screen sizes
- Confirm broken image placeholders appear in gallery (expected)

### What NOT to Fix
- **DO NOT** try to fix the 404 image errors - these are expected
- **DO NOT** add build tools or testing frameworks - keep it simple
- **DO NOT** add package.json or other dependency files

## Common Tasks

### File Structure
```
.
├── .github/
│   └── copilot-instructions.md
├── index.html              # Main HTML file (Hebrew content)
├── style.css              # CSS styling
└── pool.webp              # Single actual image (1920x1280 WebP)
```

### Editing Guidelines
- **HTML changes**: Edit `index.html` for content changes
- **Styling changes**: Edit `style.css` for visual changes
- **Language**: Website is in Hebrew (lang="he") with RTL text direction
- **Images**: Only `pool.webp` exists; gallery references missing images (intended)

### Development Workflow
1. Make changes to HTML/CSS files
2. Start HTTP server: `python3 -m http.server 8000`
3. Test in browser at `http://localhost:8000/`
4. Verify Hebrew text and styling work correctly
5. Stop server when done

### Important Notes
- **No linting tools** - Manual code review only
- **No CI/CD pipeline** - No GitHub workflows exist
- **Hebrew language** - Text is right-to-left (RTL)
- **Static hosting ready** - Can be deployed to any static hosting service
- **CORS limitation** - Must use HTTP server, cannot open `index.html` directly in browser

## Project Context
- **Purpose**: Hotel website for Radisson Beach Larnaca
- **Language**: Hebrew (עברית)
- **Technology**: Pure HTML5 and CSS3
- **Hosting**: Static file hosting (GitHub Pages compatible)
- **Maintenance**: Minimal - just update content in HTML/CSS as needed

## Troubleshooting
- **If website doesn't load**: Ensure HTTP server is running on correct port
- **If styles don't apply**: Check that `style.css` exists and is linked correctly
- **If Hebrew text appears broken**: Ensure browser supports UTF-8 and RTL text
- **If images show as broken**: This is expected for gallery images (only pool.webp exists)