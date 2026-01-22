# 🎨 Serenity Animations

> **Production-ready CSS animation library featuring 20+ smooth, GPU-accelerated animations including fadeIn, pulse, shimmer, float, and more. Zero dependencies, mobile-optimized, respects prefers-reduced-motion. Built for performance and user experience.**

[![Version](https://img.shields.io/badge/version-2.2.1-blue.svg)](https://github.com/syntaxserenity-dev/serenity-animations)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![CSS3](https://img.shields.io/badge/CSS-3-1572B6.svg)](https://www.w3.org/Style/CSS/)
[![Browser Support](https://img.shields.io/badge/browsers-modern-success.svg)](#browser-support)
[![Made with Love](https://img.shields.io/badge/made%20with-❤️-red.svg)](https://www.syntaxserenity.co.ao)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Quick Start](#-quick-start)
- [Installation](#-installation)
- [Usage](#-usage)
- [Animation Catalog](#-animation-catalog)
- [Customization](#-customization)
- [Performance](#-performance)
- [Browser Support](#-browser-support)
- [Examples](#-examples)
- [Best Practices](#-best-practices)
- [Contributing](#-contributing)
- [License](#-license)
- [Credits](#-credits)

---

## 🎯 Overview

**Serenity Animations** is a meticulously crafted CSS animation library that provides a collection of smooth, performant, and reusable animations for modern web applications. Built with performance and developer experience in mind, this library offers everything from subtle micro-interactions to eye-catching visual effects.

### 🌟 Why Serenity Animations?

- **🚀 Performance-First**: All animations use GPU-accelerated properties (transform, opacity)
- **📱 Mobile-Optimized**: Tested and optimized for mobile devices and touch interfaces
- **♿ Accessible**: Respects `prefers-reduced-motion` for better accessibility
- **🎨 Comprehensive**: 20+ carefully designed animations for every use case
- **📦 Lightweight**: Zero dependencies, pure CSS3
- **🔧 Customizable**: Easy to extend and modify via CSS variables
- **📖 Well-Documented**: Detailed documentation with usage examples

---

## ✨ Features

### 🎭 Animation Categories

#### 🌊 Entrance Animations
- **fadeIn** - Gentle scale and fade entrance
- **fadeInUp** - Slide up with fade effect
- **slideInLeft** - Slide from left with fade
- **slideInRight** - Slide from right with fade
- **slideIn** - Quick slide entrance
- **dropdownFadeIn** - Optimized for dropdown menus

#### 🌅 Exit Animations
- **fadeOut** - Smooth scale and fade exit
- **fadeInScroll** - Subtle scroll-triggered fade

#### 🔄 Continuous Animations
- **pulse** - Expanding pulse effect
- **pulse-soft** - Gentle pulsation
- **pulse-strong** - Dramatic pulsation
- **float** - Floating with rotation
- **floatRotateY** - 3D floating effect
- **rotate** - 360° continuous rotation
- **blink** - Intermittent blinking

#### ✨ Visual Effects
- **shimmer** - Horizontal shimmer effect
- **shine** - Light reflection sweep
- **mirror-reflection** - Diagonal mirror effect
- **colorWave** - Gradient color wave
- **gradientSlide** - Vertical gradient movement

### 🛠️ Technical Features

- ✅ **GPU-Accelerated** - Uses `transform` and `opacity` for optimal performance
- ✅ **No Reflow/Repaint** - Animations don't trigger layout recalculations
- ✅ **Responsive** - Works seamlessly across all screen sizes
- ✅ **Modular** - Use only what you need
- ✅ **BEM Compatible** - Follows naming conventions
- ✅ **Framework Agnostic** - Works with React, Vue, Angular, vanilla JS

---

## 🚀 Quick Start

### CDN (Fastest)

```html
<!-- Add to your HTML <head> -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/syntaxserenity/serenity-animations@latest/animations.css">
```

### Basic Usage

```html
<!-- Apply animation to any element -->
<div class="my-element" style="animation: fadeInUp 0.6s ease-out;">
  Content appears with smooth animation
</div>

<!-- Using inline styles -->
<button style="animation: pulse-soft 2s ease-in-out infinite;">
  Pulsing Button
</button>

<!-- With CSS class -->
<style>
  .animated-card {
    animation: fadeIn 0.4s ease-out;
  }
  
  .animated-card:hover {
    animation: float 3s ease-in-out infinite;
  }
</style>

<div class="animated-card">
  Hover me!
</div>
```

---

## 📦 Installation

### Option 1: NPM

```bash
npm install @syntaxserenity/animations
```

```css
/* In your CSS/SCSS */
@import '@syntaxserenity/animations';
```

### Option 2: Download

1. Download `animations.css` from [releases](https://github.com/syntaxserenity-dev/serenity-animations/releases)
2. Place in your project's CSS directory
3. Import in your HTML:

```html
<link rel="stylesheet" href="css/animations.css">
```

### Option 3: Copy-Paste

Copy the animations you need directly from [animations.css](animations.css) into your stylesheet.

---

## 💡 Usage

### Basic Syntax

```css
.element {
  animation: [animation-name] [duration] [timing-function] [delay] [iteration-count] [direction] [fill-mode];
}
```

### Common Patterns

#### Single Animation

```css
.fade-in-element {
  animation: fadeIn 0.5s ease-out;
}
```

#### Multiple Animations

```css
.complex-animation {
  animation: 
    fadeInUp 0.6s ease-out,
    pulse-soft 2s ease-in-out 0.6s infinite;
}
```

#### With Animation Events (JavaScript)

```javascript
const element = document.querySelector('.animated');

element.addEventListener('animationstart', () => {
  console.log('Animation started!');
});

element.addEventListener('animationend', () => {
  console.log('Animation completed!');
  // Do something after animation
});
```

#### Dynamic Animations

```javascript
function animateElement(element, animationName) {
  element.style.animation = `${animationName} 0.5s ease-out`;
  
  element.addEventListener('animationend', function() {
    element.style.animation = '';
  }, { once: true });
}

// Usage
animateElement(document.querySelector('.card'), 'fadeInUp');
```

---

## 🎨 Animation Catalog

### 📥 Entrance Animations

#### fadeIn
**Purpose**: Gentle entrance with scale and fade  
**Best For**: Modals, tooltips, cards  
**Recommended Settings**: `0.3s - 0.6s ease-out`

```css
.modal {
  animation: fadeIn 0.4s ease-out;
}
```

#### fadeInUp
**Purpose**: Slide up from bottom with fade  
**Best For**: Page sections, list items, cards  
**Recommended Settings**: `0.4s - 0.8s ease-out`

```css
.section {
  animation: fadeInUp 0.6s ease-out;
}
```

#### slideInLeft / slideInRight
**Purpose**: Horizontal slide entrance  
**Best For**: Sidebars, navigation, alternating content  
**Recommended Settings**: `0.5s - 0.8s ease-out`

```css
.sidebar {
  animation: slideInLeft 0.6s ease-out;
}

.content {
  animation: slideInRight 0.6s ease-out;
}
```

### 📤 Exit Animations

#### fadeOut
**Purpose**: Smooth exit with scale reduction  
**Best For**: Dismissing modals, removing notifications  
**Recommended Settings**: `0.2s - 0.4s ease-in`

```css
.notification.closing {
  animation: fadeOut 0.3s ease-in forwards;
}
```

### 🔄 Continuous Animations

#### pulse / pulse-soft / pulse-strong
**Purpose**: Attention-grabbing pulsation  
**Best For**: Badges, notifications, CTAs  
**Recommended Settings**: `1.5s - 3s ease-in-out infinite`

```css
/* Subtle pulse */
.notification-badge {
  animation: pulse-soft 2s ease-in-out infinite;
}

/* Strong pulse for urgency */
.alert-badge {
  animation: pulse-strong 1.5s ease-in-out infinite;
}
```

#### float / floatRotateY
**Purpose**: Gentle floating motion  
**Best For**: Icons, illustrations, decorative elements  
**Recommended Settings**: `3s - 6s ease-in-out infinite`

```css
.floating-icon {
  animation: float 4s ease-in-out infinite;
}

/* With 3D effect (requires perspective on parent) */
.phone-mockup {
  animation: floatRotateY 5s ease-in-out infinite;
}
```

#### rotate
**Purpose**: 360° continuous rotation  
**Best For**: Loaders, spinners, refresh icons  
**Recommended Settings**: `1s - 2s linear infinite`

```css
.spinner {
  animation: rotate 1s linear infinite;
}
```

### ✨ Visual Effects

#### shimmer
**Purpose**: Loading shimmer effect  
**Best For**: Skeleton screens, loading states  
**Recommended Settings**: `1.5s - 2.5s linear infinite`

```css
.skeleton-loader::after {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  height: 100%;
  width: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
  animation: shimmer 2s linear infinite;
}
```

#### shine
**Purpose**: Light reflection sweep  
**Best For**: Buttons, cards, hover effects  
**Recommended Settings**: `0.6s - 1.2s ease-in-out`

```css
.premium-button {
  position: relative;
  overflow: hidden;
}

.premium-button::before {
  content: '';
  position: absolute;
  top: 0;
  left: -75%;
  width: 50%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255,255,255,0.4), transparent);
  animation: shine 1s ease-in-out;
}

.premium-button:hover::before {
  animation: shine 1s ease-in-out;
}
```

#### colorWave / gradientSlide
**Purpose**: Animated gradient backgrounds  
**Best For**: Hero sections, premium buttons  
**Recommended Settings**: `3s - 6s ease-in-out infinite`

```css
.gradient-bg {
  background: linear-gradient(45deg, #667eea 0%, #764ba2 100%);
  background-size: 200% 200%;
  animation: colorWave 5s ease-in-out infinite;
}
```

---

## 🎛️ Customization

### Using CSS Variables

Define your own timing and easing:

```css
:root {
  --animation-duration-fast: 0.2s;
  --animation-duration-normal: 0.4s;
  --animation-duration-slow: 0.8s;
  
  --animation-easing-smooth: cubic-bezier(0.4, 0, 0.2, 1);
  --animation-easing-bounce: cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.custom-element {
  animation: fadeIn var(--animation-duration-normal) var(--animation-easing-smooth);
}
```

### Creating Animation Classes

```css
/* Utility classes for common patterns */
.animate-fade-in {
  animation: fadeIn 0.4s ease-out;
}

.animate-slide-up {
  animation: fadeInUp 0.6s ease-out;
}

.animate-pulse {
  animation: pulse-soft 2s ease-in-out infinite;
}

/* With delays */
.delay-100 { animation-delay: 0.1s; }
.delay-200 { animation-delay: 0.2s; }
.delay-300 { animation-delay: 0.3s; }

/* Usage */
.card {
  opacity: 0; /* Start invisible */
}

.card.visible {
  opacity: 1;
  animation: fadeInUp 0.6s ease-out;
}
```

### Extending Animations

```css
/* Create variations */
@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translateY(-20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInTop {
  from {
    opacity: 0;
    transform: translateY(-100px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
```

---

## ⚡ Performance

### Performance Best Practices

✅ **DO:**
- Use `transform` and `opacity` (GPU-accelerated)
- Apply `will-change` for complex animations
- Remove animations when not visible (`display: none`)
- Use `animation-fill-mode: forwards` to prevent reflows

❌ **DON'T:**
- Animate `width`, `height`, `top`, `left` (causes reflow)
- Use too many simultaneous animations
- Forget to remove `will-change` after animation
- Animate on scroll without throttling/debouncing

### Optimization Tips

```css
/* Use will-change for complex animations */
.complex-element {
  will-change: transform, opacity;
  animation: floatRotateY 5s ease-in-out infinite;
}

/* Remove will-change after animation */
.complex-element {
  animation: fadeIn 0.5s ease-out forwards;
}

.complex-element.animation-complete {
  will-change: auto;
}
```

```javascript
// Remove will-change after animation
element.addEventListener('animationend', () => {
  element.style.willChange = 'auto';
});
```

### Performance Monitoring

```javascript
// Measure animation performance
const observer = new PerformanceObserver((list) => {
  for (const entry of list.getEntries()) {
    console.log('Animation duration:', entry.duration);
  }
});

observer.observe({ entryTypes: ['measure'] });

performance.mark('animation-start');
// ... animation happens ...
performance.mark('animation-end');
performance.measure('animation', 'animation-start', 'animation-end');
```

---

## 🌐 Browser Support

| Browser | Version | Status |
|---------|---------|--------|
| Chrome | 90+ | ✅ Full Support |
| Firefox | 88+ | ✅ Full Support |
| Safari | 14+ | ✅ Full Support |
| Edge | 90+ | ✅ Full Support |
| Opera | 76+ | ✅ Full Support |
| Samsung Internet | 14+ | ✅ Full Support |

### Fallback for Older Browsers

```css
/* Disable animations for older browsers */
@supports not (animation: fadeIn 1s) {
  * {
    animation: none !important;
    transition: none !important;
  }
}
```

### Accessibility: Reduced Motion

```css
/* Respect user preferences */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 📚 Examples

### Example 1: Staggered List Animation

```html
<ul class="staggered-list">
  <li style="animation-delay: 0s;">Item 1</li>
  <li style="animation-delay: 0.1s;">Item 2</li>
  <li style="animation-delay: 0.2s;">Item 3</li>
  <li style="animation-delay: 0.3s;">Item 4</li>
</ul>

<style>
.staggered-list li {
  opacity: 0;
  animation: fadeInUp 0.5s ease-out forwards;
}
</style>
```

### Example 2: Loading Skeleton

```html
<div class="skeleton-card">
  <div class="skeleton-image"></div>
  <div class="skeleton-text"></div>
  <div class="skeleton-text short"></div>
</div>

<style>
.skeleton-image,
.skeleton-text {
  position: relative;
  background: #e0e0e0;
  overflow: hidden;
}

.skeleton-image::after,
.skeleton-text::after {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  height: 100%;
  width: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.5),
    transparent
  );
  animation: shimmer 2s infinite;
}
</style>
```

### Example 3: Attention-Grabbing CTA

```html
<button class="cta-button">
  <span>Get Started</span>
  <div class="shine-effect"></div>
</button>

<style>
.cta-button {
  position: relative;
  overflow: hidden;
  animation: pulse-soft 3s ease-in-out infinite;
}

.cta-button .shine-effect {
  position: absolute;
  top: 0;
  left: -75%;
  width: 50%;
  height: 100%;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.3),
    transparent
  );
}

.cta-button:hover .shine-effect {
  animation: shine 0.8s ease-in-out;
}
</style>
```

### Example 4: Scroll-Triggered Animations

```javascript
// Intersection Observer for scroll animations
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.style.animation = 'fadeInUp 0.6s ease-out';
      observer.unobserve(entry.target);
    }
  });
}, {
  threshold: 0.1
});

// Observe all elements with .animate-on-scroll
document.querySelectorAll('.animate-on-scroll').forEach(el => {
  observer.observe(el);
});
```

---

## 📖 Best Practices

### 1. **Choose the Right Duration**

```css
/* Quick interactions */
.button { animation: fadeIn 0.2s ease-out; }

/* Standard transitions */
.card { animation: fadeInUp 0.4s ease-out; }

/* Attention-grabbing */
.notification { animation: pulse-soft 2s ease-in-out infinite; }

/* Ambient animations */
.background { animation: colorWave 6s ease-in-out infinite; }
```

### 2. **Use Appropriate Easing**

```css
/* Entrance: ease-out (starts fast, ends slow) */
.entering { animation: fadeIn 0.4s ease-out; }

/* Exit: ease-in (starts slow, ends fast) */
.exiting { animation: fadeOut 0.3s ease-in; }

/* Both: ease-in-out (smooth start and end) */
.floating { animation: float 3s ease-in-out infinite; }

/* Consistent: linear (no acceleration) */
.rotating { animation: rotate 2s linear infinite; }
```

### 3. **Limit Simultaneous Animations**

```javascript
// ❌ Bad: Too many animations at once
document.querySelectorAll('.item').forEach(item => {
  item.style.animation = 'fadeInUp 0.5s ease-out';
});

// ✅ Good: Stagger animations
document.querySelectorAll('.item').forEach((item, index) => {
  item.style.animation = `fadeInUp 0.5s ease-out ${index * 0.1}s`;
});
```

### 4. **Clean Up After Animations**

```javascript
element.addEventListener('animationend', function cleanup() {
  element.style.animation = '';
  element.style.willChange = 'auto';
  element.removeEventListener('animationend', cleanup);
});
```

### 5. **Consider Mobile Performance**

```css
/* Reduce animations on mobile if needed */
@media (max-width: 768px) {
  .complex-animation {
    animation-duration: 0.3s; /* Faster on mobile */
  }
  
  .heavy-animation {
    animation: none; /* Disable on mobile */
  }
}
```

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup

```bash
# Clone the repository
git clone https://github.com/syntaxserenity-dev/serenity-animations.git

# Create a feature branch
git checkout -b feature/new-animation

# Make your changes and commit
git commit -m "Add new animation: bounceIn"

# Push and create a pull request
git push origin feature/new-animation
```

### Adding a New Animation

1. Add the `@keyframes` definition to `animations.css`
2. Include comprehensive documentation (purpose, use cases, recommended settings)
3. Add examples to the README
4. Test across browsers
5. Submit a pull request

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Syntax Serenity

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software...
```

---

## 🏆 Credits

**Developed by [Syntax Serenity](https://www.syntaxserenity.co.ao)**

- 🌐 Website: https://www.syntaxserenity.co.ao
- 📧 Email: fs.developerfullstack@gmail.com
- 🐙 GitHub: [@SyntaxSerenity-dev](https://github.com/SyntaxSerenity-dev)

### Development Team

- **Fanilton F. Samuel** - Lead Developer
- **Palanca Wilson** - Developer

---

## 🌟 Showcase

Projects using Serenity Animations:

- [KENDAAGRO](https://www.kendaagro.co.ao) - Agricultural logistics platform
- _(Submit your project via PR!)_

---

## 📞 Support

- 📧 Email: fs.developerfullstack@gmail.com
- 🐛 Issues: [GitHub Issues](https://github.com/syntaxserenity-dev/serenity-animations/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/syntaxserenity-dev/serenity-animations/discussions)

---

## ⭐ Show Your Support

If this library helped your project, please consider:

- ⭐ **Starring** the repository
- 🐦 **Sharing** on social media
- 🤝 **Contributing** improvements
- ☕ **Supporting** via [Buy Me a Coffee](https://buymeacoffee.com/syntaxserenity)

---

<div align="center">

**Made with ❤️ by [Syntax Serenity](https://www.syntaxserenity.co.ao)**

[![Star on GitHub](https://img.shields.io/github/stars/syntaxserenity/serenity-animations.svg?style=social)](https://github.com/syntaxserenity-dev/serenity-animations)

</div>
