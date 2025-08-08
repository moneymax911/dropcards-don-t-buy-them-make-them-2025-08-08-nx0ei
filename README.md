# Dropcards Landing Page - Maintenance Guide

This guide will help you maintain and customize the Dropcards landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text:**
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">Dropcards</a>
```
- Replace "Dropcards" with your desired text
- Keep the classes to maintain the gradient effect

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
- Modify link text between `<a>` tags
- Keep the `href` attributes matching your section IDs
- Maintain the classes for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">Dropcards - Don't Buy Them - Make Them</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl mx-auto">An Inexpensive Way To Advertise Your Biz</p>
```
- Update heading and subheading text as needed
- Keep responsive classes (`text-4xl md:text-5xl lg:text-6xl`) for proper scaling
- Maintain gradient effect with existing classes

### Tailwind CSS Class Guide
Common classes explained:
- `text-[size]`: Controls text size (xl, 2xl, etc.)
- `md:`: Applies styles at medium screen sizes
- `bg-gradient-to-r`: Creates right-flowing gradient
- `hover:`: Applies styles on mouse hover
- `transition-`: Controls animation effects

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://www.facebook.com/alton.pooser/" class="bg-gradient-to-r from-purple-600 to-blue-500 text-white px-6 py-2 rounded-full">Get Started</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute:
   - For internal sections: Use `#section-id`
   - For external pages: Use full URL
   - For local pages: Use relative path (`./privacy.html`)

Example:
```html
<!-- Before -->
<a href="https://www.facebook.com/alton.pooser/">Get Started</a>

<!-- After -->
<a href="https://your-new-link.com">Get Started</a>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer section:
```html
<div class="border-t border-gray-800 pt-8 text-center">
    <p class="text-gray-400">&copy; 2024 Dropcards. All rights reserved.</p>
</div>
```

2. Add new links before the copyright notice:
```html
<div class="border-t border-gray-800 pt-8 text-center">
    <div class="mb-4">
        <a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300 mx-2">Privacy Policy</a>
        <a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300 mx-2">Terms of Service</a>
    </div>
    <p class="text-gray-400">&copy; 2024 Dropcards. All rights reserved.</p>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Gradient Effects:**
   - Ensure all gradient classes remain together:
   ```html
   bg-gradient-to-r from-purple-600 to-blue-500
   ```

2. **Responsive Issues:**
   - Check that `md:` and `lg:` prefixes are preserved
   - Verify the viewport meta tag exists:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Link Problems:**
   - Confirm section IDs match navigation hrefs
   - Test all external links
   - Use complete URLs for external links
   - Use relative paths for local files

### Need Help?
- Double-check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all sections have matching IDs and href attributes
- Test the page at different screen sizes
- Ensure all custom files (privacy.html, terms.html) exist in the correct location

Remember to always test changes in multiple browsers and screen sizes before deploying to production.