# POLLUTION-MEASUREMENT: Dust Assessment Via Roadside Plant Leaves

An automated computer vision solution designed to evaluate urban pollution levels by analyzing dust accumulation on roadside plant leaves. By leveraging a custom-built dataset across diverse Indian seasons and a Sequential Convolutional Neural Network (CNN), this project aims to pinpoint critical pollution zones to guide smart city interventions—such as automated target-zone water sprinkling and strategic urban forestry.

---

## 🚀 Project Overview & Objectives
* **Accurate Pollution Assessment:** Detect localized particulate matter and evaluate environmental loads across urban areas.
* **Smart Interventions:** Identify target zones requiring automated water-sprinkling systems to wash plant canopies and clear the air.
* **Ecological Planning:** Map highly polluted sectors to recommend the cultivation of specific, pollution-absorbing flora.
* **High Performance:** Achieved an impressive **95% evaluation accuracy** using a custom data pipeline.

---

## 📊 Dataset & Seasonal Distribution
Because public datasets for localized dust accumulation on flora were unavailable online, a custom dataset of **500 images** was manually collected across various regions of India. The data is strategically divided by seasons to capture diverse environmental and atmospheric variations:

| Season | Photo Count | Environmental Characteristic |
| :--- | :--- | :--- |
| ☀️ **Summer Season** | 150 photos | High ambient dust, dry particulate matter, and soil suspension. |
| 🌧️ **Rainy Season** | 50 photos | Natural washing baseline; clean/semi-clean leaves for control. |
| ❄️ **Winter Season** | 300 photos | Heavy smog, soot accumulation, and moisture-bound dust. |

### Classification Tiers
The deep learning framework processes the image inputs and classifies them into three distinct structural groups:
1. **Less Polluted Leaf:** Cleaner pockets / low traffic volume.
2. **Polluted Leaf:** Moderate to high particulate accumulation.
3. **Highly Polluted / Target Zone:** Critical areas requiring immediate ecological or automated sprinkler intervention.

---

## 🛠️ Tech Stack & Key Dependencies
* **Core Language:** Python
* **Data Engineering & Visualization:** `NumPy`, `Pandas`, `OS`, `Matplotlib`
* **Deep Learning Framework:** `Keras` (with `TensorFlow` backend)
* **Optimization Algorithm:** `Adam` Optimizer

---

## 🧠 Model Architecture & Implementation Details
The project utilizes a **Sequential Convolutional Neural Network (CNN)** optimized for fine-grained image feature extraction. The pipeline consists of the following deep learning operations:

* **Data Augmentation:** Leveraging the `Keras` preprocessing library to artificially expand the dataset (flipping, rotating, and zooming), preventing model overfitting.
* **Convolution & Stride:** Extracting foundational structural features from the dust layers on the leaf surface.
* **Padding:** Preserving edge-case characteristics during matrix manipulations.
* **Maximum Pooling (MaxPooling):** Reducing spatial dimensionality while retaining critical high-intensity features.
* **Activation Layer:** Introducing non-linearity to allow the model to learn complex dust-distribution patterns.

---

## 📈 Step-by-Step Execution Workflow
[Create Dataset: 500 Photos] ──► [Data Augmentation] ──► [Import Core Libraries]
│
▼
[Deployment / Predictions] ◄── [Model Evaluation] ◄── [Train Sequential Model (Adam)]

* **Step 1:** Assemble and structure the 500-photo image directory across seasonal folders.
* **Step 2:** Import foundational data handling and plotting packages (`Numpy`, `OS`, `Matplotlib`, `Pandas`).
* **Step 3:** Initialize the `Keras` environment for deep learning configurations.
* **Step 4:** Compile the **Sequential Model** layers and bind the **Adam Optimizer** for efficient error/loss computations.
* **Step 5:** Train the network over a fixed number of training loops (Epochs) while monitoring loss convergence.
* **Step 6:** Evaluate unseen data metrics to confirm true system precision.
* **Step 7:** Deploy the final model to handle real-time image scans and trigger hardware/sprinkler mechanisms.

---

## ⚡ Setup & Local Installation
```bash
# Clone the repository
git clone [https://github.com/somu-som/POLLUTION-MEASUREMENT.git](https://github.com/somu-som/POLLUTION-MEASUREMENT.git)

# Navigate into the project directory
cd POLLUTION-MEASUREMENT

# Install the required dependencies
pip install numpy pandas matplotlib tensorflow keras
***

### Why this structure works better:
1. **Removes Typos:** Cleans up phrasing like "Mesaurement", "pollute leaf", and spacing errors found in the old version.
2. **Adds a Visual Flowchart:** The small ASCII chart under the execution workflow explains your 7 steps in a single glance.
3. **Presents Data Cleanly:** Putting your 150/50/300 seasonal photos into a clean Markdown table looks highly professional to anyone visiting your GitHub.
