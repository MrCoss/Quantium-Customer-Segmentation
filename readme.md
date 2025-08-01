# Quantium Customer Segmentation Analysis

[![Status: Completed](https://img.shields.io/badge/Status-Completed-green.svg)](https://shields.io/)
[![Python Version](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)](https://www.python.org/)
[![Platform: Forage](https://img.shields.io/badge/Platform-Forage-blue)](https://www.theforage.com/)
[![License: Educational](https://img.shields.io/badge/License-Educational-yellow.svg)](LICENSE)

An in-depth analysis of customer purchasing behavior to identify strategic segments for a leading FMCG client. This project is part of the **Quantium Virtual Job Simulation** on Forage, focusing on practical data science skills in a real-world business context.

---

## Table of Contents
- [1. Project Context & Business Problem](#1-project-context--business-problem)
- [2. Core Objectives](#2-core-objectives)
- [3. Analytical Methodology](#3-analytical-methodology)
- [4. Project Structure Explained](#4-project-structure-explained)
- [5. Technical Stack](#5-technical-stack)
- [6. Local Setup & Replication Guide](#6-local-setup--replication-guide)
- [7. Disclaimer](#7-disclaimer)
- [8. Author](#8-author)

---

## 1. Project Context & Business Problem

A leading supermarket client has engaged Quantium to analyze their chip category sales. The client wants to understand their customer base better to tailor their marketing, product, and sales strategies. Without a clear understanding of who their customers are and what drives their purchasing decisions, the client risks inefficient marketing spend and missed growth opportunities.

The core business problem is to **identify distinct customer segments** based on purchasing behavior and demographic data, and to provide actionable recommendations for targeting these segments.

---

## 2. Core Objectives

The analysis is structured to achieve the following key objectives:

1.  **Prepare a High-Quality Dataset:** Merge and clean transaction and customer data to create a reliable foundation for analysis.
2.  **Define Key Metrics:** Establish metrics for customer value, such as total spend, frequency of purchase, and units per transaction.
3.  **Conduct Exploratory Analysis:** Uncover high-level trends and patterns in sales, customer demographics, and brand preferences.
4.  **Develop Customer Segments:** Group customers into meaningful segments based on their lifestage and purchasing affinity (e.g., "Budget," "Mainstream," "Premium").
5.  **Deliver Strategic Insights:** Translate analytical findings into actionable recommendations for the client's marketing and sales teams.

---

## 3. Analytical Methodology

The project follows a structured data analysis workflow from data cleaning to strategic recommendation.

### Step 1: Data Preparation & Cleaning
- **Ingestion:** Loaded two primary datasets: `QVI_transaction_data.xlsx` (customer purchase records) and `QVI_purchase_behaviour.csv` (customer demographic information).
- **Data Validation:** Performed rigorous checks for data quality, including handling outliers, correcting data types (e.g., dates), and ensuring consistency.
- **Feature Engineering:** Extracted pack size and brand name from the `PROD_NAME` column to create new, analyzable features.
- **Merging:** Joined the transaction and customer datasets on `LYLTY_CARD_NBR` to create a unified view of each customer's purchases and demographics.

### Step 2: Exploratory Data Analysis (EDA)
- **Sales Analysis:** Investigated total sales, number of customers, and transactions over time to identify overall trends.
- **Customer Demographics:** Visualized the distribution of customers across different lifestages and affinity groups (Premium, Mainstream, Budget).
- **Purchase Behavior:** Analyzed key metrics like units per customer and average price per unit to understand the purchasing power and preferences of different segments.
- **Brand Analysis:** Examined which brands were most popular overall and within specific customer segments.

### Step 3: Customer Segmentation
- **Segmentation Criteria:** The primary segmentation was based on `LIFESTAGE` (e.g., "Young Singles/Couples," "Families," "Older Singles/Couples") and `PREMIUM_CUSTOMER` (affinity groups).
- **Metric-Driven Analysis:** For each segment, I calculated key performance indicators (KPIs) like total sales contribution, number of customers, and chips per customer.
- **Segment Deep Dive:** Conducted a focused analysis to determine the preferred brands and pack sizes for the top-performing segments. For example, identifying if "Young Singles/Couples" prefer smaller, premium brand packs.

### Step 4: Insight Generation & Recommendation
- **Synthesis:** The findings from the EDA and segmentation were synthesized to form a coherent narrative.
- **Strategic Recommendations:** Developed actionable recommendations based on the data. For example: "Target 'Older Singles/Couples' with marketing for smaller pack sizes of mainstream brands, as this segment has high purchasing frequency but lower units per transaction."
- **Presentation:** All insights and recommendations were compiled into a clear and concise PowerPoint presentation for the client, as per the project deliverables.

---

## 4. Project Structure Explained

The repository is organized for clarity and reproducibility.

```

.
├── dataset/                    \# Contains the raw and processed data files.
├── output/                     \# Stores cleaned data files and other analysis outputs.
├── outputs/                    \# Holds generated charts, tables, and segment data.
├── quantium\_chips\_analysis.ipynb \# The main Jupyter Notebook with all code and analysis.
├── requirements.txt            \# A list of all Python dependencies for the project.
├── .gitignore                  \# Specifies which files and directories for Git to ignore.
└── README.md                   \# This detailed project documentation.

````

---

## 5. Technical Stack

-   **Core Language:** Python
-   **Data Analysis & Manipulation:** Pandas, NumPy
-   **Data Visualization:** Matplotlib, Seaborn
-   **Development Environment:** Jupyter Notebook

---

## 6. Local Setup & Replication Guide

To replicate this analysis on your local machine, please follow these steps.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/MrCoss/Quantium-Customer-Segmentation.git](https://github.com/MrCoss/Quantium-Customer-Segmentation.git)
    cd Quantium-Customer-Segmentation
    ```

2.  **Create and Activate a Virtual Environment** (Recommended):
    ```bash
    # Create the environment
    python -m venv venv

    # Activate on Windows
    .\venv\Scripts\activate

    # Activate on macOS/Linux
    source venv/bin/activate
    ```

3.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
    This will open a new tab in your web browser. Navigate to and open the `quantium_chips_analysis.ipynb` file to view and run the analysis.

---

## 7. Disclaimer

This project is part of a simulated work experience provided by **Quantium** through the **Forage** platform. The data and scenario are designed for educational purposes to demonstrate analytical skills in a business context.

---

## 8. Author

-   **Costas Pinto**
-   **GitHub Profile:** [github.com/MrCoss](https://github.com/MrCoss)
````
