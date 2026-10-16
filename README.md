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
## Student Informaton

Student number: ST10246260
Student name: Sivakele 
Student surname: Molapo
Course : Diploma in Software Development
Module: Web Development

##Primary goal
To increase customer trust. In a market where many manufacturers are seen as unreliable, a professional website lets Nubian Express demonstrate the reliability and attention to quality the business prides itself on (Nubian Express, 2026).## Design Basis

##Objectives
Present a professional, consistent brand identity (gold, silver, black and white palette; premium heading typeface; legible body typeface) on every page.
Give visitors, whether school administrators, corporate procurement staff or individual clients, a clear route to any page in no more than one click from the navigation.
Make contact details and an enquiry route reachable from every page.
Display the full product and service range with sizes, colours, minimum quantities and prices where fixed.
Display customer testimonials to act as trust signals.
Work well on phones, tablets and desktops.
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

##Timeline and Milestones

Phase	Period	Milestone	Status
Planning	August 2026	Website proposal completed: company background, mission and vision, goals, features, design direction, domain and hosting recommendation	Complete
Part 1: structure	August to early September 2026	First version of the site in HTML: home, about, products, services and contact pages	Complete
Part 1: feedback	September 2026	Feedback reviewed and corrections recorded in the changelog	Complete
Part 2: styling	September to October 2026	External stylesheet, typography, layout, colour, pseudo-classes	Complete
Part 2: responsiveness	September to October 2026	Media queries for tablet and mobile; responsive navigation, layout, typography and images	Complete
Part 2: GitHub	September to October 2026	Project committed to GitHub with descriptive commits; README, changelog and references added	In progress
Part 3	
Launch	After final submission	Register a .co.za domain, set up South African hosting with SSL, publish the site	Planned



##CHangeLog
Added
Complete rebuild of the site from the Nubian Express Website Proposal (August 2026).
New pages: catalogue.html (products, services and a cost calculator), reviews.html and checkout.html.
External stylesheet css/style.css, linked on every page, with CSS custom properties for the gold, silver, black and white palette, a type scale and a spacing scale.
Fraunces (headings) and Work Sans (body) as free substitutes for the proposal's Azurite Stockholm and Clear Sans.
CSS Grid with grid-template-areas on the contact and checkout pages; Flexbox for header, footer and cards.
Pseudo-classes (:hover, :focus, :focus-visible, :active, :focus-within) on links, buttons, form fields and cards.
Media queries at 48em (tablet) and 64em (desktop) adjusting layout, typography, navigation and images.
Mobile hamburger menu (js/nav.js) that becomes a horizontal bar from tablet width.
js/calculator.js: live order estimate with a 10% bulk discount at 50 or more items.
js/checkout.js: on-page order confirmation.
Fluid, aspect-ratio-based map embed.
prefers-reduced-motion and print styles.
README sections for goals, timeline, Part 1 details and sitemap; REFERENCES.md in Harvard style.

Changed
products.html and services.html merged into catalogue.html.
Identical header, navigation and footer on every page.
Product and service images moved out of <head> into the page body.
Footer text changed from the placeholder "VVV" to "Nubian Express".

Fixed
Missing < on <!DOCTYPE html> in the original products page.
Missing <html> and <head> opening tags and a stray > in the original contact page.
Duplicate id attributes (size, colour, quantity repeated three times each); every field id is now unique.
Several <h1> elements on one page; each page now has one <h1>.
<footer> content placed outside </body>.
A <p> placed directly inside a <ul>.
Logo and headings placed inside <head>.
Hard-coded width="600" map iframe that overflowed on phones.
Page title "About Us" on the home page.
Navigation links that pointed to the wrong files (About linked to the home page; Products linked to product.html).

## Reference 
Anthropic (2026) Claude [Large language model]. Available at: https://claude.ai (Accessed: 16 October 2026).
Google (n.d.) Fraunces. Google Fonts. Available at: https://fonts.google.com/specimen/Fraunces (Accessed: 16 October 2026).
Google (n.d.) Work Sans. Google Fonts. Available at: https://fonts.google.com/specimen/Work+Sans (Accessed: 16 October 2026).
MDN Web Docs (n.d.) CSS grid layout. Mozilla. Available at: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout (Accessed: 16 October 2026).
MDN Web Docs (n.d.) Basic concepts of flexbox. Mozilla. Available at: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_flexible_box_layout/Basic_concepts_of_flexbox (Accessed: 16 October 2026).
MDN Web Docs (n.d.) Using media queries. Mozilla. Available at: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_media_queries/Using_media_queries (Accessed: 16 October 2026).
MDN Web Docs (n.d.) Pseudo-classes. Mozilla. Available at: https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes (Accessed: 16 October 2026).
MDN Web Docs (n.d.) Responsive images. Mozilla. Available at: https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Responsive_images (Accessed: 16 October 2026).
Nubian Express (2026) Nubian Express website proposal. Unpublished client document. August.
W3C (n.d.) Markup Validation Service. World Wide Web Consortium. Available at: https://validator.w3.org/ (Accessed: 16 October 2026).
