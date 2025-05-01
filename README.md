# SydneyWeb Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the SydneyWeb landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- CTA Section
- Footer

### Updating Text Content

#### Hero Section
Look for this section in the HTML:
```html
<section class="relative min-h-screen flex items-center">
    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
        Best Web Agency In Sydney
    </h1>
    <p class="text-xl md:text-2xl text-gray-300">
        Grow your business with clicks
    </p>
</section>
```
To update:
1. Locate the `<h1>` tag for the main heading
2. Replace the text between the tags
3. For the subtitle, modify the text within the `<p>` tag

#### Features Cards
Find the features section:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
    <div class="bg-gray-900 p-8 rounded-xl">
        <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
        <p class="text-gray-400">Intuitive interfaces...</p>
    </div>
    <!-- Additional feature cards follow -->
</div>
```
To modify:
1. Each feature card is contained in a `<div>` with class `bg-gray-900`
2. Update the `<h3>` title and `<p>` description within each card
3. Maintain the same structure to keep consistent styling

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
Example from the navigation:
```html
<div class="hidden md:flex space-x-8">
```
- `hidden`: Hides element by default
- `md:flex`: Shows element as flex container on medium screens and larger
- `space-x-8`: Adds horizontal spacing between child elements

#### Common Style Modifications

To change colors:
```html
<!-- Original -->
<div class="bg-gray-900">

<!-- Modified (example) -->
<div class="bg-blue-900">
```

To adjust padding/margin:
```html
<!-- Original -->
<section class="py-24 px-6">

<!-- Modified (example) -->
<section class="py-12 px-4">
```

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. For section links, use `#section-id`
3. For external links, use full URL: `https://example.com`

### Footer Links
Current footer links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-blue-400">About</a></li>
    <li><a href="#" class="hover:text-blue-400">Services</a></li>
    <li><a href="#" class="hover:text-blue-400">Blog</a></li>
</ul>
```

To update:
1. Replace `#` with actual URLs
2. Example: `<a href="https://sydneyweb.com/about">About</a>`
3. Maintain the `hover:text-blue-400` class for consistent styling

## Adding Privacy and Terms Pages

### Footer Legal Section
Locate this section:
```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-blue-400">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-blue-400">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

**Problem**: Links not working
- Check that `href` values match exact file names or section IDs
- Ensure section IDs exist in the HTML
- Verify file paths are correct relative to index.html

**Problem**: Styles not applying
- Check for typos in Tailwind class names
- Verify the Tailwind CSS CDN link is working
- Ensure classes are space-separated

**Problem**: Responsive design issues
- Test with different screen sizes using browser dev tools
- Verify responsive classes (sm:, md:, lg:) are correctly ordered
- Check for conflicting responsive classes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers
- Make one change at a time and test before proceeding

Remember to always backup your files before making significant changes, and test thoroughly across different devices and browsers.