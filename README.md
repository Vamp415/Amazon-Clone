# Amazon Clone

> A responsive, static e-commerce UI clone inspired by Amazon's design, featuring product showcases, hero sliders, and mobile-first responsive layout.

---

## Table of Contents

- [Live URL](#live-url)
- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Local Setup](#local-setup)
- [Docker Deployment](#docker-deployment)
- [Customization](#customization)
- [Browser Support](#browser-support)
- [License](#license)

---

## Live URL

**🌐 https://amazonclone.thinkpixel.org/**

The live version of this project is hosted and powered by Think Pixel.

---

## Overview

Amazon Clone is a static frontend implementation that replicates the visual design and user interface of Amazon's e-commerce platform. The project demonstrates responsive web design principles, CSS grid/flexbox layouts, and vanilla JavaScript for interactive components. It serves as a reference implementation for e-commerce UI patterns and responsive design techniques.

The website features a hero image slider, product category sections, horizontal product carousels, promotional banners, and a comprehensive footer layout - all implemented using pure HTML, CSS, and JavaScript without any external frameworks or dependencies.

---

## Features

### Implemented Features

- **Hero Image Slider**: Interactive carousel with navigation controls (6 promotional images)
- **Responsive Navigation**: Multi-level header with search, cart, and account sections
- **Product Category Grid**: 4-column responsive layout for category displays (12 categories across 3 rows)
- **Horizontal Product Carousels**: Scrollable product showcases with wheel-based navigation
- **Product Cards with Pricing**: Discount badges, deal tags, and pricing display
- **Responsive Footer**: Multi-column footer with links and legal information
- **Mobile-First Design**: Optimized layouts for phones, tablets, and desktops
- **Google Fonts Integration**: Outfit font family for modern typography
- **Smooth Scrolling**: Horizontal scroll interactions for product sections

### UI Components

- Navigation bar with logo, location selector, search, language, account, and cart
- Secondary navigation with category menu and quick links
- Hero slider with previous/next navigation controls
- Category boxes with images and "Shop More" links
- Product sliders with image-only displays
- Product cards with pricing, discounts, and deal badges
- Comprehensive footer with 4-column layout

---

## Technology Stack

- **HTML5**: Semantic markup and structure
- **CSS3**: Styling with Flexbox, responsive design, and media queries
- **Vanilla JavaScript**: Slider logic and scroll interactions (no frameworks)
- **Google Fonts**: Outfit font family
- **Docker**: Nginx-based containerization for deployment

---

## Project Structure

```
Amazon-Clone/
├── index.html          # Main HTML file
├── css/
│   └── style.css      # All styling and responsive design
├── js/
│   └── script.js      # Slider and scroll interactions
├── assets/            # Images and static assets
│   ├── amazon_logo.png
│   ├── header1.jpg - header6.jpg    # Hero slider images
│   ├── box1-1.jpg - box3-4.jpg      # Category box images
│   ├── product1-1.jpg - product2-12.jpg  # Product images
│   └── [icons and UI elements]
├── Dockerfile         # Nginx container configuration
├── LICENSE           # MIT License
└── README.md         # Project documentation
```

---

## Local Setup

### Prerequisites

- A web browser (Chrome, Firefox, Safari, Edge)
- A local web server (optional, but recommended)

### Option 1: Direct File Opening

1. Clone the repository:
   ```bash
   git clone https://github.com/Vamp415/Amazon-Clone.git
   cd Amazon-Clone
   ```

2. Open `index.html` directly in your browser

### Option 2: Using a Local Server

Using Python:
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Using Node.js (http-server):
```bash
npx http-server
```

Using PHP:
```bash
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

---

## Docker Deployment

### Build and Run with Docker

1. Build the Docker image:
   ```bash
   docker build -t amazon-clone .
   ```

2. Run the container:
   ```bash
   docker run -d -p 8080:80 amazon-clone
   ```

3. Access the site at `http://localhost:8080`

### Docker Compose (Optional)

Create a `docker-compose.yml` file:

```yaml
version: '3'
services:
  web:
    build: .
    ports:
      - "8080:80"
    restart: unless-stopped
```

Run with:
```bash
docker-compose up -d
```

---

## Customization

### Changing Images

Replace images in the `assets/` directory with your own. Maintain the same filenames to avoid updating HTML references:

- Hero banners: `header1.jpg` through `header6.jpg`
- Category images: `box1-1.jpg` through `box3-4.jpg`
- Product images: `product1-1.jpg` through `product2-12.jpg`

### Modifying Colors

Edit `css/style.css` to customize the color scheme:

- Header background: `.nav` (currently `#131921`)
- Secondary nav: `.nav-bottom` (currently `#232f3e`)
- Accent color: `.nav-search-icon` (currently `#ffd64f`)
- Deal badges: `.product-offer p` (currently `#be0b3b`)

### Adding/Removing Products

Edit the corresponding sections in `index.html`:

- For image-only products: Add `<img>` tags in `.products` divs
- For product cards with pricing: Add `.product-card` divs with the required structure

### Responsive Breakpoints

Modify media queries in `css/style.css`:

- Desktop: `min-width: 1200px`
- Tablet: `768px` to `1199px`
- Large phones: `576px` to `767px`
- Small phones: `max-width: 575px`

---

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Credits

Created as a static frontend demonstration of responsive e-commerce UI patterns using vanilla HTML, CSS, and JavaScript.
