# Web Scraper and Crawler (Python)

A lightweight Python web scraper and crawler that extracts and logs information from webpages.  
The scraper maintains visited links, follows new ones, and saves extracted content into text files for later analysis.  

---

## Features
- **Crawling**: Starts from a seed list of URLs (`links.txt`) and explores linked pages.  
- **Duplicate Prevention**: Tracks visited pages (`visited.txt`) to avoid redundant scraping.  
- **Content Extraction**: Extracts raw text from HTML and saves it into `extracted.txt`.  
- **Logging**: Records progress, successes, and errors into `output.log`.  
- **Configurable**: Input URLs can be customized through `links.txt`.  

---

## Requirements
- Python 3.8+  
- Install dependencies:  
  ```bash
  pip install requests beautifulsoup4
---
## Usage

### Clone the repository
```bash
git clone https://github.com/yourusername/webscraper.git
cd webscraper
```
### Add seed links to links.txt (one URL per line)

### Run the scraper

python scraper.py

### Check the output

- extracted.txt → cleaned text extracted from pages
- visited.txt → list of visited links
- output.log → crawl log

---
## Example Output

The scraper extracts contact information (emails, phone numbers, and addresses) and outputs them in structured `(URL, TYPE, VALUE)` tuples.

Sample run on a local test page (`test.html`):

(file:///test.html, EMAIL, test@example.com)
(file:///test.html, PHONE, 410-555-1234)
(file:///test.html, ADDRESS, Baltimore, MD 21218)

This demonstrates the program’s ability to recognize and categorize different types of information consistently across pages.


---
## Contributions

This project was developed independently.

My work included:
- Implementing the core crawling logic (scraper.py).
- Designing link tracking (visited.txt) to prevent duplicates.
- Building logging and output features for extracted content.
- Debugging edge cases (broken links, timeouts).

--- 

### Future Improvements

- Add command-line arguments for flexible input/output paths
- Support multi-threaded crawling for faster performance
- Export results to CSV or JSON for data analysis pipelines





