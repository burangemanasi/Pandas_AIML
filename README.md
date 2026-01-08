# Pandas for Real Data — FAANG-Level Lab

**Goal:** Teach students how FAANG engineers actually use Pandas — not toy examples, but real, messy, production-like data.

**Outcome:** Students can clean, analyze, and prepare real datasets while explaining *performance, correctness, and tradeoffs*.

---

## Lab Rules (FAANG Style)

- ❌ No unnecessary loops
- ✅ Prefer vectorized Pandas operations
- ✅ Always question data correctness
- ✅ Explain *why* a transformation is needed

---

## Dataset

Use **Adult Income Dataset** (UCI / Kaggle version)

- Mixed numeric + categorical
- Missing values represented as `?`
- Realistic bias & noise

---

## Section 1 — Loading & First Inspection

### Task 1.1: Load the Data

- Load CSV into Pandas
- Display first 5 rows
- Inspect shape, columns, dtypes

**FAANG Question:**

> What potential issues do you notice immediately?

---

### Task 1.2: Basic Sanity Checks

- Check for duplicate rows
- Check missing values per column
- Identify columns with suspicious values

**Interview Angle:**

- Why blind `.dropna()` is dangerous

---

## Section 2 — Data Cleaning (Real World)

### Task 2.1: Handling Missing Values

- Replace `?` with NaN
- Decide column-wise strategy:
  - Drop
  - Impute
  - Keep as category

**Explain:** Why each decision makes sense

---

### Task 2.2: Fixing Data Types

- Convert numeric columns stored as strings
- Convert categorical columns to `category`

**FAANG Note:**

- Memory optimization matters at scale

---

## Section 3 — Indexing, Filtering & Querying

### Task 3.1: Conditional Filtering

Examples:

- Age > 40 and income > 50K
- Education = Masters OR Doctorate

Compare:

- Boolean indexing
- `.query()`

---

### Task 3.2: Indexing Gotchas

- Set and reset index
- Show when index silently breaks logic

**Interview Trap:**

- Index ≠ column

---

## Section 4 — GroupBy & Aggregations (Core FAANG Skill)

### Task 4.1: GroupBy Single Column

- Mean hours-per-week by education
- Median age by income

---

### Task 4.2: Multi-Level GroupBy

- Education × Gender → income rate
- Sort by meaningful metrics

**Explain:** Split–Apply–Combine

---

## Section 5 — Feature Engineering with Pandas

### Task 5.1: Creating New Features

- Age buckets
- Hours-per-week bins

---

### Task 5.2: Encoding Categorical Variables

- One-hot encoding (`get_dummies`)
- Discuss high-cardinality issues

**FAANG Question:**

- When should encoding **NOT** be done in Pandas?

---

## Section 6 — Time & Performance Awareness

### Task 6.1: Vectorization vs Apply

- Rewrite `.apply()` logic using vectorized operations

Measure execution time.

---

### Task 6.2: Memory Profiling

- Check memory usage before & after optimization

---

## Section 7 — Data Leakage & Validation

### Task 7.1: Train/Test Split Mistakes

- Identify leakage examples
- Fix them

**FAANG Reality:**

- Most production ML bugs are data bugs

---

## Section 8 — Mini Case Study (ML-Ready Data)

Prepare final dataset for modeling:

- Cleaned
- Encoded
- No leakage
- Ready for sklearn

Explain each step in Markdown.

---

## Submission Expectations

Students must submit:

- Clean Pandas notebook
- Markdown reasoning for decisions
- Before/after data stats

---

## FAANG Evaluation Rubric

| Skill                   | Evaluated |
|-------------------------|-----------|
| Data cleaning decisions | ✅        |
| GroupBy mastery         | ✅        |
| Performance awareness   | ✅        |
| Leakage prevention      | ✅        |
| Explanation clarity     | ✅        |

---

## Stretch (Optional, Strong Candidates)

- Compare Pandas vs Polars
- Optimize categorical memory further
- Detect hidden bias in features

---

**End Result:** Students handle real data like FAANG ML engineers — not notebook tourists.
