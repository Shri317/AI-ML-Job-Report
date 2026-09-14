# AI & ML Job Report — Power BI Dashboard

An interactive Power BI dashboard for analyzing **AI & ML job-market data** across locations, companies, roles, experience levels, skills, salaries, and work arrangements.

## Dashboard Preview

### 1. Overview
The Overview page provides a high-level summary of the job market with KPIs such as:
- Total Jobs
- Average Salary
- Average Salary by Experience
- Median Salary
- Remote Job %

It also includes monthly job trends, experience-level distribution, and city/job-related analysis.

### 2. Location Insights
The Location Insights page focuses on geographical analysis:
- Region / Experience Level / Year / Month filtering
- Region–Country–City experience-level analysis
- Country-wise average salary
- Country-wise job distribution
- City-wise job distribution
- Geographic salary and job visualization

### 3. Company & Role Insights
This page analyzes employers and job roles:
- Jobs per company
- Job distribution by experience level
- Company/rating analysis
- Remote ratio vs salary
- Role-level salary and work-arrangement patterns

### 4. Skills & Hiring Insights
This page focuses on skills and hiring requirements:
- Skill usage by experience level
- Average skills per job
- Job title vs average salary/experience
- Skill distribution by work arrangement
- Experience-wise skill count

## Data Model

The report uses a dimensional/star-schema-style model containing:

- `Fact_Jobs` — main job-level fact table
- `Fact_Job_Skills` — job-to-skill mapping/fact table
- `Dim_Companies` — company information
- `Dim_Date` — date attributes
- `Dim_Locations` — region, country and city information
- `Dim_Skills` — skill master data

See [`Docs/Data_Model.md`](Docs/Data_Model.md) for the model documentation.

## Key KPIs

| KPI | Purpose |
|---|---|
| Total Jobs | Measures the total number of job records |
| Average Salary | Shows the average salary across jobs |
| Median Salary | Shows the middle salary value and reduces the impact of extreme salaries |
| Average Salary by Experience | Compares compensation across experience levels |
| Remote Job % | Measures the proportion of jobs offering remote work |

## Tools & Technologies

- Microsoft Power BI
- Power Query
- DAX
- Data Modeling
- Data Cleaning & Transformation
- Interactive Data Visualization
- Star/Dimensional Schema

## Power BI File

The main report file is:

`PowerBI/AI_ML_Job_Report.pbix`

> The `.pbix` file is a binary Power BI Desktop file. GitHub will store it, but it will not render the interactive dashboard directly in the browser. Use the screenshots in this repository to preview the report.

## Repository Structure

```text
AI-ML-Job-Report/
│
├── PowerBI/
│   └── AI_ML_Job_Report.pbix
│
├── Screenshots/
│   ├── 01-overview.png
│   ├── 02-location-insights.png
│   ├── 03-company-role-insights.png
│   └── 04-skills-hiring-insights.png
│
├── Docs/
│   ├── Data_Model.md
│   ├── DAX_Measures.md
│   └── Project_Documentation.md
│
├── Data/
│   └── README.md
│
├── .gitignore
└── README.md
```

## Project Workflow

```text
Raw Job Data
     ↓
Power Query
     ↓
Data Cleaning & Transformation
     ↓
Dimension / Fact Modeling
     ↓
Relationships
     ↓
DAX Measures
     ↓
Power BI Visualizations
     ↓
Interactive Dashboard
     ↓
Business Insights
```

## Business Questions Addressed

- How many AI & ML jobs are available?
- What is the average and median salary?
- How does salary vary with experience?
- Which locations have the highest job activity?
- Which companies have more job opportunities?
- Which skills are most frequently required?
- How does remote work availability vary?
- Which roles have higher salary levels?
- How are skills distributed across experience levels?
- What relationships exist between remote work, skills, roles and salary?

## How to Use

1. Install **Power BI Desktop**.
2. Clone or download this repository.
3. Open `PowerBI/AI_ML_Job_Report.pbix`.
4. If the report asks for a data-source path, update the source location in **Power Query**.
5. Refresh the data.
6. Explore the four report pages using the available filters and interactive visuals.

## Notes

- Replace the files in `Data/` only if you are distributing the underlying dataset.
- Do not upload confidential, private, or licensed data that you are not permitted to redistribute.
- If the dataset has a specific public source, add its name and URL in `Data/README.md`.

## Author

**Shriyansh Barsaiya**

Power BI | Data Analytics | Data Visualization

---

⭐ If you find this project useful, consider giving the repository a star.
