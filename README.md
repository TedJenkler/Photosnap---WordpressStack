# Photosnap - WordPress Stack

## Table of Contents
1. [Breakpoints](#breakpoints)
2. [Cross-Browser Testing](#cross-browser-testing)
3. [Fluid Layouts](#fluid-layouts)
4. [Mobile-First](#mobile-first)
5. [Performance Optimization](#performance-optimization)
   - [Image Optimization](#image-optimization)
   - [Font Optimization](#font-optimization)
   - [Lazy Loading and JavaScript Optimization](#lazy-loading-and-javascript-optimization)
6. [Accessibility (a11y)](#accessibility-a11y)
   - [Keyboard Navigation](#keyboard-navigation)
   - [ARIA Roles](#aria-roles)
   - [Alt Text for Images](#alt-text-for-images)

---

## Breakpoints

These are the breakpoints used in the project, targeting various device screen widths:

- **414px**: Small smartphones (portrait)
- **480px**: Smaller smartphones (portrait)
- **540px**: Small-medium smartphones
- **600px**: Larger smartphones or small tablets (portrait)
- **640px**: iPhones (landscape)
- **800px**: Small tablets (landscape)
- **1024px**: Tablets (portrait) or small laptops
- **1200px**: Desktop or large tablets
- **1280px**: Standard laptops or desktops
- **1366px**: Laptops or small desktops
- **1600px**: Large desktops or wide laptops
- **1920px**: Full HD monitors
- **2560px**: Ultra-wide or 4K displays

## Cross-Browser Testing

I ensured consistent design performance across **Mozilla Firefox**, **Google Chrome**, and **Microsoft Edge**, focusing on different viewport widths for each browser.

- **Mozilla Firefox**: Firefox showed a slightly wider desktop screen due to a smaller scrollbar, so I adjusted the layout to account for this.
- **Google Chrome**: Chrome displayed a larger scrollbar, which resulted in a slightly narrower desktop viewport, requiring small layout tweaks.

I applied **browser-specific CSS prefixes** and tested the design across mobile and desktop versions to ensure optimal rendering on all platforms.

## Fluid Layouts

In this project, I have ensured that the layout is fully responsive and adapts smoothly to different screen sizes. For a pixel-perfect design, I focused on three key breakpoints: mobile (375px), tablet (768px), and desktop (1440px). 

To achieve fluidity across all screen sizes, I used **percentage-based widths**, **Flexbox**, and **CSS Grid** to create flexible layouts. These techniques allow elements to scale and adjust based on the available screen space, ensuring the design remains consistent and functional.

Moreover, I utilized **root calculations** (`rem` and `em` units) to maintain consistent spacing, font sizes, and other elements across all devices, ensuring a seamless, fluid experience regardless of screen size.

## Mobile-First

In this project, I followed a **Mobile-First** approach, designing for the smallest screens first and progressively enhancing the layout for larger devices. This strategy ensures that the core functionality and design work seamlessly on mobile devices, providing an optimal user experience even on constrained screen sizes.

Once the mobile layout was perfected, I used **media queries** to progressively enhance the design for larger screen sizes such as tablets (768px) and desktops (1440px). At each breakpoint, the layout adjusts smoothly, adding or expanding elements to take advantage of the larger screen real estate. This ensures that the design remains consistent, functional, and visually appealing across all device sizes.

---

## Performance Optimization

### Image Optimization

To enhance performance, I prioritized **image optimization** throughout the project. All images were compressed by converting them from PNG to the modern **WebP** format, significantly reducing file sizes while maintaining high-quality visuals. This optimization saved substantial storage space and improved page loading times.

For vector graphics, I retained **SVG** for icons due to their scalability and minimal file size. SVGs are ideal for responsive designs as they adapt to different resolutions without losing quality. By combining WebP for raster images and SVG for icons, the site achieves an optimal balance of performance and visual fidelity.

### Font Optimization

To enhance site performance, I focused on **Font Optimization** by preloading custom fonts and ensuring they load asynchronously. This approach reduces render-blocking issues and improves page speed significantly.

1. **Custom Fonts Preloaded**:  
   - The primary font, **DM Sans**, is preloaded using `<link rel="preload">`. This ensures that the font begins downloading early in the page lifecycle without delaying rendering.  

2. **Asynchronous Loading**:  
   - Fonts are loaded asynchronously with a backup mechanism. A `<noscript>` fallback is added for users with JavaScript disabled to maintain compatibility.

3. **Backup System**:  
   - System fonts are used as fallbacks during the initial render to avoid blank or invisible text (FOIT).

These optimizations resulted in **significant speed improvements**, as verified by tools like Google Lighthouse and PageSpeed Insights. Render-blocking delays caused by custom font loading were eliminated while maintaining the visual integrity of the design.

### Lazy Loading and JavaScript Optimization

To enhance site performance, I optimized the loading of JavaScript by using the `defer` attribute, which improves load times and overall user experience.

1. **JavaScript Deferred Loading**:  
   - I applied the `defer` attribute to non-critical JavaScript files, ensuring they load after the page content is parsed. This reduces render-blocking and allows the page to become interactive faster.

This optimization resulted in faster page load times and improved performance metrics, contributing to a better user experience.

---

## Accessibility (a11y)

### Keyboard Navigation

- I have ensured that all links are tabbable, allowing users to easily navigate through the site.

### ARIA Roles

- I have added `aria` labels on my custom components, like pricing, to improve accessibility for screen readers and assistive technologies.

### Alt Text for Images

- I have added `alt` text on all images that aren't used as background images, ensuring that screen readers can interpret them for better accessibility.
