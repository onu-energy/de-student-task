# Onu.Energy Data Engineering Task

Welcome to the Onu.Energy data engineering task! This task is designed to assess your ability to pull data from a public API using Python and write the results to a storage solution of your choice. Please ensure that this task takes no more than 2 hours to complete.

## Task Description

Your objective is to:

1. Select a public API of your choice.
2. Use Python to fetch data from the chosen API.
3. Write the fetched data to a storage solution (e.g., local file, database, cloud storage).

## Requirements

- **Programming Language:** Python
- **Time Limit:** 2 hours

## Steps to Follow

1. **Select a Public API:**
   - Choose any public API that provides data you find interesting or relevant. Some examples include:
     - [OpenWeatherMap API](https://openweathermap.org/api)
     - [NASA API](https://api.nasa.gov/)
     - [COVID-19 API](https://covid19api.com/)
     - [GitHub API](https://docs.github.com/en/rest)

2. **Fetch Data Using Python:**
   - Write a Python script to make a request to the chosen API.
   - Parse the response and extract the necessary data.

3. **Store the Data:**
   - Choose a storage solution to store the fetched data. Examples include:
     - Writing to a local file (CSV, JSON, etc.)
     - Inserting into a database (SQLite, PostgreSQL, etc.)
     - Uploading to cloud storage (AWS S3, Google Cloud Storage, etc.)

4. **Document Your Work:**
   - Create a README file explaining your approach, the API you chose, and how to run your script.
   - Include any setup instructions if necessary.
   - Address any limitations of your work.
   - Consider future improvements or extensions.

## Submission

Please submit your work as a private GitHub repository. Add the following users as collaborators to the repository:
    - <ds@onu.energy>
    - <ar@onu.energy>

## Evaluation Criteria

- **Correctness:** Does the script correctly fetch and store the data?
- **Code Quality:** Is the code well-organized, readable, and maintainable?
- **Documentation:** Is the README clear and comprehensive?

## Getting Started

Here is an example to help you get started:

### Example: Fetching Data from OpenWeatherMap API

#### Step 1: Install Required Libraries

```bash
pip install requests
```

#### Step 2: Write the Script (`fetch_data.py`)

```python
import requests
import json

def fetch_weather_data(city):
    api_key = 'your_api_key' # Maybe don't hardcode secrets in your code!
    url = f'http://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}'
    response = requests.get(url)
    return response.json()

def save_to_file(data, filename='output_data.json'):
    with open(filename, 'w') as f:
        json.dump(data, f, indent=4)

if __name__ == "__main__":
    city = 'London'
    weather_data = fetch_weather_data(city)
    save_to_file(weather_data)
```

#### Step 3: Document Your Work (`README.md`)

```markdown
# Onu.Energy Data Engineering Task

## Overview

This project demonstrates how to fetch data from the OpenWeatherMap API using Python and save it to a local JSON file.

## How to Run

1. Install the required libraries:
    ```bash
    pip install requests
    ```

2. Replace `'your_api_key'` in `fetch_data.py` with your OpenWeatherMap API key.

3. Run the script:
    ```bash
    python fetch_data.py
    ```

4. The output will be saved to `output_data.json`.
```

Good luck, and we look forward to reviewing your submission!

Best regards,

The Onu.Energy Team