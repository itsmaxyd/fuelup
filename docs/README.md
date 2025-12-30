# FuelUp Website

This directory contains the static website for the FuelUp fuel tracking application, designed to be hosted on GitHub Pages.

## Files Structure

```
docs/
├── index.html          # Main website homepage
├── privacy-policy.html # Privacy policy page
├── styles.css          # Main stylesheet with dark theme
├── favicon.ico         # Favicon file
├── favicon.svg         # SVG favicon
├── images/             # Image assets
│   ├── apple-touch-icon.png
│   ├── favicon-16x16.png
│   ├── favicon-32x32.png
│   └── og-image.jpg    # Social media preview image
└── README.md           # This file
```

## Features

### Design
- **Dark Theme**: Modern dark color scheme (#0d1117 background, #c9d1d9 text, #58a6ff accent)
- **Responsive**: Fully responsive design that works on desktop, tablet, and mobile
- **Accessibility**: WCAG compliant with proper ARIA labels, alt text, and keyboard navigation
- **Performance**: Optimized for fast loading with minimal external dependencies

### Content Sections
1. **Hero Section**: Introduction with app mockup and call-to-action
2. **Overview**: Key benefits and features overview
3. **Features**: Detailed feature list with icons and descriptions
4. **Gallery**: App screenshots (SVG mockups for demonstration)
5. **Usage Guide**: Step-by-step instructions and pro tips
6. **Footer**: Contact information and links

### Technical Features
- Semantic HTML5 structure
- CSS Grid and Flexbox for layouts
- Smooth scrolling navigation
- Intersection Observer for animations
- Mobile-first responsive design
- SEO optimized with proper meta tags
- Social media preview support

## Deployment

### GitHub Pages Setup
1. Ensure your repository has GitHub Pages enabled
2. Set the source to the main branch and `/docs` folder
3. Your site will be available at `https://yourusername.github.io/repository-name/`

### Local Development
1. Clone the repository
2. Open `docs/index.html` in your browser, or
3. Use a local server: `python -m http.server 8000` in the docs directory
4. Navigate to `http://localhost:8000`

## Customization

### Colors
Edit the CSS custom properties in `styles.css`:
```css
:root {
    --color-bg-primary: #0d1117;    /* Background */
    --color-text-primary: #c9d1d9;   /* Main text */
    --color-accent: #58a6ff;         /* Accent color */
    /* ... more colors */
}
```

### Content
- Edit `index.html` for main content
- Edit `privacy-policy.html` for privacy policy
- Update social media URLs and links in the footer
- Replace placeholder images in the `images/` directory

### Branding
- Update the FuelUp logo and branding in both HTML files
- Modify the app description and feature lists
- Update contact information and social links

## Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Mobile browsers (iOS Safari, Chrome Mobile)
- Graceful degradation for older browsers

## Performance Optimizations
- Minimal external dependencies
- Optimized CSS with efficient selectors
- SVG icons for crisp display at all sizes
- Lazy loading for non-critical content
- Compressed assets (where applicable)

## Accessibility
- WCAG 2.1 AA compliance
- Keyboard navigation support
- Screen reader friendly
- High contrast ratios
- Focus indicators
- Skip links for navigation

## SEO Features
- Semantic HTML structure
- Meta descriptions and keywords
- Open Graph tags for social sharing
- Twitter Card support
- Structured data (where applicable)
- XML sitemap (generate separately)

## License
This website template is part of the FuelUp project. See the main repository license for details.

## Support
For questions about the website, please open an issue in the main repository or contact the development team.