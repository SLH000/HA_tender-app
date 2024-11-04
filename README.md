# HK HA Tender Award App

## Features

- **Data Filtering**: Select specific hospitals and tender categories to filter the data.
- **Category Assignment**: Automatically assigns tenders to categories based on keywords in the subject.
- **Download Filtered Data**: Export your filtered contractor list to a CSV file for further analysis.

## Installation

To set up and run the application locally, follow these steps:

### Prerequisites
Python 3.x installed on your system.
1. Install dependencies with the following command:
   ```
   $ pip install streamlit pandas numpy
   ```
2. Clone this repository
   ```
   git clone <repository_url>
   cd HA_tender-app

   ```
3. Download the Data
   Place your haTender.csv file in a Data folder within the project directory:

   ```
   HA_tender-app/
   ├── Data/
   │   └── haTender.csv
   ├── streamlit_app.py
   └── README.md
   Running the App
   ```
4. To launch the app, run the following command from the project directory:

   ```
   streamlit run streamlit_app.py
   This command will open a new tab in your web browser with the dashboard.
   ````
## Code Explanation

### Data Cleaning and Processing
1. ***Data Loading***:  Reads the haTender.csv file from the Data folder.
2. ***Column Renaming***: Renames columns to standardize the format.
3. ***Row and NA Removal***: Drops irrelevant rows and rows with missing values in the "Subject" column.
4. ***Filtering and Category Assignment***: Defines keyword-based conditions to categorize tenders automatically (e.g., Pharma, Device, Testing).
5. ***Separate DataFrames***: Creates filtered DataFrames for specific categories for ease of analysis.

### Streamlit Dashboard
1. **Filters**: Sidebar filters for selecting specific hospitals and categories.
2. **Data Display**: Displays a table of filtered contractor information.
3. **Download Feature**: Allows users to download filtered contractor data as a CSV file.

## Usage
1. Use the sidebar to filter contractors by hospital and category.
2. View the Contractor List section, which updates dynamically based on the filters.
3. Click the Download Contractor List as CSV button to save the filtered list for external use.

## File Structure
- `streamlit_app.py`: Contains the main application code.
- `Data/haTender.csv`: The input data file containing HA tender information.
- `README.md`: Documentation for setting up and using the app.

### Example

When you launch the app, you’ll see the “Contractor List” with a title and description. Use the filters on the sidebar to narrow down the list based on hospitals or categories, then download the filtered list if needed.

This README should provide a clear guide for setting up and using the HK HA Tender Award App. 