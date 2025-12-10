# Student Performance Analysis

A comprehensive data analysis project exploring student performance metrics using Python and Pandas. This educational project analyzes a dataset of 1 million student records to understand the relationships between study habits, attendance, participation, and academic outcomes.

## 📊 Project Overview

This project performs exploratory data analysis on student performance data, examining key factors that influence academic success including:

- Weekly self-study hours
- Attendance percentage
- Class participation
- Total scores and grades

## 🗂️ Project Structure

```
student-performance/
│
├── main.ipynb                    # Main Jupyter notebook with analysis
└── student_performance.csv       # Dataset (1M student records)
└── README.md
```

## 📁 Dataset

The dataset contains **1,000,000 student records** with the following features:

| Column | Description |
|--------|-------------|
| `student_id` | Unique identifier for each student |
| `weekly_self_study_hours` | Hours spent studying per week |
| `attendance_percentage` | Percentage of classes attended |
| `class_participation` | Participation score (0-10) |
| `total_score` | Final academic score |
| `grade` | Letter grade (A, B, C, D) |

## 🔍 Analysis Performed

The notebook explores the following questions:

1. **Basic Data Exploration**
   - Dataset dimensions
   - Column names and data types
   - First and last 10 rows

2. **Statistical Analysis**
   - Maximum weekly study hours
   - Top performers by study time
   - Highest attendance and participation students
   - Perfect score analysis (100.0)

3. **Feature Engineering**
   - `score_level`: Categorizes scores as High (≥90), Medium (70-89), or Low (<70)
   - `effeciency`: Study efficiency ratio (total_score ÷ weekly_self_study_hours)
   - `study_category`: Categorizes study habits as Light (<10h), Moderate (10-20h), or Heavy (>20h)

## 🛠️ Technologies Used

- **Python 3.x**
- **NumPy**: Numerical computing
- **Pandas**: Data manipulation and analysis
- **Jupyter Notebook**: Interactive development environment

## 🚀 Getting Started

### Prerequisites

```bash
pip install numpy pandas jupyter
```

### Running the Analysis

1. Clone the repository:

```bash
git clone https://github.com/MeetBataviya13/Python-Pandas-Projects.git
cd student-performance
```

2. Launch Jupyter Notebook:

```bash
jupyter notebook main.ipynb
```

3. Run all cells to reproduce the analysis

## 📈 Key Findings

- **166 students** studied the maximum 40 hours per week
- **67,378 students** achieved perfect attendance (100%)
- **24,128 students** had maximum class participation (10.0)
- **268,121 students** scored perfect 100.0 on total_score

## 📝 Educational Purpose

This project is designed for:

- Learning data analysis with Pandas
- Understanding exploratory data analysis (EDA) techniques
- Practicing feature engineering
- Analyzing large datasets efficiently

## 👤 Author

**Meet Bataviya**

- GitHub: [@MeetBataviya13](https://github.com/MeetBataviya13)

## 📄 License

This project is open source and available for educational purposes.

## 🤝 Contributing

This is an educational project, but suggestions and improvements are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch
3. Submit a pull request

## ⭐ Show Your Support

Give a ⭐️ if this project helped you learn something new!

---

*Note: This is an educational project created for learning data analysis concepts and techniques.*
