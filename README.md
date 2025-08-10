# Cofface Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Cofface coffee landing page. Follow these steps to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-white">Cofface</div>
```
- Replace "Cofface" with your desired company name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Serving you high-quality coffee beans. Always in all ways
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Premium Beans, Perfectly Roasted—Crafted for Every Cup.
</p>
```

To modify:
1. Replace the text between the `<h1>` tags for your main headline
2. Update the subheading text between the `<p>` tags
3. The `text-4xl` class controls text size on mobile, while `md:text-5xl` affects tablet and `lg:text-6xl` affects desktop views

### Tailwind CSS Color Classes
To change colors, locate classes starting with:
- `text-` (text color)
- `bg-` (background color)
- `border-` (border color)

Example:
```html
<!-- Original -->
<div class="bg-amber-600 text-white">

<!-- To change to blue -->
<div class="bg-blue-600 text-white">
```

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. For internal links (same page sections), use `#section-name`
3. For external links, use the full URL: `https://example.com`

### Shop Now Button
The main call-to-action button appears twice:

```html
<!-- Update this URL in both locations -->
<a href="https://tinyurl.com/coffaceph" class="inline-block bg-amber-600 hover:bg-amber-700 text-white font-semibold px-8 py-4 rounded-lg">
    Shop Now
</a>
```

To modify:
1. Replace `https://tinyurl.com/coffaceph` with your shop's URL
2. Ensure you update both instances (hero section and CTA section)

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the legal links section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-3 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:

1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update the footer links:
   ```html
   <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Section IDs should not contain spaces
   - Example: `href="#features"` links to `<section id="features">`

2. **Responsive Design Problems**
   - Check that you maintain the responsive classes:
     - `md:` prefix for tablet
     - `lg:` prefix for desktop
   - Don't remove `container` or `mx-auto` classes as they center content

3. **Animation Issues**
   - Verify `data-aos` attributes remain intact
   - Check that the AOS script is loaded:
   ```html
   <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
   ```

### Need Help?
If you encounter issues:
1. Verify all changes against the original code
2. Check the browser console for errors
3. Ensure all required scripts are loading
4. Test the page across different devices and browsers

Remember to always backup your code before making changes, and test thoroughly after each modification.