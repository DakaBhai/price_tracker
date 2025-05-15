# Boat Airdopes 100 Price Tracker

This Python script monitors the real-time price of the Boat Airdopes 100 on Amazon.in and automatically saves the price and date to a `price_tracker.csv` file daily.

## How it Works

The script does the following:

1.  **Scrapes Amazon:** Uses the `requests` library to fetch the product page and `BeautifulSoup` to parse the HTML content.
2.  **Extracts Information:** Identifies and extracts the product title and current price.
3.  **Saves to CSV:** Writes the title, price, and current date into the `price_tracker.csv` file. If the file doesn't exist, it creates it with a header row. Subsequent runs append the new data to the file.
4.  **Continuous Monitoring :** The script is set up to run indefinitely, checking the price every 86400 seconds (daily).

## Setup

1.  **Clone the Repository:**
    ```bash
    git clone <repository_url>
    cd <repository_name>
    ```

2.  **Install Dependencies:**
    Make sure you have the necessary libraries installed. You can install them using pip:
    ```bash
    pip install beautifulsoup4 requests pandas
    ```

## Running the Script

To start the price tracker, simply run the Python script:

```bash
python price_tracker.py
