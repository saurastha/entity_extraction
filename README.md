# Entity Extraction and Question Answer

### Overview
This project focuses on extraction of entities (subject, object and their relationship, usually given by verb, and build a directed graph using the extracted entities. The graph is then saved and used for Question Answering user queries which is in natural language.

### Installation
All the required packages are listed in **requirements.txt** file. Install the dependencies as:

```$ pip install -r requirements.txt```

Next is to install spacy which requires setting up the configuration based on the user's device. Installation of spacy is clerly explained in their website:

```https://spacy.io/usage```

Also make sure you have downloaded trained pipeline for english medium:

```$ python -m spacy download en_core_web_md```

### Technical Aspect
There are three ipynb notebook. Each carrying out different functionality.

1. Data_Collection.ipynb  
This notebook focuses solely on data collection. Articles from *Online Khabar* is scraped and saved into file.

2. Entity_and_Relationship_Extraction.ipynb  
Using the raw data collected in prevoius step, this notebook focues on cleaning the collected data, extracting the entities and their relationship and finally storing the information in a graph. **networkx** library is used to create and save the graph.

3. Get_Answer.ipynb  
Finally, the stored information is used in order to answer user query. Since the user query is in natural language, the query is first cleaned and then using spacy some information from the query is extracted. These extracted informations is used to traverse the graph and find and return answer (if any).


### Graph Database Visualization
!([Graph_Visualize.png](https://github.com/saurastha/entity_extraction/blob/master/Graph_Visualize.png))


