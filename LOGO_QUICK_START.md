# 🚀 Logo Quick Start Guide

## Copy-Paste Ready Code

### Import
```tsx
import { Logo, LogoIcon, LogoDark, LogoSquare, LogoMonochrome } from "@/app/components/Logo";
```

---

## Most Common Uses

### 1. Website Header (Light Background)
```tsx
<Logo variant="default" />
```
**Result**: Deep Indigo icon + "Hello Client.in" text

---

### 2. Footer / Dark Section
```tsx
<LogoDark />
```
**Result**: White icon with cyan hover glow + white text

---

### 3. Favicon (Browser Tab)
```tsx
<LogoIcon size={24} />
```
**Result**: 24x24px icon only

---

### 4. Mobile App Icon (iOS/Android)
```tsx
{/* iOS - Gradient background */}
<LogoSquare size={512} background="gradient" />

{/* Android - Solid background */}
<LogoSquare size={512} background="solid" />
```
**Result**: 512x512px square with background

---

### 5. Icon Only (No Text)
```tsx
<Logo iconOnly />
{/* or */}
<LogoDark iconOnly />
```

---

## Download SVG Files

```tsx
import { downloadSVG, LogoSVGFull, LogoSVGIcon, LogoSVGSquareGradient } from "@/app/components/LogoExport";

// Download full horizontal logo
downloadSVG(LogoSVGFull, 'helloclient-logo.svg');

// Download icon only
downloadSVG(LogoSVGIcon, 'helloclient-icon.svg');

// Download app icon
downloadSVG(LogoSVGSquareGradient, 'helloclient-app-icon.svg');
```

---

## Colors Reference

```css
/* Primary */
--logo-deep-indigo: #3730A3;    /* Main icon color */
--logo-electric-indigo: #4F46E5; /* Accent */
--logo-cyan: #06B6D4;           /* Highlight */

/* Typography */
--logo-text-dark: #111827;      /* "Hello Client" */
--logo-text-gray: #6B7280;      /* ".in" */
```

---

## Size Guide

| Use Case | Component |
|----------|-----------|
| Favicon | `<LogoIcon size={24} />` |
| Header | `<Logo />` (40px default) |
| Mobile Header | `<LogoIcon size={32} />` |
| App Icon | `<LogoSquare size={512} background="gradient" />` |
| Social Media | `<LogoSquare size={256} background="gradient" />` |

---

## All Components

```tsx
// Primary Logo
<Logo variant="default" />          // Light backgrounds
<Logo variant="dark" />              // Dark backgrounds (deprecated, use LogoDark)
<Logo iconOnly />                    // Icon only, no text

// Dark Mode Logo (Recommended for dark backgrounds)
<LogoDark />                         // White with cyan glow
<LogoDark iconOnly />                // Icon only on dark

// Icon Only
<LogoIcon size={40} variant="default" />  // Indigo icon
<LogoIcon size={40} variant="dark" />     // White icon

// Square App Icon
<LogoSquare size={512} background="gradient" />    // Gradient bg
<LogoSquare size={512} background="solid" />       // Solid bg
<LogoSquare size={512} background="transparent" /> // No bg

// Monochrome (Print/Single Color)
<LogoMonochrome variant="dark" />   // Black for light backgrounds
<LogoMonochrome variant="light" />  // White for dark backgrounds
```

---

## Props Reference

### Logo
```tsx
interface LogoProps {
  variant?: "default" | "dark";  // Default: "default"
  iconOnly?: boolean;             // Default: false
}
```

### LogoIcon
```tsx
interface LogoIconProps {
  size?: number;                  // Default: 40
  variant?: "default" | "dark";   // Default: "default"
}
```

### LogoSquare
```tsx
interface LogoSquareProps {
  size?: number;                  // Default: 512
  background?: "gradient" | "solid" | "transparent";  // Default: "gradient"
}
```

### LogoMonochrome
```tsx
interface LogoMonochromeProps {
  variant?: "dark" | "light";    // Default: "dark"
}
```

---

## Design Rules

✅ **DO**
- Use provided components
- Maintain clear space (equal to icon height)
- Scale proportionally
- Use on solid backgrounds

❌ **DON'T**
- Don't change colors
- Don't rotate or distort
- Don't add shadows/outlines to icon
- Don't use on busy backgrounds
- Don't recreate the logo

---

## Full Documentation

- **Complete Guide**: `/LOGO_BRAND_GUIDE.md`
- **Summary**: `/LOGO_SUMMARY.md`
- **Component Code**: `/src/app/components/Logo.tsx`
- **Export Functions**: `/src/app/components/LogoExport.ts`
- **Visual Showcase**: `/src/app/components/LogoShowcase.tsx`

---

**Need help?** Check `/LOGO_BRAND_GUIDE.md` for comprehensive documentation.
