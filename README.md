# 📚 GoodReads Books Analysis | Power BI Project

## 📌 Overview
This Power BI project analyzes a large-scale GoodReads dataset containing over **88K books** to uncover insights related to authors, publishing trends, reader engagement, and genre distribution.

The dashboard was built using **Power BI Desktop**, with data cleaning and transformation performed in **Power Query** and calculations created using **DAX Measures**.


# 🛠️ Tools & Technologies Used

<p align="left">
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black"/>
  <img src="https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white"/>
  <img src="https://img.shields.io/badge/DAX-0F6CBD?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/CSV-4CAF50?style=for-the-badge"/>
</p>


# 📂 Dataset Information

| Feature | Details |
|---|---|
| 📚 Total Books | 88,728 |
| ✍️ Total Authors | 39.6K |
| 📄 Total Pages | 25 Million |
| 🏷️ Genres | 589 |
| 📑 Rows | 89,340 |
| 📊 Columns | 10 |

## 📌 Dataset Columns
- `id`
- `title`
- `rating`
- `rat_rev`
- `page`
- `year`
- `author_detail`
- `genre`
- `desc`
- `author_link`


# 🧹 Data Cleaning & Transformation

The raw dataset contained several inconsistent text-based fields which were transformed using **Power Query**.

## ✔️ Data Preparation Steps
- Removed unnecessary columns:
  - `desc`
  - `author_link`

- Extracted:
  - ⭐ Number of Ratings
  - 📝 Number of Reviews
  - 📄 Page Count
  - 📅 Publication Year
  - 🗓️ Publication Month

- Corrected data types for:
  - Numeric fields
  - Year column
  - Page column


# 📊 DAX Measures Created

```DAX
Total Books = COUNTROWS('GoodRead_Books')

Total Authors = DISTINCTCOUNT('GoodRead_Books'[author_detail])

Total Pages = SUM('GoodRead_Books'[page])

Total Genres = DISTINCTCOUNT('GoodRead_Books'[genre])
```

## Additional Measures
- Count of Ratings
- Count of Reviews
- Month-wise publication count
- Year-wise publication count


# 📈 Dashboard Features

## 📌 KPI Cards
- 📄 Total Pages
- 🏷️ Total Genres
- ✍️ Total Authors
- 📚 Total Books

## 📌 Interactive Visuals
- 📅 Month with Highest Books Published
- 📆 Year with Highest Books Published
- 📖 Top Author by Total Pages Written
- ✍️ Top Author by Number of Books Written
- ⭐ Top Author by Ratings & Reviews
- 📚 Top 5 Books List

## 🎚️ Interactive Filter
- Rating Range Slicer (0–5)


# 🔍 Key Business Questions Answered

| Business Question | Answer |
|---|---|
| ✍️ Which author has written the most books? | William Shakespeare (418 Books) |
| 📄 Which author has written the maximum pages? | Mary T. Reynolds (~100K Pages) |
| ⭐ Which author has the highest ratings & reviews count? | William Shakespeare |
| 📅 Which month has the highest number of books published? | January (~48K Books) |
| 📆 Which year has the highest number of books published? | 2006 (~5.1K Books) |


# 📊 Key Insights & Findings

## 📖 Author Analysis
- William Shakespeare dominates across multiple KPIs because of the large number of editions and collections cataloged on GoodReads.
- Stephen King consistently ranks among the top modern authors in productivity and reader engagement.
- Mary T. Reynolds contributes the highest share of total pages written.

## 📅 Publishing Trends
- Book publications steadily increased between **2002 and 2006**.
- January shows a significantly higher publication count than other months.

## ⭐ Reader Engagement
- Popular authors receive substantially higher ratings and reviews.
- Review-to-rating patterns indicate strong reader interaction for top authors.

## 📚 Dataset Characteristics
- Multiple editions of the same title exist as separate records.
- Genre values contain multiple genre tags in a single field.


# 🖼️ Dashboard Preview

<img width="594" height="335" alt="Image" src="https://github.com/user-attachments/assets/214ac104-4356-4a8b-af23-9f62e0f0a14d" />


# 🚀 How to Use

1. Download the repository
2. Open the `.pbix` file in **Power BI Desktop**
3. Load or refresh the CSV dataset if prompted
4. Explore the interactive dashboard visuals


# 🎯 Project Objectives

This project was built to:
- Analyze publishing patterns
- Identify top-performing authors
- Measure reader engagement
- Build an interactive BI dashboard
- Practice Power BI, Power Query, and DAX skills


# 📌 Conclusion

This Power BI project transforms raw GoodReads book data into an interactive analytical dashboard that uncovers insights related to books, authors, publication trends, and reader engagement. The project demonstrates practical business intelligence workflows including data cleaning, feature engineering, DAX calculations, and dashboard development using Power BI.
