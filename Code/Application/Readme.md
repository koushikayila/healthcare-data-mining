# Backend and Frontend part of Application

# Flask and Streamlit Application

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [License](#license)

## Getting Started

### Prerequisites

Make sure you have the following installed on your machine:

- Python (version >= 3.6)
- [pip](https://pip.pypa.io/en/stable/installation/)

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/flask-streamlit-app.git
    ```

2. Navigate to the Application project directory:

    ```bash
    cd Application
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

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

## License

This project is licensed under the [MIT License](LICENSE).
