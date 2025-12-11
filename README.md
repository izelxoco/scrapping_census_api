## Scrapper of Migration Flows in The Bronx, NYC 
This repository contains data scrapped from the US Census data on migration flows from state-to-state, county-to-county, and other smaller-scale entities. Some migration flows include continental regions. The data was compiled from a sample of American Community Survey responses that were collected over a five-year period from 2018 to 2022. 

#### API used: [The ACS 5-Year Migration Flow Files](https://www.census.gov/data/developers/data-sets/acs-migration-flows.html)

#### The API comes from the US Census. 

#### Methodology
The notebook scrapping-census-api.ipynb performs the following steps:

- Part 1: Defines the target dictionary
Using the variables [listed by the US Census for this API] (https://api.census.gov/data/2022/acs/flows/variables.html), the first step was to input all relevant data columns into a dictionary called "target_dict." The dictionary values were re-names of the US Census data that would help improve readability once the information is scrapped later on in the notebook.
 
- Part 2: Create Components of the Endpoint 
In this section, the base_url, query_string, and individualized API key were used to compile a reusable endpoint request. Since the data was collected over a five-year period, the only variables that could change until the newest dataset publishes are the target_county and target_state. In this notebook, we focused on The Bronx County in New York. It is imperative to use the target county and state's respective FIPS code. 

- Part 3: Request & Response
Once the request was processed successfully, the next and nearly final step was to convert the data into JSON, input the data into a dataframe, and finally turn the dataframe into a .csv file. 

#### Outputs
The notebooks output contains a .csv file titled: "bronx_migration_flows_2022.csv"

#### Running the analysis yourself
You can run the analysis yourself. To do so, you'll need the following installed on your computer:

Python 3
The Python libraries specified in requirements.txt
US Census API Key
You would need to retrieve your own US Census API key and save it as a .env file. 
Licensing
All code in this repository is available under the MIT License. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

Feedback / Questions?
Contact Gabriela Flores at 23floresg@gmail.com or Gabriela.Flores07@journalism.cuny.edu. 
