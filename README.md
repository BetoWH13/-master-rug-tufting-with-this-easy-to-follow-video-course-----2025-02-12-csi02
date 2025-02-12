# Tufting.xyz Landing Page Maintenance Guide

This guide will help you maintain and customize the Tufting.xyz landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

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
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Tufting.xyz  <!-- Change this text to update the logo -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-8 leading-tight">
    Master Rug Tufting with This Easy-to-Follow Video Course! 🧶
    <!-- ☝️ Update this text for your main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Learn Rug Tufting & Create Custom Rugs Like a Pro!
    <!-- ☝️ Update this text for your subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:

- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-4`, `mb-8`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color

Example of modifying a button:
```html
<!-- Original button -->
<a href="#" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-full">

<!-- To make button larger -->
<a href="#" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-10 py-5 rounded-full">
```

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
1. For internal section links, ensure the `href` matches the section's `id`
2. For external links, replace the `#` with the full URL
3. Example:
```html
<!-- Internal link -->
<a href="#features">Features</a>

<!-- External link -->
<a href="https://example.com/features">Features</a>
```

### Call-to-Action Links
Update the main CTA links:
```html
<!-- Find this in the hero section -->
<a href="https://www.digistore24.com/redir/524735/BetoWH72/" class="bg-gradient-to-r...">
    Start Learning Now
</a>
```

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Locate the footer section and update these links:

```html
<!-- Original footer links -->
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-purple-400">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-purple-400">Terms of Service</a></li>
    </ul>
</div>

<!-- Updated footer links -->
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match the href attributes exactly
   - Example: `<section id="features">` matches `<a href="#features">`

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - These control how elements appear on different screen sizes
   - Example: `text-xl md:text-2xl lg:text-3xl`

3. **Social Media Links**
   ```html
   <div class="flex space-x-4">
       <!-- Update href attributes with your social media URLs -->
       <a href="https://instagram.com/youraccount" class="text-gray-400 hover:text-purple-400">
           <i class="fab fa-instagram text-2xl"></i>
       </a>
   </div>
   ```

### Need Help?
- Double-check that all HTML tags are properly closed
- Verify that class names are spelled correctly
- Ensure all links begin with either `#`, `./`, or `https://`
- Test the page on different devices to ensure responsive design works

Remember to always backup your files before making changes, and test all modifications in a development environment first.