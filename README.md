# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
Simply replace "TWD" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
The main banner section contains:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Best Websites In Texas</p>
```
- Change the h1 text to update your main headline
- Modify the paragraph text for your subheading

### Tailwind CSS Class Guide
Common classes used in this template:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-[weight]`: Controls text thickness (bold, semibold)
- `text-[color]-[shade]`: Changes text color (blue-600, gray-900)
- `bg-[color]-[shade]`: Changes background color
- `px-[size]`: Horizontal padding
- `py-[size]`: Vertical padding
- `mb-[size]`: Bottom margin

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. For internal section links, ensure the href matches the section ID
2. For external links, replace # with full URL:
```html
<a href="https://yoursite.com/page">Link Text</a>
```

### Call-to-Action Buttons
Update the "Get Started" button links:
```html
<!-- Find these lines -->
<a href="https://twd.com" class="...">Get Started</a>
```
Replace `https://twd.com` with your actual URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html pages
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match href attributes
- Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
- Check mobile display using browser dev tools
- Verify all `md:` and `lg:` responsive classes are intact

3. **Missing Icons**
- Confirm Font Awesome is properly loaded
- Check icon class names match Font Awesome 6.0 syntax

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all CDN links are working
3. Ensure Tailwind CSS is properly loaded
4. Double-check all href attributes for typos

Remember to test all changes across different devices and browsers before publishing updates.