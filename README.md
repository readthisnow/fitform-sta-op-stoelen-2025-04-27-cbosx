# Fitform Landing Page Maintenance Guide

This guide will help you maintain and customize the Fitform landing page. It's written for beginners and provides detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation menu. To update the company name:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-gray-800">Fitform</a>
```

To change the company name, simply replace "Fitform" with your desired text.

### Hero Section
The hero section is the main banner area. Key elements to update:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    Fitform Sta Op Stoelen
    <span class="block text-blue-600 mt-2">Tijdelijk 10% Korting</span>
</h1>
```

Tailwind CSS class explanation:
- `text-4xl`: Base text size
- `sm:text-5xl`: Larger text on small screens
- `lg:text-6xl`: Largest text on large screens
- `text-gray-900`: Dark gray text color
- `mb-8`: Bottom margin spacing

### Features Section
To add or modify features:

1. Locate the features grid:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

2. Copy an existing feature card and modify:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Your New Feature</h3>
    <p class="text-gray-600">Your feature description</p>
</div>
```

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden lg:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Kenmerken</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update a link:
1. Locate the `href` attribute
2. Replace the value with your new link
3. Update the text between `<a>` tags
4. Remember to update both desktop and mobile menu versions

### Call-to-Action Links
Important CTA links to update:

```html
<a href="https://sta-opstoelen.nl" class="inline-flex items-center justify-center px-8 py-4 text-lg font-medium text-white bg-blue-600 rounded-full hover:bg-blue-700">
    Bekijk Aanbod
</a>
```

Replace `https://sta-opstoelen.nl` with your actual product page URL.

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the footer's legal section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Juridisch</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
    </ul>
</div>
```

To add privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Ensure file names match exactly (case-sensitive)
   - Verify files are in the correct directory

2. **Responsive Design Issues**
   - Don't remove responsive classes (e.g., `sm:`, `md:`, `lg:` prefixes)
   - Test on multiple screen sizes
   - Keep the viewport meta tag intact:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Style Problems**
   - Maintain the Tailwind CSS link in the header
   - Don't modify the Alpine.js script tag unless updating versions
   - Keep class order consistent when copying styles

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Alpine.js functionality in the browser console
- Test all links before deploying changes
- Maintain backup copies of working files

Remember to test all changes thoroughly before pushing to production!