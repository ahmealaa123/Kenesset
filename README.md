Knesset Data Analysis and Visualization Project

📘 Project Overview

The Knesset Data Analysis and Visualization Project is an interactive web application built using Streamlit and Pandas. This project provides users with an intuitive way to explore and visualize voting results from the 25th Knesset elections. Users can view detailed voting data, filter results by city, and analyze how different political parties performed across regions.

The main goal of the project is to offer an accessible, user-friendly interface for anyone interested in understanding and analyzing the election results.



🎯 Key Features

Interactive User Interface: The application allows users to explore election data interactively.

City-Specific Analysis: Users can filter the voting data by selecting a specific city from a dropdown list.

Dynamic Charts: The application generates interactive visualizations (line charts) to display the total votes for each party in the selected city.

Data Table View: The full election dataset is displayed in tabular format, making it easy for users to browse raw data.



📂 Project Structure:
project-folder
├── 📁 data
│    └── knesset_25.xlsx     # Excel file containing voting data for the 25th Knesset elections
├── 📄 Streamlit_app.py      # Main Streamlit application file
└── 📄 README.md             # Project documentation (this file)



🚀 Technologies Used

Python: Main programming language for data processing and application logic.

Pandas: Used for loading and manipulating the election data from Excel.

Streamlit: Used to create an interactive web application for visualizing the election results.

Excel: The election data is stored in an Excel file (knesset_25.xlsx).



⚙️ Setup and Installation:
To run this project locally, follow these steps:
pip install streamlit pandas openpyxl.

Run the Streamlit Application:
streamlit run Streamlit_app.py
View the Application:
Open your web browser and navigate to http://localhost:8501/.


📊 Data Explanation:
The main dataset for this project is stored in an Excel file named knesset_25.xlsx. The structure of the data is as follows:
Column

Description

city_name

Name of the city where votes were counted

total_votes

Total number of votes cast in that city

party_1

Number of votes received by Party 1

party_2

Number of votes received by Party 2

The columns after total_votes contain the vote counts for specific parties. Each row corresponds to the voting results for a specific city.



📱 How to Use the Application
Start the Application by running the following command: streamlit run Streamlit_app.py
Select a City from the dropdown menu at the top of the page.

View the Data: Once a city is selected, the following information will be displayed:

Data Table: Shows the detailed voting data for all parties in the selected city.

Line Chart: Visualizes the number of votes each party received in that city.

Analyze and Explore: You can change the selected city at any time to see how the votes change between regions.




🔧 Project Files

1. Streamlit_app.py

This file contains the main logic of the Streamlit web application.

It imports the election data from knesset_25.xlsx and processes it using Pandas.

It includes a simple, intuitive interface with options to filter and visualize the voting data.

2. knesset_25.xlsx

This is the raw data file that contains the voting results.

Each row corresponds to a city, and the columns contain information on the total votes and the votes for each party.




📋 Code Walkthrough

The Streamlit_app.py script follows these main steps:

Import Libraries:
import streamlit as st
import pandas as pd
Streamlit is used for the app interface, and Pandas is used to load and process the Excel file.

Load Data:
file_path = "knesset_25.xlsx"
data = pd.read_excel(file_path)
The script reads the Excel file and loads it into a Pandas DataFrame.

User Interface:
st.title("عرض نتائج الانتخابات")
st.write("### بيانات الأصوات حسب المدن")
st.dataframe(data)
The app displays a title and shows the raw data as a table for user exploration.


🛠️ Possible Improvements

Add more visualizations: Bar charts, pie charts, and comparative views across cities.

Search and Filter: Allow users to search for specific parties or filter data by additional criteria.

Export Data: Enable users to export filtered data as CSV or Excel files.

Multi-language Support: Add support for English, Hebrew, or other languages.


📚 Resources and References

Streamlit Documentation

Pandas Documentation

Python Official Documentation




