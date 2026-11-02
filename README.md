# Nubian Express Website

A responsive website for **Nubian Express**, a uniform manufacturer based in Flora Park, Polokwane (Limpopo), that makes school, corporate and sports uniforms with embroidery, printing and custom branding.

- **Repository:** https://github.com/Sivakele/Nubian-Express-website-Xane-
- **Live site (GitHub Pages):** https://sivakele.github.io/Nubian-Express-website-Xane-/
  *(this is the address GitHub Pages will give the site once Pages is switched on for the `main` branch, root folder)*

---

## Project structure

```
Nubian-Express-website-Xane-/
├── index.html          Home page
├── about.html          Company story, mission, vision, values
├── catalogue.html      Products, cost calculator, branding services
├── reviews.html        Customer testimonials
├── enquiries.html      Custom quote request form
├── contact.html        Contact details, message form, map
├── checkout.html       Order summary (built from the cart) and delivery details
├── robots.txt          Instructions for search engine crawlers
├── sitemap.xml         List of public pages for search engines
├── css/
│   └── style.css       One stylesheet for the whole site
├── js/
│   └── script.js       One script for the whole site (menu, calculator, cart, forms)
└── images/             Optimised images (WebP + JPEG fallback), favicon, share image
```

---

## Part 3: SEO and publishing — what I did and why

I worked through the *Student SEO and Publishing Guide* (which uses a bakery website as its example) and applied each step to Nubian Express. Where the guide used bakery examples, I swapped in our own business, products and location.

### 1. On-page SEO

**Search phrases.** I picked a phrase that honestly describes each page, the way a real customer might search, and used it naturally instead of repeating it:

| Page | Search phrase I aimed for |
|---|---|
| Home | uniform manufacturer in Polokwane |
| About | about Nubian Express / uniform company Polokwane |
| Catalogue | uniform catalogue and prices, soccer kits, staff uniforms |
| Reviews | Nubian Express reviews |
| Enquiries | request a uniform quote |
| Contact | Nubian Express contact details, Flora Park Polokwane |

