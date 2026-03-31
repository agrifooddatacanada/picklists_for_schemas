# Picklists for schemas

Picklists, also known as enumerations (enums), define a controlled set of allowable values for a field in a schema. Instead of accepting free-text input, a picklist restricts entries to predefined options (e.g., "Low", "Medium", "High").

In schema design, picklists serve two primary purposes:

* Data consistency – Prevents spelling variations, synonyms, and ambiguous entries
* Validation – Ensures that only approved values are recorded, improving downstream analysis and interoperability.

Within the Semantic Engine, you can:
* Select an existing picklist from pick lists catalogued in this repository, or
* Generate a custom picklist tailored to your project needs.

When a schema containing picklists is used to generate a Data Entry Excel sheet, these controlled values appear as dropdown menus. This constrains user input at the point of entry and reduces the need for later data cleaning.

Picklists are especially useful for categorical variables such as status, method type, location category, or classification codes, where consistent terminology is essential for reliable aggregation and analysis.

# Syntax for .csv picklists
The first 9 rows contain space for the picklist metadata with headings on row 1. 
The general row is for language independent information. Below are rows available for language specific metadata. The order of the language doesn't matter, but the first column must specify the language used.

Starting on row 10 are the headings of the picklist itself and picklist data is contained in row 11.

There is no requirement for the syntax of the picklist, users can look at the column titles and select which picklist columns they want to use in their schema.

| | title | description | keywords | source |  
|----------|-------|-------------|----------|--------|
| general  |       |           |   |https://soilquality.nres.illinois.edu/bulk-density/ | 
| en       | Bulk density class | Generalized classes; specific restrictive thresholds depend on texture. |          |        |
| fr       | Classe de densité apparente | Classes généralisées; les seuils restrictifs dépendent de la texture. |          |        |
|es |Clase de densidad aparente | Clases generalizadas; los umbrales restrictivos específicos dependen de la textura.| | |
| | | | | |
| | | | | |
| | | | | |
| | | | | |
| Code | Class_en | Description_en | Class_fr | Description_fr |
|------|----------|----------------|----------|----------------|
| BDL  | Low      | Favorable for root growth (texture-dependent) | Faible   | Favorable à l’enracinement (selon la texture) |
| BDM  | Moderate | May affect growth (approaching restrictive) | Modéré  | Peut affecter la croissance (proche du restrictif) |
| BDH  | High     | Restrictive to roots (texture-dependent) | Élevé   | Restrictif pour les racines (selon la texture) |
