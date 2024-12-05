# Datascientest News NLP Project

<a target="_blank" href="https://cookiecutter-data-science.drivendata.org/">
    <img src="https://img.shields.io/badge/CCDS-Project%20template-328F97?logo=cookiecutter" />
</a>


NLP Project of Datascientest Cohort Aug 2024: Extract and track topics and sentiments in news articles over time across different media outlets and countries. Predict how coverage evolves over time (frequency, sentiment)

# Topic Extraction and Trend Analysis Across Media and Countries

## Objective:
  - ### Primary Goals:
    - Extract and track topics and sentiments in news articles (of a specific narrowed down field) over time across different media outlets and possibly countries.
    - Predict how coverage evolves over time (frequency, sentiment)
  - ### Secondary Goals:
    - Analyze the frequency of coverage of specific topics in various regions.
    - Perform sentiment analysis on topics to gauge public opinion (from articles and possibly comments)
    - Visualize topic coverage geographically.
    - Predict how topic coverage in one country/region or specific media outlet may predict coverage in another (frequency, sentiment) 
## Data:
  - Web scraping: Extract data from 3 news pages (one website per person) -> title, article text and comments (Playwright)
  - Sources: The Independent, The Washington Post..
  - API extraction: [Newscatcher API](https://newscatcherapi.com/)
 
## Modeling:
  - Topic Extraction: Extract topics from title and article text (whole text or just summary?) with unsupervised model (LDA or NMF, BERTopic)
  - Time-Series Analysis: How does frequency and sentiment evolve over time (ARIMA or RNN/LSTM ?)
  - Sentiment Analysis: Understand the sentiment on the topics over time 
      - if we get labels from an aggregator/API: regression/supervised
      - else unsupervised: dictionary approach(e.g. VADER) or adjusted LDA/NMF or BERT)

## Data Visualization: 
  - Trends and Timelines for topics and sentiments
  - Distribution of topics across media and countries/regions
  - Creating geospatial maps (Plotly or GIS systems)

## Data/news source: https://newscatcherapi.com/


## Project Organization

```
├── LICENSE            <- Open-source license if one is chosen
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- A default mkdocs project; see www.mkdocs.org for details
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         src and configuration for tools like black
│
├── references         <- Data dictionaries, manuals, and all other explanatory materials.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Generated graphics and figures to be used in reporting
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── src   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes src a Python module
    │
    ├── config.py               <- Store useful variables and configuration
    │
    ├── dataset.py              <- Scripts to download or generate data
    │
    ├── features.py             <- Code to create features for modeling
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- Code to run model inference with trained models          
    │   └── train.py            <- Code to train models
    │
    └── plots.py                <- Code to create visualizations
```

--------

