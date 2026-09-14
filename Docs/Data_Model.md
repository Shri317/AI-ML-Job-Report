# Data Model

## Tables

### Fact_Jobs
Main job-level table containing job records and measures/attributes used for salary, experience, location, company, role and work-arrangement analysis.

### Fact_Job_Skills
Bridge/fact table connecting jobs with the skills associated with each job.

### Dim_Companies
Company master/dimension table used for company-level analysis.

### Dim_Date
Date dimension used for year, month and time-based analysis.

### Dim_Locations
Location dimension containing geographical attributes such as region, country and city.

### Dim_Skills
Skill dimension containing the skill master list.

## Model Concept

```text
Dim_Date ───────────┐
Dim_Companies ──────┤
Dim_Locations ──────┼──> Fact_Jobs
                    │
Dim_Skills ─────────> Fact_Job_Skills
                         │
                         └── Job relationship to Fact_Jobs
```

> Update this diagram if the final PBIX relationship view differs from the documented model.

## Modeling Approach

The report follows a dimensional modeling approach so that descriptive attributes are separated from job-level and skill-level fact data. This makes filtering, aggregation and dashboard analysis easier to manage.
