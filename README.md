# YAIPAK Rack Scan

Phone and handheld scan page for the YAIPAK warehouse inventory system.

**Live page:** https://yaipak.github.io/yaipak-rack-scan/

## What it does

1. Driver scans a beam label or placard (phone camera or handheld scanner). The spot fills in.
2. Driver picks In, Out, or Count.
3. Driver scans the item UPC. The item name shows up live from the open product databases.
4. Driver enters the count and taps Save.

Each save goes into the **YAIPAK Warehouse Scan** Jotform (form 262725329716059). The Make scenario **YAIPAK Inventory - Scan to Stock** picks it up from there and updates Stock, the Price Book, the Outbound log, and Slack.

## Shelf Count page

**Live page:** https://yaipak.github.io/yaipak-rack-scan/shelf.html

Tablet page for the ON THE SHELVES count sheet (13 bays, 291 slots).

1. Tap a bay and a slot. Scan the UPC with the handheld. The description fills in from the open product databases (or from names already logged on this device).
2. Type Pkg Type, Qty, Box/ and Items/. Enter moves to the next box and then the next slot.
3. Export .xlsx at the end of each shift. Load sheet restores an exported file.

Work saves in the tablet's browser only. The export is the backup. UPC names it learns are shared with Rack Scan on the same device.

## Notes

- No passwords or keys live in this page. It only posts to the public Jotform form.
- Scans made with no signal are saved on the phone and sent when it reconnects.
- Field names in `index.html` must match the Jotform field names Make reads (for example `q3_q3_dropdown1`). Change them only together with the Make scenario.
