# ML.Data

![Project Banner](https://socialify.git.ci/fepaziani/ML.Data/image?custom_description=This+project+trains+a+custom+NER+model+using+spaCy+in+Portuguese+to+extract+specific+entities+%28REF1+and+REF2%29+from+structured+text+data.+&description=1&language=1&name=1&owner=1&pattern=Solid&stargazers=1&theme=Dark)


## 📌 Overview

ML.Data is a machine learning project that extracts relevant data from invoices. One specific column in an Excel file contains a mix of useful and irrelevant data. Since the relevant data appears in various formats, a custom ML model was trained to identify and extract only the desired information from each cell.

## 🚀 Features

- Trains a Named Entity Recognition (NER) model using **spaCy**.
- Extracts specific entities (REF1 and REF2) from structured text data.
- Handles diverse data formats within a single column of an Excel file.
- Supports **Portuguese language processing**.

## 🛠 Tech Stack

- **Machine Learning**: Python, spaCy
- **Data Handling**: Pandas, OpenPyXL
- **Model Training**: Custom NER with supervised learning
- **File Formats**: Excel (XLSX, CSV)

## 📂 Project Structure

```
ML.Data-main/
│-- code/                 # Source code
│-- README.md             # Project documentation
│-- .gitignore            # Git ignore file
|-- requirements.txt      # Required Modules to Run the Program
```

## 🚀 Getting Started

### 1️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 2️⃣ Train the Model

```bash
python train_model.py
```

### 3️⃣ Extract Data

```bash
python extract_data.py input.xlsx
```

## 📌 Example

### 📝 Input (Dirty Cell)

```
2003           1    Payment referring to electricity bill for Subsede MONTE         0027           301049                            470.13                  470.13                          CARMELO - OUT/2022
```

### ✅ Output (Cleaned Version)

```
Payment referring to electricity bill for Subsede MONTE CARMELO - OUT/2022
```

This extraction occurs by determining which characters are useful and filtering out the rest. The training data defines the positions of relevant information, as shown below:

```python
TRAIN_DATA = [("2003           1    Payment referring to electricity bill for Subsede MONTE         0027           301049                            470.13                  470.13                          CARMELO - OUT/2022", {
    'entities': [(20, 82, 'REF1'), (196, 214, 'REF2')]
})]
```

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

## 📜 License

This project is licensed under the MIT License.

## 📊 Project Stats

![GitHub Repo stars](https://img.shields.io/github/stars/fepaziani/ML.Data?style=social)
![GitHub forks](https://img.shields.io/github/forks/fepaziani/ML.Data?style=social)
![GitHub issues](https://img.shields.io/github/issues/fepaziani/ML.Data)
![GitHub last commit](https://img.shields.io/github/last-commit/fepaziani/ML.Data)

---

*Developed by fepaziani*
