<div align="center">

# 🤖 AI Lead Generator

### Automated Lead Generation Tool Using AI / Data Scraping / Data Processing

![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](httpshttps://img.shields.io/badge/Pandas-Data--Processing-150458?style=for-the-badge&logo=pandas)
![Requests](https://img.shields.io/badge/Requests-HTTP-007ACC?style=for-the-badge&logo=python&logoColor=white)
![CSV](https://img.shields.io/badge/CSV-Export-lightgrey?style=for-the-badge)

**A Python-based automation tool that generates potential leads by scraping, filtering, and processing public data — producing structured CSV lists of contacts for outreach or business development.**

[📖 Documentation](#features) | [🐛 Report Bug](https://github.com/TanayV24/Ai-Lead-Generator/issues) | [💡 Request Feature](https://github.com/TanayV24/Ai-Lead-Generator/issues)

</div>

---

## ✨ Features

### 🧑‍💼 **Lead Generation Features**
- 🌐 **Web Scraping / Data Collection** – Fetch data from public sources or directories  
- 🧹 **Data Cleaning & Filtering** – Remove duplicates, invalid entries, missing values  
- 🧪 **Data Processing & Enrichment** – Normalize data fields, format phone/email, add metadata  
- 📄 **CSV / Excel Export** – Output clean lead lists for outreach or CRM import  
- 🔍 **Search & Filter Options** – Filter leads by location, industry, tags, status  
- 🔄 **Batch Processing** – Handle large data sets efficiently  

### 🔧 **Technical Features**
- 🐍 **Python 3.8+** – Core programming language  
- 🛠 **Requests / BeautifulSoup (or Scrapy)** – For web scraping  
- 🐼 **Pandas** – Data manipulation & cleaning  
- 📂 **Modular Scripts** – Separation of scraping, cleaning, exporting logic  
- 🧪 **Reusable Pipeline** – Easy to adapt for any data source or format  

---

## 🛠 Tech Stack

<table>
<tr>
<td width="50%" valign="top">

### Core Libraries
- **Python 3.8+**  
- **Requests / BeautifulSoup (or Scrapy)** – HTTP & scraping  
- **Pandas** – Data analysis & processing  
- **CSV / Excel** – Output formatting  

</td>
<td width="50%" valign="top">

### Utilities
- **Logging** – Track scraping status, errors  
- **Config Files** – For source URLs, filters, export settings  
- **Modular Architecture** – Scraper, processor, exporter modules  

</td>
</tr>
</table>

---

## 📋 Prerequisites

| Tool | Version | Link |
|------|---------|------|
| 🐍 Python | 3.8+ | https://python.org |
| 📦 pip | Latest | Comes with Python |
| 💻 Git | Latest | https://git-scm.com |

Install dependencies:

```

pip install -r requirements.txt

```

Check version:

```

python --version

````

---

## ⚙️ Installation & Setup

### 🚀 Quick Start

```bash
git clone https://github.com/TanayV24/Ai-Lead-Generator.git
cd Ai-Lead-Generator
python run.py
````

> The lead generation pipeline will start scraping, processing, and export leads into an output file (e.g. `leads.csv`).

---

## 🎮 How to Use

1. Open the project directory
2. Configure `config.json` (or equivalent) with target URLs, filters, and output settings
3. Run:

   ```bash
   python run.py
   ```
4. Once done, check output directory — download your leads (CSV / Excel)
5. Optionally: Load leads into CRM, outreach tools, or analysis pipelines

---

## 📁 Detailed Project Structure

```
Ai-Lead-Generator/
│
├── run.py                      # Entry point — orchestrates scraping → processing → export
├── scraper/                    
│   ├── base_scraper.py         # Core scraper class (fetch HTML, request handling)
│   ├── target_site_scraper.py  # Scraper logic for specific website/domain
│   └── utils.py                # Helper functions (HTML parsing, URL cleaning, delays)
│
├── processor/                 
│   ├── cleaner.py              # Data cleaning & sanitization
│   ├── filterer.py             # Filtering logic (remove duplicates, invalid entries)
│   └── enricher.py             # Data enrichment (formatting, metadata additions)
│
├── exporter/                   
│   ├── csv_exporter.py         # Exports data to CSV format
│   ├── excel_exporter.py       # (Optional) Exports to Excel (.xlsx)
│   └── utils.py                # Shared exporter utilities (date, naming, IO)
│
├── config/                     
│   └── config.json             # Config file: list of target URLs, filters, export settings
│
├── logs/                       
│   └── scraper.log             # Scraping logs, errors, status for debugging  
│
├── output/                     # Output folder  
│   └── leads.csv               # Final leads data output  
│
├── requirements.txt            # Python dependencies  
└── README.md                   # Project documentation
```

---

## 🐛 Troubleshooting

<details>
<summary>No data scraped / empty output</summary>

* Check if target URLs in `config.json` are correct
* Ensure site structure hasn’t changed (inspect HTML selectors)
* Add delay or headers to avoid bot-blocking

</details>

<details>
<summary>Encoding / Unicode errors in exported file</summary>

Ensure CSV is saved with UTF-8 encoding:

```python
df.to_csv('leads.csv', encoding='utf-8', index=False)
```

</details>

<details>
<summary>Duplicates in output list</summary>

Run `python run.py --clean` or use filter step to remove duplicates

</details>
