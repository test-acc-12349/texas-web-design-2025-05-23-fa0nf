# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To modify:

1. **Logo Text**: Find this line and change "TWD":
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```

2. **Navigation Menu Items**: Located in the header `<div class="hidden md:flex space-x-8">`. Each item follows this pattern:
```html
<a href="#section-name" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Menu Item</a>
```

### Hero Section
Find the hero section starting with `<section class="pt-32 pb-24">`:

1. **Main Heading**: Update the text between `<h1>` tags:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
```

2. **Subheading**: Modify the text in the `<p>` tag:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-10">Best Websites In Texas</p>
```

### Tailwind CSS Class Guide
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-blue-600`, `bg-white`, `text-gray-600`
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-6` (margin bottom)
- Responsive classes: `md:text-5xl` (applies at medium screens and up)

To modify a style, simply change the corresponding class value. For example:
```html
<!-- Original -->
<h3 class="text-xl font-bold mb-4">Free Hosting</h3>

<!-- Modified to be larger and blue -->
<h3 class="text-2xl font-bold mb-4 text-blue-600">Free Hosting</h3>
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update these:
1. The `#` symbol indicates an internal page link
2. The text after `#` must match the `id` of the target section
3. Example: To link to a new section, add `id="new-section"` to that section and use `href="#new-section"`

### Call-to-Action Links
Find and update these important links:
```html
<!-- Hero section CTA -->
<a href="https://twd.com" class="inline-block bg-blue-600...">Get Started Today</a>

<!-- Bottom CTA section -->
<a href="https://twd.com" class="inline-block bg-white...">Contact Us Now</a>
```

Replace `https://twd.com` with your actual website URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Find this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section `id` attributes match exactly with their corresponding `href` values
   - IDs are case-sensitive: `href="#FAQ"` won't link to `id="faq"`

2. **Styling Not Applied**
   - Verify the Tailwind CSS CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```
   - Check for typos in class names

3. **Responsive Design Issues**
   - Test different screen sizes using browser developer tools
   - Look for classes starting with `md:` or `lg:` for responsive behaviors
   - The mobile menu button appears when the screen width is below the `md` breakpoint

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Test all links after making changes
- Ensure all HTML tags are properly closed
- Maintain the existing indentation pattern for readability

Remember to always save your changes and test the page in multiple browsers before publishing updates.