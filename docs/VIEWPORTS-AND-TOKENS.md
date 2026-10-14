# eMobility tools: viewports and tokens

Every value in the Figma file and in the HTML prototypes is a DS3 Web UI Kit 2.1 token (Dark theme). This page lists the viewports and the tokens each part of the page uses.

- Token names are the Figma variable and style names, shown without the `Sys/` prefix. In the HTML prototypes the same values are CSS custom properties in `:root`.
- Figma file "Design (Full Version)", page `[All] Ready for Dev`.
- DS3 components (Select Field, Radio Button Group, Slider, Text Input, Accordion, Button, Dialog, Text Link, icons) carry their own tokens, so they are only named here.
- Behaviour and animation are in the HTML prototypes.

## Viewports

Each tool has six frames: 320, 375, 768, 1024, 1440 and 1920.

| Viewport | Layout |
|---|---|
| 320, 375 | One column. Mobile top bar. Sticky result bar at the bottom of the screen. |
| 768 | One column with wider margins and larger type. Sticky result bar. |
| 1024 | Two columns: inputs (4fr) and result (2.2fr), inputs in a bordered card. No sticky bar. |
| 1440, 1920 | Same two columns with more spacing and larger type. |

- The top bar uses the mobile layout (hamburger) up to 1496 px and the desktop layout (logo and links) from 1497 px, so only the 1920 frame shows the desktop one.
- Tariffs: the cards scroll sideways below 1440. From 1440 up to three cards sit side by side.

Tokens that change with the viewport (px):

| Token | 320 | 375 | 768 | 1024 | 1440 | 1920 |
|---|---|---|---|---|---|---|
| PageMargin | 16 | 28 | 40 | 60 | 96 | 96 |
| Space/Relative/XL | 28 | 28 | 28 | 28 | 32 | 40 |
| Space/Relative/2XL | 36 | 36 | 36 | 40 | 56 | 72 |
| Space/Relative/3XL | 40 | 40 | 48 | 56 | 72 | 88 |
| Space/Relative/4XL | 48 | 48 | 64 | 72 | 88 | 104 |
| FontSize / LineHeight Display/Order2 | 36 / 52 | 36 / 52 | 44 / 60 | 52 / 76 | 60 / 84 | 72 / 100 |
| FontSize / LineHeight Headline/Order2 | 24 / 36 | 24 / 36 | 24 / 36 | 28 / 40 | 32 / 44 | 36 / 52 |
| FontSize / LineHeight Headline/Order3 | 20 / 32 | 20 / 32 | 20 / 32 | 20 / 32 | 24 / 36 | 24 / 36 |
| FontSize / LineHeight Headline/Order4 | 16 / 24 | 16 / 24 | 16 / 24 | 16 / 24 | 18 / 28 | 20 / 32 |

Everything else (Space/Fixed, Space/Relative/MD = 16 and LG = 24, colours, radii, Copy and Label type) is the same at every viewport.

## Tokens by segment

Read from the 1440 frames of Range, Charging Time, Cost and Tariffs.

### Page (all tools)
- Colour: `Color/Canvas/200` (background)
- Space: `PageMargin` (left and right), `Space/Relative/2XL` (top), `Space/Relative/4XL` (bottom; Charging Time uses 2XL)

### Top bar (all tools)
- DS3 icons: off-canvas (menu), Audi Rings, search, favorite, user
- Colour: `Color/Canvas/100` (background)
- Space: `PageMargin` (sides), `Space/Fixed/0`, `/150`, `/300`

### Header (all tools)
- Colour: `Color/Text/Headline/Default`
- Type: `Typography/Headline/Order2/Normal`
- Space: `Space/Fixed/250`

### Two columns and input card (Range, Charging Time, Cost)
- Colour: `Color/Canvas/200` (card fill), `Color/Surface/Neutral/400` (card border)
- Space: `Space/Relative/2XL` (gap between the columns, card padding), `Space/Relative/XL` (gap between questions)
- Radius, border: `BorderRadius/MD`, `BorderWidth/100`. The Charging Time desktop card is 28 px, a live value with no DS3 radius token, so it is not bound.

### Question (label and info icon)
- DS3 icon: info-circle
- Colour: `Color/Text/Copy/Default` (70 %)
- Type: `Typography/Copy/Order1/Normal`
- Space: `Space/Fixed/50`, `/100`

