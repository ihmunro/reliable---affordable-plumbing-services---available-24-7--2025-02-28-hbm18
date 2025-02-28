# PureFlow Plumbing Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the PureFlow Plumbing landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:
```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm shadow-md z-50">
    <nav class="container mx-auto px-6 py-4">
        <!-- To update company name -->
        <a href="/" class="text-2xl font-bold text-blue-600">PureFlow</a>
```
To modify:
- Change "PureFlow" to your company name
- Adjust text size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)
- Modify color using `text-blue-600` (options: `text-red-600`, `text-green-600`, etc.)

### Hero Section
The main banner section contains your primary message:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 text-gray-900">
    Fast, Reliable & Affordable Plumbing Solutions – 24/7!
</h1>
```
To modify:
- Update headline text between the `<h1>` tags
- Adjust responsive text sizes:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Common Tailwind Classes Explained
- `px-6`: Padding left/right 1.5rem
- `py-4`: Padding top/bottom 1rem
- `mb-8`: Margin bottom 2rem
- `rounded-full`: Circular border radius
- `hover:bg-blue-700`: Background color on hover
- `transition-colors`: Smooth color transitions

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Keep the `#` symbol
   - Match the ID of the target section
   - Example: `href="#services"` jumps to `<section id="services">`

2. External links:
   - Replace with full URL
   - Example: `href="https://yourwebsite.com/services"`

### Call-to-Action Links
Update the phone number and booking links:
```html
<!-- Phone number -->
<a href="tel:1234567890">Call Now</a>

<!-- Booking link -->
<a href="https://PureFlowPlumbing.com">Book Now</a>
```
Replace with your actual:
- Phone number: `tel:YOUR-PHONE-NUMBER`
- Website: `https://YOUR-WEBSITE.com`

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add new links:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <div>
        <h4 class="text-lg font-semibold mb-6">Quick Links</h4>
        <ul class="space-y-3">
            <!-- Add these new lines -->
            <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Step 2: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

2. Use the same header and footer as `index.html`

3. Maintain consistent styling:
```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check mobile-first classes (without prefix)
   - Then tablet (`md:`) and desktop (`lg:`) variants
   - Example: `text-xl md:text-2xl lg:text-3xl`

3. **Style Inconsistencies**
   - Copy existing Tailwind classes for similar elements
   - Maintain color scheme using `text-blue-600`, `bg-blue-600`
   - Keep consistent spacing with `px-6`, `py-4`, etc.

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Check Tailwind documentation for [class references](https://tailwindcss.com/docs)
- Test responsiveness using browser dev tools

Remember to always test changes across different devices and browsers before publishing updates.