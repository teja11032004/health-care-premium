# Health Insurance Cost Predictor

This project provides a Streamlit web application to predict health insurance costs based on various user inputs. It also includes Jupyter notebooks for data analysis, model training, and evaluation.

## Project Structure

The project is organized into the following directories and files:

-   `main.py`: The main Streamlit application file. This is the entry point for the web interface.
-   `prediction_helper.py`: A Python module containing helper functions for data preprocessing and making predictions using the trained machine learning models.
-   `artifacts/`: This directory stores the trained machine learning models and scalers in `.joblib` format.
    -   `model_rest.joblib`: Trained model for individuals above 25 years of age.
    -   `model_young.joblib`: Trained model for individuals 25 years of age or younger.
    -   `scaler_rest.joblib`: Scaler object for individuals above 25 years of age.
    -   `scaler_young.joblib`: Scaler object for individuals 25 years of age or younger.
-   `data/`: This directory contains the Excel datasets used for model training and evaluation.
    -   `premiums.xlsx`: Original dataset.
    -   `premiums_rest.xlsx`: Dataset for individuals above 25 years of age.
    -   `premiums_young.xlsx`: Dataset for individuals 25 years of age or younger.
    -   `premiums_young_with_gr.xlsx`: Dataset for individuals 25 years of age or younger, including genetical risk.
-   `notebooks/`: This directory holds Jupyter notebooks used for data segmentation, exploratory data analysis (EDA), and model development.
    -   `data_segmentation.ipynb`: Notebook for segmenting the main dataset.
    -   `ml_premium_prediction.ipynb`: Main notebook for premium prediction model development.
    -   `ml_premium_prediction_rest.ipynb`: Notebook for developing the model for individuals above 25 years of age.
    -   `ml_premium_prediction_rest_with_gr.ipynb`: Notebook for developing the model for individuals above 25 years of age, including genetical risk.
    -   `ml_premium_prediction_young.ipynb`: Notebook for developing the model for individuals 25 years of age or younger.
    -   `ml_premium_prediction_young_with_gr.ipynb`: Notebook for developing the model for individuals 25 years of age or younger, including genetical risk.
-   `requirements.txt`: Lists all the Python dependencies required to run the project.

## Installation

To set up the project locally, follow these steps:

1.  **Clone the repository (if applicable):**
    ```bash
    git clone <repository_url>
    cd <repository_name>
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    ```

3.  **Activate the virtual environment:**
    -   **Windows:**
        ```bash
        .\venv\Scripts\activate
        ```
    -   **macOS/Linux:**
        ```bash
        source venv/bin/activate
        ```

4.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

### Running the Streamlit Application

To start the health insurance cost predictor web application, navigate to the project's root directory and run:

```bash
streamlit run main.py
```

This will open the application in your default web browser. You can then input various parameters to get a predicted health insurance cost.

### Running Jupyter Notebooks

To explore the data analysis and model training notebooks:

1.  **Start Jupyter Lab or Jupyter Notebook:**
    ```bash
    jupyter lab
    # or
    jupyter notebook
    ```

2.  Navigate to the `notebooks/` directory within the Jupyter interface and open any of the `.ipynb` files to view or run the analysis.

## Dependencies

The project relies on the following Python libraries, listed in `requirements.txt`:

-   `streamlit`: For building the interactive web application.
-   `pandas`: For data manipulation and analysis.
-   `joblib`: For saving and loading Python objects, particularly the trained models and scalers.
-   `numpy`: For numerical operations.
-   `matplotlib`: For data visualization.
-   `seaborn`: For enhanced data visualizations.
-   `scikit-learn`: For machine learning tasks, including model training and preprocessing.
-   `statsmodels`: For statistical modeling and analysis.

## API Documentation

The `prediction_helper.py` module contains the core logic for prediction.

### `prediction_helper.predict(input_dict)`

-   **Description**: Takes a dictionary of input features and returns the predicted health insurance cost.
-   **Parameters**:
    -   `input_dict` (dict): A dictionary where keys are feature names (e.g., 'Age', 'Gender', 'Income in Lakhs') and values are the corresponding input values.
-   **Returns**:
    -   `int`: The predicted annual health insurance cost.

## Contribution Guidelines

Contributions are welcome! If you'd like to contribute, please follow these steps:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and ensure the code adheres to the existing style.
4.  Write appropriate tests (if applicable).
5.  Submit a pull request with a clear description of your changes.

