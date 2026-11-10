# Wedding and event photo sharing apps: an open dataset

Prices, free plans, limits and hosting of 26 event and wedding photo sharing services, every value read on the provider's own website and dated. Free to use under CC BY 4.0.

Last checked: 2026-11-08. Browse the same data as a table: [event photo sharing apps compared](https://event.pics/en/event-photo-sharing-database/) and the [wedding view](https://event.pics/en/best-wedding-photo-sharing-apps.html).

## Disclosure

This dataset is maintained by [EventPics](https://event.pics), the photo sharing app for weddings and parties, made by Aigner Software e. U. in Austria. Two of the 26 rows are ours: EventPics and its sister app [EventUpload](https://eventupload.app). They follow the same rules as every other row and get no field the others do not have.

## Services

Camdeed, Catchmemo, Chivent, EventPics, EventShare, EventUpload, Eventocam, Fotify, GUESTPIX, GuestCam, Guestlense, Kululu, LiveWall, Picaggo, PixelParty, POV, Rompolo, Scene, Snapeen, Waldo Photos, Wedbox, Weddies, Wedding Arrivals, WeddingPhoto App, Wedibox, WedUploader.

## Files

| File | Content |
|---|---|
| `data/data.json` | Every value with its source URL, the date it was read and a confidence level |
| `data/data.csv` | The same values as one row per service, without sources |

In `data.json`, each field looks like this:

```json
"free_plan": {"v": "false, two paid plans only", "s": "https://camdeed.com/", "d": "2026-11-08", "c": "high"}
```

`v` is the value, `s` the page it was read on, `d` the date, `c` the confidence (`high` or `medium`). Values with low confidence are never published.

## Columns

| Column | Meaning |
|---|---|
| `free_plan` | Whether a free plan exists, and what kind |
| `free_limit` | What the free plan allows |
| `price_paid_min`, `price_paid_max` | Cheapest and most expensive paid option, as stated |
| `billing_model` | One-time, subscription, or both |
| `event_duration` | How long uploads stay open and photos stay online |
| `live_slideshow`, `zip_download`, `moderation` | Whether the feature is offered |
| `eu_hosting`, `gdpr_statement` | Where data is stored, and what the provider says about GDPR |
| `guest_app_required` | Whether guests must install an app to upload |
| `qr_access` | Whether guests join by QR code |
| `plans` | Every plan with its price, as listed |
| `last_checked` | When the provider's pages were last read |

"Not stated" means the provider's own pages do not say. It does not mean the feature is missing.

## Method

Only the provider's own pricing, product and help pages count as a source. No reviews, no third-party roundups. Prices are recorded as shown to a visitor from Austria, since several providers localise the currency. The full method is on the [comparison page](https://event.pics/en/event-photo-sharing-database/#methodology).

## Corrections

If a value is wrong or out of date, open an issue in this repository with the page that says otherwise. Corrections are applied with their date.

## License and citation

The data is licensed under [CC BY 4.0](LICENSE). Please credit "EventPics, wedding and event photo sharing apps dataset" with a link to https://event.pics/en/event-photo-sharing-database/. See [CITATION.cff](CITATION.cff).
