# PC Shop POS

A clean, StoreHub-style POS starter for a Malaysian computer shop. It is intentionally original rather than copying StoreHub's code or UI.

## Included
- Dashboard: today's sales, invoice count, inventory and low-stock alerts
- POS checkout with barcode/SKU scanning
- Cash / QR / Card payment selection
- Item-level and overall discounts
- Automatic stock deduction after paid sale
- Invoice numbering
- Product inventory with cost, selling price, opening stock and minimum stock
- Quotation API and quotation database model
- Daily sales closing by payment method
- Accounting ledger entries and CSV export for year-end bookkeeping

## Barcode scanner
Most USB barcode scanners work as a keyboard. Put the cursor in **Scan barcode / enter SKU**, scan the item, and press Enter (many scanners send Enter automatically).

## Run locally
```bash
npm install
cp .env.example .env
npx prisma generate
npx prisma migrate dev --name init
npm run dev
```
Open http://localhost:3000

## GitHub
```bash
git init
git add .
git commit -m "Initial PC Shop POS"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/pc-shop-pos.git
git push -u origin main
```

## Production notes
For a real shop deployment, replace SQLite with PostgreSQL, add staff accounts/roles, proper invoice PDF printing, quotation-to-invoice conversion, customer records, purchase/stock-in module, expenses, supplier records, backups, audit logs, and Malaysia tax/e-Invoice compliance rules as required. Do not treat the accounting CSV as a substitute for advice from your accountant.
