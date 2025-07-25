# DeFi Academy Landing Page - Maintenance Guide

This guide will help you maintain and customize the DeFi Academy landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-xl font-bold text-blue-500">DeFi Academy</a>
```
Simply replace "DeFi Academy" with your desired text.

2. **Navigation Items:**
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">Master DeFi Fast: Wallets, Yield & Safety</h1>
```
- Change the heading text between the `<h1>` tags
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control text size at different screen sizes

### Tailwind CSS Tips
- Color classes follow this pattern: `text-{color}-{shade}` (e.g., `text-blue-500`)
- Spacing classes use this format: `m{side}-{size}` or `p{side}-{size}`
  - Example: `mb-8` means margin-bottom: 2rem
- Responsive classes start with screen sizes: `md:` or `lg:`

## Managing Links

### Navigation Menu Links
Current links in the navigation:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://defionlineacademy.com">Start Learning</a>
</div>
```

To update links:
1. Internal links (starting with #) point to sections on the same page
2. External links (starting with http) point to other websites
3. Replace `href` values with your desired destinations

### Call-to-Action Buttons
Located throughout the page:
```html
<a href="https://defionlineacademy.com" class="inline-block px-8 py-4 bg-blue-600 hover:bg-blue-700 rounded-full">Start Your Journey Today</a>
```
Update the `href` attribute with your enrollment or signup page URL.

## Adding Legal Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files: `privacy.html` and `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match the href values
- Example: `href="#features"` needs a matching `id="features"` in the page

2. **Responsive Design Issues**
- Check that you maintain the responsive classes when editing
- Look for classes starting with `md:` or `lg:`
- Test on different screen sizes after making changes

3. **Style Consistency**
- Copy existing classes when adding new elements
- Example for a new link in navigation:
```html
<a href="/new-page" class="text-gray-300 hover:text-white transition-colors duration-300">New Page</a>
```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling references
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test all links after making changes
- Always backup your files before making major changes

Remember to maintain the existing responsive design and styling patterns when making updates to ensure consistency across the site.