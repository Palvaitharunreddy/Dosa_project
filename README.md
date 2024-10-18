
Restaurant Order Analysis
Project Overview
The goal of this project is to help a new Dosa restaurant analyze their orders and derive insights from their customers' purchasing behavior. The restaurant has provided JSON data containing individual order details from the past year. We aim to process this data to create two key outputs:

Customers Information: A JSON file containing phone numbers and their associated customer names.
Items Information: A JSON file summarizing the number of orders and the price of each item.
The project is designed to make it easier for the restaurant to review past orders and better understand their customers and menu items.

Requirements:
Running this script necessitates Python on your system, leaning solely on Python's intrinsic libraries for functionality, thereby negating the need for external package installations.

Design and Implementation:
The script's core revolves around parsing a JSON file populated with orders, each detailing a customer's contact information and their selected items. This data is then organized into two separate JSON files—customers.json and items.json—streamlining customer information and item statistics for subsequent analysis or application.

Data Storage Mechanisms:

1)Customers Dictionary: Utilizes phone numbers as unique keys linked to customer names, ensuring direct access to customer data.
2)Items Dictionary: Employs item names as keys, mapping to sub-dictionaries that record item prices and purchase frequencies, facilitating item data management and updates.

Data Processing Workflow
JSON Input Management: Leverages Python's json.load() to transform the JSON file into a manipulable Python structure, setting the stage for data iteration.
Order Iteration: Each order undergoes a twofold analysis:
1)Customer Data Extraction: Harvests and catalogs customer names and phone numbers in the customers dictionary.
2)Item Data Compilation: Evaluates each item within an order, initializing or updating its record in the items dictionary based on presence and purchase count.

Output Generation
customers.json Output: This step translates the customers dictionary into a neatly indented JSON file, mapping phone numbers to customer names.
items.json Output: Similarly, the items dictionary is converted into a JSON file, detailing item prices and order counts.

Script Execution
Path Configuration: An input_file_path variable is predefined within the script to point towards the JSON file location. Adjustments may be necessary to align with the actual file path.
Operational Feedback: Post-execution, the script signals the successful creation of output files through a console message.

Instructions
1)Place your JSON order file in the script's directory or specify the file's full path.
2)Ensure the order file matches the expected structure, akin to example_orders.json.
3)djust the input_file_path within the script to your JSON file's path:input_file_path = 'path_to_your_order_file.json'
4)Execute the script:python python_script.py
After completion, the output directory will house the customers.json and items.json files.

Input and Output Formats
Input Format: The script expects a JSON file with an array of orders, each containing a customer's phone number, name, and a list of purchased items.
Output Files:
1)customers.json: Maps customer phone numbers to names.
2)items.json: Details each item's price and total order count.

Additional Notes
1)The script will overwrite existing customers.json and items.json files in the output directory.
2)Correct input file formatting is crucial for error-free processing.





