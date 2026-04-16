# JPCC Product Design Catalog

**Jeremiah's Pick Coffee Co.** — Product image & packaging design reference.

---

## Scope

| | Count |
|---|---:|
| Unique products | 45 |
| Total designs needed | 273 |
| Reference images | 113 |
| Categories | 6 |

> Every design row has its **own specific image** — Ground 10oz shows a different bag than Whole Bean 1lb.

### By Category

| Category | Products | Designs | Images |
|----------|:--------:|:-------:|:------:|
| Premium | 16 | 82 | 45 |
| Organic | 17 | 69 | 37 |
| Specialty-Single-Origins | 14 | 36 | 23 |
| Decaffeinated | 6 | 36 | 19 |
| Flavored-Coffees | 8 | 38 | 22 |
| Pick-of-the-Harvest | 7 | 12 | 7 |

---

## What is a "Design"?

One product like **Guatemala** needs **6 separate designs**, each with its **own reference image**:

| # | Grind | Size | Reference Image |
|---|-------|------|-----------------|
| 1 | Ground | 10oz Bag | `10-oz-Single-Origin-Ground-Guatemala-Oriente.jpg` |
| 2 | Ground | 1lb Bag | `1-lb-Premium-Guatemala-Oriente.jpg` |
| 3 | Ground | 5lb Bag | `5-lb-blue-orange-bags.jpg` |
| 4 | Whole Bean | 10oz Bag | `10-oz-Premium-Whole-Bean-Single-Origin-Guatemala-Oriente.jpg` |
| 5 | Whole Bean | 1lb Bag | `1-lb-Premium-Guatemala-Oriente.jpg` |
| 6 | Whole Bean | 5lb Bag | `5-lb-blue-orange-bags.jpg` |

Each combination of **grind type** x **bag size** = a separate design with its own reference photo.

---

## This Folder is Self-Contained

Everything you need is here — no external dependencies:

| What | Where |
|------|-------|
| Current product images (local) | `reference-images/` folder — **113 images** |
| Current product images (online) | `online_image_url` column in CSV |
| Product pages on old website | `product_page_url` column in CSV |
| Progress tracking | `status` + `new_image_filename` columns |
| Finished work drop zone | `completed/` folders |

---

## Folder Structure

```
designer-catalog/
│
├── README.md                          ← you are here
├── DESIGNER-CATALOG.csv               ← master tracker (all 273 designs)
├── reference-images/                  ← ALL 113 current product images (DO NOT MODIFY)
├── completed/                         ← drop ALL finished designs here
│
├── Premium/
│   ├── Premium-catalog.csv            (82 designs)
│   ├── reference-images/              (45 images)
│   └── completed/
│
├── Organic/
│   ├── Organic-catalog.csv            (69 designs)
│   ├── reference-images/              (37 images)
│   └── completed/
│
├── Specialty-Single-Origins/
│   ├── Specialty-Single-Origins-catalog.csv  (36 designs)
│   ├── reference-images/              (23 images)
│   └── completed/
│
├── Decaffeinated/
│   ├── Decaffeinated-catalog.csv      (36 designs)
│   ├── reference-images/              (19 images)
│   └── completed/
│
├── Flavored-Coffees/
│   ├── Flavored-Coffees-catalog.csv   (38 designs)
│   ├── reference-images/              (22 images)
│   └── completed/
│
└── Pick-of-the-Harvest/
    ├── Pick-of-the-Harvest-catalog.csv (12 designs)
    ├── reference-images/              (7 images)
    └── completed/
```

---

## How to Work

### Step 1 — Pick a category

Open a category folder (e.g. `Premium/`) and open its CSV file.

### Step 2 — For each row in the CSV

| Column | What to do |
|--------|-----------|
| `reference_image` | Open this file from `reference-images/` — this is the **exact variant image** |
| `online_image_url` | Same image on the live website (backup reference) |
| `product_page_url` | Full product page for context |
| `roast_level` | Guides the color tone of the design |
| `grind_type` | Determines front label text: **Ground** or **Whole Bean** |
| `size` | Determines bag dimensions: **10oz**, **1lb**, or **5lb** |

