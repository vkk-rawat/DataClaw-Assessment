# Task: JSON Sales Summary

Read `/app/input.json` and write `/app/output.json`.

## Input format

`/app/input.json` contains a JSON array of sales records. Each record has:

- `region` (string)
- `item` (string)
- `quantity` (integer)
- `unit_price` (number)

## Required processing

1. Group records by `region`.
2. For each region, compute:
   - `total_revenue`: sum of `quantity * unit_price` over records in that region
   - `transactions`: number of records in that region
3. Round each `total_revenue` to exactly 2 decimal places.
4. Sort regions alphabetically by region name.

## Output format

Write `/app/output.json` as a JSON object with one key:

- `regions`: an array of objects, each with:
  - `region`
  - `transactions`
  - `total_revenue`

Example entry:

```json
{
  "region": "North",
  "transactions": 2,
  "total_revenue": 125.5
}
```
