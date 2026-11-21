# Price list section for davesfish.com

A replacement for the Price List Pro app, built as a normal theme section. It
needs no app and no monthly fee, and because it is a section it can go on any
page, including the home page.

## What's here

| File | What it is |
| --- | --- |
| `sections/price-list.liquid` | The price list. One self-contained file. |
| `templates/page.price-list.json` | A ready-made page template with Dave's 18 collections already chosen, in the same order as the current list. |
| `preview/price-list-preview.html` | A preview you can open in a browser. It runs the real section code on a snapshot of the live catalog. |

## What it does that the app doesn't

- Loads with the page. The app page loads empty, then makes 36 background requests to fill itself in.
- Search box that filters as you type, by fish name, size or group name.
- "Jump to" menu that stays on screen and shows which group you are in.
- Sort by name or price, collapse or expand groups, and a one-click "New only" filter fed by the New Arrivals collection.
- Quantity buttons on every row. Shoppers pick fish down the list, then add them all to the cart in one step.
- Tap a photo to enlarge it.
- Print / PDF gives a clean two-column list (about 5 pages for the current catalog). Excel downloads a real `.xlsx` file. Both respect the current search.
- Sold-out and sale badges, optional SKU, vendor and stock columns.
- Uses the theme's own fonts, colors and button shapes, and works on phones.
- Search engines can read every fish and price, because the list is in the page itself.

## Install (about 5 minutes)

Do this on a copy of the theme first, so the live site is untouched until you are happy.

1. **Online Store → Themes → ⋯ → Duplicate.** Work in the copy.
2. On the copy, **⋯ → Edit code**.
3. Under **Sections**, click **Add a new section**, name it `price-list`, replace everything in the new file with the contents of `sections/price-list.liquid`, and **Save**.
4. Under **Templates**, click **Add a new template**, choose **page**, type **JSON**, name it `price-list`, replace everything with the contents of `templates/page.price-list.json`, and **Save**.
5. **Online Store → Pages → Add page.** Title it "Price List", set **Theme template** to `price-list`, and **Save**. Preview the theme copy and open `/pages/price-list`.
6. When it looks right, **Publish** the copy.
7. **Online Store → Navigation**: point the "List of Fish" menu link at the new page.
8. Uninstall Price List Pro.

## Make it the home page

1. **Online Store → Themes → Customize** (it opens on the home page).
2. **Add section → Price list**, and drag it where you want it. To make the price list the whole home page, hide or remove the "New Arrivals & Specials" section, or leave it above the list.
3. In the section settings, pick the collections under **Collections** and drag them into order. Set **Badge collection** to New Arrivals and the two "what a product is called" fields to `fish`.
4. Set **Heading level** to H1 if the price list is the main thing on the page, then **Save**.

The home page and the separate page can both exist. They are two copies of the same section with their own settings.

## Settings worth knowing

- **Collections**: each one becomes a group. Left empty, every collection is listed automatically.
- **Badge collection**: products in it get a badge and the one-click filter.
- **Hide sold-out products**: off by default, so sold-out fish show with a "Sold out" badge.
- **Quantity buttons and Add to cart**: turn off for a read-only list.
- **Columns on paper** and **Include photos when printing**: control the printed copy.
- **Color scheme, maximum width, padding**: match the rest of the page.

## Limits

- Up to 50 collections, and up to 250 products per collection. These are Shopify limits for a single page.
- Built for Dawn-family themes (Crave, Dawn, Sense, Craft and similar). The color scheme setting needs a theme from that family.
- A fish that belongs to two collections appears in both groups, the same as in the current app.

## How it was checked

It has not been installed on the live store yet. Before handing it over it was
checked three ways: Shopify's own theme linter reports no issues in either
file; the section was rendered with a Liquid engine against the live catalog
(18 groups, 233 fish); and 63 browser tests covered search, sorting, jumping,
ordering, the cart request, exports and printing. Installing on a duplicate
theme first (step 1) is the final check.
