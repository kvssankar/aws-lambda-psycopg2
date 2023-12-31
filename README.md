
# Introduction
Simplify PostgreSQL database interactions within your Python-based Lambda functions!

***This repository provides pre-built Lambda layers containing the psycopg2 library for Python versions 3.7, 3.8, 3.9, 3.10, 3.11, and 3.12.***

## Using the Layers

 1. Choose the Appropriate Layer. 
 2. Select the layer matching your Python runtime and download the corresponding ZIP file.
 3. Upload the Layer to AWS. 
 4. Navigate to the Lambda console and create a new layer.
 5. Upload the selected ZIP file and specify a name (e.g., psycopg2-py38).
 6. Attach the Layer to Your Lambda Function.
 7. Edit your Lambda function's configuration.
 8. Under "Layers", add the newly created layer.

## Usage in Your Lambda Function:

Import the Library:



    import psycopg2


Connect to Your PostgreSQL Database:

    conn = psycopg2.connect(
        database="your_database_name",
        user="your_username",
        password="your_password",
        host="your_database_host",
        port="5432"  # Default PostgreSQL port
    )


Execute Queries and Perform Actions:


    cur = conn.cursor()
    cur.execute("SELECT * FROM your_table")
    rows = cur.fetchall()
    for row in rows:
        print(row)
    conn.close()


## Additional Information

Supported Python Versions: 3.7, 3.8, 3.9, 3.10, 3.11, 3.12
Layer Size: Approximately 3 - 5 MB each
License: MIT


## License

This project is licensed under the MIT License. See the LICENSE file for details.
