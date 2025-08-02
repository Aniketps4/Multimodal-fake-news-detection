📰 Multimodal Fake News Detection using Precomputed Embeddings
This project builds a binary fake news classifier using multimodal features — both visual (images) and textual (titles) — extracted using pretrained models. The notebook is designed for efficient processing and training within the Kaggle ecosystem or similar GPU-enabled environments.

📁 Project Structure
Input Data

Image embeddings: .npy files in nested folders (image_embeddings_merged-*)

Title embeddings: .npy files (title_embeddings-*)

Ground truth labels: multimodal_train.tsv

Output

Combined final_data.parquet for training

Model training logs and performance metrics

Confusion matrix and ROC curve

📦 Dependencies
Ensure the following Python packages are installed:

bash
Copy
Edit
pip install numpy pandas torch scikit-learn matplotlib seaborn tqdm psutil
🚀 Key Components
1. System Status Utility
Displays current CPU usage and GPU memory.

Useful for monitoring resource usage during training.

2. Data Verification
Checks existence and file counts of .npy embeddings for both image and text modalities.

3. Data Preparation
Merges embeddings and labels using id keys.

Filters for valid records where both modalities and labels are available.

Saves the resulting dataset to final_data.parquet.

🧠 Model Training (Not Shown in Initial Cells)
This part likely:

Loads the merged dataset.

Builds a neural architecture combining image and text embeddings.

Trains and evaluates the model using metrics such as:

Accuracy

F1-score

ROC-AUC

Confusion matrix

📊 Example Outputs
Final dataset stats:

✅ Image embeddings found: N

✅ Text embeddings found: M

✅ Matched entries: X

Class distribution of labels:

bash
Copy
Edit
0 (Fake): ###
1 (Real): ###
📝 Notes
Designed for use with pre-extracted .npy embeddings from large-scale datasets.

Ideal for use in Kaggle Notebooks, Colab, or local Jupyter environments with GPU support.

📂 To Run This Notebook
Upload or mount the embedding folders and multimodal_train.tsv.

Adjust INPUT_PATH to point to the correct dataset location.

Run all cells in sequence.
