# YAIPAK Rack Scan

Phone and handheld scan page for the YAIPAK warehouse inventory system.

**Live page:** https://yaipak.github.io/yaipak-rack-scan/

## What it does

1. Driver scans a beam label or placard (phone camera or handheld scanner). The spot fills in.
2. Driver picks In, Out, or Count.
3. Driver scans the item UPC. The item name shows up live from the open product databases.
4. Driver enters the count and taps Save.

Each save goes into the **YAIPAK Warehouse Scan** Jotform (form 262725329716059). The Make scenario **YAIPAK Inventory - Scan to Stock** picks it up from there and updates Stock, the Price Book, the Outbound log, and Slack.

## Notes

- No passwords or keys live in this page. It only posts to the public Jotform form.
- Scans made with no signal are saved on the phone and sent when it reconnects.
- Field names in `index.html` must match the Jotform field names Make reads (for example `q3_q3_dropdown1`). Change them only together with the Make scenario.
