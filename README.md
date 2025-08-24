# Service Completion Time Prediction

## 🚀 Overview

This project uses a machine learning model to predict the processing time for a booked government service. Given an appointment date, time, and task ID, the model estimates how many minutes the staff will take to complete the task once it has started. This helps manage citizen expectations and improve operational efficiency.

The model is an **XGBoost Regressor** trained on historical booking, staffing, and task data.

---

## 📂 Repository Files

-   `Task01.ipynb`: The main Jupyter Notebook that contains all the steps for data exploration, feature engineering, and model training.
-   `predict.py`: A standalone Python script that loads the pre-trained model to make new predictions.
-   `requirements.txt`: A list of all the Python libraries needed to run the project.
-   `service_completion_artifacts.pkl`: The saved file containing the trained model and all necessary helper objects (encoders, feature lists, etc.).
-   `/data/`: A folder containing the raw datasets:
    -   `bookings_train.csv`: Historical data of all appointments.
    -   `staffing_train.csv`: Historical data of daily staffing levels.
    -   `tasks.csv`: A list of all possible tasks and their corresponding sections.
    -   `task1_test_inputs.csv`: An example input file for which predictions are needed.

---

## ⚙️ Setup and Installation

To get started, clone the repository and install the required libraries.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/service-completion-time-prediction.git](https://github.com/your-username/service-completion-time-prediction.git)
    cd service-completion-time-prediction
    ```

2.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

---

## 🛠️ How to Use

There are two main steps: training the model and making predictions.

### 1. Training the Model (Optional)

If you want to retrain the model with new data, run the `Task01.ipynb` notebook from top to bottom. This will generate an updated `service_completion_artifacts.pkl` file.

### 2. Making Predictions

To make predictions on a new set of appointments:

1.  Make sure your input data is in a CSV file with the columns `row_id`, `date`, `time`, and `task_id`. An example is `task1_test_inputs.csv`.

2.  Run the `predict.py` script from your terminal:
    ```bash
    python predict.py
    ```

3.  The script will:
    -   Load the pre-trained model from `service_completion_artifacts.pkl`.
    -   Read the `task1_test_inputs.csv` file.
    -   Generate predictions for each row.
    -   Save the results in a new file named `task1_predictions.csv`.

The output file will contain the original `row_id` and the new `expected_completion_time_minutes` column.# Service Completion Time Prediction

## 🚀 Overview

This project uses a machine learning model to predict the processing time for a booked government service. Given an appointment date, time, and task ID, the model estimates how many minutes the staff will take to complete the task once it has started. This helps manage citizen expectations and improve operational efficiency.

The model is an **XGBoost Regressor** trained on historical booking, staffing, and task data.

---

## 📂 Repository Files

-   `Task01.ipynb`: The main Jupyter Notebook that contains all the steps for data exploration, feature engineering, and model training.
-   `predict.py`: A standalone Python script that loads the pre-trained model to make new predictions.
-   `requirements.txt`: A list of all the Python libraries needed to run the project.
-   `service_completion_artifacts.pkl`: The saved file containing the trained model and all necessary helper objects (encoders, feature lists, etc.).
-   `/data/`: A folder containing the raw datasets:
    -   `bookings_train.csv`: Historical data of all appointments.
    -   `staffing_train.csv`: Historical data of daily staffing levels.
    -   `tasks.csv`: A list of all possible tasks and their corresponding sections.
    -   `task1_test_inputs.csv`: An example input file for which predictions are needed.

---

## ⚙️ Setup and Installation

To get started, clone the repository and install the required libraries.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/service-completion-time-prediction.git](https://github.com/your-username/service-completion-time-prediction.git)
    cd service-completion-time-prediction
    ```

2.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

---

## 🛠️ How to Use

There are two main steps: training the model and making predictions.

### 1. Training the Model (Optional)

If you want to retrain the model with new data, run the `Task01.ipynb` notebook from top to bottom. This will generate an updated `service_completion_artifacts.pkl` file.

### 2. Making Predictions

To make predictions on a new set of appointments:

1.  Make sure your input data is in a CSV file with the columns `row_id`, `date`, `time`, and `task_id`. An example is `task1_test_inputs.csv`.

2.  Run the `predict.py` script from your terminal:
    ```bash
    python predict.py
    ```

3.  The script will:
    -   Load the pre-trained model from `service_completion_artifacts.pkl`.
    -   Read the `task1_test_inputs.csv` file.
    -   Generate predictions for each row.
    -   Save the results in a new file named `task1_predictions.csv`.

The output file will contain the original `row_id` and the new `expected_completion_time_minutes` column.
