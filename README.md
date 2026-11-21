# New price list for davesfish.com

This replaces the Price List Pro app with a price list that is part of the
theme. There is no app and no monthly fee, and it can also go on the home page.

**Nothing in these steps changes what is on the site today.** The old price
list keeps working the whole time, and you switch over only when you are happy.

## Set it up (about 10 minutes)

### Step 1: Add the price list to the theme

1. In your Shopify admin, click **Online Store**.
2. Next to your current theme, click the **⋯** button, then **Edit code**.
3. In the list on the left, right-click the **sections** folder and choose **New file…**. Type `price-list.liquid` and press Enter.
4. Open [price-list.liquid](https://github.com/jlibasci/davesfish/blob/main/sections/price-list.liquid) in a new tab. Click the **Copy raw file** button (two overlapping squares, top right of the code).
5. Back in Shopify, click into the new file. If it is not empty, select everything and delete it. Paste, then click **Save**.
6. Right-click the **templates** folder and choose **New file…**. Type `page.price-list.json` and press Enter.
7. Open [page.price-list.json](https://github.com/jlibasci/davesfish/blob/main/templates/page.price-list.json), copy it the same way, paste it into the new file (replacing anything already there), and click **Save**.

### Step 2: Create the page

1. Go to **Online Store → Pages** and click **Add page**.
2. Title: `Price List`
3. On the right, under **Theme template**, choose **price-list**.
4. Scroll down to **Search engine listing**, click the pencil, and paste these in:
   - **Page title:** `Rare African Cichlid & Catfish Price List`
   - **Meta description:** `Current prices for 200+ rare African cichlids, catfish and other aquarium fish, including Tanganyikans, Tropheus and Malawi peacocks. Search and order online.`
5. Click **Save**.

The new list is now at **davesfish.com/pages/price-list**. Nothing links to it yet, so only you know it is there. Open it and have a look.

### Step 3: Add a second menu link to try it

1. Go to **Content → Menus** and click **Main menu**.
2. Click **Add menu item**. Name it `New Price List`. In the link box choose **Pages**, then **Price List**.
3. Click **Save**.

The menu now has both: **List of Fish** (the old one) and **New Price List**.

### Step 4: Try it

- Type a fish name in the search box.
- Tap **+** on a few fish, then **Add to cart**, and check the cart.
- Open it on your phone.
- Try **Print / PDF** and **Excel**.

### Step 5: Switch over when you are happy

1. Go to **Content → Menus → Main menu**. Delete the old **List of Fish** link and rename **New Price List** to whatever you like. Click **Save**.
2. Go to **Settings → Apps and sales channels**, find **Price List Pro**, and uninstall it.

One thing to know: after the app is gone, the old address
(`davesfish.com/tools/pricelist`) stops working, and Shopify does not allow
forwarding from addresses that start with `/tools/`. If you have shared that
address anywhere else, such as emails or social profiles, update those links
before you uninstall.

### Changed your mind?

Delete the menu link and the page. Nothing else on the site was touched.

## Day to day

New fish and price changes show up on their own. The list reads straight from
your products.

### Reorder, hide or add a collection

1. Go to **Online Store** and click **Edit theme**.
2. At the top, click the drop-down that says **Home page**, choose **Pages**, then **price-list**.
3. On the left, under **Price list**, every collection is its own row:
   - **Reorder:** drag a row up or down.
   - **Turn off:** click the eye icon on the row. Click it again to turn it back on.
   - **Add:** click **Add block**, choose **Collection**, then pick the collection.
   - **Remove for good:** click the row, then **Remove block**.
4. Click **Save**.

### Other switches

Click **Price list** on the left to see its settings. The useful ones:

- **Show product photos:** on by default. Turn it off for a text-only list with no photos.
- **Include photos when printing:** off by default, so printed copies are text only. Turn it on to print the photos too.
- **Badge collection:** fish in this collection get a "New" badge and a one-click filter. It is set to New Arrivals.
- **Hide sold-out products:** off, so sold-out fish show with a "Sold out" badge.
- **Quantity buttons and Add to cart:** turn off for a list people can only read.
- **Intro text** and **Contact line:** the words under the heading.
- **Columns on paper:** one or two columns on the printed copy.

## Put it on the home page (optional)

1. Go to **Online Store** and click **Edit theme**. It opens on the home page.
2. On the left, click **Add section** and choose **Price list**. Drag it where you want it.
3. It starts by listing every collection from A to Z. To choose which ones and their order, click **Add block → Collection** for each one, the same as above.
4. In the section settings, set **Badge collection** to New Arrivals and both "what a product is called" boxes to `fish`.
5. Click **Save**.

The home page list and the Price List page are separate, each with its own
settings. You can keep both.

## What it does for search engines

- **The list is part of the page.** The old app loaded the list a moment after the page opened, which search engines can miss. Now every fish name and price is in the page itself.
- **Every fish links to its product page**, and every group links to its collection, which helps search engines find and connect your pages.
- **Clear headings:** one main heading, then one heading per group.
- **Photo descriptions:** each photo is labelled with the fish name.
- **Structured data:** the page includes a machine-readable list of every product for search engines.
- **Title and description:** the two lines you pasted in Step 2 are what shows in search results.
- Shopify adds the new page to your sitemap by itself.

These make the page easy for search engines to read. They do not guarantee a
ranking, which also depends on things outside the page.

## What's in this folder

| File | What it is |
| --- | --- |
| `sections/price-list.liquid` | The price list. |
| `templates/page.price-list.json` | The page setup, with your 18 collections already in order. |
| `preview/price-list-preview.html` | A preview. GitHub only shows its code, so download it and open it in a browser. |

## Limits

- Up to 50 collections, and up to 250 products in each. These are Shopify limits.
- A fish that is in two collections shows in both groups, the same as the old list.
- Made for Shopify's Dawn family of themes, which includes the Crave theme the store uses.

## How it was checked

It has not been installed on the live store yet. Before hand-off, Shopify's own
theme checker found no problems in either file, the list was built from the
live catalog (18 groups, 233 fish), and 63 automated browser tests covered
search, sorting, ordering, the cart, exports and printing. Step 4 above is the
final check on the real site.
