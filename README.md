
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


How It Works

The project script consists of the following key functions:

read_orders(file_path): Loads the orders from the given JSON file.
format_phone_number(phone): Formats the phone number into a xxx-xxx-xxxx format.
process_customer_info(orders_data): Extracts customer data, mapping formatted phone numbers to customer names.
process_item_info(orders_data): Counts the number of orders for each item and stores the item prices.
write_to_json(data, file_path): Writes the given data to a specified JSON file.
main(input_file_path): Orchestrates the entire workflow.

Usage Instructions:
we need to place our JSON file containing the orders in the same directory as the script or provide its full path.
Make sure the required example_orders.json file is in the same directory as dosa.py.
Run the script using the command:python <script_name.py>  <order_file.json> for me it is python dosa_script.py example_orders.json

Additional Notes
1)The script will overwrite existing customers.json and items.json files in the output directory.
2)Correct input file formatting is crucial for error-free processing.





