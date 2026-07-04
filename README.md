# CrunchCo Data Room

Five files for the brand performance diagnostic, at **daily** grain covering
**January 2022 through early June 2026**. They were exported from different
systems and are provided as-is.

| File | Grain | Notes |
|------|-------|-------|
| `sales_daily.csv` | day × banner × store × SKU | Sell-through: units, gross/net sales, promo flag, stores selling. ~494k rows. |
| `media_spend.csv` | day × channel | Planned spend, actual spend, impressions. |
| `product_master.xlsx` | SKU | Product reference: name, sub-brand, pack size, category, list price, launch. |
| `store_region.csv` | store | Store → banner → region mapping and market tier (45 stores). |
| `promo_log.csv` | week × banner × SKU | Which promotions were planned vs. actually executed. |

This is a large, store-level daily dataset — you will need to aggregate it in
code, not read it by hand. Validate before you trust it: confirm join keys line
up, units are consistent, time coverage is complete, and each field means what
its name suggests.
