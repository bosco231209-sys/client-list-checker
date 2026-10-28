# Client List Checker

A free web tool for checking TTAND client mailing lists before a direct-mail send.

Upload the client list (Excel `.xlsx` or `.csv`) and the tool:

- marks rows with unusable mailing details in **red** (bad address, city, province or postal code)
- changes provinces to two-letter codes (`Ontario`, `ONT`, `ON - ONTARIO` → `ON`)
- fixes common city misspellings and puts city names in one consistent style
- adds **Validation Status** and **Issues / Corrections** columns, plus a **Cleanup Log** tab
- gives you the checked file to download. Nothing is deleted.

The check runs entirely in your browser. Client data is never uploaded anywhere.

## How to use

1. Open the tool (the GitHub Pages link for this repository, or `index.html` on your computer).
2. Drop in the spreadsheet and choose the sheet (it picks `AMA` automatically if there is one).
3. Press **Check list**, review the results, then press **Download checked file**.

## Colour key

| Colour | Meaning |
|---|---|
| Red row | Invalid. Review before mailing |
| Orange city | Possible misspelling. Please check |
| Yellow cell | Corrected automatically |

## Columns it looks for

`CustomerAddress1`, `CustomerCity`, `CustomerProvince`, `CustomerPostalCode` (required), plus `CustomerFirstName`, `CustomerLastName`, `CustomerCountry`, `AgentLastName` if present.
