
# Exploratory Data Analysis on Laptops prices 2023

This project involves an in-depth Exploratory Data Analysis (EDA) of a dataset containing specifications of various laptops scraped from Flipkart.com in August 2023. The dataset comprises 984 laptop records with 21 features, encompassing details such as brand, price, type, processor information, storage capacities, screen specifications, and more. The primary objective of this analysis is to uncover insights into the factors influencing laptop prices. This exploration delves into the relationships between laptop attributes and their impact on pricing, providing valuable insights for both consumers and the laptop industry. 

Please note that laptop prices can fluctuate based on various factors, including seasonal promotions and market dynamics.

## A Brief roadmap of the Project:

### 1. Data Gathering: 
The dataset for this project was collected through web scraping from [flipkart.com](https://www.flipkart.com/), a popular e-commerce platform. Initially, there was an attempt to scrape data from Amazon, but technical challenges such as server responses and varying webpage structures led to the decision to use Flipkart.com as the data source. A total of 984 laptop records were successfully scraped from Flipkart.com.

#### Web scraping:
Website Selection: 
- Flipkart.com was chosen as the data source due to its consistent webpage structure and responsiveness, making it more suitable for web scraping.

Handling Missing Data: 
- During the web scraping process, special attention was given to handling missing information. Placeholder values, such as 'No,' 'None,' or '0,' were assigned where specific laptop specifications were unavailable, ensuring comprehensive data coverage.

Data Storage: 
- The scraped data was stored in a dictionary format for initial processing.

#### Converting Data to Excel Format:

To prepare the dataset for analysis, the following steps were taken:

- The data in dictionary format was converted to a JSON file, facilitating data manipulation and organization.

- From the JSON file, only the most relevant features that have a primary impact on laptop prices were retained. Features like Name, Type, Price, SSD, SSD Capacity, HDD Capacity, EMMC Storage Capacity, Screen Type, GPU, and others were selected for further analysis.

- The dataset was then converted into an Excel format, making it easily accessible and compatible with various data analysis tools.

[See Data Gathering Notebook](https://github.com/Kartik-137/EDA-on-Laptops-prices-2023/blob/main/Scrapping_to_csv_code%20(Main%20Notebook).ipynb)

#### ----------------------------------------------------------------------------

### 2. Data Assessing and cleaning:

The success of any data analysis project relies heavily on the quality and cleanliness of the dataset. In the case of this laptops EDA project, a meticulous data assessing and cleaning process was undertaken to ensure the dataset's reliability and integrity.

Here are the key steps involved:

#### Manual Data Assessment: 
- The process began with a comprehensive manual assessment of the dataset. This step involved identifying and documenting various types of unclean data, which can be categorized as "Dirty Data" and "Messy Data."
- During the manual assessment, several quality issues within the dataset were identified. These quality issues encompassed:
    1. Completeness Issue: 
    - Some variables contained missing data, notably in attributes like processor generation, clock speed, and graphic processor.
    2. Validity Issue: 
    - Duplicate entries and incorrect values were found within the dataset, compromising its accuracy.
    3. Accuracy Issue: 
    - Inconsistencies in the format of attribute values, including variations in letter case (uppercase/lowercase), and inaccuracies within certain attributes were noted.
    4. Consistency Issue: 
    - Variability in the pattern of strings and multiple units of measurement for certain attributes contributed to inconsistencies within the dataset.

#### Programmatic Handling of Quality Issues: 
- Once all quality issues were thoroughly documented, a systematic approach was taken to address each issue programmatically. The cleaning process followed a specific order, with completeness issues tackled first, followed by the resolution of other identified issues.

#### Creation of a Clean Dataset: 
- After meticulous data cleaning, a final, cleaned dataset was generated. This dataset was now free from quality-related problems and ready for the next and final step of data analysis.

[See Data Assessing and cleaning Notebook](https://github.com/Kartik-137/EDA-on-Laptops-prices-2023/blob/main/Laptops_DataAssessing.ipynb)


#### ----------------------------------------------------------------------------

### 3. Data Vizualization:

In the context of this laptops project, EDA was employed as the foundation for understanding the data, validating assumptions, and guiding future feature engineering.

- The following are the key highlights of the EDA process:
    
    1. Column Labeling: 
    - The initial step involved categorizing the dataset columns into two main types: categorical and numerical.

    2. Univariate Analysis: 
    - Both numerical and categorical variables underwent separate univariate analyses. 
    - For numerical variables, visualizations such as boxplots and histograms were employed to understand their distributions and uncover potential outliers. 
    - For categorical variables, count plots and pie charts were utilized to visualize the distribution of categories.

    3. Bivariate Analysis: 
    - Given the project's primary focus on understanding the impact of various laptop features on pricing, the bivariate analysis primarily revolved around the "Price" attribute. 
    - This step involved Numerical-Numerical Analysis and Numerical-Categorical Analysis

    4. Multivariate Analysis: 
    - To gain deeper insights, multivariate analyses were conducted. Various types of plots, including scatterplots, barplots, and heatmaps, were created to explore relationships among at least three variables simultaneously. This provided a holistic view of complex interactions within the dataset.

    5. Recording Observations: 
    - Throughout the EDA process, meticulous observations were documented at each step. These recorded observations served as valuable inputs for identifying outliers, detecting frequently occurring categories, and guiding decisions related to feature engineering.

[See EDA on Laptops dataset](https://github.com/Kartik-137/EDA-on-Laptops-prices-2023/blob/main/EDA_LaptopsData.ipynb)

#### ----------------------------------------------------------------------------

### Some important findings from EDA on the Laptops dataset:
1. Price Range: On average, laptops in the dataset cost around 80,000 rupees, with 50% of laptops falling within the 44K to 100K range—a sweet spot for ideal specifications.

2. SSD Prevalence: Nearly 97.57% of laptops have Solid State Drives (SSDs), showcasing the industry's widespread adoption of faster storage technology.

3. Weight vs. Type: Laptops typically weigh between 1.5kg to 2kg, with gaming laptops being the heaviest and most expensive. However, handheld gaming PCs defy this trend.

4. ASUS Dominance: ASUS laptops dominate the dataset on Flipkart, with thin and light versions being popular among various brands. These lightweight laptops cater to students, professionals, and travelers.

5. Price Variability: Laptop prices vary significantly, especially as specifications approach the high end. This reflects the diverse options available to consumers.

6. Feature Cost: Laptops with extras like touchscreen displays, backlit keyboards, and fingerprint sensors tend to be slightly pricier, offering enhanced functionality for users.

These findings align with real-world market dynamics, emphasizing the prominence of SSDs, the impact of laptop weight on portability, and the appeal of feature-rich laptops to consumers seeking added convenience and functionality.