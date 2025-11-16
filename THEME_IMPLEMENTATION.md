# Light/Dark Theme Toggle Implementation

## Overview
This implementation uses **pure HTML and CSS only** (no JavaScript) to provide a theme toggle functionality across all pages.

## How It Works

### 1. **CSS Variables (theme.css)**
- Defines all color variables for both dark (default) and light themes
- Uses `:root` for dark theme and `:root:has(#theme-toggle:checked)` for light theme
- Variables include backgrounds, text colors, accents, borders, and gradients

### 2. **Hidden Checkbox**
- Each HTML page has a hidden checkbox: `<input type="checkbox" id="theme-toggle">`
- When checked, it activates the light theme
- When unchecked, it shows the dark theme (default)

### 3. **CSS :has() Selector**
- Modern CSS selector that detects when checkbox is checked
- Automatically switches all CSS variables when state changes
- No JavaScript required!

### 4. **Theme Toggle Button**
- Replaced `<button>` with `<label for="theme-toggle">`
- Clicking the label toggles the checkbox
- Icon rotates 180° when theme changes for visual feedback

## Files Modified

### New File:
- `theme.css` - Contains all theme variables and toggle logic

### Updated Files:
- `home.html` - Added checkbox and theme.css link
- `contacts.html` - Added checkbox and theme.css link
- `news.html` - Added checkbox and theme.css link
- `events.html` - Added checkbox and theme.css link
- `discovery.html` - Added checkbox and theme.css link
- `resources.html` - Added checkbox and theme.css link
- `home.css` - Updated to use CSS variables instead of hardcoded colors

## Usage
Simply click the brightness icon in the header to toggle between light and dark themes. The theme applies instantly across the entire page.

## Browser Compatibility
- Modern browsers (Chrome, Firefox, Safari, Edge) support `:has()` selector
- Works on all pages consistently
- Smooth transitions between themes

## Benefits
✅ Pure HTML/CSS - No JavaScript required
✅ Consistent across all pages
✅ Easy to maintain with CSS variables
✅ Smooth transitions
✅ Accessible with proper labels
