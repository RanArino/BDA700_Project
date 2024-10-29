# Brain Tumor Image Analysis Project

This project, conducted at Seneca Polytechnic, focuses on the segmentation of brain tumors in multimodal MRI scans using the BraTS 2020 dataset. The goal is to accurately segment three tumor sub-regions: GD-enhancing tumor (ET), peritumoral edema (ED), and necrotic and non-enhancing tumor core (NCR/NET). By developing an automated segmentation method using deep learning techniques, we aim to assist medical professionals in more efficiently and accurately analyzing brain tumor MRI scans for improved diagnosis, treatment planning, and monitoring.


## Setting Up Virtual Environment

On Mac/Linux:
```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

On Windows:
```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

## Kaggle API Setup

To download the dataset, you need to authenticate with your Kaggle API.

1. Follow the instrunctions (https://www.kaggle.com/docs/api#getting-started-installation-&-authentication)
2. Create a `.kaggle` directory in your home directory and add the `kaggle.json` file to it. For example:
    - /Users/<your-username>/.kaggle (Mac/Linux)
    - C:\Users\<your-username>\.kaggle (Windows)
3. Add `kaggle.json` which you downloaded in step 1 to the `.kaggle` directory.

