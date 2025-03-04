# **Zeolites Web Scraping Project**

## 📌 **Overview**
This project was developed as part of an **introduction and initiation research internship** at the Laboratory of Separation and Reaction Processes - Laboratory of Catalysis and Materials (LSRE-LCM). The primary objective was to create a comprehensive database for future **Machine Learning applications** by scraping data from the **[International Zeolite Association (IZA)](https://www.iza-structure.org/databases/)** website. This website contains various properties of zeolites, which were extracted and organized for further analysis.
The Python routine created gathers and processes data from HTML pages to extract relevant information about zeolites. It cleans and structures tabular data, retrieves specific text elements from web pages using BeautifulSoup, and formats extracted values for inclusion in a final dataframe. The code includes handling of missing values, string formatting, and HTTP requests to ensure accurate and structured data collection.

---

## 🛠 **Tools and Libraries Used**
To achieve the project's goals, the following **Python libraries** were utilized:

- **Pandas**: For data manipulation and analysis, especially for reading HTML tables and converting them into DataFrames.
- **NumPy**: For handling data through arrays.
- **BeautifulSoup**: For parsing HTML and extracting the necessary information.
- **Requests**: For making HTTP requests to fetch HTML content from web pages.
- **Openpyxl**: For reading and writing Excel files, used for advanced data processing and formatting.

---

## 🔍 **Methodology**
The project involved researching and developing a methodology to search and extract the required properties from the **IZA website**. A Python routine was developed in **Google Collaboratory** to automate this process.

### 📌 **Data Extraction Methods**
1. **Using Pandas:**
   - The `pd.read_html` function was used to search for HTML tables on the web page and convert them into Pandas DataFrames.

2. **Using BeautifulSoup:**
   - When the required information was not found within HTML tables, the `requests.get` function was used to fetch the entire HTML content of the page.
   - BeautifulSoup was then used to parse the HTML and extract information from specific tags and attributes.

---

## 📊 **Database Contents**
The resulting database contains information on **251 zeolites**, including:

- **Zeolite Types**
- **Unit Cell Shape**
- **Space Group**
- **Lengths (a, b, c)**
- **Angles (α, β, γ)**
- **Framework Density**
- **Ring Sizes**
- **Channel Dimensions**
- **Maximum Diameter of a Sphere (inclusion and diffusion)**
- **Accessible Volume**
- **Natural Tiling**
- **Composite Building Units**
- **Chemical Formula**

Additionally, a separate database was created containing the list of **🧬 T-atoms** for each zeolite.

---

## 📂 **Example Outputs**
Below are examples of the generated databases in **Excel format**:

- **Zeolite Properties Table**

![Zeolite Properties Table](https://github.com/user-attachments/assets/fa6b7131-b751-4e2c-92fc-6dad193d7aea)
- **T-Atoms List**

![T-Atoms List](https://github.com/user-attachments/assets/59392b20-e12b-457e-be43-993b9b563e40)

---

## ✅ **Conclusion**
This project provided me valuable experience in **Python programming** and **HTML parsing**. It enabled the extraction and consolidation of data from multiple web pages into a single **DataFrame**, creating a useful resource for future **Machine Learning applications**.

---

### 🚀 **Future Improvements**
- Enhancing data extraction techniques for better accuracy and completeness.
- Expanding the database with additional properties and sources.
- Developing **machine learning models** to analyze the extracted data.
