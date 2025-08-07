# ACCENTURE-EXCEL-DATA-PROJECT


## 📊 Project Overview: Content Popularity Analysis for Accenture

### 🧭 Objective
As part of a business task from Accenture following my completion of an Introduction to Excel course, I was asked to analyze client content data to determine the **top 5 content categories with the largest popularity**. The goal was to provide actionable insights into which types of content resonate most with users based on reaction scores.

---

### 📁 Data Source & Structure
The analysis was based on three interconnected datasets:
- **Content**: Contains content ID, category, and content type.
- **Reaction**: Includes user reactions tied to content ID.
- **Reaction Type**: Maps each reaction type to a sentiment and a numeric score.

Popularity was defined by the **aggregate reaction score** per content category. To calculate this, I needed to merge the datasets and sum scores by category.
<img width="753" height="478" alt="image" src="https://github.com/user-attachments/assets/bc5d63a1-dbc8-415a-b0bc-f4f2bc57ba99" />

---

### 🧹 Data Cleaning
Using Excel, I performed the following cleaning steps:
- **Removed duplicates** using Excel’s “Remove Duplicates” tool.
- **Filtered and deleted blank rows** from key columns using the filter function.
- **Eliminated irrelevant columns** such as User ID and URL to streamline the dataset.
- Ensured the final cleaned dataset contained **24,574 rows** of valid data.

---

### 🔗 Data Modeling
To prepare the data for analysis:
- I **converted the cleaned data into structured tables**.
- Using **VLOOKUP**, I merged:
  - The **Reaction** table with the **Content** table via `Content ID` to retrieve category and content type.

<img width="806" height="254" alt="image" src="https://github.com/user-attachments/assets/0d2a182e-3534-409e-87e9-cbe24118d84f" />

  - The **Reaction** table with the **Reaction Type** table via `Reaction Type` to retrieve sentiment and score.
<img width="766" height="421" alt="image" src="https://github.com/user-attachments/assets/fa98504f-a6b9-4aa8-9955-a10657a911af" />


This created a unified dataset where each reaction was linked to its content category and associated score.

---

### 📈 Analysis & Insights
To identify the most popular categories:
- I extracted a list of **unique content categories**.
- Using **SUMIF**, I calculated the **total reaction score** for each category:
  ```excel
  =SUMIF('Cleaned data modelled table'!F:F, 'Popular Categories'!A2, 'Cleaned data modelled table'!H:H)
  ```

<img width="614" height="546" alt="image" src="https://github.com/user-attachments/assets/b584426e-62be-488b-a2cd-39499292166a" />

- I then **sorted the categories by total score in descending order** to identify the top 5.

---

### 🧠 Outcome
The final result was a ranked list of the **top 5 content categories** based on user engagement and sentiment scores. This analysis provides the client with a clear view of which content types are driving the most positive reactions, helping guide future content strategy.
<img width="517" height="343" alt="image" src="https://github.com/user-attachments/assets/73c5262a-f4ea-4008-9cc5-3a4259c95c64" />

---

### 📂 Worksheets Used
- `Content`
- `Reaction`
- `Reaction Type`
- `Cleaned & Merged Data`
- `Popular Categories Summary`

---
Content sheet
https://onedrive.live.com/edit.aspx?resid=EEC9C4B233DF8639!sb0f2f15695be469d9cfff101cf09fba8&migratedtospo=true&wdinitialsession=eaf82974-849a-448f-86e2-90b7ca31fc18&wdrldsc=2&wdrldc=1&wdrldr=PromptEditInBrowser%2CReloadInEditMode%2CTransitionNon

Reaction type sheet

https://onedrive.live.com/edit.aspx?resid=EEC9C4B233DF8639!s9e88850d5859459692603e44f8cd425d&migratedtospo=true&wdinitialsession=66c04c1d-a932-432a-ae39-244a7179fe2e&wdrldsc=2&wdrldc=1&wdrldr=PromptEditInBrowser%2CReloadInEditMode%2CTransitionNon

Reaction sheet
https://onedrive.live.com/edit.aspx?resid=EEC9C4B233DF8639!s9b0ddd810a924395a0f0b5197c96cf6e&migratedtospo=true&wdinitialsession=8f1f86d5-cc38-401f-be4f-504da930b46e&wdrldsc=2&wdrldc=1&wdrldr=ReloadInEditMode%2CTransitionNonMetro%2COnSaveAsWebMet
