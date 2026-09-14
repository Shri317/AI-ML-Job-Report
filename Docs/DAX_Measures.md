# DAX Measures

Document the final measures used in the PBIX here.

Example measures:

```DAX
Total Jobs =
COUNTROWS(Fact_Jobs)
```

```DAX
Average Salary =
AVERAGE(Fact_Jobs[Salary_USD])
```

```DAX
Median Salary =
MEDIAN(Fact_Jobs[Salary_USD])
```

```DAX
Remote Job % =
DIVIDE(
    CALCULATE(
        COUNTROWS(Fact_Jobs),
        Fact_Jobs[IsRemote] = "Remote"
    ),
    COUNTROWS(Fact_Jobs)
)
```

> The exact column names and filter logic should match the final PBIX model. Replace the examples above with the measures actually used in the project.
