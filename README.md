# Audi Range Simulator (prototype)

An interaction demo of the Audi electric range simulator. It shows how the screen looks and responds, so the live tool can be compared with the design. It is not production code.

## Open it
Open `index.html` in a browser. There is nothing to install or build, and it works offline.

## Files
| File | What it is |
|---|---|
| `index.html` | The default page, as on the live tool |
| `italy-market/index-italy.html` | The Italy market version: adds the question "How old is your battery?" |
| `next-step/index-section-group.html`, `next-step/index-cta-emerged.html` | Work in progress, needs further development: result section with call-to-action buttons. The client prefers the layout in `index-section-group.html` (buttons in their own card); `index-cta-emerged.html` is the alternative (buttons directly under the result card). Figma: page `[Range] Add Next Step CTAs`, sections "Section Group (Client Preferred)" and "CTA Emerged". |
| `assets/` | Fonts, icons and model images |

## What you can try
- Drag the two handles to split your driving between city, country road and motorway.
- Answer the questions (speed, tyres, outside temperature, heating or air conditioning, load). The estimated range updates straight away; there is no calculate button.
- Pick a model and powertrain next to the result. The car image and consumption text change.
- Click the (i) buttons for an explanation. `Esc` or a click outside closes it.
- Open the FAQ rows (one at a time).
- Make the window narrower than 1024 px to see the result bar stick to the bottom of the screen.

## Design reference
Figma, page `[All] Ready for Dev`, section "Range" (six frames: 320, 375, 768, 1024, 1440, 1920). The Italy version follows the page `[Range] Italy Market Legal Requirement`.

## Good to know
- Colours, type and spacing come from the DS3 Web UI Kit 2.1 tokens. They are the `--sys-*` custom properties at the top of the file; change a value there, not in the rules below.
- Copy is English (UK). The result is shown in miles.
- The calculation and selection logic is simplified and not the production logic. Accessibility is out of scope.
- The top bar imitates the live Audi header for context.
