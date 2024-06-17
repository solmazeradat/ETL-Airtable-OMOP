# ETL-Airtable-OMOP [UNDER DEVELOPMENT]
The purpose of this Python Jupyter notebook to convert a subset of the Synthea dataset to the Person OMOP CDM using Airtable APIs. The project is a result of a [nocode Build day](https://lu.ma/nocodescotland) Hackathon event organised by [nocode.scot](https://www.nocode.scot/)

- The slides to the presentation can be found under [slides](slides)
- The notebook can be found under [notebook](notebook)
- The video to the presentation can be found [to be added after the 20th July ](here)

# Development Setup 
Before running the Python notebook, the follwoing prerequisities need to be setup:

## Prerequisities 

### Airtable 
- The test dataset for this project can be found under under [patients](https://github.com/OHDSI/Tutorial-ETL/blob/master/data/syntheaRaw/patients.csv). Using the ``Add or import`` function in Airtable, the dataset can be added and data types can be changed.
- The test script which was adapted to trasfom the dataset can be found under [Insert_Person](https://github.com/OHDSI/Tutorial-ETL/blob/master/materials/Implementation/Insert_Person_Lauren.sql).
- To placeholder for the [Person](https://ohdsi.github.io/CommonDataModel/cdm54.html#person) table can be added ready to be populated with the transfomed data.

This project used Airtable API to interact with your Airtable bases. 

**Key Concepts:**

- **Base ID:** Each Airtable base has a unique identifier that you'll need to use in your API calls. You can find this in the base URL when viewing your base in the Airtable interface.
- **API Key:** To access your Airtable data securely, you'll need to generate an API key from your account settings. There are different key types (personal access tokens, service accounts) with varying access levels.
- **RESTful API:** Airtable uses a RESTful API architecture. This means you interact with your data using standard HTTP verbs like GET (retrieve data), POST (create records), PUT (update records), and DELETE (delete records).

### Python & VS code
- It is recommended to use [VS Code](https://code.visualstudio.com/) as your IDE for developing this project.

**Repo Setup**
1. Clone this repository to your machine
2. ``cd`` into the repo directory and set up a virtual environment:
```
python3 -m venv airtable-env
```
3. Now activate the virtual environment by running
```
source airtable-env/bin/activate
```
4. Install ``ipykernel`` by running
```
pip3 install ipykernel
```
5.Create a new kernal by running
```
# That would create a kernel named 'airtable-etl'
python3 -m ipykernel install --user --name=airtable-etl
```
6. Select the created kernal ``airtable-etl`` from the top right hand corner of Vscode. Alternatley,To choose your kernel in Vscode

- Open the Vscode search bar: cmd+shift+p.
- Type in the word ``kernal`` & choose: “Notebook: Select Notebook Kernel”.
- Select the kernal ``airtable-etl``