**Unique titles and descriptions.** Every page now has its own `<title>` (all under 60 characters, so search results don't cut them off) and its own `<meta name="description">` (about 145–160 characters). Before this, the titles were just "About - Nubian Express" and similar, and no page had a description.

```html
<title>Uniform Manufacturer in Polokwane | Nubian Express</title>
<meta name="description" content="Nubian Express makes quality school, corporate and sports uniforms in Polokwane, Limpopo, ...">
```

**Heading structure.** Each page has exactly one `<h1>`, then `<h2>` for main sections and `<h3>` for sub-sections, without skipping levels. On the catalogue page, the product cards used `<h3>` straight under the `<h1>`, so I added a "Soccer kits and staff uniforms" `<h2>` above them. I also changed the home page `<h1>` to mention what we make and where: *"Quality uniforms for schools, businesses and teams in Polokwane"*.

**Image file names and alt text.** I renamed every image to describe what's in it, using lowercase words and hyphens, and rewrote the alt text to be specific:

| Before | After |
|---|---|
| `Images/pinkKit.jpeg` | `images/pink-soccer-kit.webp` |
| `Images/colourfulSkull.jpeg` | `images/dtf-printed-colourful-design.webp` |
| `Images/shellLogoEmbroidery.jpeg` | `images/embroidered-logo-work-shirt.webp` |
| `Images/Logo colour.jpeg` | `images/nubian-express-logo.webp` |
| alt="colourful skull" | alt="Full-colour skull artwork printed with direct-to-film (DTF) transfer" |

The logo in the header has `alt=""` on purpose. It sits inside a link that already says "Nubian Express", so a screen reader would otherwise read the name twice.

**Descriptive link text.** I replaced vague buttons like "Contact us" with text that says where the link goes, for example *"Request a uniform quote"*, *"Explore our branding services"* and *"Read how Nubian Express started"*. I also added more links between related pages (home → catalogue → enquiries → checkout), and a footer with links to every main page.

**Mobile layout.** Every page keeps the viewport tag. I tested every page at 375px wide (a typical phone) and confirmed there's no sideways scrolling.

### 2. Off-page SEO and local presence

Off-page SEO happens outside the website, but I prepared the site for it:

- **Consistent business details (NAP: name, address, phone).** The address, phone number and email are now written exactly the same way everywhere: header, footer, contact page and structured data. Before, one page said "15 Euphorbia Street, Polokwane" and another said "Flora Park".
- **Structured data (JSON-LD).** I added a `LocalBusiness` block to the home and contact pages. It gives search engines our name, address, phone, email, map location and social media profiles in a format they can read reliably.
- **Social sharing previews.** Every page has Open Graph tags (`og:title`, `og:description`, `og:image`). When someone shares a link on WhatsApp, Facebook or LinkedIn, it shows a proper preview with our logo. This supports the guide's advice to promote useful pages on social media.
- **Social links.** All social links open in a new tab with `rel="noopener noreferrer"`. I also added WhatsApp to the footer, because many local customers use it.
- **Honest reviews.** The reviews page now invites customers to share honest feedback, good or bad. Following the guide, we will never buy reviews, write fake ones, or offer rewards for positive reviews.

**Outreach ideas (student activity from the guide).** These are organisations that could genuinely want to link to us, because it helps their audience:
1. Local schools and school governing bodies in Polokwane (for our school uniform page)
2. Local sports clubs and community leagues (for our soccer kits)
3. The Polokwane / Limpopo business chamber or a local business directory

> *Example outreach message:* "Good day, I'm reaching out from Nubian Express, a uniform manufacturer in Flora Park, Polokwane. We make school uniforms and sports kits locally and create jobs in the community. If you keep a list of local suppliers for parents or members, we would appreciate being included: https://sivakele.github.io/Nubian-Express-website-Xane-/catalogue.html. Thank you!"

*Example social post:* a photo of a finished team kit, with "New season kits are ready. See colours and prices:" and a link to the catalogue page.

Outreach doesn't guarantee backlinks or a particular search ranking, and we won't buy links or join link-swap schemes.

### 3. robots.txt, sitemap, speed and security

**robots.txt** sits next to `index.html`. It allows all crawlers and points to the sitemap.

**sitemap.xml** lists the six public pages with the live GitHub Pages addresses. I left the checkout page out of the sitemap and gave it a `noindex` tag, because it's a working page, not something people search for. I used `noindex` rather than blocking it in robots.txt, so crawlers can still read the instruction.

> **Note:** search engines only read `robots.txt` at the root of a domain. A GitHub *project* site lives in a sub-folder (`/Nubian-Express-website-Xane-/`), so search engines will ignore this robots.txt until the site moves to its own domain or a `username.github.io` repository. The sitemap still works: it can be submitted directly in Google Search Console.

**Speed improvements:**
- I resized every image to a sensible display size (800px maximum, 240px for the logo) and compressed it. I saved each one as **WebP**, with a JPEG fallback, using `<picture>`. Total image weight dropped from about **2.1 MB to about 380 KB**. The logo alone went from 425 KB to 10 KB.
- Images further down the page use `loading="lazy"` and `decoding="async"`. The first image on the home page doesn't, as the guide recommends.
- Every image has `width` and `height` set, so the page doesn't jump around while images load.
- I moved the Google Fonts loading out of the CSS `@import` and into the HTML with `preconnect`, so the fonts start downloading sooner.
- All the JavaScript is one small file, loaded with `defer`, so it never blocks the page from showing.

**Security and privacy:**
- The site contains no passwords, API keys or customer data.
- Every external link that opens in a new tab has `rel="noopener noreferrer"`.
- The forms don't secretly send data anywhere. As the guide points out, client-side form checks can't securely store or deliver submissions. So after checking the details, the form opens the visitor's own email app or WhatsApp with the message already written, and they send it themselves. This is honest and needs no server.
- GitHub Pages serves the site over HTTPS. Tick "Enforce HTTPS" in the Pages settings.

### 4. Publishing (GitHub Pages)

The site is ready for GitHub Pages: `index.html` is in the root folder, and all file names are lowercase with no spaces. To publish: **Settings → Pages → Deploy from a branch → `main` → `/ (root)` → Save**, then open the URL above and test each page.

---

## Fixes and improvements I made to the site

While going through the guide I found some things that would have broken the live site, so I fixed them:

- **Missing JavaScript.** Every page loaded `js/nav.js`, `js/calculator.js` and `js/checkout.js`, but no `js/` folder existed. That meant the mobile menu couldn't open and the cost calculator didn't work. I replaced them all with one working `js/script.js`.
- **Image folder capitalisation.** The folder was called `Images/`, but some pages pointed to `images/`. Windows doesn't mind, but GitHub Pages treats them as different folders, so those images would have shown as broken online. The folder is now `images/`, and every file name is lowercase with no spaces.
- **Old draft pages.** `product.html` and `service.html` were unstyled early drafts that repeated the catalogue content and linked to pages that don't exist. I removed them (they are still in the Git history). I rebuilt `enquiries.html`, which was an unstyled copy of the contact page with a stray `>` and a "VVV" footer, into a proper **quote request page** and added it to the navigation.
- **Readability.** The light silver used for form labels and small notes was hard to read on white (about 2.6:1 contrast). I added a darker silver (`--silver-dark`) for small text, which meets accessibility guidelines. The gold/silver/black/white palette is otherwise unchanged.
- **Accessibility.** I added a "Skip to main content" link for keyboard users, made the star ratings readable by screen readers, used `<blockquote>` for review quotes, and gave the checkout table a caption.
- **Footer.** I rebuilt it with our address, phone number, email, page links and social links, and the copyright year now updates itself.
- **Small fixes.** I fixed garbled characters (`â€”`) in the CSS comments. On the About page, the list items were splitting the bold value name from its description; they now stay together.

---

## JavaScript features I added (`js/script.js`)

1. **Mobile menu.** The hamburger button opens and closes the menu, updates `aria-expanded` for screen readers, and the menu closes when you press **Escape**.
2. **Live cost calculator** (catalogue). The estimate updates as you change product, quantity and embroidery. At 50 or more units it applies the 10% bulk discount and shows how much you save. Below 50, it tells you how many more units you need to unlock the discount.
3. **Shopping cart** (catalogue → checkout). "Add to order" checks that a size and colour were chosen and that the minimum quantity is met. The item is saved in the browser's `localStorage`, a pop-up confirms it, and a gold badge next to *Checkout* shows how many items are in your order. Adding the same product, size and colour again increases the quantity instead of adding a new line.
4. **Real order summary** (checkout). The summary is now built from the cart instead of being hard-coded. It shows line totals, the bulk discount and the estimated total, and each item has a **Remove** button.
5. **Form validation** (contact, enquiries, checkout). Each field gets a friendly message underneath, such as "Please enter a valid email address" or "Please enter a phone number with at least 10 digits". The first problem field gets focus, and the message clears as soon as it's fixed.
6. **Email / WhatsApp hand-off.** Once a form is valid, a confirmation panel offers **Send by email** and **Send on WhatsApp** buttons with the message already written. For checkout, that includes the full order list and total. There's also an **Edit my details** button to go back and change something.
7. **Automatic copyright year** in the footer.

---

## Testing

- I ran a script over every page to check that every internal link, image, stylesheet and script points at a file that exists **with the exact same capitalisation** (important for GitHub Pages). It also checks that each page has one `<h1>`, no skipped heading levels, alt text on every image, no duplicate IDs, a unique title and description, and valid JSON-LD. Result: no problems.
- I tested the site in headless Chrome at **375px (phone)**, **820px (tablet)** and **1440px (desktop)**. Every page loads with no JavaScript errors, no broken images and no sideways scrolling on a phone.
- I tested every JavaScript feature in the browser: the menu (open, close, Escape); the calculator (60 kits with embroidery = R26 730.00 after the bulk discount); adding to the cart, including the error messages; the cart badge; the checkout total with the bulk discount; removing items; form errors for empty fields, a bad email and a short phone number; and the pre-filled email and WhatsApp messages.
- `sitemap.xml` is valid XML.

---

## Design basis

Built from the *Nubian Express Website Proposal* (August 2026):

- **Positioning:** high-end uniform manufacturer focused on quality, reliability and craftsmanship.
- **Colour palette:** Gold (accent), Silver (secondary accent), Black (text and backgrounds), White (negative space).
- **Typography:** the proposal specifies *Azurite Stockholm* and *Clear Sans*, which are paid fonts with no free web licence. I used **Fraunces** (headings) and **Work Sans** (body) instead, in the same roles.

### Responsive breakpoints

| Breakpoint | Width | Behaviour |
|---|---|---|
| Mobile (default) | up to 767px | Single column, collapsible menu |
| Tablet | from 768px (`48em`) | Two-column grids, horizontal menu |
| Desktop | from 1024px (`64em`) | Three/four-column grids, wider type |

---

## Changelog

**Part 3: SEO, performance and JavaScript (31 October 2026)**
- Added unique titles, meta descriptions, canonical links and Open Graph tags to every page
- Fixed the heading structure; rewrote alt text and link text to be descriptive
- Added `LocalBusiness` structured data and made the business details consistent everywhere
- Added `robots.txt` and `sitemap.xml`
- Renamed, resized and compressed all images; added WebP versions (about 2.1 MB → 380 KB)
- Moved font loading into the HTML with `preconnect`
- Added `rel="noopener noreferrer"` to every external link that opens a new tab
- Created `js/script.js`: mobile menu, calculator, cart, checkout summary, form validation, email/WhatsApp hand-off
- Rebuilt `enquiries.html` as a quote request page; removed the old drafts `product.html` and `service.html`
- Fixed the `Images/` vs `images/` capitalisation problem
- Improved text contrast, added a skip link, and rebuilt the footer

**Part 2: CSS**
- Added the external stylesheet, design tokens, responsive layouts and breakpoints

**Part 1: HTML**
- Created the page structure and content

---

## References

- Google Search Central, *SEO Starter Guide*: https://developers.google.com/search/docs/fundamentals/seo-starter-guide
- Google Search Central, *Introduction to robots.txt*: https://developers.google.com/search/docs/crawling-indexing/robots/intro
- Google Search Essentials: https://developers.google.com/search/docs/essentials
- Google Search spam policies (link spam): https://developers.google.com/search/docs/essentials/spam-policies
- Sitemaps protocol: https://www.sitemaps.org/protocol.html
- Schema.org, *LocalBusiness*: https://schema.org/LocalBusiness
- The Open Graph protocol: https://ogp.me/
- MDN Web Docs, *Client-side form validation*: https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation
- MDN Web Docs, *Window.localStorage*: https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
- web.dev, *Use WebP images*: https://web.dev/articles/serve-images-webp
- GitHub Docs, *Creating a GitHub Pages site*: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- *Student SEO and Publishing Guide*, Web Development course material
