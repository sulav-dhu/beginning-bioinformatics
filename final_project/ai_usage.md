# AI Usage

I used AI tools for this project.

## Tools and what they did

- **OpenAI Codex** created an initial empty project folder.
- **Claude Code (Anthropic)** helped me with the following:
  - reading the OpenKBP-Opt code to understand how the two data files are made and how to join them
  - finding problems in the data: the "Prediction" rows that are not plans, and the 61 empty plans
  - planning the patient-level split and how to avoid data leakage
  - writing the code in the notebook


## How I checked the AI's work

- I compared the claims about the dataset with the real files: 100 patients, 19 prediction sets, 4 optimizers, 23 DVH metrics, 7,600 plans.
- I checked the empty plans in the data myself. All of a patient's empty plans have the same error.
- The notebook includes `assert` checks: the expected number of plans, and that no patient is in two sets.
- The test patients are not used until the final evaluation.
- I ran the notebook from start to finish myself.


## Ethics and privacy

- The data are public and de-identified. No raw data are uploaded to this repository.
- Dose error compared with the reference plan is not the same as clinical plan quality.
