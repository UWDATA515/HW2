# Homework 2: Data Analysis Basics

## Dataset
Obtain the CSV (comma separated variable) file containing the counts of
bicycles crossing the Fremont Bridge since 2012 (as described in
`https://data.seattle.gov/Transportation/Fremont-Bridge-Hourly-Bicycle-Counts-by-Month-Octo/65db-xm6k`).

## Folder Structure
```
.
├── .github
|   └── ISSUE_TEMPLATE
|       └── homework-grade.md
├── LICENSE
├── README.md
└── project
    ├── README.md
    ├── analysis
    │   └── hw2.ipynb
    └── data
        └── bicycle_data.csv
```
Clone your git repository and create a directory called `project`. 

Inside `project`, create 2 subdirectories called `data` and `analysis` and 1 file `README.md` (files with `.md` format are [markdown files](https://www.markdownguide.org/cheat-sheet/) which GitHub renders for you). 

Download the data from
`https://data.seattle.gov/api/views/65db-xm6k/rows.csv?accessType=DOWNLOAD` and
put it in the `data` directory as `bicycle_data.csv`. 

Create a Jupyter notebook `hw2.ipynb` in `analysis` folder to analyze these data.

## Problem
In the notebook, please complete the following (total 10 points):
1. Read the CSV file into a pandas dataframe `1pt`
1. Remove the existing "Fremont Bridge Total" column from the datagrame `1pt`
1. Add columns to the dataframe containing:
   * The total (East + West) bicycle count - in a column called "total" `1pt` (Yes, you just deleted a similar column in the previous step. We're making you calculate it yourself)
   * The hour of the day - in a column called "hour" `1pt`
   * The year - in a column called "year" `1pt`
1. Create a new dataframe with the subset of data from the year 2016 `1pt`
1. For the dataframe in the previous step (for data from 2016), use pandas + matplotlib to plot the counts by hour, as a **bar chart** (i.e. hour of the day on the x-axis, total daily counts on the y-axis). Pick your favorite color and/or style for the plot - use at least one customization. `1pt`
1. Use python (and pandas) programming to computationally determine what is (on average) the busiest hour of the day. In other words, which hour has the highest average number of bicycle counts? After the computation, include a Markdown cell that is a one-sentence answer to the busiest-hour question in human-readable terms (ie what does this mean in our normal way of talking about time) `1pt`
1. In the README.md file you create in the `project` folder, use proper Markdown to include your one-sentence answer from the previous question and list any resources you used in the process of completing this assignment (what websites/searches/documentation/manuals etc you used) `1pt`

`Push your homework to GitHub. Please avoid uploading your data folder. (1pt)` Extra cheer for people who use [.gitignore](https://git-scm.com/docs/gitignore) for this. 

Note that we fully expect this analysis to cover some unfamiliar ground, and
require teaching yourself a bit about Python and/or the Pandas package. Part of
the intent of this assignment is to give you practice seeking help via the web,
which (in our experience) is an essential part of using any data science
tool. For example, if you type a question about Pandas into search engine, you’ll
often find an existing answer to your question or something similar on the
website StackOverflow.

A couple other online resources that might be helpful as you work through this:

* [The Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) (free online) has a chapter devoted to Pandas
* [Jake’s Jupyter Workflow Video Series](http://jakevdp.github.io/blog/2017/03/03/reproducible-data-analysis-in-jupyter/) shows some examples of working with this particular dataset in a Jupyter notebook. 

## Hints
The “date” field is a string coded as “yyyy-mm-dd hh” where “yyyy” is the
year, “mm” is the month, “dd” is the day, and “hh” is the hour. (You’ll need to
write python code to decode the string.)

## Bonus
If you're already familiar with pandas, convert the whole "Date" column to a
datetime format, e.g., `datetime.datetime` or `numpy`'s datetime or the default
Pandas datetime format. Write a little about the difference between these
formats in the `README.md` file you created in the `project` folder. Extra learning points if your readme file uses
different kinds of markdown syntax.
