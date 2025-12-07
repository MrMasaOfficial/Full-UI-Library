# UI Library

> A lightweight, modern, and responsive UI component library for building beautiful web applications without dependencies.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Bundle Size](https://img.shields.io/badge/Bundle%20Size-%3C10KB-brightgreen)](/)
[![Responsive Design](https://img.shields.io/badge/Responsive-✓-blue)](/)
[![Dark Mode](https://img.shields.io/badge/Dark%20Mode-✓-purple)](/)

## Table of Contents

- [Features](#features)
- [Components](#components)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [API Reference](#api-reference)
- [Browser Support](#browser-support)
- [Contributing](#contributing)
- [License](#license)

## Features

- **🚀 Zero Dependencies** - Pure HTML, CSS, and vanilla JavaScript
- **📦 Lightweight** - Optimized bundle size under 10KB
- **🎨 Highly Customizable** - CSS custom properties for easy theming
- **📱 Fully Responsive** - Mobile-first design approach
- **🌓 Dark Mode Support** - Built-in theme switching with persistence
- **⚡ Performance-Optimized** - Fast loading and smooth interactions
- **♿ Accessibility First** - Semantic HTML and keyboard navigation
- **🎯 Easy to Use** - Minimal setup required, intuitive API
- **🔧 Production Ready** - Tested and reliable components

## Components

### 1. **Buttons**
Versatile button component with multiple variants and sizes.

**Variants:** Primary, Secondary, Success, Danger, Warning, Info  
**Sizes:** Small, Medium (default), Large  
**Styles:** Solid, Outline

### 2. **Cards**
Flexible container component for displaying grouped content.

**Sections:** Header, Image, Body, Footer  
**Variants:** Standard, Raised (elevated)

### 3. **Modals**
Dialog overlay component with smooth animations and multiple close methods.

**Features:** Smooth animations, click-outside to close, ESC key support, customizable sizes

### 4. **Grid System**
Responsive CSS Grid-based layout system with automatic collapsing.

**Options:** 2-column, 3-column, 4-column layouts  
**Responsive:** Automatically adapts to mobile and tablet screens

### 5. **Theme System**
Built-in dark/light mode with automatic preference persistence.

**Features:** One-click theme toggle, localStorage persistence, smooth transitions

## Getting Started

### Quick Preview

View live components at:
- **Components Showcase**: Open `index.html`
- **Full Documentation**: Open `docs/index.html`

### Installation

1. **Clone or download** the repository
2. **Include the CSS and JavaScript files** in your HTML

## Usage

### Basic Setup

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My App</title>
    <link rel="stylesheet" href="path/to/css/style.css">
</head>
<body>
    <!-- Your content here -->
    <script src="path/to/js/main.js"></script>
</body>
</html>
```

### Component Examples

#### Button Component

```html
<!-- Primary Button -->
<button class="btn btn-primary">Click Me</button>

<!-- Secondary Button -->
<button class="btn btn-secondary">Secondary</button>

<!-- Success Button -->
<button class="btn btn-success">Success</button>

<!-- Danger Button -->
<button class="btn btn-danger">Delete</button>

<!-- Button Sizes -->
<button class="btn btn-primary btn-sm">Small</button>
<button class="btn btn-primary">Medium</button>
<button class="btn btn-primary btn-lg">Large</button>

<!-- Outline Button -->
<button class="btn btn-primary btn-outline">Outline</button>

<!-- Disabled State -->
<button class="btn btn-primary" disabled>Disabled</button>
```

#### Card Component

```html
<div class="card">
    <div class="card-header">
        Card Title
    </div>
    <div class="card-image">
        <img src="image.jpg" alt="Description">
    </div>
    <div class="card-body">
        <p>Your card content goes here.</p>
    </div>
    <div class="card-footer">
        <button class="btn btn-primary btn-sm">Action</button>
    </div>
</div>

<!-- Raised Card -->
<div class="card card-raised">
    <!-- content -->
</div>
```

#### Modal Component

```html
<!-- Trigger Button -->
<button class="btn btn-primary" onclick="openModal('exampleModal')">
    Open Modal
</button>

<!-- Modal -->
<div id="exampleModal" class="modal">
    <div class="modal-content">
        <div class="modal-header">
            <h2>Modal Title</h2>
            <button class="modal-close" onclick="closeModal('exampleModal')">&times;</button>
        </div>
        <div class="modal-body">
            <p>Your modal content here.</p>
        </div>
        <div class="modal-footer">
            <button class="btn btn-secondary" onclick="closeModal('exampleModal')">
                Close
            </button>
            <button class="btn btn-primary">Save Changes</button>
        </div>
    </div>
</div>
```

#### Grid System

```html
<!-- 2 Column Grid -->
<div class="grid grid-2">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
</div>

<!-- 3 Column Grid -->
<div class="grid grid-3">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
</div>

<!-- 4 Column Grid -->
<div class="grid grid-4">
    <div class="grid-item">Item 1</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
    <div class="grid-item">Item 4</div>
</div>
```

## API Reference

### JavaScript Functions

#### Modal Functions

```javascript
// Open a modal
openModal('modalId');

// Close a modal
closeModal('modalId');
```

**Example:**
```javascript
<button onclick="openModal('myModal')">Open</button>
<button onclick="closeModal('myModal')">Close</button>
```

### Theme Functions

The theme system automatically handles switching. Click the theme toggle button (🌙/☀️) in the navbar to switch between light and dark modes. Your preference is automatically saved.

## Customization

### CSS Variables

All colors and properties are defined using CSS custom properties. Override them in your stylesheet:

```css
:root {
  --primary-color: #007bff;
  --secondary-color: #6c757d;
  --success-color: #28a745;
  --danger-color: #dc3545;
  --warning-color: #ffc107;
  --info-color: #17a2b8;
  
  --text-dark: #212529;
  --text-light: #6c757d;
  --bg-light: #f8f9fa;
  --bg-white: #ffffff;
  --border-color: #dee2e6;
  
  --spacing-xs: 0.25rem;
  --spacing-sm: 0.5rem;
  --spacing-md: 1rem;
  --spacing-lg: 1.5rem;
  --spacing-xl: 2rem;
  --spacing-2xl: 3rem;
  
  --border-radius: 0.375rem;
  --border-radius-lg: 0.5rem;
  --transition-speed: 0.2s;
  --font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
}

/* Dark Mode Customization */
[data-theme="dark"] {
  --text-dark: #e9ecef;
  --text-light: #adb5bd;
  --bg-light: #212529;
  --bg-white: #1a1a1a;
  --border-color: #495057;
}
```

### Example: Custom Theme

```css
/* Create a custom color theme */
:root {
  --primary-color: #ff6b6b;
  --success-color: #51cf66;
  --danger-color: #fa5252;
  --font-family: 'Inter', -apple-system, sans-serif;
}
```

## File Structure

```
ui-library/
├── index.html              # Live component showcase
├── README.md              # Project documentation
├── css/
│   └── style.css          # All component styles (8.57 KB)
├── js/
│   └── main.js            # Theme & modal functionality (1.49 KB)
└── docs/
    └── index.html         # Complete documentation with examples
```

## Browser Support

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | Latest | ✅ Full Support |
| Firefox | Latest | ✅ Full Support |
| Safari | Latest | ✅ Full Support |
| Edge | Latest | ✅ Full Support |
| IE 11 | - | ❌ Not Supported |

## Responsive Design

The library implements a mobile-first responsive design approach:

- **Grid 2 & 3**: Collapse to 1 column on screens below 480px
- **Grid 4**: Becomes 2 columns below 768px
- **Buttons**: Stack vertically on mobile devices
- **Modals**: Automatically resize for smaller screens
- **Cards**: Adapt to container width

## Performance

- **Bundle Size**: < 10 KB total
- **No Dependencies**: Pure CSS and JavaScript
- **Fast Load Time**: Optimized for quick rendering
- **Smooth Animations**: Hardware-accelerated CSS transitions

## Best Practices

1. **Always include viewport meta tag** for responsive design
2. **Use semantic HTML** with the provided components
3. **Customize CSS variables** instead of modifying component CSS
4. **Test on multiple browsers** before production deployment
5. **Leverage dark mode** for user accessibility

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the **MIT License** - see the LICENSE file for details.

## Support

For issues, questions, or suggestions, please create an issue in the repository.

## Changelog

### Version 1.0.0
- ✨ Initial release
- 📦 Buttons component
- 📦 Cards component
- 📦 Modals component
- 📦 Grid system
- 🌓 Dark mode support

---
