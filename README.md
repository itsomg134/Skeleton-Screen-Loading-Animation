# Skeleton Screen Loading Animation

A modern, customizable skeleton loading component with a vibrant color-shifting shimmer effect. Built with pure HTML and CSS — no JavaScript required.

![Skeleton Screen Preview](preview.png)

## Features

- **Pure CSS** — Zero dependencies, just HTML and CSS
- **Colorful Shimmer** — Multi-color gradient animation that cycles through vibrant hues
- **Responsive Design** — Adapts seamlessly to different screen sizes
- **Content-Aware Layout** — Mirrors real content structure with:
  - Avatar placeholder
  - Title lines
  - Image pitchers (photo grids)
  - Text paragraphs
  - Meta information bars
  - Action badges
- **Accessible** — Respects reduced motion preferences
- **Dark Theme Optimized** — Colors pop against dark backgrounds

## Animation Details

The skeleton uses a sophisticated shimmer effect:
- **Gradient Colors**: Gold, pink, blue, green, orange, violet
- **Blend Mode**: `overlay` for vibrant color integration
- **Timing**: 2.4s infinite cycle with custom easing
- **Movement**: Smooth diagonal wave across elements

## Quick Start

1. Clone the repository:
```bash
git clone https://github.com/yourusername/skeleton-screen-animation.git
```

2. Open `index.html` in your browser

Or copy the code directly into your project:

```html
<!-- Copy the entire skeleton structure from index.html -->
```

## Usage Examples

### Basic Implementation
```html
<div class="skeleton avatar"></div>
<div class="skeleton line"></div>
<div class="skeleton pitcher"></div>
```

### Custom Skeleton Elements
```css
/* Add custom skeleton shapes */
.custom-card {
  width: 100%;
  height: 200px;
  border-radius: 16px;
}
```

## Customization

### Modify Shimmer Colors
Edit the gradient in the `.skeleton::after` rule:

```css
.skeleton::after {
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 215, 0, 0.4),    /* gold */
    rgba(255, 105, 180, 0.5),   /* pink */
    rgba(0, 191, 255, 0.5),     /* blue */
    transparent
  );
}
```

### Adjust Animation Speed
Change the `animation` duration:

```css
.skeleton::after {
  animation: colourShimmer 1.5s infinite; /* faster */
  /* or */
  animation: colourShimmer 3.5s infinite; /* slower */
}
```

### Light Theme Variant
For light backgrounds, adjust the base color and blend mode:

```css
.skeleton {
  background: rgba(0, 0, 0, 0.05);
}

.skeleton::after {
  mix-blend-mode: screen; /* better for light backgrounds */
}
```

## Component Structure

```
Card Container
├── Header
│   ├── Avatar (circle)
│   └── Title Lines (2 lines)
├── Pitcher Grid
│   ├── 3 Square Images
│   └── Mixed Aspect Row
├── Text Block (4 lines)
├── Meta Row
│   ├── Icon + Text (2x)
│   └── Badge
└── Timestamp Line
```

## Use Cases

- **Content Loading States** — Show while fetching data
- **Image Galleries** — Perfect for photo-heavy interfaces
- **Profile Pages** — Avatar and user info loading
- **E-commerce** — Product card placeholders
- **Blog Posts** — Article preview skeletons

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Opera (latest)
- Mobile browsers

##  Performance

- **File Size**: < 5KB minified
- **Render Performance**: Hardware-accelerated animations
- **No Layout Shift**: Fixed dimensions prevent content jumping

##  Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Share color scheme variations

##  License

MIT License — feel free to use in personal and commercial projects.
