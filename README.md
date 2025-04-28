# 101Headshots Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
The main headline and subheading are located in the first `<section>` after `<main>`:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Lenexa, Kansas Corporate Headshot Photography Services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl">
    Polished portraits reflecting the spirit of Lenexa's business community.
</p>
```
To update:
1. Locate these elements (around line 30)
2. Replace the text between the opening and closing tags
3. Maintain the existing HTML structure

#### Services Section
Each service card contains:
- Icon (SVG)
- Heading
- Description

Example of a service card structure:
```html
<div class="bg-gray-50 rounded-2xl p-8 hover:shadow-lg transition-shadow duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Design Guide</h3>
    <p class="text-gray-600">Professional guidance on styling, posing, and presentation for optimal results.</p>
</div>
```

### Tailwind CSS Class Modifications

#### Understanding Responsive Classes
The landing page uses Tailwind's responsive prefixes:
- `md:` - Applied at medium screens (768px and up)
- `lg:` - Applied at large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: `text-4xl` (2.25rem)
- Tablet: `text-5xl` (3rem)
- Desktop: `text-6xl` (3.75rem)

#### Common Tailwind Classes Used
- Layout: `container`, `mx-auto`, `px-6`, `py-4`
- Spacing: `mb-4`, `mt-12`, `space-x-8`
- Colors: `bg-white`, `text-gray-900`, `hover:text-blue-400`
- Typography: `text-xl`, `font-semibold`, `tracking-tight`

## Fixing Broken Links

### Navigation Menu Links
Located in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace the value with:
   - Internal section: Use `#section-id`
   - External page: Use full URL (e.g., `https://example.com`)

### Book Now Button
Located in multiple places:
```html
<a href="https://www.101headshots.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">Book Now</a>
```

Update the `href` attribute with your booking system URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Located at the bottom of the page:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-sm hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-sm hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-sm hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-sm hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href values
   - Check for typos in IDs
   - Verify that sections have unique IDs

2. **Responsive Design Issues**
   - Check that you're maintaining responsive classes (`md:`, `lg:`)
   - Test on different screen sizes
   - Don't remove container classes (`container`, `mx-auto`)

3. **Style Inconsistencies**
   - Keep consistent color classes (e.g., `text-gray-600`, `bg-blue-600`)
   - Maintain spacing patterns (`mb-4`, `py-24`)
   - Preserve hover states (`hover:` classes)

### Need Help?
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify HTML structure remains intact
3. Test all links after modifications
4. Ensure all sections have proper closing tags

Remember to always backup your files before making changes!