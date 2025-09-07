# ProbioticFy Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the ProbioticFy landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu:

```html
<a href="/" class="text-2xl font-bold text-green-700">ProbioticFy</a>
```

To update the company name:
1. Locate this line in the header section
2. Replace "ProbioticFy" with your desired name
3. Adjust text size using Tailwind classes if needed:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main headline and subtitle are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Transform Your Soil Naturally
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Harness the power of beneficial microorganisms for healthier crops
</p>
```

To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Update the text between the `<p>` tags for the subtitle
3. Maintain the responsive text sizes:
   - `text-4xl` (mobile)
   - `md:text-5xl` (medium screens)
   - `lg:text-6xl` (large screens)

### Features and Benefits Sections
Each feature/benefit card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg">
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description text here.</p>
</div>
```

To update:
1. Locate the card you want to modify
2. Change the title text between `<h3>` tags
3. Update the description between `<p>` tags
4. Maintain existing classes for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-green-700">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-green-700">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-green-700">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-green-700">Contact</a>
</div>
```

To update:
1. For internal section links, keep the `#` prefix (e.g., `#features`)
2. For external links, use the full URL (e.g., `https://example.com`)
3. Update the link text between `<a>` tags
4. Maintain the hover effect classes (`hover:text-green-700`)

### Call-to-Action (CTA) Links
The main CTA buttons currently link to "firstcrop.in":

```html
<a href="https://firstcrop.in" class="inline-block bg-green-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>
```

To update:
1. Replace `https://firstcrop.in` with your desired URL
2. Update button text as needed
3. Maintain the styling classes for consistent appearance

## Adding Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy policy page (e.g., `privacy.html`)
2. Create your terms page (e.g., `terms.html`)
3. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs and href values
   - Verify that section IDs are unique

2. **Responsive Design Issues**
   - Don't remove responsive classes (e.g., `md:`, `lg:` prefixes)
   - Test on different screen sizes using browser dev tools
   - Maintain the existing grid structure (`grid-cols-1 md:grid-cols-3`)

3. **Animation Problems**
   - Verify AOS script is loaded correctly
   - Check data-aos attributes in elements
   - Ensure AOS initialization remains in the footer:
```html
<script>
    AOS.init({
        duration: 1000,
        once: true
    });
</script>
```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for styling classes
- Verify all changes in a development environment before deploying
- Keep a backup of the original code before making changes
- Test all links and functionality after updates

Remember to maintain the responsive design and consistent styling throughout your modifications. When in doubt, reference the existing patterns in the code.