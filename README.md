# 🌐 Data Collection Techniques using Python

A practical Python project demonstrating **data collection and web scraping techniques** using popular Python libraries such as **Requests** and **BeautifulSoup**.

This repository is designed for beginners and Data Science learners who want to understand how data can be collected from web pages and prepared for further analysis.

---

## 🚀 About the Project

Data collection is one of the most important steps in a Data Science workflow.

Before analyzing or visualizing data, we first need to obtain useful and structured data. Python provides powerful libraries that make it possible to collect information from websites and work with HTML documents.

This project demonstrates:

* 🌐 Sending HTTP requests
* 📄 Retrieving web page content
* 🥣 Parsing HTML using BeautifulSoup
* 🔍 Extracting information from HTML elements
* 📊 Storing collected data
* 🐼 Preparing data for analysis

The repository provides hands-on Jupyter Notebook examples using **Requests** and **BeautifulSoup**.

---

## 📚 Topics Covered

| # | Topic                           | File                  |
| - | ------------------------------- | --------------------- |
| 1 | HTTP Requests                   | `Requests.ipynb`      |
| 2 | Web Scraping with BeautifulSoup | `Beautifilsoup.ipynb` |
| 3 | HTML Data                       | `htmls/`              |
| 4 | Collected Dataset               | `data.csv`            |

---

## 🗂️ Repository Structure

```text
Data-Collection-Technique-using-Python/
│
├── htmls/
│   └── HTML files / web content
│
├── Beautifilsoup.ipynb
├── Requests.ipynb
├── data.csv
│
└── README.md
```

---

## 🛠️ Technologies Used

* 🐍 **Python**
* 🌐 **Requests**
* 🥣 **BeautifulSoup**
* 📓 **Jupyter Notebook**
* 📄 **HTML**
* 📊 **CSV**

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/sarhan-003/Data-Collection-Technique-using-Python.git
```

### 2. Navigate to the Project

```bash
cd Data-Collection-Technique-using-Python
```

### 3. Install Required Libraries

```bash
pip install requests beautifulsoup4 pandas jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

Open the notebooks and execute the cells step by step.

---

# 🌐 1. HTTP Requests

The **Requests** library allows Python programs to communicate with web servers and retrieve web resources.

A basic request can be made using:

```python
import requests

url = "https://example.com"

response = requests.get(url)

print(response.status_code)
print(response.text)
```

### Important Concepts

The Requests notebook introduces concepts such as:

* Sending GET requests
* HTTP response status codes
* Accessing response content
* Working with URLs
* Retrieving HTML pages

---

# 🥣 2. BeautifulSoup

**BeautifulSoup** is used to parse HTML and extract useful information from web pages.

Example:

```python
import requests
from bs4 import BeautifulSoup

url = "https://example.com"

response = requests.get(url)

soup = BeautifulSoup(response.text, "html.parser")

print(soup.title.text)
```

---

## 🔍 Extracting HTML Elements

BeautifulSoup can be used to locate specific HTML elements.

```python
for heading in soup.find_all("h1"):
    print(heading.text)
```

You can also extract links:

```python
for link in soup.find_all("a"):
    print(link.get("href"))
```

---

# 📊 3. Collecting Data

After extracting information from a web page, the collected data can be stored in Python structures such as lists and dictionaries.

Example:

```python
data = []

for item in soup.find_all("h2"):
    data.append({
        "title": item.text.strip()
    })

print(data)
```

The collected information can then be converted into a Pandas DataFrame.

```python
import pandas as pd

df = pd.DataFrame(data)

print(df.head())
```

---

# 💾 4. Saving Data to CSV

Collected data can be saved for future analysis.

```python
df.to_csv("data.csv", index=False)
```

The repository also contains a `data.csv` dataset for working with collected data.

---

# 🔄 Data Collection Workflow

The overall workflow demonstrated by this project can be summarized as:

```text
       Website
          │
          ▼
   Send HTTP Request
          │
          ▼
   Receive HTML Page
          │
          ▼
    Parse HTML
   using BeautifulSoup
          │
          ▼
  Extract Required Data
          │
          ▼
    Store the Data
          │
          ▼
       CSV File
          │
          ▼
   Data Analysis
```

---

## 🧠 What You Will Learn

After completing this project, you will understand:

* How websites communicate using HTTP
* How to send requests using Python
* How to retrieve HTML content
* How to parse HTML documents
* How to find HTML elements
* How to extract text and links
* How to collect structured information
* How to store collected data in CSV format
* How collected data can be prepared for Data Analysis

---

## 🎯 Learning Path

For beginners, follow the project in this order:

```text
Python Basics
     ↓
HTTP & Web Requests
     ↓
Requests Library
     ↓
HTML Structure
     ↓
BeautifulSoup
     ↓
HTML Element Extraction
     ↓
Data Collection
     ↓
CSV Storage
     ↓
Data Analysis
```

---

## 🔐 Responsible Web Scraping

When collecting data from websites, always use responsible practices.

### Recommended practices

* Respect the website's `robots.txt` and terms of service.
* Avoid sending excessive requests.
* Add appropriate delays when necessary.
* Collect only publicly available information.
* Do not bypass authentication or access controls.
* Respect copyright and privacy requirements.
* Use APIs when an official API is available.

---

## 🔮 Future Improvements

This project can be expanded with:

* [ ] Advanced BeautifulSoup selectors
* [ ] CSS selectors
* [ ] Web scraping multiple pages
* [ ] Pagination handling
* [ ] Request headers
* [ ] Error handling
* [ ] Request timeouts
* [ ] Scraping structured tables
* [ ] JSON data collection
* [ ] API-based data collection
* [ ] Selenium automation
* [ ] Scrapy framework
* [ ] Automated data pipelines
* [ ] Real-world web scraping projects

---

## 🤝 Contributing

Contributions are welcome!

### 1. Fork the repository

### 2. Clone your fork

```bash
git clone https://github.com/YOUR-USERNAME/Data-Collection-Technique-using-Python.git
```

### 3. Create a new branch

```bash
git checkout -b feature/new-technique
```

### 4. Make your changes

### 5. Commit your changes

```bash
git add .
git commit -m "Add new data collection technique"
```

### 6. Push your branch

```bash
git push origin feature/new-technique
```

### 7. Create a Pull Request

---

## ⭐ Support

If this project helped you learn **Python Data Collection and Web Scraping**, consider giving the repository a ⭐ on GitHub.

---

## 👨‍💻 Author

### Sarhan Bakarman

GitHub: **[@sarhan-003](https://github.com/sarhan-003)**

---

## 🔗 Repository

**Data Collection Technique using Python**

https://github.com/sarhan-003/Data-Collection-Technique-using-Python

---

## 📜 License

This project is created for **educational and learning purposes**.

---

### 🌐 Collect Data → Clean Data → Analyze Data → Build Insights 🚀
