# Topo Daytona Configurator — Base44 Prompt

Paste everything below this line into Base44.

---

Build a **Topo Daytona car configurator** web app. Use the image manifest and options schema below to drive everything. No 3D engine is required by default — images swap instantly when the user picks a color or angle.

---

## Image Manifest

```json
{
  "colors": {
    "celeste_blue":     { "label": "Celeste Blue",     "hex": "#66A6D9", "rgb": [0.40, 0.65, 0.85] },
    "blue_scuro":       { "label": "Blue Scuro",       "hex": "#192E66", "rgb": [0.10, 0.18, 0.40] },
    "bianco_polo":      { "label": "Bianco Polo",      "hex": "#F5F5F2", "rgb": [0.96, 0.96, 0.95] },
    "nero":             { "label": "Nero",              "hex": "#0D0D0D", "rgb": [0.05, 0.05, 0.05] },
    "rosso_dino":       { "label": "Rosso Dino",       "hex": "#B81414", "rgb": [0.72, 0.08, 0.08] },
    "oro_chiaro":       { "label": "Oro Chiaro",       "hex": "#D9B84D", "rgb": [0.85, 0.72, 0.30] },
    "verde_scuro":      { "label": "Verde Scuro",      "hex": "#1E4724", "rgb": [0.12, 0.28, 0.14] },
    "turchese_molvedo": { "label": "Turchese Molvedo", "hex": "#26A699", "rgb": [0.15, 0.65, 0.60] },
    "marrone_dino":     { "label": "Marrone Dino",     "hex": "#61381F", "rgb": [0.38, 0.22, 0.12] },
    "grigio_argento":   { "label": "Grigio Argento",   "hex": "#8C8C8C", "rgb": [0.55, 0.55, 0.55] },
    "giallo_dino":      { "label": "Giallo Dino",      "hex": "#F2D11A", "rgb": [0.95, 0.82, 0.10] }
  },
  "angles": {
    "front_quarter": { "label": "Front",    "icon": "⬡" },
    "rear_quarter":  { "label": "Rear",     "icon": "⬡" },
    "side_profile":  { "label": "Side",     "icon": "⬡" },
    "wheel_detail":  { "label": "Wheel",    "icon": "⬡" },
    "interior":      { "label": "Interior", "icon": "⬡" },
    "top_down":      { "label": "Top",      "icon": "⬡" }
  },
  "image_path_template": "topo-renders/{color}/{color}_{angle}.png",
  "glb_path": "topo-renders/topo-daytona-optimized.glb",
  "default_color": "bianco_polo",
  "default_angle": "front_quarter"
}
```

---

## Full Options Schema

```json
{
  "systems": {
    "paint": {
      "label": "Paint",
      "options": [
        { "id": "celeste_blue",     "label": "Celeste Blue",     "hex": "#66A6D9", "price": 0 },
        { "id": "blue_scuro",       "label": "Blue Scuro",       "hex": "#192E66", "price": 0 },
        { "id": "bianco_polo",      "label": "Bianco Polo",      "hex": "#F5F5F2", "price": 0 },
        { "id": "nero",             "label": "Nero",              "hex": "#0D0D0D", "price": 0 },
        { "id": "rosso_dino",       "label": "Rosso Dino",       "hex": "#B81414", "price": 0 },
        { "id": "oro_chiaro",       "label": "Oro Chiaro",       "hex": "#D9B84D", "price": 3500 },
        { "id": "verde_scuro",      "label": "Verde Scuro",      "hex": "#1E4724", "price": 0 },
        { "id": "turchese_molvedo", "label": "Turchese Molvedo", "hex": "#26A699", "price": 0 },
        { "id": "marrone_dino",     "label": "Marrone Dino",     "hex": "#61381F", "price": 0 },
        { "id": "grigio_argento",   "label": "Grigio Argento",   "hex": "#8C8C8C", "price": 0 },
        { "id": "giallo_dino",      "label": "Giallo Dino",      "hex": "#F2D11A", "price": 3500 }
      ]
    },
    "wheels": {
      "label": "Wheels",
      "options": [
        { "id": "polished_spoke",   "label": "Polished Spoke",   "price": 0 },
        { "id": "matte_center",     "label": "Matte Center Lock","price": 2800 },
        { "id": "bronze_forged",    "label": "Bronze Forged",    "price": 4200 },
        { "id": "gloss_black",      "label": "Gloss Black",      "price": 1500 }
      ]
    },
    "suspension": {
      "label": "Suspension",
      "options": [
        { "id": "standard",         "label": "Standard",         "price": 0 },
        { "id": "sport",            "label": "Sport (-20mm)",    "price": 1800 },
        { "id": "track",            "label": "Track (-35mm)",    "price": 3200 },
        { "id": "coilover",         "label": "Adjustable Coilover","price": 5500 }
      ]
    },
    "interior": {
      "label": "Interior",
      "options": [
        { "id": "nero_leather",     "label": "Nero Full Leather",    "price": 0 },
        { "id": "tan_leather",      "label": "Cuoio Tan Leather",    "price": 1200 },
        { "id": "rosso_leather",    "label": "Rosso Leather",        "price": 1200 },
        { "id": "carbon_alcantara", "label": "Carbon + Alcantara",   "price": 4800 }
      ]
    },
    "brightwork": {
      "label": "Brightwork",
      "options": [
        { "id": "chrome",           "label": "Polished Chrome",  "price": 0 },
        { "id": "satin_silver",     "label": "Satin Silver",     "price": 800 },
        { "id": "gloss_black",      "label": "Gloss Black",      "price": 800 },
        { "id": "rose_gold",        "label": "Rose Gold",        "price": 2200 }
      ]
    },
    "carbon": {
      "label": "Carbon Fiber",
      "options": [
        { "id": "none",             "label": "None",             "price": 0 },
        { "id": "hood",             "label": "Hood Only",        "price": 3800 },
        { "id": "aero_pack",        "label": "Aero Pack (Hood + Diffuser + Lip)", "price": 8500 },
        { "id": "full_exterior",    "label": "Full Exterior",    "price": 16000 }
      ]
    },
    "audio": {
      "label": "Audio",
      "options": [
        { "id": "standard",         "label": "Standard",         "price": 0 },
        { "id": "bose",             "label": "Bose Premium",     "price": 2200 },
        { "id": "burmester",        "label": "Burmester Surround","price": 5800 }
      ]
    },
    "engine": {
      "label": "Engine",
      "options": [
        { "id": "standard_v12",     "label": "5.0L V12 — 620hp",    "price": 0 },
        { "id": "sport_v12",        "label": "5.0L V12 Sport — 680hp","price": 12000 },
        { "id": "track_v12",        "label": "5.0L V12 Track — 720hp","price": 24000 }
      ]
    },
    "accessories": {
      "label": "Accessories",
      "multi": true,
      "options": [
        { "id": "luggage_set",      "label": "Matching Luggage Set",    "price": 3200 },
        { "id": "car_cover",        "label": "Bespoke Car Cover",       "price": 850 },
        { "id": "tool_roll",        "label": "Leather Tool Roll",       "price": 420 },
        { "id": "helmet_bag",       "label": "Helmet Bag",              "price": 380 },
        { "id": "titanium_exhaust", "label": "Titanium Exhaust Upgrade","price": 7800 }
      ]
    },
    "packages": {
      "label": "Packages",
      "multi": true,
      "options": [
        {
          "id": "sport_pack",
          "label": "Sport Pack",
          "description": "Sport suspension, Bose audio, gloss black brightwork",
          "price": 5800,
          "includes": ["sport", "bose", "gloss_black"]
        },
        {
          "id": "track_pack",
          "label": "Track Pack",
          "description": "Track suspension, Aero carbon pack, Track V12, titanium exhaust",
          "price": 38000,
          "includes": ["track", "aero_pack", "track_v12", "titanium_exhaust"]
        },
        {
          "id": "grand_touring",
          "label": "Grand Touring Pack",
          "description": "Burmester audio, full leather interior, matching luggage",
          "price": 11200,
          "includes": ["burmester", "tan_leather", "luggage_set"]
        }
      ]
    }
  }
}
```

