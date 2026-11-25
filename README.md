# Online Courses Analysis (Power BI)

An interactive Power BI dashboard that explores course supply, viewer demand, skills and instructor ratings across 2,693 Coursera courses.

**Project page:** https://claude.ai/artifact/FfLHBwAnH4rDLRXbrGpeDs

## Objective

- Which categories and sub-categories attract the most viewers?
- Which skills appear most often across courses?
- How are courses spread across course types and languages?
- How does viewership relate to subtitle languages?

## Dashboard features

- Summary cards for total courses, total viewers, average rating and sub-categories
- Slicers for course category and instructor sub-category
- Courses by type and by language
- Average viewers by sub-category, with drill-down to language
- Word cloud of skills
- Average viewers by number of subtitle languages
- Number of courses by duration
- Top 5 categories by average viewers
- Average skills and duration by category
- Highest-rated instructors

## Key findings

| Area | Finding |
|---|---|
| Demand | Data Science has about 32% of total viewers (2.64M of 8.36M) |
| Supply | Business has the most courses (871) |
| Skills | Data Analysis (148 courses), Python Programming (128) and Machine Learning (105) appear most often |
| Language | 97.3% of courses are taught in English |
| Subtitles | Median viewers are 1,488 for courses with 9 or more subtitle languages and 131 for courses with one |

Viewer figures cover the 2,579 courses that have a viewer count. The subtitle finding is an association and does not show cause.

## Tools and techniques

- **Power Query:** removed unused fields from a 45-column CSV, filtered incomplete rows and derived a subtitle-language count
- **Data modelling:** related the course and instructor tables by course ID
- **DAX:** `RANKX` measures to rank categories by average viewers and instructors by rating
- **Power BI Desktop:** cards, slicers, charts, matrix tables and a custom word cloud visual

## How to open

1. Download `Edtec_Analysis_Resume.pbix`.
2. Open it in Power BI Desktop.
3. To refresh the data, update the CSV file path in Power Query. The source CSV is read from a local path.

## Known limitations

- The instructor table misses names for 2,041 courses whose instructor text has no comma, so the instructor ranking is based on partial data.
- The subtitle-language count is stored as text, so it may not sort in numeric order.
