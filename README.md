# CoffeeMax Landing Page - Maintenance Guide

This guide will help you maintain and customize the CoffeeMax landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Company Name**:
```html
<span class="font-bold text-xl">CoffeeMax</span>
```
Simply replace "CoffeeMax" with your desired name.

2. **Navigation Menu Items**:
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Features</a>
```
- Replace the text between `<a>` tags to change menu items
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
Located at the top of the page:

1. **Main Heading**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-8">
    Create Great Coffee at Home
</h1>
```
- Replace the text while maintaining the surrounding tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

2. **Subheading**:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Master the art of grinding coffee beans for the perfect brew, every single time.
</p>
```
- Update the text between the `<p>` tags
- Keep the classes for consistent styling

### Features Section
To modify feature cards:

```html
<div class="group bg-white rounded-xl shadow-md hover:shadow-xl p-8 transition-all duration-300">
    <div class="text-brown-600 mb-4">
        <i class="fas fa-magic text-4xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to Follow</h3>
    <p class="text-gray-600">Simple, straightforward instructions for perfect coffee grinding every time.</p>
</div>
```

1. **Icon**: Change `fa-magic` to any [Font Awesome](https://fontawesome.com/icons) icon name
2. **Title**: Update text in the `<h3>` tag
3. **Description**: Modify text in the `<p>` tag

## Managing Links

### Navigation Menu Links
Current links in the header:

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
<a href="https://coffeemax.com">Get Started</a>
```

To update:
1. Internal links (starting with #) connect to sections with matching IDs
2. External links (starting with http) go to other websites
3. Replace `https://coffeemax.com` with your actual website URL

### Call-to-Action (CTA) Buttons
Located in hero and CTA sections:

```html
<a href="https://coffeemax.com" class="inline-flex items-center justify-center px-8 py-4 text-lg font-medium text-white bg-brown-600 rounded-md hover:bg-brown-700">
    Start Brewing
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

- Update the `href` attribute with your target URL
- Modify button text between the `<a>` tags
- Keep the `<i>` tag for the arrow icon

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>
```

To link to policy pages:

1. Create new files:
   - Create `privacy.html` in your website folder
   - Create `terms.html` in your website folder

2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Example: `href="#features"` needs a matching `id="features"` in the target section

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These ensure proper display on different screen sizes

3. **Icon Not Showing**
   - Verify Font Awesome is properly loaded in the head section
   - Check icon names against the [Font Awesome website](https://fontawesome.com/icons)

4. **Styling Problems**
   - Keep the `class` attributes intact when updating content
   - Don't remove Tailwind CSS classes unless you're replacing them with alternatives

### Need More Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Verify all links begin with either `#` (internal) or `http`/`https` (external)