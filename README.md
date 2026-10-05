# Social Media Analysis Project

This folder contains notebooks and datasets for exploring social media engagement, cleaning post metrics, predicting growth, and experimenting with sentiment analysis. The notebooks are working documents: some of them were built around datasets stored elsewhere, so their file paths may need updating before you run them.

## A good place to start

1. Open **`read_&_clean.ipynb`** and run it from top to bottom. It reads the local synthetic dataset, checks its quality, cleans it, and summarizes engagement.
2. Review **`cleaned_social_media_data.csv`**, which the cleaning notebook creates. It removes exact duplicate rows and clips negative interaction counts to zero.
3. Explore **`predictive_growth_analysis.ipynb`** for a growth-prediction workflow. Check its dataset path and installed Python packages before running it.
4. Use **`predictive analysis.ipynb`** for the larger collection of time-series prediction and sentiment-analysis work. Its cells refer to several external datasets and may need paths and dependencies adjusted.

## Files in this folder

| File | What it is for |
| --- | --- |
| `read_&_clean.ipynb` | Reads, audits, and cleans the social media metrics dataset. It also compares engagement levels and platforms and saves a cleaned CSV. |
| `predictive_growth_analysis.ipynb` | A notebook for predicting social media growth from post metrics. It expects a CSV with platform, view, like, share, comment, and engagement-level fields. |
| `predictive analysis.ipynb` | A broader notebook with experiments for time-series forecasting and sentiment classification, including text preprocessing and model evaluation. |
| `synthetic_social_media_data.csv` | The source dataset for the cleaning notebook. It contains 10,000 rows with platform, views, likes, shares, comments, and engagement level. |
| `cleaned_social_media_data.csv` | The cleaned output produced by `read_&_clean.ipynb`. It contains 9,999 rows; negative metric values are set to zero and one duplicate row is removed. |
| `.ipynb_checkpoints/` | Jupyter's automatic checkpoint folder. It is maintained by Jupyter and is not a separate analysis. |

## Running the notebooks

Use Jupyter Notebook or JupyterLab with Python. The cleaning notebook uses **pandas** and **NumPy**. The prediction and sentiment experiments may also require packages such as scikit-learn, Matplotlib, Seaborn, TensorFlow, PyTorch, NLTK, Transformers, and VADER, depending on which cells you run.

Some older analysis cells contain paths to files outside this project folder. If a notebook reports that a dataset cannot be found, update the path in that notebook to point to the correct local dataset. Run notebook cells in order, since later cells often use variables created earlier.

## Notes on interpreting results

The engagement labels in the source CSV are retained during cleaning. Summary tables describe patterns in this dataset; correlations show association and do not establish that one metric causes another. The dataset is synthetic, so results should be treated as practice and demonstration rather than evidence about real audiences.
