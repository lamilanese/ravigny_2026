# Claude Design System: Modern, Clean, Slightly Mystical Aesthetic

## Overview
This guide provides principles and techniques for creating HTML + CSS interfaces that embody a modern, clean, and slightly mystical feel. Use these guidelines to craft experiences that feel sophisticated, calming, and subtly enchanting.

---

## Core Design Principles

### 1. **Color Philosophy**
- **Primary Palette**: Light blues (e.g., rgb(180, 251, 250), rgb(200, 252, 251), rgb(160, 250, 248);)
- **Accent Colors**: Soft lavenders, periwinkles, and muted purples (`#9370db`, `#dda0dd`, `#ba55d3`)
- **Text Colors**: Light grays with slight blue tints (`#e0e0e0`, `#c0c0d8`, `#b8b8d0`)
- **Avoid**: Pure blacks, harsh whites, saturated neons
- **Prefer**: Gradients over solid colors, especially for backgrounds and text

### 2. **Spacing & Whitespace**
- Use generous spacing (60px+ margins, 40px+ padding)
- Let content breathe—never crowd elements
- Consistent rhythm: multiples of 5 or 10 for margins and padding
- Increase line-height to 1.6-1.8 for readability and elegance

### 3. **Typography**
- **Font Choice**: System fonts or clean sans-serifs (`-apple-system`, `'Segoe UI'`, `system-ui`)
- **Weight**: Prefer light to regular weights (300-400); use 600+ sparingly
- **Letter Spacing**: Increase for headers (2-8px) to create airiness
- **Size Scale**: Use a clear hierarchy (e.g., 4rem → 2rem → 1.2rem → 1rem)
- **Text Effects**: Gradient text fills, subtle glows, semi-transparent colors

---

## Mystical Elements

### 4. **Background Treatments**
```css
/* Multi-layered gradients */
background: linear-gradient(135deg, #0a0e27 0%, #1a1a2e 50%, #16213e 100%);

/* Radial gradient overlays */
background: radial-gradient(circle, rgba(138, 43, 226, 0.1) 0%, transparent 50%);

/* Animated atmospheric effects */
animation: mysticalPulse 15s ease-in-out infinite;
```

### 5. **Glass Morphism**
- Use `backdrop-filter: blur(20px)` for frosted glass effects
- Combine with semi-transparent backgrounds: `rgba(26, 26, 46, 0.6)`
- Add subtle borders: `1px solid rgba(147, 112, 219, 0.2)`
- Layer multiple shadows for depth

### 6. **Glow Effects**
```css
/* Text glow */
filter: drop-shadow(0 0 20px rgba(147, 112, 219, 0.5));

/* Box glow */
box-shadow: 0 0 40px rgba(147, 112, 219, 0.2);

/* Animated glow */
@keyframes glow {
    0%, 100% { filter: drop-shadow(0 0 20px rgba(147, 112, 219, 0.5)); }
    50% { filter: drop-shadow(0 0 40px rgba(147, 112, 219, 0.8)); }
}
```

### 7. **Particle Effects**
- Small floating orbs with `border-radius: 50%`
- Use `position: fixed` with low z-index
- Animate with slow, organic movements (15-25s duration)
- Keep opacity low (0.3-0.7) for subtlety
- Use `pointer-events: none` to avoid interference

---

## Animation Guidelines

### 8. **Movement Philosophy**
- **Slow & Organic**: 0.3s to 3s transitions; avoid snappy animations
- **Ease Functions**: `ease-in-out` or custom cubic-bezier curves
- **Floating**: Combine translateX, translateY, and opacity
- **Pulsing**: Gentle scale and opacity changes (1.0 to 1.1 scale max)
- **Entrance Animations**: Fade + slide from below or above

### 9. **Hover States**
```css
transition: all 0.3s ease;

/* Lift effect */
&:hover {
    transform: translateY(-5px);
    box-shadow: 0 30px 80px rgba(0, 0, 0, 0.6);
}

/* Glow enhancement */
&:hover {
    border-color: rgba(147, 112, 219, 0.4);
    box-shadow: 0 0 40px rgba(147, 112, 219, 0.3);
}
```

