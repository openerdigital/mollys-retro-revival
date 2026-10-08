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

## Staging

The merchant store has an unpublished theme named **Molly's Retro Revival - Staging**, ID `167542653125`.

- [Staging preview](https://pzz1vh-21.myshopify.com/?preview_theme_id=167542653125)
- [Theme editor](https://pzz1vh-21.myshopify.com/admin/themes/167542653125/editor)

The storefront is password protected. Visitors need the store's storefront password to view the preview.

To upload changes to the existing staging theme:

```bash
shopify theme push --store pzz1vh-21.myshopify.com --theme 167542653125 --strict
```

GitHub stores the source code. Deployments currently use Shopify CLI; pushing to GitHub alone does not update the staging theme. Shopify hosts the storefront and checkout, so this Liquid theme does not require a Vercel deployment.
