# 📱 Google Play Store Dataset - Data Cleaning and Exploratory Data Analysis (EDA)

Welcome to my Exploratory Data Analysis (EDA) project on the **Google Play Store Dataset**.  
This project focuses on data cleaning, exploratory analysis, and visualization of key insights about apps on the Play Store.

---

## 📑 Dataset Overview
| Column Name        | Description                                                                                                        |
| :----------------- | :----------------------------------------------------------------------------------------------------------------- |
| **App**            | Name of the application on the Play Store.                                                                         |
| **Category**       | The category to which the app belongs (e.g., FAMILY, GAME, TOOLS).                                                 |
| **Rating**         | Average user rating of the app (on a scale of 1.0 to 5.0).                                                         |
| **Reviews**        | Number of user reviews for the app. Stored as numeric values.                                                      |
| **Size**           | Size of the app (e.g., `14M` for 14 MB, `8.7M` for 8.7 MB, `Varies with device` if size is unspecified).           |
| **Installs**       | Total number of times the app has been installed by users (e.g., `1,000+`, `5,000,000+`).                          |
| **Type**           | Specifies whether the app is **Free** or **Paid**.                                                                 |
| **Price**          | Cost of the app (in US dollars), if it’s a paid app; otherwise `0`.                                                |
| **Content Rating** | Age group recommendation for the app (e.g., Everyone, Teen, Mature 17+).                                           |
| **Genres**         | Additional classification of apps (could be a specific or multi-category genre, like `Action`, `Puzzle`, `Tools`). |
| **Last Updated**   | Date on which the app was last updated on the Play Store.                                                          |
| **Current Ver**    | Current version of the app available for download.                                                                 |
| **Android Ver**    | Minimum required Android OS version needed to install the app (e.g., `4.1 and up`, `Varies with device`).          |


## 📦 Project Structure
##  Data Cleaning Process

- **Converted `Reviews` column**:
  - Replaced unimportant symbols like `:`, `,`, `.`.
  - Replaced invalid entries with `NaN` and dropped them.
  - Converted valid values to `int`.
  
- **Cleaned `Size`, `Installs`, and `Price` columns**:
  - Removed extra characters like `M`, `k`, `$`, `+`, `,`.
  - Converted invalid entries to `NaN`.
  - Dropped invalid records and converted cleaned values to appropriate numeric types (`int` or `float`).

- **Modified `Last Updated` column**:
  - Extracted `Date`, `Month`, and `Year` into separate new columns for detailed temporal analysis.

- **Checked for duplicate rows and dropped them.**

- **Checked number of numerical and categorical columns** using `df.dtypes` and classified them.

---

## 📊 Exploratory Data Analysis (EDA) Process

- **Drew a KDE Plot** to visualize the distribution (proportion of count) for all numerical features.
- **Created a Countplot** to show the distribution of counts across all categorical features.
- **Plotted a Pie Chart** to visualize which app categories are widely present and popular in the Play Store.
- **Created a Bar Chart** displaying the **Top 10 App Categories** based on app count.

---

## 📈 Key Visualizations

- 📊 Proportion of numerical features (KDE Plot) - Rating and Year are left skewed.Reviews, size , installs and price are right skewed - Most apps on playstore are free.
- 📊 Proportion of categorical features (Countplot)
- 📊 Pie chart of app categories by count - there are more kinds of apps in playstore which are      under category of family , games and tools. Beauty , comics, arts and weather kind of apps        are very less in playstore
- 📊 Bar chart for Top 10 app categories - family category has the most number of apps followed       by games category . least number of apps belong to beauty category

