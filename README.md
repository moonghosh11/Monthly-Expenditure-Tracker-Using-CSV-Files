Monthly Expenditure Tracker (Python + CSV)

A simple and efficient Monthly Expenditure Tracker built using Python and CSV files.
This project allows users to record expenses, categorize them, view monthly summaries, and analyze spending patterns — all through a lightweight, file-based system without needing a database.


---

# Features

 Add new expenses (amount, category, date, description)

 Store all data in CSV format

 View monthly expense totals

 Generate category-wise summaries

 Retrieve all transactions for a given month

 Lightweight, portable, and beginner-friendly

 No external libraries required (uses only Python's built-in CSV module)



---

# Project Structure

monthly-expenditure-tracker/
│
├── main.py                     # Main application logic
├── tracker.py                  # Functions for reading/writing CSV data
├── utils.py                    # Helper functions (date handling, validations)
├── data/
│   └── expenses.csv            # Expense records stored here
└── README.md                   # Project documentation


---

# CSV Format

The expenses.csv file stores data in this format:

date	category	amount	description

2025-01-03	Food	150	Lunch with friend
2025-01-05	Transport	50	Bus fare
2025-01-07	Bills	800	Electricity bill



---

# How It Works

1. Adding an Expense

Users can enter:

Date (YYYY-MM-DD)

Expense category (Food, Bills, Transport, etc.)

Amount

Optional description


The entry is appended to the CSV file.

2. Viewing Monthly Summary

The program:

Reads all rows from the CSV

Filters entries by month

Calculates total spending

Displays category-wise totals


3. Listing All Transactions

Users can view all expenses for any month in a clean, formatted table.


---

# Getting Started

Requirements

Python 3.x

No additional libraries needed



---

1. Clone the repository

git clone https://github.com/yourusername/monthly-expenditure-tracker.git

2. Navigate to project folder

cd monthly-expenditure-tracker

3. Run the program

python3 main.py


---

# Example Code Snippet

import csv
from datetime import datetime

def add_expense(date, category, amount, description):
    with open("data/expenses.csv", "a", newline="") as file:
        writer = csv.writer(file)
        writer.writerow([date, category, amount, description])

def load_expenses():
    with open("data/expenses.csv", "r") as file:
        reader = csv.reader(file)
        return list(reader)


---

# Future Enhancements

Add graphs for monthly reports using matplotlib

Export reports to PDF or Excel

Add a Tkinter or Web-based UI

Integrate income tracking

Categorization suggestions using AI/ML

Automatic detection of recurring expenses



---

# License

This project is open-source and available under the MIT License.


---

# Contributing

Contributions are welcome!
Feel free to open issues, suggest features, or create pull requests.


---

# Author

Munmun Ghosh
25BET10009


---
