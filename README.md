# Heart Disease Predictor

**Authors**: Yuhao Gao, Sarika Tasnim, Christa Ingabire, Nassiba Taib

A data analysis project for DSCI 522 (Data Science Workflows), a course in the Master of Data Science program at the University of British Columbia.

## About

In this project, we build a classification model that uses routine clinical measurements, such as age, chest pain type, resting blood pressure, cholesterol and maximum heart rate, to predict whether a patient has heart disease.
 
<!-- TODO: fill in once the results are final (2-3 sentences). -->
Our final <model name, e.g., logistic regression> model reached a <metric, e.g., recall> of <score> on an unseen test set of <n> patients, compared to <baseline score> for a baseline that always predicts the most common class. <One sentence on the kinds of mistakes the model made, e.g., how many patients with heart disease it missed.> <One sentence on what this means, e.g., the model shows promise as a screening aid but needs more work before it could be used in a clinic.>
 
The data set we used is the Heart Disease data set (Janosi et al. 1989), created by Andras Janosi, William Steinbrunn, Matthias Pfisterer and Robert Detrano, and sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/45/heart+disease). We use the Cleveland Clinic Foundation subset, where each row represents one patient: 13 clinical measurements plus a diagnosis of heart disease, recorded on a scale from 0 (no disease) to 4. We combine values 1 to 4 into a single "heart disease present" class, so the question becomes a yes/no classification.


## Report
The final report can be found [here](https://ubc-mds-2026-27.github.io/DSCI-522-Group-08/analysis/<report-name>.html).

## Usage
For the first time you run the project:
1. Install [uv](https://docs.astral.sh/uv/getting-started/installation/) and [Quarto](https://quarto.org/docs/get-started/). Both have installers for Mac and Windows.
2. Clone this repository and move into it : 

```
git clone https://github.com/UBC-MDS-2026-27/DSCI-522-Group-08.git
cd DSCI-522-Group-08
```

3. Create the virtual environment. This installs the exact Python version and package versions the project uses (uv downloads python for you if needed):
```
uv sync
```
To run the analysis and render the report, run this from the root of the repository:
```
uv run quarto render analysis/<report-name>.qmd
```

Rendering runs the whole analysis from scratch. It downloads the data again from the UCI Machine Learning Repository (so you need an internet connection), overwrites the files in data/raw/ and data/processed/, and writes the report to analysis/<report-name>.html, replacing the version in this repository.

## Dependencies
1. [uv](https://docs.astral.sh/uv/) (version 0.12 or higher)
2. [Quarto](https://quarto.org/) (version 1.8 or higher)
3. Python 3.14 (installed automatically by `uv sync`) and the packages listed in [`pyproject.toml`](pyproject.toml)(exact versions are locked in [`uv.lock`](uv.lock))

## AI use statement
<!-- TODO: each teammate adds how they used AI. -->
We used generative AI tools during this project. Christa Ingabire used Claude (Anthropic) to troubleshoot errors in setting up the environment. <Add how other teammates used AI, or state that they did not.> All AI suggestions were reviewed, tested and edited by the authors, who take full responsibility for the content of this repository. All issues and pull requests were opened, reviewed and merged by the authors.

Example prompts:
- "Why does uv sync fail with 'Expected a Python module at: src/dsci_522_group_08/__init__.py', and how do I fix it?"

## License
The Heart Disease Predictor report contained in this repository is licensed under the [Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License](https://creativecommons.org/licenses/by-nc-nd/4.0/). See [the license file](LICENSE.md) for more information. If re-using, please provide attribution and link to this repository. The software code contained in this repository is licensed under the MIT license. See [the license file](LICENSE.md) for more information.


## References
Detrano, Robert, Andras Janosi, Walter Steinbrunn, Matthias Pfisterer, Johann-Jakob Schmid, Sarbjit Sandhu, Kern H. Guppy, Stella Lee, and Victor Froelicher. 1989. "International Application of a New Probability Algorithm for the Diagnosis of Coronary Artery Disease." *The American Journal of Cardiology* 64 (5): 304–10. <https://doi.org/10.1016/0002-9149(89)90524-9>.
 
Janosi, Andras, William Steinbrunn, Matthias Pfisterer, and Robert Detrano. 1989. "Heart Disease." UCI Machine Learning Repository. <https://doi.org/10.24432/C52P4X>.