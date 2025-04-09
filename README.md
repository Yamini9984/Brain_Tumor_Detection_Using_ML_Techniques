# 🧠 MRI Brain Tumor Dataset Setup Instructions

## ✅ Dataset Download

This project uses the [MRI Brain Tumor Dataset](https://www.kaggle.com/datasets/josshhh/mri-scans-brain-tumor-image-dataset) from Kaggle.

### 📦 Steps to Download Using Kaggle CLI:

1. Go to [Kaggle > My Account](https://www.kaggle.com/account) and click **Create API Token**.
2. This will download a file named `kaggle.json`.
3. Upload it into your environment (e.g., Google Colab or Jupyter).

### 🧾 Code to Run

```python
!pip install -q kaggle

from google.colab import files
files.upload()  # Upload kaggle.json here

!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json

!kaggle datasets download -d josshhh/mri-scans-brain-tumor-image-dataset -p ./ --unzi
