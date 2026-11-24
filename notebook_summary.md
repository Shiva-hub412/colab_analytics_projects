# Google Colab Notebooks Summary

## 1. NumPy Fundamentals & Fitness Data Analysis
* **Tools:** `numpy`
* **Core Practice:** 1D/2D array creation (`np.array`, `np.arange`), indexing, slicing, `.ndim`, and `.shape` using sample cricket runs and stock price arrays.
* **Fitness Dataset (`fitness.txt`):** 
  * Loaded a `(96, 7)` array and transposed columns (`date`, `step_count`, `mood`, `calories_burned`, `hours_of_sleep`, `activity_status`, `weight`).
  * Calculated step statistics:
    * **Total:** `281,850`
    * **Max:** `7,422`
    * **Min:** `25`
    * **Average:** `2,935.94`
  * Mapped mood codes (`100` → `sad`, `200` → `Neutral`, `300` → `Happy`) and computed step averages/ranges by mood *(note: `mood=='Sad'` returned `NaN` due to lowercase `'sad'`)*.

---

## 2. Global Demographics & Economics (`mckinsey.csv`)
* **Tools:** `pandas`, `numpy`
* **Core Practice:** Loaded a `1,704 × 6` dataset (`country`, `year`, `population`, `continent`, `life_exp`, `gdp_cap`) and performed initial inspection and schema cleaning.
* **Key Operations:** 
  * Inspected data using `.head()`, `.tail()`, `.shape`, `.columns`, `.info()`, `.describe(include='all')`, and `.value_counts()` (`142` countries across `5` continents).
  * Renamed `country` and `continent` to `New_Country` and `New_Continent` in-place.
  * Tested dropping the `life_exp` column.

---

## 3. Movies & Directors Exploratory Analysis (`movies.csv` & `directors.csv`)
* **Tools:** `pandas`, `numpy`
* **Core Practice:** Loaded `movies.csv` (`1,465` rows) and `directors.csv` (`2,349` rows, `199` unique directors in movies), merged them on `director_id` = `id` (`left` join), and dropped redundant ID columns (`director_id`, `id_y`).
* **Key Operations:** 
  * Inspected summary statistics and scaled `revenue` (divided by `1,000,000`) and `budget` (divided by `100,000`).
  * Outlined analysis goals covering top popular/rated movies, releases per year, highest budgets, top/highest-budget directors, and monthly rating extremes.