# Follow Proper Instructions to Run this Scraper Easily:

## YouTube Channel Data Scraper

This Python script extracts data from a YouTube channel, including:
- Channel name
- Subscriber count
- Join date (from the 'About' tab)

It uses **Selenium WebDriver** to automate browser interaction and **WebDriverManager** to handle the ChromeDriver installation.

## Prerequisites

- Python 3.6 or newer
- Google Chrome (latest version) installed on your system
## Installation

### 1. Clone or download the repository:
If you don't have the script locally, you can clone or download the repository.

```bash
git clone https://github.com/techykaif/youtube_scraper
```

### 2. Install Python dependencies:
You can install the necessary Python libraries using **pip**:

```bash
pip install -r requirements.txt
```

## Usage

### Running the Script:
1. Open a terminal or command prompt.
2. Navigate to the folder where the script is saved.
3. Run the script:

```bash
python youtube.py
```
### Script Input:
- You will be prompted to **enter the URL of the YouTube channel**.
- The script will then fetch the channel's name, subscriber count, and join date from the 'About' tab.

### Example Input:

```text
Enter the YouTube channel URL: https://www.youtube.com/@channelname
```

### Script Output:
The script will save the data into a JSON file named after the channel's name. Example:

```json
{
  "Channel Name": "Name of the Channel",
  "Subscribers": "Number of Subscribers",
  "Joined Date": "Nov 12, 2015"
}
```

The file will be saved in the current directory.

## Running in Headless Mode
The script runs Chrome in **headless mode** by default. This means the browser window won't open during execution, making it ideal for running on servers or automated systems.

If you prefer to see the browser window, you can modify the script to disable headless mode by commenting out the following line in the `setup_driver()` function:

```python
chrome_options.add_argument("--headless")  # Run in headless mode for performance
```

### Platform-Specific Requirements

- **Linux (Ubuntu/Debian)**: If running on Linux, you might need to install additional libraries to support headless Chrome. Run the following command:

```bash
sudo apt-get install libnss3 libx11-xcb1 libatk-bridge2.0-0
```

- **macOS and Windows**: Make sure you have **Google Chrome** installed.

## Troubleshooting
**Error: ChromeDriver not found**
   - Ensure you have Google Chrome installed on your system.
   - The **WebDriverManager** will automatically handle the ChromeDriver download, but you can manually download it from [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/) if needed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

#### Mohd Kaif Ansari

### Key Sections in the README:

- **Prerequisites**: Lists the required Python version and necessary software.
- **Installation**: Explains how to install the dependencies and run the script.
- **Usage**: Provides instructions for running the script and describes what it does.
- **Running in Headless Mode**: Informs the user that the script runs in headless mode by default, with an option to disable it.
- **Platform-Specific Requirements**: Explains any additional steps needed based on the platform.
- **Troubleshooting**: Provides solutions for common issues users might encounter.

This should guide users through setting up and running your YouTube Channel Data Scraper script. Let me know if you need to make any additional adjustments!
