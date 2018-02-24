For more details on this template, including what each section is for, see 
https://gist.github.com/PurpleBooth/109311bb0361f32d87a2. 

For info on markdown standards, see 
https://github.com/carwin/markdown-styleguide


# Getting Started

This project enables quick and comprehensive data profiling as a starting point 
for data exploration and assessing data quality.

# Prerequisites

# Installing

# Automated test






# Deployment


# Built with

# Contributing

# Authors


# Licensing
This project is licensed under GNU GPLv3. See LICENSE.md for details

# Features and Roadmap

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

For all columns, grab system information including remarks, data type, nullable,
primary keys, indexes, etc.

Attempt to identify if values are categorical, range, etc.

Summary
- Number of variables
- Total size in memory
- time to execute
- Variable types
- - Numeric
- - Categorical
- - Bolean
- - Text (unique(?))
- - Rejected
- - Unsupported


For all data types:
- Count distinct
- Count nulls (allows nulls but has no nulls)
- Percent missing
- Uniqueness
- Length
- Warnings
- - % missing > threshold
- - % 0 > threshold
- - high cardinality but not unique
- - high correlation > threshold
- - constant value



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

For Strings:
- How many are max length (could indicate truncation)
- Spellcheck?
- Identify upper, lower, mixed case, all start with capital, etc.

Warnings that are available:


### cross-column analysis
- identify prospective keys
- identify correlation (codes should be 1:1 with description etc.)
- - identify multiple standards for flags (True/False 0/1 Y/N 1/blank account
    for nulls)

### Inter-table Analysis
- overalapping value sets that may represent foreign key relatinships


## Output
- Begin with simple plaintext python output
- Provide sample data (random, quasi-random, or just top?)
- Progress to something user-readable, like an html output?
- Finally an interactive interface would be amazingly effective. 

- Ability to see all distinct values or link to other queries

# Greg's ideas and questions

What are automated tests and what do they do? Do they apply here?

Always be thinking of error handling

Similar project: 
https://github.com/pandas-profiling/pandas-profiling/blob/master/README.md


