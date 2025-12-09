# Anime Feature Extraction Project

A data analysis project that extracts and analyzes features from anime data using Python, pandas, and regular expressions.

## 📋 Project Overview

This project demonstrates feature extraction techniques on anime dataset, including parsing complex text fields, date handling, and statistical analysis. It's designed for educational purposes to showcase data cleaning, transformation, and exploratory data analysis skills.

## 🗂️ Project Structure

```
anime-feature-extraction/
│
├── anime.csv                      # Dataset containing anime information
├── feature-extraction.ipynb       # Jupyter notebook with analysis
├── regex_guide.pdf               # Reference guide for regex patterns
└── README.md                     # Project documentation
```

## 🎯 Features Extracted

### 1. **Episode Count**

- Extracted episode numbers from title strings using regex pattern `\((.*?)\)`
- Cleaned and converted to integer format
- Example: "TV (64 eps)" → 64

### 2. **Time Stamp**

- Parsed airing period using regex pattern `([A-Za-z]{3} \d{4} - [A-Za-z]{3} \d{4})`
- Format: "Apr 2009 - Jul 2010"
- Handles month and year extraction

### 3. **Duration in Months**

- Calculated total runtime using `dateutil.relativedelta`
- Converts time periods to months (+1 to include starting month)
- Useful for analyzing anime series length

## 📊 Analysis Performed

### Key Insights

- **Highest Scored Anime**: Fullmetal Alchemist: Brotherhood (9.10 score, 64 episodes, 16 months)
- **Longest Episode Count**: Gintama (201 episodes, 48 months runtime)
- **Longest Running Series**: Ginga Eiyuu Densetsu (110 episodes over 111 months)

### Queries Implemented

1. Finding anime with highest score
2. Top 5 highest scoring anime
3. Anime with most episodes
4. Top 5 anime by episode count
5. Longest running anime series

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical operations
- **dateutil**: Date parsing and calculation
- **Regular Expressions**: Pattern matching for text extraction

## 📦 Installation

```bash
# Clone the repository
git clone https://github.com/MeetBataviya13/anime-feature-extraction.git

# Navigate to project directory
cd anime-feature-extraction

# Install required packages
pip install pandas numpy python-dateutil jupyter
```

## 🚀 Usage

1. Open Jupyter Notebook:

```bash
jupyter notebook feature-extraction.ipynb
```

2. Run all cells sequentially to:
   - Load the anime dataset
   - Extract features from title column
   - Perform data analysis
   - View results and insights

## 📝 Code Highlights

### Episode Extraction

```python
df["Episode_Count"] = df["Title"].str.extract(r"\((.*?)\)")
df["Episode_Count"] = df["Episode_Count"].str.replace(" eps", "")
df["Episode_Count"] = df["Episode_Count"].astype(int)
```

### Time Period Parsing

```python
df["Time_Stamp"] = df["Title"].str.extract(r"([A-Za-z]{3} \d{4} - [A-Za-z]{3} \d{4})")
```

### Duration Calculation

```python
def calculate_total_months(period):
    start_str, end_str = period.split(' - ')
    start_date = datetime.strptime(start_str, '%b %Y')
    end_date = datetime.strptime(end_str, '%b %Y')
    r = relativedelta(end_date, start_date)
    return r.years * 12 + r.months + 1
```

## 📈 Dataset Information

- **Total Entries**: 50 anime series
- **Columns**: Rank, Title, Score, Episode_Count, Time_Stamp, Months
- **Score Range**: 8.76 - 9.10
- **Data Types**: Integer (Rank, Episode_Count, Months), Float (Score), String (Title, Time_Stamp)

## 🎓 Learning Outcomes

- Text parsing using regular expressions
- Data cleaning and transformation
- Feature engineering from unstructured text
- Date/time manipulation
- Pandas DataFrame operations
- Statistical analysis and sorting

## 📚 Resources

- `regex_guide.pdf`: Comprehensive guide for understanding regex patterns used in this project

## 🤝 Contributing

This is an educational project, but suggestions and improvements are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## 📄 License

This project is created for educational purposes. Feel free to use and modify for learning.

## 👨‍💻 Author

**Meet Bataviya**

- GitHub: [@MeetBataviya13](https://github.com/MeetBataviya13)

## 📞 Contact

For questions or feedback, please open an issue on GitHub.

## ⭐ Show Your Support

⭐ If you find this project helpful, please consider giving it a star!

*Note: This is an educational project created for learning data analysis concepts and techniques.*
