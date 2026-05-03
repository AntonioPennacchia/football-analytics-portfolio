# ⚽ Data-Driven Player Similarity Framework  
### Supporting scouting decisions through player profiling and analytics

---

## Vision

Modern scouting should not rely exclusively on observation.

The goal of this project is not to replace traditional scouting, but to support it through data: narrowing the search space, highlighting hidden profiles, and helping scouts focus their attention on the most relevant players.

This framework reflects the way I personally approach football analytics: combining **profiling**, **segmentation**, and **decision support** to support recruitment and squad planning.

---

## The Scouting Challenge

Scouting departments often face recurring questions:

- Who could replace a current first-team player?
- Which young profiles resemble a top player we admire?
- Where can we find a similar player at a lower acquisition cost?
- Which leagues or markets are currently generating compatible profiles?

This framework aims to answer these questions through a structured similarity model.

---

## Core Use Cases

### 1. Replacement Scouting

Example:

> Find players similar to Brooke Norton-Cuffy.

---

### 2. Aspirational Benchmarking

Example:

> Find younger and more affordable profiles similar to Lamine Yamal.

---

## User Workflow

```text
Select Benchmark Player
            ↓
Apply Filters
(Role • Age • League • Market Value • Experience)
            ↓
Generate Similarity Ranking
            ↓
Open Detailed Player Comparison
            ↓
Support Recruitment Decision
```

---

## Filtering Layer

The user defines the scouting perimeter through dynamic filters:

| Filter |
|--------|
| Position / Role |
| Age Range |
| Market Value |
| League / Geographic Area |
| Minutes Played |
| Season |
| Contract Status |
| Dominant Foot |

---

## Data Architecture

### Player Master Data

- Name
- Date of Birth
- Height
- Nationality
- Dominant Foot
- Primary Position

### Seasonal Performance Data

- Minutes Played
- Goals
- xG
- xA
- Progressive Passes
- Progressive Carries
- Defensive Duels
- Pressures
- Dribbles
- Touches by Pitch Zone

### Market & Context Data

- Transfermarkt Value
- Contract Expiry
- League Strength
- Experience Level

---

## Similarity Engine

| Component | Weight |
|-----------|--------|
| Technical Profile | 40% |
| Tactical Usage | 25% |
| Physical Profile | 15% |
| Context Adjustment | 10% |
| Market Fit | 10% |

---

## Dashboard Concept

The similarity matrix is precomputed outside the visualization layer.

Power BI acts as the final decision-support interface for scouts and decision-makers.

---

### Page 1 — Similarity Ranking

Features:

- Benchmark player selection
- Dynamic filters
- Ranked shortlist
- Similarity score
- Age
- League
- Club
- Market value

---

### Page 2 — Player Comparison

Detailed drill-through page including:

- Technical comparison
- Tactical comparison
- Physical comparison
- Heatmaps
- Market data
- Development potential
- Risk indicators

---

## Club Applications

This framework can support:

- First Team Scouting
- Succession Planning
- Loan Market Analysis
- Emerging Talent Identification
- Benchmarking Against Elite Players
- Budget-Constrained Recruitment



This project represents the football analytics approach that best reflects my current professional mindset: transforming data into actionable decision support for technical and scouting departments.
