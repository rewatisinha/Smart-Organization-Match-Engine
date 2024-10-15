# **** Smart-Organization-Match-Engine ****
This project aims to match user-entered credit union organization names with the names in a master database to identify existing clients. The system follows a stepwise matching approach, starting with address-based matching and refining the process to ensure a high degree of accuracy.

# Project Overview
When users provide a list of organization names (credit unions), the goal is to match those names with the existing entries in the master database. In cases where key details such as addresses are missing, the project uses ChatGPT to fetch the missing addresses before proceeding with the matching process. The matching itself is done in several stages to maximize match accuracy and ensure no duplicates or mismatches occur.

# Key Features:
Stepwise Matching Process:
- First match on name and address.
- Second match on name, city, and state for remaining records.
- Final match based on name alone for those that remain unmatched.
  
Automatic Address Retrieval: For entries where addresses are missing in the user list, the system uses ChatGPT to retrieve the address information.

Multiple Matching Criteria: Matches are made using a combination of name, address, city, and state to ensure robust identification of existing clients.

# Methodology:
Data Preprocessing:
The user list of credit union organization names is cleaned and prepared.
Missing addresses are fetched from ChatGPT for entries without address details.

Matching Process:
Stage 1: Match based on exact address and name for all organizations that have complete address information.
Stage 2: For the remaining unmatched organizations, match using name, city, and state.
Stage 3: If any organizations are still unmatched, match them using only the name.

Validation:
Multiple criteria are used to verify the accuracy of the matches, and mismatches are flagged for manual review.

# Tech Stack:
Python for processing and matching logic.
Pandas for data handling and transformation.
OpenAI GPT API to retrieve missing addresses.
Fuzzy Matching (optional) for enhancing name match accuracy.

# Use Cases:
Client Identification: Efficiently match user-provided organization names with a master database to identify existing clients.
Data Enrichment: Automatically fetch missing address data for credit unions using GPT to ensure more comprehensive data matching.
Stepwise Matching Logic: Helps ensure accuracy in client identification by applying multiple stages of criteria.

# How to Run the Model:
Install required packages from requirements.txt.
Prepare the user list and master database of organizations.
Run the Python script to initiate the stepwise matching process.
Review and validate matches using the output file.
