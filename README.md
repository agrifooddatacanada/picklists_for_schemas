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

