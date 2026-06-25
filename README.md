# PySpark Sales Data Analysis Application

This repository contains a containerized PySpark application that reads a sales dataset, performs various analytical transformations, and saves filtered metrics to a CSV file.

## Project Structure
- `sales.csv`: Source dataset.
- `app.py`: PySpark core application code.
- `Dockerfile`: Multi-layered build tool for environment reproducibility (Java, Python, Spark).
- `high_sales_output/`: Auto-generated directory containing the filtered high-value sales dataset.

## Setup & Local Execution

### Prerequisites
- Docker installed on your machine.

### After cloning this repo:
    ### Step 1: Build the Docker Image
        Navigate to the root project directory and build the container:
        ```bash
        docker build -t assign17-app .
        ```

    ### Step 2: Run the Application
        ```bash
        docker run --rm -it -p 8080:8080 -v $(pwd):/workspace assign17-app
        ```

    ### Step 3: After running the app.ipynb file , cell by cell :
        high_sales_output- folder will be visible and in that there will be a csv file of partition-0 ,that is your output