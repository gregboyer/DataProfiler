For more details on this template, including what each section is for, see 
https://gist.github.com/PurpleBooth/109311bb0361f32d87a2. 

For info on markdown standards, see 
https://github.com/carwin/markdown-styleguide


# Getting Started

This project enables quick and comprehensive data profiling as a starting point 
for data exploration and assessing data quality.

While primarily intended as a group learning project, this will also be a
functioning tool

# Prerequisites

- Git (https://git-scm.com/downloads)
- github account (https://github.com)
- Python 3.6 (included in anaconda)
- Pandas (included in anaconda)

Recommended:
- Anaconda, a full package of python tools (https://www.anaconda.com)
- Pycharm, which has a community edition and a full version that's free with 
  .edu addresses. http://jetbrains.com/pycharm

# Learning Resources and Useful Links

Wiki: What is data profiling?
https://en.wikipedia.org/wiki/Data_profiling

Free python course on Udacity
https://classroom.udacity.com/courses/ud1110

The no deep shit guide to git
http://rogerdudler.github.io/git-guide/

Data sets that can be used for testing
https://www.dataquest.io/blog/free-datasets-for-projects/


# Installing



# Automated test






# Deployment


# Built with

Python 3.6
Pandas


# Contributing

Project is hosted at https://github.com/gregboyer/DataProfiler. 

All pull requests require peer review of code before they can be merged. This is
enforced via git.


# Licensing
This project is licensed under GNU GPLv3. See LICENSE.md for details


# Acknowledgments

In researching this project, the pandas-profiling provided validation that
this could really work:
https://github.com/pandas-profiling/pandas-profiling/blob/master/README.md




# Possible Features and Brainstorming

## Goals
To assess data quality and characterics with minimum configuration, modification
or other human interaction

## Priority
Priority in terms of ease and performance will be to begin with single-column,
move to cross-column analysis, and progress to inter-table analysis

## Database connections
Would like to connect to a wide range of files with as little modification as 
possible before beginning analysis.

## Analysis

### Database Analysis
- What schemas/tables are in the DB. What size. What indexes. When were stats
last run. Are there any pending reorgs. 
- Potentially drill in to individual tables and even columns

### Single column analysis (one table)

- For all columns, grab system information including remarks, data type, 
nullable, primary keys, indexes, etc.

- Attempt to identify if values are categorical, range, etc.

- Validation rules. Ability to create a quick library of rules that can be
validated, maybe in the form of a regex expression? Can that deal with nulls?

- Visualize distributions

Summary
- Number of variables
- Total size in memory
- time to execute
- Variable types
-- Numeric
-- Categorical
-- Bolean
-- Text (unique(?))
-- Rejected
-- Unsupported


For all data types:
- Count distinct
- Count nulls (allows nulls but has no nulls)
- Percent missing
- Uniqueness
- Length
- Warnings
-- % missing > threshold
-- % 0 > threshold
-- high cardinality but not unique
-- high correlation > threshold
-- constant value



For Ints:
- Count 0s
- Min
- Max
- Mean
- Mode (top 5 most common values)
- Distribution
- Standard deviation
- Frequency(?)
- Count
- Sum
- min/max/average length

For Strings:
- How many are max length (could indicate truncation)
- Identify upper, lower, mixed case, all start with capital, etc.
- pattern analysis. Phone numbers, addresses, emails, etc.

Warnings that are available:


### cross-column analysis
- identify prospective keys
- identify correlation (codes should be 1:1 with description etc.)
-- identify multiple standards for flags (True/False 0/1 Y/N 1/blank account
   for nulls)

### Inter-table Analysis
- overalapping value sets that may represent foreign key relatinships
- visualize joins
- cardinality
- validate key integrity


## Output
- Begin with simple plaintext python output
- Provide sample data (random, quasi-random, or just top?)
- Progress to something user-readable, like an html output?
- Finally an interactive interface would be amazingly effective. 

- Ability to see all distinct values or link to other queries

# Greg's ideas and questions

What are automated tests and what do they do? Do they apply here?

Always be thinking of error handling




