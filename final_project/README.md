# Predicting Radiation Dose Error from DVH Features Using Machine Learning

Bioinformatics final project, Sulav Dhungana.

**Question:** can the dose-volume histogram (DVH) measurements of a radiotherapy treatment plan predict how different that plan's dose is from the patient's reference plan?

- **Data:** OpenKBP-Opt, with 100 head-and-neck cancer patients and 7,600 treatment plans (Babier et al., 2022).
- **Features:** 23 DVH metrics of each plan.
- **Label:** each plan's mean absolute dose difference from the reference plan (Gy).
- **Models:** a mean baseline, a pipeline baseline, Ridge Regression and Random Forest.
- **Evaluation:** MAE, RMSE and R² on patients the model has not seen.

## Files

| File | Contents |
| --- | --- |
| `dose_error_prediction.ipynb` | The whole project. **Part A:** load the two data files, build one row per plan, remove empty plans, check missing values, split patients into train/validation/test. **Part B:** baselines, Ridge, Random Forest, validation results, figures, the patient-split check, and the final test (run once at the end). |
| `data/` | Put the two data files here (not uploaded to GitHub) |
| `requirements.txt` | Python packages |
| `ai_usage.md` | How AI tools were used |

## How to run

1. **Install the packages**:

   ```bash
   pip install -r requirements.txt
   ```

2. **Get the data.** Download `experiments-data.zip` from the OpenKBP-Opt repository (https://github.com/ababier/open-kbp-opt, "Getting started", step 4). Copy these two files into `data/`:
   - `open-kbp-opt-data/results-data/dose_error_df.csv`
   - `open-kbp-opt-data/results-data/dvh_metric_df.csv`

3. **Run `dose_error_prediction.ipynb` from top to bottom.** It takes about a minute.

The random seed is `20261118`, so the results are the same every run.

## Reference

Babier, A., et al. (2022). OpenKBP-Opt: An international and reproducible evaluation of 76 knowledge-based planning pipelines. *Physics in Medicine & Biology, 67*(18), 185012. https://doi.org/10.1088/1361-6560/ac8044
