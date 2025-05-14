# Landing Page Maintenance Guide

This guide will help you maintain and customize the Plumbing & Electrical Services landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<div class="text-xl font-bold text-gray-800">Plomberie & Électricité</div>
```

To change the company name:
1. Locate this div in the header section
2. Replace the text between the div tags
3. Keep the existing classes to maintain styling

### Hero Section
The main headline and subheading are in the first section after the header:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Vos travaux de plomberie et d'électricité pour particuliers et professionnels
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Vos travaux de plomberie et d'électricité à la Réunion
</p>
```

To modify:
1. Update the text while keeping the HTML tags intact
2. Maintain the class attributes for responsive design
   - `text-4xl`: Base text size
   - `md:text-5xl`: Tablet size
   - `lg:text-6xl`: Desktop size

### Services Cards
Each service card follows this structure:

```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-wrench text-3xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Dépannage</h3>
    <p class="text-gray-600">Intervention rapide pour tous vos problèmes urgents</p>
</div>
```

To update service cards:
1. Locate the service section (`id="services"`)
2. Change the icon by updating the `fa-` class (e.g., `fa-wrench` to `fa-tools`)
3. Modify the heading and description text
4. Keep all Tailwind CSS classes for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#avantages" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Avantages</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update navigation links:
1. The `href="#services"` format links to sections within the page
2. Match the href value to the `id` of the target section
3. Keep the class attributes for hover effects and styling

### Contact Information
Update the email address in two locations:

```html
<!-- In the contact section -->
<a href="mailto:plumbing-electricity@outlook.fr" class="inline-block bg-white text-blue-600 px-8 py-4 rounded-lg font-semibold hover:bg-gray-100 transform hover:scale-105 transition-all duration-300">
    plumbing-electricity@outlook.fr
</a>

<!-- In the footer -->
<p class="text-gray-400">plumbing-electricity@outlook.fr</p>
```

## Adding Privacy and Terms Pages

### Current Footer Links
The placeholder links are located in the footer:

```html
<div>
    <h3 class="text-xl font-semibold mb-4">Légal</h3>
    <ul class="text-gray-400">
        <li class="mb-2"><a href="#" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new HTML files named `privacy.html` and `terms.html`
2. Update the href attributes:

```html
<li class="mb-2"><a href="terms.html" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - Check for typos in IDs and href attributes
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `container` and `mx-auto` classes on parent divs
   - Maintain the existing padding classes (`px-6`, etc.)

3. **Icon Problems**
   - Verify the Font Awesome CDN link is present in the head section
   - Check that icon class names are correct (e.g., `fas fa-wrench`)
   - Use the [Font Awesome website](https://fontawesome.com/icons) to find correct icon names

Remember to:
- Test all changes in multiple browsers
- Check the page at different screen sizes
- Maintain consistent spacing and indentation in the HTML
- Keep a backup of the original file before making changes