# **Global research trends, hotspots and collaborative networks in brain-derived extracellular vesicles: A multi-database Bibliometric Analysis**  

## 🔬 **About the Project**
This repository contains a comprehensive Python-based Jupyter Notebook (PGI-RV-02.ipynb) designed to perform advanced, multi-database bibliometric analysis. By aggregating, cleaning, and curating publication data from PubMed, Scopus, and Web of Science, this pipeline extracts deep insights into the global research trends, institutional collaborative networks, and emerging thematic hotspots within the study of Brain-Derived Extracellular Vesicles (bdEVs).

## ✨ **Analytical Pipelines**
The notebook is modularized into several robust data processing and visualization pipelines:

###### 1. Data Ingestion & Integration: - Automates the loading of raw data from PubMed, Scopus, and Web of Science.
- Cleans, parses, and normalizes records into a single curated dataset.

###### 2. Publication Trend Analysis: - Evaluates and plots annual and cumulative publication growth.

###### 3. Country & Geographic Analysis: - Generates geographic density maps (chloropleth) of global publication distribution using GeoPandas and pycountry.
- Constructs country collaboration networks with curved edges and strength-based color mapping.

###### 4. Author Analysis: - Ranks top authors by publication count, total citations, and H-index.
- Builds co-authorship network graphs utilizing Louvain community detection clustering to group frequent collaborators.
- Generates bubble scatter plots to track top authors' production over time.

###### 5. Institutional Analysis: - Identifies top institutions and maps their collaborations.
- Uses T-SNE dimensionality reduction to create a Density Heatmap of Institutional Hotspots.
- Creates Three-field Connection plots mapping the flow from Institutions → Research Areas → Countries.

###### 6. Journal Analysis: - Evaluates core journals by citation averages, records, and H-index.
- Generates Top 100 Journal Co-occurrence Networks using concentric circle layouts based on weighted degree.

###### 7. Keyword & Thematic Analysis: - Standardizes and normalizes variable keyword spellings (e.g., evs, bdevs, exosomes, miRNAs).
- Generates Burst Detection Heatmaps to identify keywords trending over time.
- Constructs a Strategic Quadrant Diagram (Motor, Niche, Emerging/Declining, and Basic Themes) leveraging centrality and density metrics.
- Plots keyword co-occurrence networks bound by convex hulls to visualize distinct thematic clusters.

## 🛠 **Prerequisites**
Ensure you have Python 3.8+ installed. The script relies on several core data science, NLP, and network analysis libraries. You can install the required dependencies using pip:

```pip install pandas numpy matplotlib seaborn plotly networkx python-louvain scikit-learn nltk wordcloud geopandas pycountry fsspec adjustText scipy```

(Note: NLTK requires the punkt and stopwords datasets, which the script will automatically attempt to download upon its first run).

## 🚀 **Usage**

###### 1. Clone the repository:

```
git clone https://github.com/AdhishMazumder/PGI-RV-02.git
cd PGI-RV-02
```

###### 2. Setup Data Directories:
Ensure your raw CSV/XLS data and curated Excel files are placed in the exact directory paths referenced above.

###### 3. Run the Notebook:
Launch Jupyter and open the pipeline:

```jupyter notebook PGI-RV-02.ipynb```

###### 4. Execution: 
Run the cells sequentially. The script will automatically compute the metrics, cluster the networks, and save the resulting tables and figures.

## 📊 **Outputs**

The script automatically exports results into the ```2. Analysis/2.3. Bibliometric Analysis/``` subfolders:
- Data Tables: Exported as .csv files (e.g., top countries, authors, journals, and keywords summaries).
- Visualizations: Exported in multiple publication-ready formats including PNG, SVG, TIFF, and PDF at an ultra-high resolution of 1000 DPI.
