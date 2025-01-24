# The Karri Clinic Landing Page - Maintenance Guide

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the clinic name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-semibold text-gray-800">The Karri Clinic</a>
```

To change the clinic name:
1. Locate this line in the header section
2. Replace "The Karri Clinic" with your desired text
3. Adjust font size by modifying `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Breast Reduction Surgery
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Rediscover comfort and confidence...
</p>
```

To modify:
1. Replace text between the `<h1>` tags for the main headline
2. Update the paragraph text between the `<p>` tags
3. Common Tailwind classes used here:
   - `text-4xl`: Controls text size
   - `md:text-5xl`: Changes text size on medium screens
   - `mb-6`: Adds margin bottom spacing
   - `text-gray-900`: Sets text color

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300 p-8">
    <h3 class="text-xl font-semibold mb-4">Before-and-After Gallery</h3>
    <p class="text-gray-600 leading-relaxed">View our extensive collection...</p>
</div>
```

To update:
1. Locate the feature cards in the "Our Services" section
2. Replace text in `<h3>` tags for feature titles
3. Update descriptions in `<p>` tags
4. Key classes explained:
   - `rounded-xl`: Rounds corners
   - `shadow-lg`: Adds shadow effect
   - `p-8`: Adds padding
   - `hover:shadow-xl`: Enhances shadow on hover

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#gallery">Gallery</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact Us</a>
</div>
```

To update:
1. Replace `#services` with the actual URL or section ID
2. Ensure section IDs match in the HTML (e.g., `id="services"`)
3. For external links, use full URLs: `href="https://example.com"`

### Footer Links
Located at the bottom of the page:

```html
<ul class="space-y-2">
    <li><a href="#services">Services</a></li>
    <li><a href="#gallery">Gallery</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#faq">FAQ</a></li>
</ul>
```

To update:
1. Match these links with navigation menu links
2. Replace email address: `info@thekarriclinic.co.uk`
3. Update website URL: `https://www.thekarriclinic.co.uk`

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer:

```html
<!-- Add this to the Quick Links section in footer -->
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Check responsive classes like `md:` and `lg:`
   - Test on different screen sizes
   - Use browser developer tools to debug

3. **Styling Inconsistencies**
   - Keep color classes consistent (e.g., `text-gray-600`)
   - Maintain consistent spacing with `m-` and `p-` classes
   - Use the same hover effects (`hover:` classes)

For additional help:
- Consult [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser inspection tools (F12) to examine elements
- Test all links after making changes

Remember to backup your files before making significant changes!