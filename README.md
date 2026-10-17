# 🏃 Health & Fitness Trends Analysis

## 📌 Project Overview

Health & Fitness Trends Analysis is a Python-based data analysis project developed for a sample company called **VitalityApp**.

VitalityApp tracks users' daily movement and body measurements. The goal of this project is to understand activity levels, identify highly active users, study the relationship between height and weight, and segment users into Active and Inactive groups.

The analysis uses Python, Pandas, and Matplotlib to calculate statistics, filter data, create visualizations, and generate insights that could support personalized fitness engagement strategies.

## 🎯 Project Objectives

- Calculate the average daily steps across all users.
- Identify power users who walk more than 10,000 steps per day.
- Visualize the distribution of daily steps using a histogram.
- Analyze the relationship between height and weight using a scatter plot.
- Create an `Active_User` column based on daily step counts.
- Count Active and Inactive users.
- Calculate the percentage of users in each activity segment.

## 🛠️ Technologies Used

- **Python** — programming language
- **Pandas** — data manipulation and analysis
- **Matplotlib** — data visualization
- **Jupyter Notebook** — interactive coding environment
- **Google Colab** — cloud-based notebook environment

## 📂 Project Structure

```text
health-fitness-trends-analysis/
│
├── README.md
├── Health_fitness.ipynb
└── health_fitness_dataset.csv
```

**Note:** The CSV file is required to run the notebook. Upload `health_fitness_dataset.csv` if you have the dataset and permission to share it. The dataset was referenced in the notebook but was not included as a separate uploaded file.

## 📊 Dataset Description

The notebook expects a CSV file named `health_fitness_dataset.csv` with these columns:

| Column | Description |
|---|---|
| `Person_ID` | Identifier for each person |
| `Daily_Steps` | Number of steps recorded per day |
| `Height_cm` | Height in centimetres |
| `Weight_kg` | Weight in kilograms |

The exact dataset size and its source should be added here when confirmed.

## 🔍 Analysis Performed

### 1. Average Daily Steps

Calculates the average number of daily steps across all users using Pandas.

```python
average_daily_steps = df["Daily_Steps"].mean()
print(f"Average daily steps: {average_daily_steps:.1f}")
```

This provides a baseline for understanding the activity levels represented in the dataset.

### 2. Identify Power Users

Filters users who walk **more than 10,000 steps per day**.

```python
power_users = df[df["Daily_Steps"] > 10000]
```

The results are sorted from highest to lowest step count. The notebook also displays the number of power users and their average daily steps.

### 3. Daily Step Distribution

Creates a histogram of daily steps using Matplotlib.

The visualization includes:
- Chart title
- X-axis label: Daily Steps
- Y-axis label: Number of Users
- Average-step reference line
- Summary statistics, including median and standard deviation

The histogram helps show how daily activity levels are distributed across the dataset.

### 4. Height and Weight Relationship

Creates a scatter plot comparing `Height_cm` and `Weight_kg`.

The notebook also calculates the correlation coefficient between these two variables. This can help identify a possible linear relationship in the dataset, but correlation alone does not establish causation.

### 5. Active and Inactive User Segmentation

Creates an `Active_User` column using the following rule:

- **Active:** Daily steps are greater than or equal to 8,000.
- **Inactive:** Daily steps are fewer than 8,000.

```python
df["Active_User"] = df["Daily_Steps"] >= 8000
```

The notebook also creates an `Activity_Segment` column with the labels `Active` and `Inactive`.

### 6. Activity Segment Comparison

Counts users in each segment and calculates each segment's percentage of the dataset.

This helps summarize the proportion of users who meet the activity threshold and those who do not.

## 📈 Expected Outcomes

After running the notebook, the analysis provides:

- Average daily steps
- A list and count of power users
- A histogram of daily steps
- Descriptive statistics for step counts
- A height-versus-weight scatter plot
- A height–weight correlation coefficient
- Active and Inactive user counts
- The percentage of users in each segment

Actual numerical results depend on the dataset used.

## 💡 Potential Business Applications

The analysis could help a fitness application team:

- Understand user activity patterns.
- Identify highly active users.
- Develop activity-based user segments.
- Plan personalized workout notifications.
- Explore engagement strategies for less-active users.

These are potential applications; the notebook does not measure the effectiveness of any marketing campaign.

## ⚙️ Requirements

Install Python and the required libraries:

```bash
pip install pandas matplotlib jupyter
```

## ▶️ How to Run the Project

### Option 1: Google Colab

1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `Health_fitness.ipynb`.
3. Upload `health_fitness_dataset.csv` to the session.
4. Run the notebook cells in order.

### Option 2: Run Locally

1. Download or clone this GitHub repository.
2. Install the required Python libraries.
3. Place the notebook and CSV file in the same folder.
4. Open a terminal in that folder.
5. Run:

```bash
jupyter notebook
```

6. Open `Health_fitness.ipynb` and execute the cells.

**Important:** Some notebook cells use the Google Colab path `/content/health_fitness_dataset.csv`, while another uses the relative path `health_fitness_dataset.csv`. For local execution, use a consistent path such as:

```python
df = pd.read_csv("health_fitness_dataset.csv")
```

## 🎓 Learning Outcomes

This project demonstrates practical experience with:

- Reading CSV datasets using Pandas
- Calculating averages and descriptive statistics
- Filtering records using conditions
- Sorting data
- Creating Boolean and categorical columns
- Counting and comparing user segments
- Creating histograms and scatter plots
- Calculating correlation
- Interpreting data for potential business applications

## 🚀 Future Enhancements

- Add more visualizations for activity patterns.
- Compare activity levels across user groups if additional data is available.
- Add missing-value checks and data validation.
- Build an interactive dashboard using Streamlit.
- Explore activity trends over time if date information is available.
- Evaluate user engagement after personalized notifications, if campaign data becomes available.

## 👩‍💻 Author

**Poorvi N S**

B.Tech — Artificial Intelligence and Machine Learning

## 📄 License

This project is intended for educational and learning purposes. Add a license file if you want to define how others may reuse or distribute the project.
