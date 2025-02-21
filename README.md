# Landing Page Maintenance Guide

This guide will help you maintain and customize the landing page by providing detailed instructions for common updates and modifications.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Logo
</div>
```
Replace "Logo" with your company name. The gradient styling will automatically apply.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
Update the text between `<a>` tags to change menu items. Keep the classes to maintain hover effects.

### Hero Section
Located at the top of the main content:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent mb-8">
    Lorem ipsum dolor
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Lorem ipsum dolor
</p>
```
- Replace both "Lorem ipsum dolor" instances with your headline and subheading
- The `md:` and `lg:` prefixes control responsive text sizes - keep these intact

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition duration-300 transform hover:scale-105">
    <div class="w-12 h-12 bg-purple-100 rounded-xl mb-6 flex items-center justify-center">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Lorem ipsum dolor</h3>
    <p class="text-gray-600">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
</div>
```
- Update the heading and description text
- Maintain the class structure for consistent styling
- To add more cards, copy the entire `<div>` block

## Managing Links

### Navigation Links
Current placeholder links use `#`. Update them like this:
```html
<!-- Before -->
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>

<!-- After -->
<a href="/features.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```

### Call-to-Action Buttons
Update the "Get Started" button links:
```html
<!-- Header button -->
<button class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-6 py-2 rounded-full font-medium hover:shadow-lg transform hover:scale-105 transition duration-300">
    Get Started
</button>

<!-- Hero section button -->
<a href="/signup.html" class="inline-block bg-gradient-to-r from-purple-600 to-pink-600 text-white text-lg px-8 py-4 rounded-full font-medium hover:shadow-xl transform hover:scale-105 transition duration-300">
    Get Started Now
</a>
```
Replace `href="#"` with your actual signup or registration page URL.

## Adding Policy Pages

### Footer Modification
Add privacy and terms links to the footer columns:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="/privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
Insert this block within the footer's grid structure.

## Troubleshooting

### Common Issues

1. **Broken Gradients**
If gradients aren't showing:
- Verify the `from-` and `to-` color classes are connected with `bg-gradient-to-r`
- Ensure `bg-clip-text` and `text-transparent` are present for text gradients

2. **Responsive Issues**
If mobile layout breaks:
- Check that `md:` prefixes are present for desktop styles
- Verify the container class: `container mx-auto px-6`
- Ensure grid classes use proper responsive prefixes: `grid-cols-1 md:grid-cols-2`

3. **Link Problems**
If links aren't working:
- Confirm file paths are correct relative to index.html
- Check for typos in href attributes
- Verify file extensions (.html) are included

### Need Help?
- Double-check all class names match exactly
- Use browser inspector to identify styling issues
- Ensure all HTML tags are properly closed
- Maintain the existing responsive design structure

Remember to test all changes across different screen sizes using browser developer tools.