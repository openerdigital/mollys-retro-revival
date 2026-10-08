# Molly's Retro Revival Shopify Theme

A custom Shopify theme for Molly's Retro Revival, a warm retro vintage ecommerce store.

## Built

- Mobile-first homepage with announcement bar, clean navigation, search/cart icons, hero CTA, category CTAs, and featured product grid.
- Product template with image area, price, description, quantity, add-to-cart, and dynamic checkout button.
- Collection template with product grid and pagination.
- Vintage palette inspired by the supplied Molly's Retro Revival artwork: olive, marigold, burnt orange, rust, cream, and dark ink.

## Store Data

The connected Shopify store has smart collections for:

- Furniture
- Glassware
- Decor
- Shop All Vintage

Sample active products were created across furniture, glassware, and decor. Replace these with final inventory before launch.

## Development

Run the local Shopify preview against the merchant store:

```bash
shopify theme dev --store pzz1vh-21.myshopify.com
```

The `main` branch is the production source branch. Develop changes on feature branches, preview them locally, and merge reviewed work into `main`.

## Password-protected review site

The merchant store's active theme is named **Molly's Retro Revival - Staging**, ID `167542653125`. It was published for client review on 8 October 2026, with storefront password protection retained.

- [Permanent review URL](https://pzz1vh-21.myshopify.com/)
- [Theme editor](https://pzz1vh-21.myshopify.com/admin/themes/167542653125/editor)

The storefront is password protected. Visitors need the store's storefront password to view it. This storefront URL does not have the two-day expiry of Shopify's visitor preview links.

To upload future changes for review without immediately updating the active theme, create a new unpublished theme:

```bash
shopify theme push --store pzz1vh-21.myshopify.com --unpublished --theme "Molly's Retro Revival - Review" --strict
```

Review the new theme before publishing it. Reuse its returned theme ID for subsequent uploads instead of creating a new theme each time.

GitHub stores the source code. Deployments currently use Shopify CLI; pushing to GitHub alone does not update Shopify. Shopify hosts the storefront and checkout, so this Liquid theme does not require a Vercel deployment.

## Cart and checkout testing

- [Test product](https://pzz1vh-21.myshopify.com/products/test-retro-daisy-trinket-dish): TEST - Retro Daisy Trinket Dish, AUD 12.00, SKU `MRR-TEST-DAISY-20261008`. Ten units were stocked on 8 October 2026. This is not a real item for fulfilment.
- [Cart](https://pzz1vh-21.myshopify.com/cart): supports quantity updates, item removal, order notes, discounts, totals, and checkout.
- Checkout branding is managed in Shopify's checkout editor, separately from theme files. The active checkout uses Molly's logo and the theme's olive, cream, marigold, and rust palette.

Verified adding the test product, changing its quantity, removing it, and passing the correct items and prices to Shopify Checkout. The existing cart items were preserved. No order or payment was submitted.

Test-payment mode is not confirmed active. Molly must activate Shopify's Test payment gateway, or complete Shopify Payments setup and enable its test mode, before simulated card purchases are attempted. Shopify Payments management is reserved for the store owner.

See [Shopify's test-payment instructions](https://help.shopify.com/en/manual/checkout-settings/test-orders/payments-test-mode). Use only the test credentials for the gateway that is actually enabled. Disable test-payment mode and archive the test products before the public launch.
