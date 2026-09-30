# Recipe-based unit costing with AI

How I used Claude Code to audit the pricing of my food startup (sold on quick-commerce apps in Lima), and what it changed.

> Real recipes and costs are confidential. The example in `example.csv` uses **fictional** numbers.

## The problem

Our prices were set from a spreadsheet cost matrix that had grown by hand over a year: new products, new suppliers, copied formulas. Nobody could say with confidence what each product really cost.

## What I did

1. **Rebuilt costs bottom-up from the source:** every recipe, broken down into ingredient × grams × current supplier price, plus packaging and platform commission.
2. **Reconciled** the rebuilt cost of every product against the matrix, cell by cell.
3. **Flagged every gap** above a tolerance and traced it to its cause (outdated price, wrong unit, missing ingredient, broken formula).

## What it found

- **52 wrong cells** in the cost matrix.
- The biggest error was in one of our flagship products (a parfait), which was **much less profitable than we believed**.
- It also raised a new product question: since the parfait includes brownie bites, it may be **cannibalizing standalone brownie sales**. That is now a hypothesis we are testing.

## The principle

Never trust a number you can't rebuild from its source. It's the same discipline I used when I owned a credit card P&L: benefit costs, pricing and margin only mean something when you can trace them back to usage and unit costs.

## Files

- `example.csv`: the structure of the recipe-level model, with fictional data.
