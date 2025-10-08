# Social Media Privacy Survey Analysis

## Abstract
This repository presents a comprehensive quantitative analysis of survey data examining social media privacy perceptions and behavioral intentions among 127 participants. The study investigates relationships between privacy concerns, demographic factors, and platform deletion behaviors using chi-square tests of independence and descriptive statistics.

## Ethics & Data Privacy Statement
This research adheres to strict ethical standards for data collection and analysis:

- The dataset contains anonymized, voluntarily provided survey responses
- No personal identifiers were collected during the survey process
- All participants responded voluntarily and anonymously
- No Institutional Review Board (IRB) oversight was required due to the non-identifiable nature of the data
- The dataset is shared solely for academic and educational purposes
- Only a small, representative sample is included for demonstration purposes
- Only aggregated or coded columns (such as those with "_coded" and "_clean" fields) are retained in the final dataset

## Project Structure
```
survey_analysis/
├── analysis_notebook.py          # Main reproducible analysis script
├── analysis_outputs/             # All output files
│   ├── cleaned_responses.csv     # Processed dataset (coded fields only)
│   ├── overview_distributions.png # Main visualizations
│   ├── delete_by_worry.png       # Cross-tabulation chart
│   ├── tables_main_crosstab.csv  # Statistical tables
│   ├── results_and_discussion.txt # Academic write-up
│   └── apa_tables.md             # APA-formatted tables
├── complete_analysis.py          # Visualization and stats script
├── analysis_script_fixed.py      # Data cleaning script
└── README.md                     # This file
```

## Methodology

### Requirements
- Python 3.7 or higher
- pandas
- numpy
- matplotlib
- scipy

### Installation
```bash
pip install pandas numpy matplotlib scipy openpyxl
```

### Execution
1. Ensure the Excel file `Polygence Survey Responses.xlsx` is in the Desktop directory
2. Execute the main analysis script:
```bash
python analysis_notebook.py
```

The analysis pipeline performs the following operations:
- Loads and processes the raw survey data
- Applies data cleaning and coding procedures
- Conducts descriptive statistical analysis
- Executes chi-square tests of independence
- Generates publication-ready visualizations
- Exports all output files for further analysis

## Results

### Sample Characteristics
- Sample size: N = 127 participants
- Age distribution: 40.2% aged 18-24, 37.0% under 18
- Gender distribution: Balanced representation (48.8% female, 48.8% male)

### Key Findings
- 72.4% of participants believe their social media activities are under surveillance
- 68.5% have deleted or are considering deleting social media platforms
- 50.4% report being "partially worried" about companies selling their personal information
- Significant gender differences observed in privacy worry levels (p = .007, V = 0.228)
- Moderate association identified between worry levels and deletion intention (p = .088, V = 0.137)

### Statistical Analysis
1. Worry Level × Deletion Intention: χ²(12) = 19.027, p = .088, V = 0.137
2. Gender × Worry Level: χ²(8) = 21.091, p = .007*, V = 0.228
3. Age × Worry Level: χ²(24) = 21.656, p = .600, V = 0.000

*Statistically significant at p < .01

## Repository Contents

### Data Files
- `cleaned_responses.csv`: Processed survey data containing only coded variables
- `tables_main_crosstab.csv`: Cross-tabulation analysis of worry levels by deletion intention

### Visualizations
- `overview_distributions.png`: Comprehensive six-panel overview of key variables
- `delete_by_worry.png`: Stacked bar chart illustrating deletion intention by worry level

### Documentation
- `results_and_discussion.txt`: Complete academic Results and Discussion sections
- `apa_tables.md`: Statistical tables formatted according to APA guidelines

### Analysis Scripts
- `analysis_notebook.py`: Primary reproducible analysis script
- `complete_analysis.py`: Visualization and statistical analysis procedures
- `analysis_script_fixed.py`: Data cleaning and preparation routines

## Reproducibility
All analyses are fully reproducible through the main script (`analysis_notebook.py`), which executes the complete analytical pipeline from raw data input to final output generation in a single execution cycle.

## Academic Standards
This analysis adheres to APA statistical reporting standards and incorporates:
- Comprehensive effect size reporting using Cramer's V
- Systematic missing data assessment

## License
This project is licensed under the MIT License - see below for details:

```
MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Project Link
This research was conducted as part of my Polygence project: https://www.polygence.org/scholars/nishant-raj-sarraf

## Contact
For inquiries regarding the analysis methodology or findings, please refer to the detailed documentation in the `results_and_discussion.txt` file.
