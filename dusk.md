# Dusk/Sunset Gradient System

A carefully crafted gradient palette inspired by twilight skies transitioning from midnight to warm sunset glow.

---

## Color Palette

### Sky Colors (Dark to Light)
| Hex       | Name                    | Usage                  |
|-----------|-------------------------|------------------------|
| `#060912` | Deeper Midnight         | Top of sky             |
| `#0a0f1a` | Rich Dark Navy          | Upper sky              |
| `#0d1321` | Dark Twilight           | Mid-upper sky          |
| `#12203a` | Twilight Blue           | Middle sky             |
| `#1a2d4d` | Deep Dusk Blue          | Lower-mid sky          |
| `#243550` | Transitional Blue       | Transition zone        |
| `#2f3d55` | Purple-touched Twilight | Pre-horizon            |
| `#3d4258` | Mauve Transition        | Horizon approach       |
| `#4a4555` | Warm Purple Base        | Horizon line           |

### Sunset Glow Colors
| Hex       | RGBA                        | Name              |
|-----------|-----------------------------|-------------------|
| `#c45830` | `rgba(196, 88, 48, 1)`      | Sunset Orange     |
| `#d4663c` | `rgba(212, 102, 60, 1)`     | Warm Horizon      |
| `#d25f2d` | `rgba(210, 95, 45, 1)`      | Left Horizon      |
| `#be502a` | `rgba(190, 80, 42, 1)`      | Right Glow        |
| `#af4623` | `rgba(175, 70, 35, 1)`      | Deep Orange       |
| `#b43c5a` | `rgba(180, 60, 90, 1)`      | Pink/Magenta      |

---

## Hero Section (Full Dusk Sky)

### Base Gradient
```css
background: linear-gradient(180deg,
  #060912 0%,        /* Deeper midnight at top */
  #0a0f1a 10%,       /* Rich dark navy */
  #0d1321 20%,       /* Dark twilight */
  #12203a 40%,       /* Twilight blue */
  #1a2d4d 55%,       /* Deep dusk blue */
  #243550 70%,       /* Transitional blue */
  #2f3d55 82%,       /* Purple-touched twilight */
  #3d4258 92%,       /* Mauve transition zone */
  #4a4555 100%       /* Warm purple base for glow */
);
```

### Sunset Glow Overlay (::before pseudo-element)
```css
background:
  /* Warm sunset glow from bottom center - enhanced */
  radial-gradient(ellipse 140% 50% at 50% 110%, rgba(196, 88, 48, 0.5) 0%, rgba(180, 70, 40, 0.25) 30%, transparent 55%),
  /* Left horizon orange accent - enhanced */
  radial-gradient(ellipse 70% 38% at 20% 100%, rgba(210, 95, 45, 0.4) 0%, transparent 50%),
  /* Right horizon warm glow - enhanced */
  radial-gradient(ellipse 60% 32% at 80% 105%, rgba(190, 80, 42, 0.35) 0%, transparent 45%),
  /* Subtle deep orange reflection mid-low */
  radial-gradient(ellipse 100% 28% at 50% 95%, rgba(175, 70, 35, 0.3) 0%, transparent 50%),
  /* Pink/magenta horizon touch */
  radial-gradient(ellipse 80% 20% at 50% 100%, rgba(180, 60, 90, 0.15) 0%, transparent 50%),
  /* Very subtle purple ambient at top */
  radial-gradient(ellipse 90% 40% at 50% -10%, rgba(70, 60, 110, 0.15) 0%, transparent 50%);
```

---

## Compact Version (Number Badges)

For smaller elements like badges, buttons, or icons:

```css
background: linear-gradient(135deg,
  #0a0f1a 0%,      /* Rich dark navy */
  #12203a 25%,     /* Twilight blue */
  #1a2d4d 45%,     /* Deep dusk blue */
  #2f3d55 65%,     /* Purple-touched twilight */
  #4a4555 80%,     /* Warm purple base */
  #c45830 95%,     /* Sunset orange */
  #d4663c 100%     /* Warm horizon */
);

box-shadow:
  0 4px 16px rgba(0,0,0,0.25),
  inset 0 1px 0 rgba(255,255,255,0.1);
```

### Typography Pairing
- **Font**: `'Bebas Neue', Impact, sans-serif`
- **Color**: `white`
- **Weight**: 400
- **Size**: 26px (for 52x52px containers)
- **Letter-spacing**: 0.02em

---

## CSS Variables Version

```css
:root {
  /* Dusk Sky */
  --dusk-midnight: #060912;
  --dusk-navy: #0a0f1a;
  --dusk-twilight-dark: #0d1321;
  --dusk-twilight: #12203a;
  --dusk-blue: #1a2d4d;
  --dusk-transition: #243550;
  --dusk-purple-touch: #2f3d55;
  --dusk-mauve: #3d4258;
  --dusk-warm-base: #4a4555;

  /* Sunset Glow */
  --sunset-orange: #c45830;
  --sunset-warm: #d4663c;
  --sunset-left: #d25f2d;
  --sunset-right: #be502a;
  --sunset-deep: #af4623;
  --sunset-pink: #b43c5a;
}
```

---

## Usage Notes

1. **Direction**: Use `180deg` for vertical (sky-like), `135deg` for diagonal (dynamic)
2. **Overlay**: The radial gradients create depth and warmth at the horizon
3. **Contrast**: White text works beautifully against all these colors
4. **Mood**: Evokes endings, transitions, reflection, and warm closure

---

*Last updated: December 2025*
*Project: The Last Lecture*
