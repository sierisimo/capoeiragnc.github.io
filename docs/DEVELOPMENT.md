# Development Guide

This document provides guidance for developers working on the Capoeira Ginga no Canavial website.

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd capoeira
   ```

2. **Install development dependencies** (optional)
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   # Option 1: Using npm script
   npm run dev
   
   # Option 2: Using Python
   python -m http.server 8000
   
   # Option 3: Using PHP
   php -S localhost:8000
   ```

## 📁 Project Structure

```
capoeira/
├── index.html                 # Main HTML file
├── assets/                    # Static assets
│   ├── css/
│   │   └── styles.css         # Main stylesheet (1126 lines)
│   ├── js/
│   │   └── script.js          # JavaScript functionality (438 lines)
│   └── images/                # All project images
│       ├── logo.png           # Academy logo
│       ├── hero.png           # Main hero image (renamed from 1.png)
│       ├── origins.png        # Origins section image
│       ├── descendents.png    # Lineage map image
│       ├── sport.png          # Sports activity image
│       └── self-defense.png   # Self-defense activity image
├── docs/                      # Documentation
│   └── DEVELOPMENT.md         # This file
├── README.md                  # Project documentation
├── package.json               # Node.js dependencies and scripts
└── .gitignore                 # Git ignore rules
```

## 🎨 Design System

### Color Palette
```css
:root {
    --primary-color: #d4af37;     /* Gold */
    --secondary-color: #1a1a1a;   /* Dark */
    --accent-color: #ff6b35;      /* Orange */
    --text-light: #666;           /* Light gray text */
    --bg-light: #f8f9fa;          /* Light background */
    --white: #ffffff;             /* White */
}
```

### Typography
- **Primary Font**: Poppins (Google Fonts)
- **Weights**: 300, 400, 500, 600, 700
- **Fallback**: sans-serif

### Responsive Breakpoints
- **Mobile**: max-width: 480px
- **Tablet**: max-width: 768px
- **Desktop**: 1200px and above

## 🛠️ Development Tools

### Available Scripts
```bash
npm run start      # Start development server
npm run dev        # Start development server with file watching
npm run validate   # Validate HTML, CSS, and JS
npm run format     # Format code with Prettier
npm run optimize   # Optimize images
```

### Code Style
- **HTML**: Semantic HTML5, proper indentation (4 spaces)
- **CSS**: BEM methodology, CSS Grid and Flexbox
- **JavaScript**: ES6+, vanilla JavaScript (no frameworks)

## 📱 Features Implementation

### 1. Responsive Navigation
- Mobile hamburger menu
- Smooth scrolling with header offset
- Active link highlighting

### 2. Interactive Elements
- Gallery lightbox functionality
- Form validation
- Scroll animations
- Parallax effects

### 3. Performance Optimizations
- Debounced scroll events
- Optimized images
- Efficient CSS animations
- Lazy loading considerations

## 🔧 Making Changes

### CSS Modifications
- All styles are in `assets/css/styles.css`
- Follow existing naming conventions
- Test responsiveness on all breakpoints
- Use CSS custom properties for consistency

### JavaScript Enhancements
- All scripts are in `assets/js/script.js`
- Maintain vanilla JavaScript approach
- Follow existing code patterns
- Add error handling for new features

### Image Updates
- Place new images in `assets/images/`
- Optimize images before adding
- Update alt text for accessibility
- Maintain consistent naming convention

## 🧪 Testing

### Manual Testing Checklist
- [ ] Test on mobile devices (320px-768px)
- [ ] Test on tablets (768px-1024px)
- [ ] Test on desktop (1024px+)
- [ ] Verify all links work correctly
- [ ] Test form submission
- [ ] Check gallery lightbox functionality
- [ ] Verify smooth scrolling
- [ ] Test navigation menu (mobile)

### Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 🚢 Deployment

### Static Hosting Options
1. **GitHub Pages**: Push to `gh-pages` branch
2. **Netlify**: Connect repository for automatic deployment
3. **Vercel**: Import project for instant deployment
4. **Traditional hosting**: Upload files via FTP

### Pre-deployment Checklist
- [ ] Validate all HTML/CSS/JS
- [ ] Optimize images
- [ ] Test all functionality
- [ ] Update contact information
- [ ] Verify all links work
- [ ] Check meta tags and SEO

## 🐛 Common Issues

### Image Loading Issues
- Verify image paths start with `assets/images/`
- Check image file extensions match exactly
- Ensure images exist in the correct directory

### CSS/JS Not Loading
- Verify paths start with `assets/css/` or `assets/js/`
- Check for typos in file names
- Ensure files exist in correct directories

### Mobile Menu Not Working
- Check JavaScript is loading correctly
- Verify hamburger click event is bound
- Test on actual mobile devices

## 📞 Support

For development questions or issues:
- Create an issue in the repository
- Contact: contacto@ginganocanavial.com
- Review existing documentation

---

*Happy coding! 🥋* 