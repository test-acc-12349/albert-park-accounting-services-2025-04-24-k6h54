# Albert Park Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Located in the nav element -->
<a href="/" class="text-2xl font-bold">Albert Park</a>
```
To modify the company name, update the text between the `<a>` tags.

#### Hero Section
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold">Albert Park accounting services</h1>
<p class="text-2xl md:text-3xl text-gray-300">Your financial success is our bottom line</p>
```
- Update the main heading and tagline by changing the text within these elements
- The different text sizes (`text-5xl`, `text-6xl`, `text-7xl`) ensure proper scaling across devices

#### Services Cards
Each service card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8">
    <h3 class="text-xl font-bold mb-4">Tax Optimization</h3>
    <p class="text-gray-400">Strategic tax planning and optimization...</p>
</div>
```
To modify services:
1. Locate the `services` section
2. Find each card within the grid
3. Update the `<h3>` title and `<p>` description

### Tailwind CSS Modifications

#### Color Scheme
The current theme uses purple and indigo gradients. To change colors:
1. Find classes starting with `from-` and `to-`
2. Replace with desired Tailwind colors:
```html
<!-- Original -->
<div class="bg-gradient-to-r from-purple-500 to-indigo-500">

<!-- Example modification -->
<div class="bg-gradient-to-r from-blue-500 to-green-500">
```

#### Spacing and Padding
- `px-6`: Horizontal padding
- `py-4`: Vertical padding
- `mb-8`: Margin bottom
- Increase/decrease numbers (1-16) to adjust spacing

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="https://theaccountants.com">Get Started</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external links, replace `https://theaccountants.com` with your desired URL

### Call-to-Action Buttons
Multiple "Get Started" buttons appear throughout the page:
```html
<a href="https://theaccountants.com" class="inline-flex items-center px-8 py-4">
    Start Your Journey
</a>
```
Update all instances to maintain consistency:
1. Search for `https://theaccountants.com`
2. Replace with your actual registration or contact page URL

## 3. Linking Privacy and Terms Pages

### Footer Legal Links
Current structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link policy pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting Tips

1. **Broken Styles**
   - Ensure the Tailwind CSS CDN link remains in the header
   - Check for typos in class names
   - Verify all classes use correct Tailwind syntax

2. **Responsive Issues**
   - Look for `md:` and `lg:` prefixes
   - Test on different screen sizes
   - Don't remove responsive classes unless replacing with alternatives

3. **Link Problems**
   - Verify file paths are correct
   - Check for proper URL formatting
   - Test all links after updates

## Additional Notes

- Always backup your files before making changes
- Test all modifications in multiple browsers
- Maintain the existing responsive design structure
- Keep the gradient theme consistent throughout
- Update the copyright year in the footer annually

For further assistance or advanced customization, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.