# Online Shoppers Purchasing Intention

Explore shopping sessions and predict purchases using Python **3.12**.

## How to run

Keep the four notebooks and `online_shoppers_intention.csv` in the same folder. Install the dependencies:

```shell
python -m pip install -r requirements.txt
```

Open the notebooks in your IDE and select your environment's Python kernel, then **Restart Kernel and Run All Cells** in this order:

1. `01_eda.ipynb`: explore the data.
2. `02_chapter3_preprocessing.ipynb`: clean and split the data, then export `data/processed/train.csv` and `data/processed/test.csv`.
3. `03_chapters4_5_training.ipynb`: load `train.csv` and train models (takes several minutes).
4. `04_chapters6_8_evaluation.ipynb`: load the prepared datasets and evaluate results.

Run notebook 02 before notebooks 03 and 04. Rerunning it overwrites both generated CSVs. The exports retain PageValues for the sensitivity experiment; main models exclude it. Encoding and scaling are fitted inside model pipelines.

Notebooks 01 and 02 read the original CSV. Results stay in the notebooks; save after running. Generated CSVs are ignored by Git.

## Data source

Sakar, C., & Kastro, Y. (2018). [Online Shoppers Purchasing Intention Dataset](https://doi.org/10.24432/C5F88Q), UCI Machine Learning Repository, licensed under CC BY 4.0. The supplied CSV is unchanged: 12,330 sessions, 17 predictors and the purchase outcome `Revenue`.