### Select and model link
- DS3: Select Field, Text Link Standalone
- Colour: `Color/Text/Copy/Default` (label), `Color/Text/Caption/Default` (small text)
- Type: `Typography/Copy/Order1/Normal`, `Typography/Copy/Order2/Normal`
- Space: `Space/Fixed/25`, `/50`, `/150`, `/500`, `Space/Relative/MD`, `/2XS`

### Radio buttons
- DS3: Radio Button Group (label uses the Question tokens)

### Slider (temperature, charge window, price)
- DS3: Slider. Cost also has a DS3 Text Input and Text Link next to the slider.
- Cost: `Typography/Copy/Order2/Normal`, `BorderRadius/Max`, `Space/Fixed/150`, `/250`, `/500`

### Distribution slider (Range, Cost)
- DS3 icons: city, country, motorway, back, forward
- Colour: `Color/Surface/Interactive/Secondary/100/Fill` (middle region), `Color/Surface/Neutral/400` (border, dividers), `Color/Canvas/200` and `Color/Foreground/Neutral/400` (handle)
- Radius: `BorderRadius/SM`
- Space: `Space/Fixed/100` (handle), `Space/Fixed/300` (icon box)

### Tiles (Charging Time: location, charger, power)
- DS3 icons: home, work, city, motorway, charging, wallbox, charging-station
- Colour: `Color/Foreground/Neutral/100`, `Color/Surface/Interactive/Secondary/100/Stroke`, `Color/Surface/Interactive/Secondary/300/Fill`, `Color/Surface/Interactive/Tile/Default/100/Fill` (two-stop gradient); disabled: `Color/Foreground/Disabled/100`, `Color/Surface/Disabled/Fill/200`, `Color/Surface/Disabled/Stroke/100`; small tiles also `Color/Surface/Neutral/100`
- Type: `Typography/Copy/Order1/Normal`, `Typography/Copy/Order2/Normal`
- Radius: `BorderRadius/MD`
- Space: `Space/Fixed/50`, `/100`, `/150`, `/200`

### Result card (all tools)
- DS3 icon: info-circle
- Colour: `Color/Surface/Interactive/Card/Default/Fill` (card), `Color/Text/Copy/Default` (label)
- Number: `Typography/Display/Order2/Normal`, colour `Color/Text/Display/Default`
- Cost also: `Typography/Headline/Order3/Normal`, `Typography/Headline/Order4/Normal`, `Typography/Copy/Order3/Normal`, `Color/Foreground/Neutral/100`
- Radius: `BorderRadius/MD`
- Space: `Space/Fixed/0`, `/50`, `/100`, `Space/Relative/LG`

### Sticky result bar (below 1024)
- Component `sticky-result`
- Colour: `Color/Surface/Interactive/Card/Default/Fill` (fill), `Color/Surface/Neutral/200` (top border)
- Type: `Typography/Display/Order2/Normal`, colour `Color/Text/Display/Default` (value)
- Effect: `Blur/Card` (background blur)

### Footnote (all simulators)
- Colour: `Color/Text/Caption/Default`
- Type: `Typography/Copy/Order3/Normal`
- Space: `Space/Fixed/0`, `/50`, `/100`, `/250`, `/450`

### FAQ (all simulators)
- DS3: AccordionUnit (rows)
- Colour: `Color/Text/Headline/Default` (heading)
- Type: `Typography/Headline/Order2/Normal`
- Space: `Space/Fixed/0`, `/100`, `/500`, `/700`

### Info layer
- DS3: Dialog, with the local component `info-layer-content` for the text

### Tariffs
- Local components: tariff, header-tariff, sum-tariff, accordion-tariff, footer-tariff. DS3: Button, Select, download icon, Text Link Standalone, Icon.
- Colour: `Color/Canvas/200` (page), `Color/Surface/Interactive/Secondary/100/Fill` (card body), `Color/Surface/Neutral/400` (dividers), `Color/Foreground/Neutral/300`, `Color/Text/Display/Default`, `Color/Text/Headline/Default`, `Color/Text/Copy/Default`, `Color/Text/Caption/Default`
- Type: `Typography/Headline/Order2/Normal`, `/Order3/Normal`, `/Order4/Normal`; `Typography/Copy/Order1` and `/Order2` Normal and Bold; `Typography/Copy/Order4/Normal`; `Typography/Link/Order2/Normal`
- Radius: `BorderRadius/SM`
- Space: `PageMargin/XL` (sides), `Space/Fixed/25`, `/100`, `/150`, `/200`, `/300`, `/400`, `Space/Relative/LG`, `/MD`, `/XL`, `/3XL`
