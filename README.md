# Price Tracker

## Overview
This project is a Python-based web scraper built in a Jupyter Notebook to track the daily price of Boat Airdopes 141 earbuds on Amazon India. The script fetches the product title and price from the Amazon product page, stores the data in a CSV file (`price_tracker.csv`), and updates it daily. The project uses BeautifulSoup for web scraping and runs continuously with a 24-hour interval between checks.

## Features
- Scrapes the product title and price from the specified Amazon URL.
- Saves data (title, price, and date) to `price_tracker.csv`.
- Automatically updates the CSV file every 24 hours.
- Displays the scraped data using pandas for quick verification.

## Prerequisites
To run this project, you need the following installed:
- Python 3.6 or higher
- Jupyter Notebook
- Python libraries:
  - `requests`
  - `beautifulsoup4`
  - `pandas`
  - `csv` (built-in)
  - `datetime` (built-in)
  - `time` (built-in)

## Installation
1. **Clone the repository**:
   ```
   git clone https://github.com/your-username/price_tracker.git
   cd price_tracker
   ```

2. **Set up a virtual environment** (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required libraries**:
   ```
   pip install requests beautifulsoup4 pandas
   ```

4. **Launch Jupyter Notebook**:
   ```
   jupyter notebook
   ```
   Open `price_tracker.ipynb` in the Jupyter interface.

## Usage
1. Open `price_tracker.ipynb` in Jupyter Notebook.
2. Run all cells to execute the script.
   - The script will:
     - Scrape the price and title from the Amazon page.
     - Save the data to `price_tracker.csv`.
     - Run continuously, updating the CSV file every 24 hours.
3. To stop the script, interrupt the kernel (Ctrl+C or the stop button in Jupyter).
4. Check the `price_tracker.csv` file for the recorded data.

## File Structure
- `price_tracker.ipynb`: The main Jupyter Notebook containing the Python script for web scraping and price tracking.
- `price_tracker.csv`: The output CSV file where the scraped data (title, price, date) is stored.

## Notes
- **Amazon URL**: The script is hardcoded to track the Boat Airdopes 141 earbuds at `https://www.amazon.in/Boat-Airdopes-141-Latency-Bluetooth/dp/B0DGTTP1K4?th=1`. To track a different product, update the `URL` variable in the script.
- **Headers**: The script uses a User-Agent to mimic a browser. If Amazon blocks the requests, you may need to update the `headers` dictionary with a different User-Agent.
- **CSV Path**: The script assumes `price_tracker.csv` is in the same directory as the notebook. If running on a different machine, update the file path in the script (e.g., replace `C:\Users\pande\price_tracker.csv` with the correct path).
- **Error Handling**: The script lacks robust error handling (e.g., for network issues or changes in Amazon's page structure). Consider adding try-except blocks for production use.
- **Scheduling**: The script uses `time.sleep(86400)` for daily updates. For more precise scheduling, consider using a library like `schedule` or a cron job.

## Contributing
Feel free to fork this repository, make improvements, and submit pull requests. Suggestions for enhancing error handling, adding visualizations, or supporting multiple products are welcome!

## License
This project is licensed under the [MIT License](LICENSE).

## Disclaimer
Web scraping may violate Amazon's Terms of Service. Use this script responsibly and at your own risk. Ensure compliance with applicable laws and regulations.
