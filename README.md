# Macon Connections Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Macon Connections landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance below.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Company Name and Header
```html
<!-- Located in the header -->
<div class="text-xl font-bold text-gray-800">
    Macon Connections  <!-- Update company name here -->
</div>
```

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Macon Connections Electrical & HVAC  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Electrician, Heating, Air Conditioning Services  <!-- Update subheading here -->
</p>
```

#### Services Section
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <i class="fas fa-bolt text-4xl text-blue-600 mb-6"></i>
    <h3 class="text-xl font-bold mb-4">Electrical Services</h3>
    <p class="text-gray-600">Complete electrical solutions...</p>
</div>
```

### Tailwind CSS Classes Explained

#### Common Class Patterns
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `text-[color]-[shade]`: Sets text color (gray-600, blue-600, etc.)
- `bg-[color]-[shade]`: Sets background color
- `p-[size]`: Sets padding (p-4, p-6, p-8, etc.)
- `mb-[size]`: Sets margin bottom
- `rounded-[size]`: Controls border radius

#### Responsive Design Classes
- `md:text-4xl`: Applies style at medium screen sizes
- `lg:text-6xl`: Applies style at large screen sizes

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
1. Locate the `href` attribute
2. Replace `#section-name` with your desired link
3. For external links, use complete URLs (e.g., `https://example.com`)

### Email Links
Current email links:
```html
<a href="mailto:maconconnectionsllc@gmail.com">Email Us Now</a>
```

To update:
1. Replace `maconconnectionsllc@gmail.com` with new email address
2. Update all instances in both CTA and footer sections

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition duration-300">
        <i class="fab fa-facebook text-2xl"></i>
    </a>
    <!-- Similar structure for Twitter and Instagram -->
</div>
```

To update:
1. Replace `#` with actual social media profile URLs
2. Ensure all social icons link to correct profiles

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Add these links to the footer section:
```html
<!-- Add this to the footer grid -->
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Styling Consistency
- Use `text-gray-400` for default state
- Add `hover:text-white` for hover effect
- Include `transition duration-300` for smooth transitions

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure proper div nesting

2. **Non-Working Links**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure anchor tags (`<a>`) are properly closed

3. **Responsive Issues**
   - Test at different screen sizes
   - Verify media query classes (md:, lg:) are correct
   - Check container widths and padding

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making significant changes, and test your updates across different browsers and devices.