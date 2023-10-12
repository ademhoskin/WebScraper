import requests
from bs4 import BeautifulSoup
import time


# Define the URL of the website
url = "https://www.lcps.org/bwhs"

# Send an HTTP GET request to the website and retrieve the content
response = requests.get(url)

# Check if the request was successful
if response.status_code == 200:
    # Parse the HTML content using BeautifulSoup
    time.sleep(3)
    soup = BeautifulSoup(response.text, 'html.parser')

    # Find the div element with the specific class
    div_element = soup.find('div', class_='gb-footer one')

    # Extract all the content within the div
    if div_element:
        div_content = div_element.get_text()
        print("Entire content of the div with class 'gb-footer-one':", div_content)
    else:
        print("Div element with class 'gb-footer-one' not found on the webpage.")
else:
    print("Failed to retrieve the webpage.")

# Note: Make sure to adjust the class name ('gb-footer-one') and the HTML structure to match the target website.
