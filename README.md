# Landing Page Maintenance Guide

This guide will help you maintain and customize the Bitcoin Wealth landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<div class="text-xl font-bold text-blue-600">Bitcoin Wealth</div>
```

To change the brand name, simply replace "Bitcoin Wealth" with your desired text.

### Hero Section
The main headline and subtitle are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Building Generational Wealth with Bitcoin and AI
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl mx-auto">
    Secure your financial future through strategic Bitcoin investments and AI-powered opportunities
</p>
```

To modify:
1. Replace the h1 text to change the main headline
2. Update the p text to change the subtitle
3. Maintain the existing classes to preserve responsive design

### Tailwind CSS Class Guide
Common classes used in this page:
- `text-[size]`: Controls text size (xl, 2xl, 4xl, etc.)
- `font-[weight]`: Controls text boldness (bold, semibold)
- `mb-[size]`: Adds bottom margin (4, 6, 8, 12, etc.)
- `px-[size]`: Adds horizontal padding
- `py-[size]`: Adds vertical padding
- `bg-[color]`: Sets background color

Example of updating a feature card:
```html
<!-- Original -->
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">

<!-- To make it blue with white text -->
<div class="bg-blue-600 text-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
```

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:

```html
<div class="hidden lg:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag you want to modify
2. Change the `href` attribute to your desired destination
3. Update the link text between the opening and closing tags

### Call-to-Action Links
The main CTA buttons are currently pointing to:
```html
<a href="https://www.ultimatepassiveprofit.com/legacywealth/?refctex=C0510518581">
```

To update:
1. Locate all instances of this URL in the code
2. Replace with your new destination URL
3. Test all buttons to ensure they work correctly

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the legal section in the footer:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly
   - Verify files are in the correct directory

2. **Styling Problems**
   - Make sure Tailwind CSS is properly loaded
   - Check for missing or mistyped classes
   - Verify closing tags are present

3. **Responsive Design Issues**
   - Test on multiple screen sizes
   - Maintain responsive classes (md:, lg:, etc.)
   - Don't remove container classes

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all changes against the original code
3. Test on multiple browsers
4. Contact technical support at the email provided in the footer

Remember to always backup your code before making changes and test thoroughly after each modification.