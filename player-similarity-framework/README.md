# ⚽ Data-Driven Player Similarity Framework  
### Supporting scouting decisions through player profiling and analytics

---

## Vision

Modern scouting should not rely exclusively on observation.

The goal of this project is not to replace traditional scouting, but to support it through data: narrowing the search space, highlighting hidden profiles, and helping scouts focus their attention on the most relevant players.

This framework reflects the way I personally approach football analytics: combining **profiling**, **segmentation**, and **decision support** to support recruitment, succession planning, and squad development.

---

## The Scouting Challenge

Scouting departments often face recurring questions:

- Who could replace a current first-team player?
- Which profiles are most similar to a player already in our squad?
- Which affordable players resemble a top player we admire?
- Where can we find similar profiles across different leagues and markets?
- How can we reduce search complexity without sacrificing scouting quality?

This framework aims to answer these questions through a structured similarity model.

---

## Core Use Cases

### 1. Replacement Scouting

Example:

> Find players similar to Brooke Norton-Cuffy.

The system identifies potential replacements or tactical alternatives based on technical, physical, contextual, and market similarity.

---

### 2. Aspirational Benchmarking

Example:

> Find affordable profiles similar to Lamine Yamal.

The system uses elite players as benchmarks to identify emerging or undervalued profiles with comparable characteristics.

---

## User Workflow

```text
Select Benchmark Player
            ↓
Apply Dynamic Filters
            ↓
Generate Compatibility Ranking
            ↓
Open Detailed One-to-One Comparison
            ↓
Support Recruitment Decision
```

---

## Filtering Layer

Once the benchmark player has been selected, scouts can progressively narrow the search perimeter through dynamic filters, combining demographic, market, contextual, and tactical-performance constraints.

| Filter Category | Examples |
|-----------------|----------|
| Role & Position | Full-back, winger, midfielder, centre-back |
| Demographic Profile | Age, height, dominant foot, nationality |
| Market Constraints | Market value, contract expiry, salary range |
| Context | League, geographic area, team level |
| Availability | Minutes played, injury history |
| Technical Performance | Goals, assists, xG, xA, progressive passes |
| Tactical Indicators | Pressures, aerial duels, defensive actions, touches by zone |
| Season Scope | Current season, last 2 seasons, rolling average |

This allows scouts and technical staff to combine **similarity logic** with **specific tactical requirements**.

---

## Data Architecture

The framework is based on a multi-layer analytical pipeline, where raw player data is progressively transformed into scouting-ready decision layers.

The process includes:

```text
Raw Data Ingestion
        ↓
Player Feature Engineering
        ↓
Context Normalization
        ↓
Similarity Computation
        ↓
Ranking Generation
        ↓
Visualization & Decision Support
```

---

### Player Master Data

Static player information:

- Name
- Date of Birth
- Height
- Nationality
- Dominant Foot
- Primary Position

---

### Seasonal Performance Data

Dynamic performance metrics:

- Minutes Played
- Goals
- Assists
- xG
- xA
- Progressive Passes
- Progressive Carries
- Defensive Duels
- Aerial Duels
- Pressures
- Dribbles
- Touches by Pitch Zone
- Possession Metrics

These variables are used both for **similarity computation** and for **user-driven filtering**.

---

### Market & Context Data

External and contextual variables:

- Transfermarkt Value
- Contract Expiry
- League Strength
- Team Context
- Experience Level
- Competition Level

These variables support both **ranking logic** and **budget-driven recruitment constraints**.

---

## Similarity Engine

Players are compared using normalized metrics adjusted by role, context, playing time, and league environment.

The weighting structure can be customized depending on club philosophy, tactical model, or recruitment priorities.

Example weighting:

| Component | Weight |
|-----------|--------|
| Technical Profile | 40% |
| Tactical Usage | 25% |
| Physical Profile | 15% |
| Context Adjustment | 10% |
| Market Fit | 10% |

The final output is not just a similarity score, but a **ranked shortlist of compatible profiles**.

---

## Dashboard Concept

The analytical workflow can be implemented through different architectural approaches depending on available infrastructure, computational resources, and scouting needs.

---

### Option 1 — Precomputed Similarity Matrix

Player features and similarity rankings are precomputed through Python / SQL pipelines.

Visualization tools such as Power BI can then act as the final decision-support interface, optimized for fast exploration and filtering.

Best suited for:

- Large datasets
- Multiple monitored leagues
- Frequent user interactions
- Scouting departments requiring immediate response times

---

### Option 2 — On-Demand Similarity Engine

When computational resources allow it, a web-based application (e.g. Streamlit) can generate similarity rankings dynamically based on real-time filters and scouting constraints.

Best suited for:

- Advanced exploratory analysis
- Dynamic parameter tuning
- Custom scouting simulations

---

The final architecture depends on:

- Dataset size
- Number of monitored leagues
- Update frequency
- Available infrastructure
- Internal scouting workflows

---

## Dashboard Design

---

### Page 1 — Similarity Ranking

The main scouting interface includes:

- Benchmark player selection
- Dynamic filtering layer
- Ranked shortlist of compatible players
- Ranking position
- Relative compatibility score
- Age
- League
- Club
- Market value
- Contract status

This page helps scouts quickly reduce the search perimeter and focus on the most relevant candidates.

---

### Page 2 — One-to-One Player Comparison

Detailed drill-through page comparing:

```text
Benchmark Player
        vs
Selected Candidate
```

The comparison includes:

- Technical comparison
- Tactical comparison
- Physical comparison
- Heatmaps
- Usage profile
- Market data
- Development potential
- Risk indicators

This supports deeper validation before live scouting or technical discussions.

---

## Club Applications

This framework can support:

- First Team Scouting
- Replacement Planning
- Succession Planning
- Loan Market Analysis
- Emerging Talent Identification
- Benchmarking Against Elite Players
- Budget-Constrained Recruitment
- Tactical Profile Discovery

---

## Human Scouting + Data

The framework is not designed to replace scout intuition or live observation.

Its purpose is to reduce search complexity, uncover hidden profiles, and help technical departments allocate human scouting resources more efficiently.

---

## Personal Note

This project represents the football analytics approach that best reflects my current professional mindset: transforming data into actionable decision support for technical and scouting departments.