### Step 3 — Create the new design

Save your file as:

```
<Product>-<Grind>-<Size>.<ext>
```

**Examples:**
- `Guatemala-Ground-10oz.png`
- `Breakfast-Blend-WholeBeans-5lb.psd`
- `Organic-Espresso-Ground-1lb.ai`

Drop it in the category's `completed/` folder (or the root `completed/` folder).

### Step 4 — Track your progress in the CSV

Fill in these columns as you work:

| Column | What to enter |
|--------|--------------|
| `new_image_filename` | The filename you saved (e.g. `Guatemala-Ground-10oz.png`) |
| `status` | **TODO** → **WIP** → **REVIEW** → **DONE** |
| `designer_notes` | Any notes, revision requests, questions |

### Example — A completed row

| Field | Value |
|-------|-------|
| no | 38 |
| product_name | Guatemala |
| roast_level | Dark Roast |
| grind_type | Ground |
| size | 10oz Bag |
| reference_image | `reference-images/10-oz-Single-Origin-Ground-Guatemala-Oriente.jpg` |
| online_image_url | `https://s3-us-west-1.amazonaws.com/...` |
| new_image_filename | `Guatemala-Ground-10oz.png` |
| status | **DONE** |
| designer_notes | Updated logo, darker tones for dark roast line |

---

## Design Notes

### Label Text

| Grind Type | Front Label |
|-----------|-------------|
| Ground | Label reads **"Ground"** |
| Whole Bean | Label reads **"Whole Bean"** |

### Packaging Sizes

| Size | Type | Notes |
|------|------|-------|
| 10oz Bag | Small bag | Most common retail size |
| 1lb Bag | Standard bag | 16oz — core retail offering |
| 5lb Bag | Bulk bag | 80oz — wholesale / bulk buyers |
| 12oz Jar | Glass jar | Specialty single origins only |

### Category Design Cues

| Category | Design Direction |
|----------|-----------------|
| **Premium** | Flagship line — clean, classic, premium look |
| **Organic** | **MUST** include organic certification mark |
| **Specialty Origins** | Origin-themed — country imagery, landscapes, flags |
| **Decaffeinated** | Clearly marked **"Decaf"** on the label |
| **Flavored Coffees** | Flavor imagery — chocolate, vanilla, nuts, etc. |
| **Pick of the Harvest** | Seasonal / limited edition badge or banner |

### Roast Level Color Guide

| Roast | Suggested Palette |
|-------|-------------------|
| Dark Roast | Deep brown, black, rich earth tones |
| Medium Roast | Warm brown, amber, caramel tones |
| Light Roast | Light tan, gold, honey tones |

### Shared Products

Some products appear in **multiple categories** — they need the same base design:

| Product | Categories |
|---------|-----------|
| Organic Chocatal | Organic, Flavored-Coffees, Premium |
| Guatemala | Premium, Specialty-Single-Origins |
| 100% Pure Jamaican Blue Mountain | Premium, Specialty-Single-Origins |
| 100% Pure Kona | Premium, Specialty-Single-Origins |
| Ethiopia Utopia | Premium, Specialty-Single-Origins |
| Sumatra Mandheling | Premium, Specialty-Single-Origins |
| Organic Water Process Decaf | Organic, Decaffeinated |
| All Pick of the Harvest items | Organic, Pick-of-the-Harvest, Specialty-Single-Origins |

> Design once, copy the completed file to each category's `completed/` folder.

### Image Notes

- Every variant row has its **own specific reference image** — not a generic product shot
- Ground variants show the **Ground** labeled bag
- Whole Bean variants show the **Whole Bean** labeled bag
- 5lb bags may share a generic bulk bag image across variants
- 1lb bags sometimes share between Ground/Whole Bean (same bag photo)
- 10oz bags typically have the most distinct images per variant