---

## UI Requirements

### Layout
- Full-viewport layout, dark background (#0a0a0a)
- Left panel (70% width): image viewer
- Right panel (30% width, scrollable): configurator options
- Mobile: stack vertically, image on top

### Image Viewer
- Large image fills the left panel, `object-fit: contain`
- Image source = `topo-renders/{selectedColor}/{selectedColor}_{selectedAngle}.png`
- Smooth crossfade transition (200ms opacity) on image swap
- Show color name + angle label as a subtle overlay (bottom-left, small caps)

### Angle Selector
- Row of 6 thumbnail buttons below the main image
- Each button shows the angle label (Front / Rear / Side / Wheel / Interior / Top)
- Active angle button has a white bottom border or highlight
- Clicking changes `selectedAngle` → swaps main image

### Color Selector (in right panel, Paint section)
- Grid of circular swatches (hex fill color), 6 per row
- Active swatch has a white ring
- Hover shows color label as tooltip
- Clicking changes `selectedColor` → swaps main image AND updates all angle thumbnails

### Right Panel — Configurator
- Sections for each system: Paint, Wheels, Suspension, Interior, Brightwork, Carbon, Audio, Engine, Accessories, Packages
- Each section is collapsible (open by default for Paint and Wheels)
- Non-paint sections use text option cards (label + price delta)
- Multi-select systems (Accessories, Packages) allow multiple active selections
- Show running total price at the bottom of the right panel, sticky
- Format prices as: "Base — $XXX,XXX" + "Options — +$XX,XXX" + "Total — $XXX,XXX"
- Base price: $285,000

### 3D View Toggle
- Small button in the top-right of the image panel: "3D View"
- When toggled ON: hide the `<img>` and angle row, show a `<model-viewer>` element instead
  ```html
  <model-viewer
    src="topo-renders/topo-daytona-optimized.glb"
    auto-rotate
    camera-controls
    environment-image="neutral"
    shadow-intensity="1"
    style="width:100%;height:100%">
  </model-viewer>
  ```
  Include the model-viewer script tag: `https://ajax.googleapis.com/ajax/libs/model-viewer/3.4.0/model-viewer.min.js`
- When toggled OFF: restore image viewer

### Typography & Style
- Font: `Inter` or system sans-serif
- Section headers: 10px uppercase letter-spaced labels in gray (#666)
- Option labels: 14px white
- Price deltas: 12px gray, right-aligned
- Total price: 20px white, bold
- Accent color: #C8A96E (gold)

### State
- All state managed in React `useState` (or vanilla JS if simpler)
- Defaults: `bianco_polo` + `front_quarter`
- URL hash updates on color/angle change so links are shareable:
  `#color=bianco_polo&angle=front_quarter`

---

## Deliverable

One self-contained HTML file (or React component if Base44 prefers) that:
1. Loads with bianco_polo front_quarter image shown
2. Color swatches swap the image instantly
3. Angle buttons swap the image instantly
4. Configurator options in the right panel track a running price total
5. "3D View" toggle button works via model-viewer
6. Looks polished and minimal — no lorem ipsum, no placeholder UI
