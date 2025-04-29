# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the SigmaSEO landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Located in the header section -->
<div class="text-2xl font-bold text-blue-600">SigmaSEO</div>
```
Simply replace "SigmaSEO" with your company name. The classes ensure:
- `text-2xl`: Large text size
- `text-blue-600`: Blue color
- `font-bold`: Bold weight

### Hero Section
The main headline and subtitle are in the first section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Websites In Texas
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```
- To modify text, simply replace the content between the tags
- The responsive classes (`md:` and `lg:`) automatically adjust text size for different screen sizes

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Intuitive interface and user-friendly design...</p>
</div>
```
To update:
1. Change the heading text between `<h3>` tags
2. Modify description text between `<p>` tags
3. Keep the existing classes to maintain styling

## Managing Links

### Navigation Menu Links
The navigation menu contains internal page links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <!-- Additional links -->
</div>
```
To update:
1. The `href="#features"` links to page sections using IDs
2. Ensure section IDs match these links (e.g., `id="features"`)
3. To link to external pages, replace `#features` with the full URL

### Call-to-Action Links
There are two main CTA buttons:
```html
<!-- Hero section -->
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg...">
    Get Started Today
</a>

<!-- Bottom CTA section -->
<a href="https://sigmaseo.io" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg...">
    Contact Us Now
</a>
```
Replace `https://sigmaseo.io` with your desired destination URL.

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the Legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match navigation href attributes exactly
   - IDs are case-sensitive: `#FAQ` is different from `#faq`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These ensure proper display on different screen sizes
   - Test your changes using browser dev tools mobile view

3. **Style Changes Not Applying**
   - Verify Tailwind CSS is properly loaded
   - Check for typos in class names
   - Ensure the CDN link is present:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 key)
2. Verify all HTML tags are properly closed
3. Ensure all links begin with either `#`, `./`, or `https://`
4. Test the page on multiple browsers

Remember to always backup your files before making significant changes.