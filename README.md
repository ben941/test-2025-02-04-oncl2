# Landing Page Maintenance Guide

This guide will help you maintain and customize the landing page, focusing on common updates and modifications. The instructions are designed for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-gray-800">Logo</div>
<!-- Replace "Logo" with your company name -->
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Each menu item follows this pattern -->
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
To modify menu items, update the text between `>` and `</a>`.

### Hero Section
The main headline and subtitle are in the first section after the header:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight tracking-tight">test</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">test</p>
```
- Replace both instances of "test" with your actual content
- The different text sizes (`text-4xl`, `text-5xl`, `text-6xl`) ensure proper scaling on different devices

### Understanding Tailwind Classes
Key classes used in this landing page:

- `container mx-auto`: Centers content and sets maximum width
- `px-6`: Adds horizontal padding (24px)
- `py-4`: Adds vertical padding (16px)
- `text-gray-600`: Sets text color
- `hover:text-gray-900`: Changes text color on hover
- `md:`: Applies styles only on medium-sized screens and up

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. For internal sections, keep the `#` prefix followed by the section ID
2. For external links, replace with full URLs:
```html
<!-- Example -->
<a href="https://yourwebsite.com/features">Features</a>
```

### Call-to-Action Buttons
Located in hero and contact sections:
```html
<!-- Find these lines -->
<a href="https://test.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">Get Started</a>
```
Replace `https://test.com` with your actual URL.

## Linking Privacy and Terms Pages

### Footer Legal Section
Locate the legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

To add links to privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout:**
   - Check that you haven't removed any essential Tailwind classes
   - Verify all `div` tags are properly closed
   - Maintain the existing responsive classes (those starting with `md:` or `lg:`)

2. **Links Not Working:**
   - Ensure URLs start with `http://` or `https://` for external links
   - For internal links, verify that section IDs match exactly (case-sensitive)
   - Check for extra spaces in URLs

3. **Styles Not Applying:**
   - Verify the Tailwind CDN link is present in the `<head>` section
   - Check for typos in class names
   - Make sure classes are space-separated

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all changes against the original code
3. Test the page on different devices and browsers
4. Ensure all required files are in the correct directory

Remember to always backup your code before making changes, and test thoroughly after each modification.