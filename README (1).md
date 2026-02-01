# Data Preprocessing Utilities (Interview Test)

This repository contains simple, self-contained implementations of two common data preprocessing functions:

1. A function to **split data into training and testing sets**.
2. A function for **normalizing data using Min-Max scaling (MinMaxScaler)**.

These utilities are intentionally minimal and easy to understand. The purpose of this repository is to serve as a **technical test for interviews**, demonstrating basic skills in data handling and preprocessing.

---

## 1. Train/Test Split Function

The train/test split function takes a dataset (features and optionally labels) and divides it into:

- **Training set** – used to fit or train a model.
- **Test set** – used to evaluate how well the model generalizes to unseen data.

Typical parameters include:

- `X`: Features (e.g., list, array, or matrix of inputs).
- `y` (optional): Targets/labels corresponding to `X`.
- `test_size`: Proportion or absolute number of samples to allocate to the test set.
- `shuffle`: Whether to randomly shuffle data before splitting.
- `random_state`: Seed to make the split reproducible.

This mirrors the behavior of common libraries like `sklearn.model_selection.train_test_split`, but is implemented manually for clarity.

---

## 2. Min-Max Normalization Function (MinMaxScaler)

The Min-Max normalization function rescales numerical features to a fixed range, typically **[0, 1]**.

For each feature value $x$:

$$
x_\text{scaled} = \frac{x - x_\text{min}}{x_\text{max} - x_\text{min}}
$$

Where:

- $x_\text{min}$ is the minimum value of that feature in the data.
- $x_\text{max}$ is the maximum value of that feature in the data.

This helps:

- Put features on a comparable scale.
- Improve the performance and stability of many machine learning algorithms.

The function usually has two main steps:

1. **Fit**: Compute `min` and `max` for each feature.
2. **Transform**: Apply the scaling formula to the data.

---

## 3. Sample Use Case

To illustrate how these functions work together, this repository includes a **sample use case** where:

1. A small example dataset is created.
2. The dataset is **split into training and testing sets** using the custom train/test split function.
3. The **training and testing features are normalized** using the Min-Max normalization function.

This example is meant to:

- Show typical usage of both functions.
- Demonstrate the preprocessing workflow from raw data to scaled train/test sets.
- Provide a clear, readable reference for interview discussions.

---

## 4. Repository Purpose

The main goal of this repository is to be used as part of a **technical interview test**. It is designed to:

- Showcase understanding of basic data preprocessing concepts.
- Provide simple, readable implementations instead of relying only on library calls.
- Serve as a starting point for further questions, modifications, or extensions during an interview.

You are encouraged to:

- Review the code,
- Run the sample use case,
- And adapt or extend the functions as needed.