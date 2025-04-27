# Stawett Landing Page Maintenance Guide

This guide will help you maintain and customize the Stawett landing page. The instructions are designed for beginners and focus on common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text**: Find this line and change "Stawett":
```html
<a href="/" class="text-2xl font-bold text-gray-800">Stawett</a>
```

2. **Navigation Items**: Located in the header's div with class `md:flex space-x-8`:
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Kenmerken</a>
```
Change the text between `>` and `</a>` to update menu items.

### Hero Section
The main banner section contains:

1. **Main Heading**: Update both lines:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Stawett Sta Op Stoel
    <span class="block text-2xl md:text-3xl text-blue-600 mt-4">Tijdelijk 10% Korting</span>
</h1>
```

2. **Urgency Message**: Modify the number of available chairs:
```html
<p class="text-xl text-gray-600 mb-8">Nog maar <span class="text-red-600 font-semibold">3 stoelen</span> beschikbaar met deze aanbieding!</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[number]`: Adds margin bottom (4, 8, 16, etc.)
- `py-[number]`: Adds padding top and bottom
- `bg-[color]`: Sets background color

Example of modifying text size:
```html
<!-- Original -->
<h2 class="text-3xl md:text-4xl font-bold">

<!-- Making text larger -->
<h2 class="text-4xl md:text-5xl font-bold">
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Kenmerken</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Change the `href="#section-name"` to point to your new section
2. Ensure the section ID matches: `<section id="section-name">`

### Call-to-Action Buttons
Located in two places:
```html
<!-- Hero section -->
<a href="https://sta-opstoelen.nl" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">

<!-- Bottom CTA section -->
<a href="https://sta-opstoelen.nl" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-full">
```

To update:
1. Replace `https://sta-opstoelen.nl` with your desired URL
2. Test the link after updating

## Adding Privacy and Terms Pages

### Current Footer Links Structure
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors">Algemene Voorwaarden</a></li>
</ul>
```

### Steps to Add Policy Pages:

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Algemene Voorwaarden</a></li>
```

3. Maintain consistent styling by copying these classes to new page links:
   - `hover:text-white`
   - `transition-colors`

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match the href attributes
   - Ensure no spaces in IDs
   - IDs should be lowercase

2. **Responsive Design Issues**
   - Check for `md:` and `lg:` prefixes in classes
   - Don't remove responsive classes without testing
   - Use browser dev tools to test different screen sizes

3. **Missing Styles**
   - Verify Tailwind CSS link is present in head:
   ```html
   <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
   ```

### Getting Help
- Check Tailwind CSS documentation for class references
- Use browser inspector to examine elements
- Test all changes in multiple browsers
- Backup your files before making changes

Remember to always test your changes in a development environment before pushing to production.