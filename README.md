# Assignment 1 - Transliteration Accuracy Testing

This project automates the testing of the Chat Sinhala transliteration function available at [https://www.pixelssuite.com/chat-translator](https://www.pixelssuite.com/chat-translator) using Playwright.

---

## Prerequisites

- Python 3.11 or 3.12
- Google Chrome (recommended) or Chromium (installed via Playwright)

---

## Installation

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd test_automation
```

### 2. Install dependencies

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

## Project Structure

```
test_automation/
├── test_automation.py          # Main Playwright test script
├── Assignment 1 - Test cases.xlsx  # Test cases with inputs and expected outputs
└── README.md                   # Project documentation
```

---

## Running the Tests

From inside the `test_automation` folder, run the following command:

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

### Command Arguments

| Argument | Description | Default |
|---|---|---|
| `--excel` | Path to the Excel test cases file | `Assignment 1 - Test cases.xlsx` |
| `--url` | URL of the application to test | `https://www.pixelssuite.com/chat-translator` |
| `--wait-ms` | Time to wait (ms) for output after each input | `5000` |
| `--type-delay-ms` | Delay (ms) between each keystroke | `80` |
| `--slow-mo-ms` | Slow motion delay (ms) for browser actions | `200` |
| `--save-every` | Save Excel file after every N test cases | `1` |
| `--keep-open` | Keep browser open after tests complete | `false` |
| `--headless` | Run browser in headless mode (no UI) | `false` |

---

## Checking Results

After running the script, open `Assignment 1 - Test cases.xlsx` and check the **Actual output** and **Status** columns which are automatically filled in by the script.

- **PASS** — Actual output matches the expected output
- **FAIL** — Actual output does not match the expected output
