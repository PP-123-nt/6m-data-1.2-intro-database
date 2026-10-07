# Normalization Interactive Tutorial

An 8-step guided tour of database normalization (1NF → 2NF → 3NF), built as a single self-contained page: [`index.html`](./index.html). It animates the same OrderDetails → Customers / Products / Orders / Order Line Items breakdown as **Activity 3** in the [lesson plan](../lesson.md), so learners can review it after working through the activity by hand.

## How to Use

- **Online:** open the published page at <https://su-ntu-ctp.github.io/6m-data-1.2-intro-database/> (this is the link used in the lesson and pre-class material).
- **Locally:** double-click `index.html`, or drag it into any browser window. No install or server needed. An internet connection is only needed to load the Open Sans font; the page still works without it.

### Navigating

- Use the **Next** and **Previous** buttons at the bottom right.
- Or use the keyboard: **→** / **Space** for next, **←** for previous.
- The crimson progress bar at the top and the "Step N / 8" counter show your position. On the last step, **Restart** returns to step 1.

## What You'll Learn

| Step | Topic | Description |
|------|-------|-------------|
| 1 | Introduction | The Update Anomaly problem: why normalization matters |
| 2 | Overview | The three normal forms (1NF, 2NF, 3NF) |
| 3 | 1NF Problem | The starting table passes the atomic-values rule but has no primary key |
| 4 | 1NF Solution | Adding LineNumber to form a composite key |
| 5 | 2NF Problem | Identifying partial dependencies on OrderID |
| 6 | 2NF Solution | Splitting into Orders and Order Line Items |
| 7 | 3NF Problem | Identifying transitive dependencies (CustomerName, ItemName/ItemPrice) |
| 8 | 3NF Solution | Final schema: Customers, Products, Orders, Order Line Items |

## Colour Legend

Cells and legends in the tables use these colours:

- **Blue**: Primary Key
- **Purple**: Foreign Key
- **Amber**: Problem areas (duplicates, partial or transitive dependencies)
- **Red tint**: Repeated data in the Update Anomaly example (step 1)
- **Green**: Successfully normalized tables (step 8)

## Tips for Learners

- Go through each step carefully before clicking Next.
- Pay attention to the highlighted cells: they show the problem being addressed in that step.
- Try predicting the fix before moving to the "Solution" step.
- After the tutorial, try the practice scenario in the lesson (Activity 3.2: Movie Rental Service).

## For Maintainers

- This page is served by GitHub Pages from the `docs/` folder. Keep it as a single file with inline CSS and JS.
- Styling follows the NTU SCTP web branding (Open Sans, navy `#1B2A4A`, crimson `#C8102E`, crimson left stripe).
- If the lesson's Activity 3 data or table names change, update `index.html` to match.
