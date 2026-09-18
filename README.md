# Nubian Express Website

A responsive website for Nubian Express, a South African uniform manufacturer

## Project Structure

```
nubian-express/
├── index.html          Home page
├── about.html          Company background, mission, vision, values
├── catalogue.html      Product catalogue, services, and cost calculator
├── reviews.html        Customer testimonials
├── checkout.html       Order details form and order summary
├── contact.html        Contact details, message form, and map
├── css/
│   └── style.css       Single external stylesheet for the whole site
├── 
├── images/              Product, service, and logo images
└── README.md
```

## Design Basis

Built from the *Nubian Express Website Proposal* (August 2026):

- **Positioning:** upper-class, high-end uniform manufacturer — quality, reliability, craftsmanship.
- **Colour palette:** Gold (accent — headings, highlights, CTAs), Silver (secondary accent — supporting text/detail), Black (primary text and backgrounds), White (backgrounds and negative space).
- **Typography:** the proposal specifies *Azurite Stockholm* for headings and *Clear Sans* for body copy. Both are paid commercial fonts with no free web licence available, so **Fraunces** (heading) and **Work Sans** (body) are used instead — matching the same premium/legible roles. If a licence for the original fonts is purchased, swap the two `--font-heading` / `--font-body` values in `css/style.css`.
- **Pages/features:** mapped directly from the proposal's feature table — Home, About, Contact, Catalogue (with cost calculator), Reviews, Checkout.

## Responsive Breakpoints

| Breakpoint | Width | Behaviour |
|---|---|---|
| Mobile (default) | up to 767px | Single-column layout, collapsible hamburger menu |
| Tablet | from 768px (`48em`) | Two-column grids, horizontal nav bar |
| Desktop | from 1024px (`64em`) | Three-column grids, wider type scale |

## Features

- External stylesheet (`css/style.css`) linked on every page, using CSS custom properties as design tokens.
- CSS Grid and Flexbox for layout, including a named-area (`grid-template-areas`) layout on the contact and checkout pages.
- Pseudo-classes (`:hover`, `:focus`, `:focus-visible`, `:active`, `:focus-within`) on all interactive elements for visible feedback and keyboard accessibility.
- `srcset`/responsive image markup and `loading="lazy"` on product and service images.
- A live cost calculator (`js/calculator.js`) that recalculates an order estimate as the user changes product, quantity, and branding options, including a bulk-order discount.
- A checkout form that displays an on-page confirmation on submit (no backend/payment processor is included — out of scope for this assignment).
- `prefers-reduced-motion` and print media queries for accessibility and printability.

## How to View

Open `index.html` in a browser, or serve the folder with any static file server. All internal links are relative, so the folder can be moved or hosted as-is.

## Testing

Tested in Chrome DevTools responsive mode at approximately 390px (mobile), 768px (tablet), and 1440px (desktop). Screenshots of each breakpoint are included in this README/submission as required by the brief.
