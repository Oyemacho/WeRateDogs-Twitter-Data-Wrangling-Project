# We Rate Dogs Project

## Introduction
The dataset analyzed and visualized in this wrangling project is the tweet archive of Twitter user @dog_rates, known as WeRateDogs. WeRateDogs humorously rates people's dogs, with ratings typically having a denominator of 10 and numerators often greater than 10 (e.g., 11/10, 12/10).

The archive includes basic tweet data (tweet ID, timestamp, text, etc.) for over 5000 tweets as of August 1, 2017.

## Data Gathering
- Downloaded the `twitter-archive-enhanced.csv` from Udacity and imported it using `pd.read_csv`.
- Programmatically retrieved `image_predictions.tsv` from Udacity's servers using the `requests` library.
- Accessed tweet data using code provided by Udacity due to inability to collect tweets via API.

## Assessing Data
- Conducted visual assessment using spreadsheet software (Excel) and programmatic assessment in Jupyter Notebook.
- Identified quality and tidiness issues as per project rubrics.
- Created copies of dataframes before proceeding with wrangling.

## Quality Issues Resolved
- Removed tweets before August 1, 2017 without image predictions.
- Addressed outliers in `rating_denominator` column.
- Corrected data types (e.g., tweet ID, timestamp).
- Extracted tweet source from tweet URLs.
- Updated `Doggo`, `Floofer`, `Pupper`, `Puppo` columns to null for "None" values.
- Handled erroneous dog names in image predictions.
- Removed non-dog predictions from image predictions.
- Cleaned hyphens in dog breed names.

## Tidiness Issues Resolved
- Removed unnecessary columns from `dog_twitter_archive`.
- Consolidated `Doggo`, `Floofer`, `Pupper`, `Puppo` columns into a single `dog type` column.
- Merged all tables into a final cleaned dataframe `dog_archive_final`.

## Conclusion
This data wrangling project successfully addressed 11 cleanliness and tidiness issues in the WeRateDogs dataset. Further efforts may be necessary to eliminate all inconsistencies.

**Note:** This summary provides an overview of the cleaning process undertaken. For detailed steps and code, refer to the Jupyter Notebook (`wrangle_act.ipynb`) provided.
