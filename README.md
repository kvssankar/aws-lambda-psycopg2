Simplify PostgreSQL database interactions within your Python-based Lambda functions!

This repository provides pre-built Lambda layers containing the psycopg2 library for Python versions 3.7, 3.8, 3.9, 3.10, 3.11, and 3.12.

## Using the Layers

Choose the Appropriate Layer:

Select the layer matching your Python runtime and download the corresponding ZIP file.
Upload the Layer to AWS:

Navigate to the Lambda console and create a new layer.
Upload the selected ZIP file and specify a name (e.g., psycopg2-py38).
Attach the Layer to Your Lambda Function:

Edit your Lambda function's configuration.
Under "Layers", add the newly created layer.
## Usage in Your Lambda Function:

Import the Library:

Python
import psycopg2
Use code with caution. Learn more
Connect to Your PostgreSQL Database:

Python
conn = psycopg2.connect(
    database="your_database_name",
    user="your_username",
    password="your_password",
    host="your_database_host",
    port="5432"  # Default PostgreSQL port
)
Use code with caution. Learn more
Execute Queries and Perform Actions:

Python
cur = conn.cursor()
cur.execute("SELECT * FROM your_table")
rows = cur.fetchall()
for row in rows:
    print(row)
conn.close()
Use code with caution. Learn more
## Additional Information

Supported Python Versions: 3.7, 3.8, 3.9, 3.10, 3.11, 3.12
Layer Size: Approximately 1 MB each
License: MIT
## Contributing

We welcome contributions! Please refer to the CONTRIBUTING.md file for guidelines.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
