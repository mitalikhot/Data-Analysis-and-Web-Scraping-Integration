# Data Analysis and Web Scraping Integration 🕷️📊

> **Problem:** What patterns emerge from popular quotes on the web — which authors dominate, what themes recur, and how do quote characteristics vary across the dataset?

This project automates data collection from [quotes.toscrape.com](http://quotes.toscrape.com/) using Python web scraping, then applies Exploratory Data Analysis to surface trends and patterns from the extracted data — covering 100 quotes across 50 unique authors.

---

## 🧠 Key Findings

* 🏆 **Albert Einstein dominates** with 10 quotes — nearly double the next most-quoted author (J.K. Rowling, 9 quotes), making him the single most represented voice in the dataset
* ❤️ **"Love" is the #1 tag** (14 occurrences), followed closely by "inspirational" and "life" (13 each) — revealing a strong bias toward emotionally resonant, motivational content
* 📏 **Quote lengths are heavily right-skewed** (skewness: 4.97), meaning the vast majority of quotes are short and punchy (avg. 122 characters), with a few outliers stretching beyond 1,000 characters
* 📚 **"Books" and "reading" rank in the top 10 tags**, reflecting the literary nature of the source platform and its audience
* 🌐 **50 unique authors** are represented across just 100 quotes, indicating high diversity — no single author monopolises the dataset beyond Einstein

---

## 🛠️ Tech Stack

| Layer | Tools |
| --- | --- |
| Web Scraping | Python, BeautifulSoup, Requests |
| Data Processing | Pandas, NumPy |
| Statistical Analysis | Skewness, Kurtosis, Central Tendency |
| Visualization | Matplotlib, Seaborn |
| Environment | Google Colab |

---

## 🚀 Project Workflow

### Phase 1 — Web Scraping

* Sent HTTP requests to [quotes.toscrape.com](http://quotes.toscrape.com/) using the **Requests** library
* Parsed HTML DOM with **BeautifulSoup** to extract three fields per quote: `Quote`, `Author`, and `Tags`
* Handled multi-page pagination to collect a complete dataset of **100 quotes**
* Exported raw scraped data to `quotes.csv` for reproducibility

### Phase 2 — Data Cleaning & Preprocessing

* Removed null and malformed entries
* Parsed comma-separated `Tags` strings into individual tag tokens for frequency analysis
* Computed derived features, including `quote_length` (character count), for distribution analysis

### Phase 3 — Exploratory Data Analysis

* Computed **skewness (4.97)** confirming a strong right-skewed distribution in quote lengths — most quotes are brief, with rare long-form outliers
* Ranked authors and tags by frequency to identify the most represented voices and themes
* Generated a **word cloud** from the quote text to visualise the most prominent vocabulary

---

## 📊 Visualizations

### Distribution of Quote Lengths

![Quote Length Distribution](https://raw.githubusercontent.com/mitalikhot/Data-Analysis-and-Web-Scraping-Integration/main/Charts/Distribution%20of%20quotes%20lengths.png)

> Quote lengths are right-skewed (skewness: 4.97) — most quotes are under 150 characters, with a long tail of verbose outliers.

### Top 10 Most Common Tags

![Top Tags](https://raw.githubusercontent.com/mitalikhot/Data-Analysis-and-Web-Scraping-Integration/main/Charts/Top%20most%20common%20tags.png)

> "Love", "inspirational", and "life" are the dominant themes — the dataset skews heavily toward motivational and emotional content.

### Top 10 Most Quoted Authors

![Top Authors](https://raw.githubusercontent.com/mitalikhot/Data-Analysis-and-Web-Scraping-Integration/main/Charts/Top%20most%20quoted%20authors.png)

> Albert Einstein leads with 10 quotes. The top 7 authors account for a disproportionate share of the dataset.

### Word Cloud — Most Frequent Words

![Word Cloud](https://raw.githubusercontent.com/mitalikhot/Data-Analysis-and-Web-Scraping-Integration/main/Charts/Word%20cloud.png)

> "Love", "life", "will", "one", and "make" dominate the vocabulary — reinforcing the motivational tone of the corpus.

---

## 📁 Repository Structure

```
├── Web_Scraping_with_EDA.ipynb    # Full notebook: scraping + cleaning + EDA
├── quotes.csv                     # Scraped dataset (100 quotes, 3 fields)
├── Charts/
│   ├── Distribution of quotes lengths.png
│   ├── Top most common tags.png
│   ├── Top most quoted authors.png
│   └── Word cloud.png
└── README.md
```

---

## ✅ Skills Demonstrated

`Python` · `BeautifulSoup` · `Requests` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Web Scraping` · `HTML Parsing` · `EDA` · `Statistical Analysis` · `Data Cleaning` · `Google Colab`

---

## ▶️ How to Run

1. **Clone the repo**
   ```bash
   git clone https://github.com/mitalikhot/Data-Analysis-and-Web-Scraping-Integration.git
   ```
2. Open `Web_Scraping_with_EDA.ipynb` in Google Colab or Jupyter
3. Run all cells to re-scrape and re-analyse — or skip straight to EDA using the pre-scraped `quotes.csv`

---

**Author:** Mitali Khot · [GitHub](https://github.com/mitalikhot) · [Project Repository](https://github.com/mitalikhot/Data-Analysis-and-Web-Scraping-Integration)

> ⭐ If you found this project useful, consider starring the repo!
