# Backend and Frontend part of Application

# Flask and Streamlit Application

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Database Configuration](#DatabaseConfiguration)
- [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [Models](#models)
- [Routes](#routes)
- [License](#license)

## Getting Started

This README file provides information and guidance on the usage and structure of the provided Flask application. The application is designed to interact with a MySQL database named "ontology" and includes models and routes related to diseases, treatments, symptoms, and posts.

### Prerequisites

Make sure you have the following installed on your machine:

- Python (version >= 3.6)
- [pip](https://pip.pypa.io/en/stable/installation/)

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/koushikayila/healthcare-data-mining/
    ```

2. Navigate to the Application project directory:

    ```bash
    cd Application
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## DatabaseConfiguration

Update the database connection URI in the following line of the code with your actual database URI

### Running the Application

1. Start the Flask backend:

    ```bash
    python -m backend.py
    ```

   This will run the Flask server.

2. Open another terminal and start the Streamlit app:

    ```bash
    streamlit run app.py
    ```

   This will launch the Streamlit app.

3. Open your web browser and go to [http://localhost:5000](http://localhost:5000) to access the Flask application and [http://localhost:8501](http://localhost:8501) for the Streamlit application.

## Project Structure

Explain the organization of your project, e.g.,

- `backend.py`: Flask application file.
- `app.py`: Streamlit application file.
- `requirements.txt`: List of Python dependencies.

## Models

Diseases: Represents information about diseases.
Treatment: Represents information about treatments.
Symptoms: Represents information about symptoms.
DiseaseSymptom: Represents the relationship between diseases and symptoms, including the count.
DiseaseTreatment: Represents the relationship between diseases and treatments, including the count.
DiseasePost: Represents posts related to diseases.

## Routes

The application includes various routes to retrieve information from the database:

/diseasenames: Retrieves a list of all disease names.
/get_symptoms_and_treatments_and_posts/<disease_name>: Retrieves symptoms, treatments, and posts for a specific disease.
/allsymptoms: Retrieves a list of all symptom names.
/get_diseases_and_percentages_for_symptom/<symptom_description>: Retrieves diseases and their percentages for a given symptom.
/getDiseasesSymptom/<symptomName>: Retrieves diseases and their counts for a given symptom.

# SympGraph Generator

## Overview

SympGraph Generator is a Python tool for creating symptom graphs from a dataset. The tool reads a CSV file (combinedData.csv) containing diseases, symptoms, treatments data, processes it, and generates a graph representation of the connections and weights between different symptoms.

## Files in the Repository

`sympgraph_generator.py`: This is the main Python script that reads the `combinedData.csv` file generated from Metamap, processes the symptom data, and generates a graph using libraries such as NumPy, Matplotlib, and NetworkX.

`requirements.txt`: Lists the Python libraries required to run the script (numpy, matplotlib, networkx).

## Installation and Setup

1. **Clone the Repository:** Clone this repository to your local machine.

2. **Install Dependencies:** Run the following command to install the necessary Python libraries:

`pip install -r requirements.txt`

## Usage

1. **Prepare Your Data:** Ensure your metamap combined data is in the `../metamap/data/` folder.

2. **Run the Script:** Execute `sympgraph_generator.py` to generate the symptom graph. The script will read the data from above mentioned file and generate `sympgraph.csv` file as consisting of the final symgraph output comprising of data  in the format `Source,Destination,Weight` and a graph visualization of a sample of first 20 posts.


# MetaMap Annotator Project README

## Introduction

The MetaMap Annotator is a Java-based application designed to annotate web data using the MetaMap annotator Java API. It efficiently processes data scraped from various sources and prepares it for further analysis. This guide will walk you through the setup and usage of the MetaMap Annotator.

## Prerequisites
Java JDK
Internet Connection for downloading necessary files

## Installation
Step 1: Download Required Software
Download the MetaMap main release from MetaMap Main Download.
Download the MetaMap Java API from MetaMap Java API Download.
Step 2: Setup MetaMap
Extract both downloads.
Merge the public_mm folder from the Java API into the public_mm folder of the main release. Ignore duplicate files during the merge.
Navigate to the public_mm directory and run the installation script:
Copy code
cd public_mm/
./bin/install.sh
Verify the successful installation by checking the install.log for the creation of mmserver.
Step 3: Start Servers
Start the WSD, MedPost, and MM servers in the following order:
bash
Copy code
./bin/wsdserverctl start
./bin/skrmedpostctl start
./bin/mmserver
Step 4: Clone and Setup MetaMap Annotator
Clone the MetaMap Annotator project.
Navigate to the MetaMapAnnotator directory.

## Launch the application:
bash
Copy code
java -jar dist/MetaMapAnnotator.jar
Usage
The application automatically processes CSV files located in the neighboring scraper/data folder.
Run the combine.py script in the resources folder to merge the annotated data from various sources into a single CSV file.