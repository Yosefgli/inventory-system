# Inventory System - Spec (Hebrew, RTL)

## Locations
- Warehouse (מחסן)
- Store (חנות)
- Picking (אזור ליקוט)

## Product fields
- SKU (unique)
- Name
- Unit
- Barcodes (one-to-many)
- Optional: description, image

## Physical location (Warehouse required)
- Zone
- Shelf
- Bin

## Stock rules
- Stock tracked per (SKU + Location)
- All changes create a Movement log record
- No negative stock by default

## Main flows (v1)
1) Receive into Warehouse
2) Transfer Warehouse -> Store
3) Transfer Warehouse -> Picking
4) Decrease stock (sale/waste)
5) Stock count (later)

## API (must)
- REST JSON
- Get stock by SKU + location
- Increase / Decrease / Transfer
- Products CRUD
- Movements list (with filters)

## Language
- Full Hebrew UI (RTL)
