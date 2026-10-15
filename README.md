# 🧹 Customer Call List: Data Cleaning with Pandas

A data cleaning project that turns a messy customer list into a clean, ready-to-use call list for a sales team, using pandas.

## The problem
The raw customer list had duplicate rows, an irrelevant column, stray symbols in last names (`/White`, `...Potter`), phone numbers in five different formats, addresses crammed into one column, inconsistent Yes/No values, and customers who had asked not to be contacted.

## What I did
- Removed duplicate records with `drop_duplicates()`
- Dropped an unneeded column
- Cleaned stray characters from names with `str.strip()`
- Standardized every phone number to `XXX-XXX-XXXX` using regex
- Split addresses into Street, State, and Zip Code columns
- Standardized `Y`/`N` values to `Yes`/`No`
- Filtered out customers with no valid phone number or who opted out of contact

## Result
**21 raw rows → 13 customers the sales team can actually call.**

| Before | After |
|---|---|
| `123/643/9775`, `876\|678\|3469`, `7066950392`, `N/a` | `123-643-9775`, `876-678-3469`, `706-695-0392`, removed |
| `/White`, `...Potter`, `Flenderson_` | `White`, `Potter`, `Flenderson` |
| `Y`, `N`, `Yes`, `No` | `Yes`, `No` |

## Files
- `Customer_Call_List_Data_Cleaning.ipynb`: the full notebook with explanations
- `Customer Call List.xlsx`: the raw dataset

## How to run
Open the notebook in Google Colab or Jupyter, run all cells, and upload `Customer Call List.xlsx` when prompted (Colab), or keep it in the same folder (Jupyter).

## Tools
Pandas · Google Colab

---
*Built by Damilola Ogundiran as part of my data analytics training.*
