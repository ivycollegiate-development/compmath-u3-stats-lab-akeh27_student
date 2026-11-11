# Unit 3 data files

Five files, all synthetic. No real people. Every file has a `#` comment line on top,
then a real header row, then data — so a loader must skip the preamble.

| file | what it is | rows | used in |
|---|---|---|---|
| `u3_donations.txt` | alumni donation amounts, one per line, USD | 200 | L05, L08, L21, L23, L25 |
| `u3_wage_comparison.csv` | payroll extract, `Annual_USD` gross | 120 | L03, L06, L09 |
| `u3_survey_times.csv` | office-hours queue survey, `Wait_Minutes` whole minutes | 240 | L08, L11 |
| `u3_clinic_visits.csv` | clinic visit log — **contains direct identifiers** | 80 | L10, L12, L15 |
| `u3_project_dataset.csv` | the project dataset | 120 | L14, L15, L17, L18, L19, L20, L21 |

`u3_clinic_visits.csv` and `u3_project_dataset.csv` carry names, zips and dates on
purpose. They are the input to the L10 PII audit and the L12 anonymization pass —
do not publish from them without running that pass first.

Paths inside the lessons are relative to this repo root: `data/u3_project_dataset.csv`.
