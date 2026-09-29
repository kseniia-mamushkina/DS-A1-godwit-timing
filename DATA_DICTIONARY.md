# Data Dictionary

This dictionary describes the variables in `2.Adult_and_juvenile_timing_forR.csv`.  
Definitions are based on the dataset contents and the methods described in Verhoeven et al. (2022). Where the exact meaning of a variable name is not explicitly documented in the article, this is noted below.

| Variable | Description | Data type | Values / units | Notes |
|---|---|---|---|---|
| `Individual` | Identifier of an individual tracked Black-tailed Godwit | Text | Individual ID | The same individual may occur in more than one migration year. |
| `Individual2` | Identifier distinguishing an individual's migration record by year | Text | Individual ID combined with year | Used to distinguish repeated observations of the same individual across years. |
| `Q50` | Estimated date, and where available time, at which the bird crossed the specified latitudinal boundary | Text / date-time | Calendar date or date-time | Exact variable-name definition is not provided in the article. Values correspond to estimated boundary-crossing timing. |
| `dQ50` | Calendar-date representation of the boundary-crossing event recorded in `Q50` | Text / date | Calendar date | Appears to represent the same crossing event as `Q50` in a standardized date format. The exact variable-name definition is not provided in the article. |
| `Date` | Numerical representation of the boundary-crossing date | Numeric | Day of year (1–366) | Used as the migration-timing variable in this audit. |
| `Latitude` | Latitudinal boundary crossed by the tracked bird | Integer | Degrees north | The dataset includes boundaries between 20°N and 52°N. The present audit uses only 52°N. |
| `To Breed` | Year associated with the migration record | Integer | Year | For southward records this corresponds to the migration year. Its exact coding across all northward and juvenile records is not explicitly defined in the article. |
| `Sahara` | Classification related to migration relative to the Sahara or subsequent fate | Categorical | `South`, `North`, `Dies`, or missing | The article distinguishes birds wintering north or south of the Sahara and records mortality. This variable is not used in the present audit. |
| `Age` | Age class | Categorical | `Juv` = juvenile; `Ad` = adult | Main grouping variable for the research question. |
| `What 2` | Migration direction | Categorical | `Southward Migration`, `Northward Migration` | The present audit uses only southward migration. |

## Variables used in the present audit

The research question uses the following variables:

- `Age` — grouping variable;
- `Date` — target variable (day of year of crossing);
- `Latitude` — used to select records at 52°N;
- `To Breed` — used to restrict the comparison to 2016 and 2017;
- `What 2` — used to select southward migration;
- `Individual` and `Individual2` — used to assess repeated observations and duplicates.

The variables `Q50`, `dQ50`, and `Sahara` are retained in the source dataset but are not directly used to estimate the defined target or estimand.
