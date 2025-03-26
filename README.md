
# Data Analyst - Bidur
# Descriptive Analysis
## Project Description: Descriptive Analysis of Rental By-Law Issues in Vancouver
## Project Title: Investigating Rental By-Law Issues in Vancouver
## Objective:
The main purpose of this research project consists of evaluating unresolved rental by-law issues in properties subject to licensing under Vancouver's housing regulations. Analysis of the provided data will reveal patterns while summarizing active violations to guide policymakers and city planners with insights necessary to resolve rental compliance matters.
## Background:
The dataset presents information about rental properties functioning with five or more units which currently maintain unresolved by-law issues. Several government standards including building standards, electrical standards, gas fitting standards, plumbing standards, zoning requirements and maintenance requirements apply to these issues. The evaluation of this data reveals how extensively rental housing quality suffers from existing violations.
## Dataset:
The dataset “[Rental standards - current issues](https://opendata.vancouver.ca/explore/dataset/rental-standards-current-issues/information/)” utilize the following data attributes for data analysis.
- businessoperator: Landlord or owner of the rental property.
-	detailurl: Webpage address for additional information on current by-law issues.
-	streetnumber: Number for street where the business is located.
-	street: Name of street where the business is located.
-	totaloutstanding: The number of unresolved by-law violations.
-	totalunits: The total number of rental units in a building.
-	geom: Spatial data indicating the property’s location.
-	geo_local_area: The planning area where the property is located.
-	geo_point_2d: Location in 2D. 
## Methodology
### Data collection and preparation:
-	Data Source: The dataset for licensed rental properties with unresolved by-law issues for the year 2025 was collected from open data portal of City of Vancouver.
-	Amazon S3: The dataset is ingested into an Amazon S3 bucket, acting as a data lake for raw files.
-	EC2 instance: An EC2 instance is configured to process data and facilitate access.
-	Multiple Servers: Data ingestion occurs from multiple sources, including general, specific, and web servers.
### Data Profiling and Cleaning:
-	AWS Glue DataBrew is used for profiling to detect missing values, inconsistencies, and formatting issues.
-	Cleaning techniques include removing rows with missing Business Operator names and replacing other missing values with null placeholders.
-	Column names are reformatted for consistency.
### Data Cataloging and Structuring:
- A curated zone is established in another S3 bucket to store structured data.
-	AWS Glue Crawlers scan the cleaned dataset for cataloging which results in a structured table present in AWS Glue Data Catalog.
### Data Summarization and Aggregation: 
-	The dataset processing occurs through AWS Athena for execution of queries.
-	Applications of SQL-based aggregation methods determine the sum of total rental units alongside outstanding violations. 
-	Filtering operations are used to extract data for different street.

### Data Visualization:
 Tableau and Excel are used for generating insights and dashboards.
-	Create visual representations such as pie chart and bar graphs to illustrate findings:
     -	Total units of rental property and Total outstandings on rental property.
     - Identifying which local areas have high outstanding amounts and high total units.
     - Identifying which street have high outstanding amounts and high total units.

### Insights and Findings:
- Each rental property contains on average one unresolved issue because there are 1,376 issues among 19,090 units or 14 units per issue. The results indicate that the majority of units follow regulations but a substantial percentage of properties still requires attention for compliance.
- A large number of outstanding violations demonstrates that property owners struggle to meet standards for buildings together with electrical systems and plumbing as well as zoning criteria. Focused inspections and policy interventions in high-density rental areas could improve compliance.
- The non-compliance issues in big rental properties impact numerous residents and affects both the quality of housing facilities and security measures. Serious violations need correction to enhance housing for a large group of residents.

### Tools and Technologies:
- Cloud Storage & Compute: AWS S3, EC2
- Data Processing & ETL: AWS Glue, Athena, SQL
- Data Profiling & Cleaning: AWS Glue DataBrew
- Data Cataloging: AWS Glue Data Catalog, Crawlers
- Data Visualization: Tableau
### Deliverables:
- A comprehensive descriptive report summarizing the analysis process and findings.
- Data visualizations highlighting key trends, compliance challenges, and problem areas.
- Recommendations for city planners and policymakers to improve rental compliance and enforcement strategies.

This descriptive analysis utilizes AWS-based cloud infrastructure to carry out a descriptive analysis that generates essential data about rental property violations in Vancouver. This study provides law enforcement authorities with useful data analytics and visualization tools that help them improve rental housing standards and enforce municipal laws.