---

## Component Patterns

### 10. **Cards**
- Rounded corners: 15-25px border-radius
- Semi-transparent backgrounds with backdrop blur
- Layered shadows (outer + inset)
- Subtle border with low opacity
- Hover: lift + enhanced glow

### 11. **Buttons**
- Rounded (50px border-radius for pill shape)
- Gradient backgrounds
- Generous padding (18px 45px)
- Letter spacing: 2px
- Shadow: colored to match gradient
- Hover: lift + brighter gradient + stronger shadow

### 12. **Text Gradients**
```css
background: linear-gradient(135deg, #9370db, #dda0dd, #ba55d3);
-webkit-background-clip: text;
-webkit-text-fill-color: transparent;
background-clip: text;
```

---

## Layout Principles

### 13. **Structure**
- Center content with max-width (900-1200px)
- Use CSS Grid for feature sections
- Maintain vertical rhythm with consistent spacing
- Single-column layouts for focus; multi-column for features

### 14. **Responsive Behavior**
- Mobile-first approach
- Reduce font sizes proportionally on smaller screens
- Stack grid items on mobile
- Maintain mystical effects but reduce complexity if needed

---

## Atmosphere Building

### 15. **Layering Technique**
1. **Base layer**: Deep gradient background
2. **Ambient layer**: Animated radial gradients (::before pseudo-element)
3. **Particle layer**: Fixed-position floating elements
4. **Content layer**: Cards and text with high z-index
5. **Effect layer**: Glows and shadows

### 16. **Depth Creation**
- Multiple box-shadows at different blur radii
- Inset shadows for inner highlights
- Transform-based lifting on interaction
- Backdrop filters for separation

### 17. **Mystical Touches**
- Subtle animations everywhere (but not overwhelming)
- Organic, flowing movements (never linear)
- Ethereal color transitions
- Symbols and icons with glow effects (✨🌙🔮⭐🌟)
- Mysterious language ("realm", "dimension", "transcend", "ethereal")

---

## Technical Best Practices

### 18. **Performance**
- Use `transform` and `opacity` for animations (GPU-accelerated)
- Set `will-change` sparingly for heavy animations
- Use `pointer-events: none` on decorative elements
- Optimize backdrop-filter usage (can be expensive)

### 19. **Accessibility**
- Maintain sufficient contrast ratios (check with tools)
- Provide reduced-motion alternatives: `@media (prefers-reduced-motion: reduce)`
- Don't rely solely on color for information
- Ensure text remains readable over animated backgrounds

### 20. **Browser Compatibility**
- Include vendor prefixes for backdrop-filter
- Test gradients in multiple browsers
- Provide fallbacks for older browsers
- Use feature queries when needed

---

## Quick Reference: Mystical Color Palette

```css
/* Dark Backgrounds */
--deep-space: #0a0e27;
--midnight: #1a1a2e;
--twilight: #16213e;

/* Accent Purples */
--mystic-purple: #9370db;
--lavender-mist: #dda0dd;
--orchid: #ba55d3;
--deep-purple: #8a2be2;

/* Text Colors */
--silver: #e0e0e0;
--moonlight: #c0c0d8;
--whisper: #b8b8d0;
--shadow: #808090;

/* Transparent Overlays */
--glass-dark: rgba(26, 26, 46, 0.6);
--glow-purple: rgba(147, 112, 219, 0.2);
--border-purple: rgba(147, 112, 219, 0.15);
```

---

## Final Notes

The key to achieving this aesthetic is **restraint** and **subtlety**. Every element should feel intentional:

- Less is more—remove elements until you can't remove anymore
- Animations should enhance, not distract
- Colors should soothe, not startle
- Spacing should create calm, not chaos

Think of the design as a quiet night sky—vast, serene, with distant points of light creating wonder without overwhelming the viewer.