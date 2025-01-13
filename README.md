# Automated-Threat-intelligence-tracker

## Overview
The Automated Threat Intelligence Tracker is a Python-based project designed to collect, process, and analyze cybersecurity threat data. This tool automates the fetching of threat intelligence from APIs, processes raw data into actionable insights, and generates detailed Excel reports. It is an essential asset for security teams aiming to stay updated on the latest cyber threats and vulnerabilities.

---

## Features
1. **Fetch Threat Data**:
   - Integrates with APIs such as VirusTotal, AlienVault OTX, and Shodan to retrieve threat intelligence.
2. **Process Raw Data**:
   - Cleans and structures raw threat data.
   - Extracts indicators of compromise (IOCs) like IPs, domains, and file hashes.
3. **Risk Scoring**:
   - Assigns severity levels (Low, Medium, High) based on custom risk calculations.
4. **Generate Excel Reports**:
   - Creates user-friendly reports with summaries, visualizations, and conditional formatting.
5. **Automation**:
   - Automates the pipeline with scheduling capabilities for periodic updates.
6. **Optional Alerts**:
   - Integrates with Slack or email to notify about high-risk threats.

---

## Project Structure
```
threat-intelligence-tracker/
│
├── fetch_threat_data.py    # Handles API calls and data extraction
├── process_data.py         # Processes and scores the threat data
├── generate_report.py      # Generates Excel reports with visualizations
├── scheduler.py            # Automates periodic script execution
├── config.py               # Stores API keys and configuration
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## Setup

### 1. Prerequisites
- Python 3.8 or higher.
- API access for:
  - VirusTotal: [Register here](https://www.virustotal.com/)
  - AlienVault OTX: [Register here](https://otx.alienvault.com/)
  - Shodan: [Register here](https://www.shodan.io/)
- Optional: Slack API for alerts.

### 2. Installation
Clone the repository and install dependencies:
```bash
git clone https://github.com/your-repo/threat-intelligence-tracker.git
cd threat-intelligence-tracker
pip install -r requirements.txt
```

### 3. Configure API Keys
Create a `config.py` file in the project directory and add your API keys:
```python
# config.py

API_KEYS = {
    "virustotal": "your_virustotal_api_key",
    "alienvault": "your_alienvault_api_key",
    "shodan": "your_shodan_api_key"
}

SLACK_TOKEN = "your_slack_token"  # Optional for alerts
```

---

## Usage

### 1. Fetch Threat Data
Run the script to retrieve threat intelligence from APIs:
```bash
python fetch_threat_data.py
```

### 2. Process Data
Clean and process the raw data:
```bash
python process_data.py
```

### 3. Generate Excel Report
Generate a detailed Excel report with insights:
```bash
python generate_report.py
```

### 4. Automate the Workflow
Schedule periodic updates using the scheduler script:
```bash
python scheduler.py
```

---

## Example Output
- **Excel Report**:
  - Summarized threat data.
  - Conditional formatting for risk levels.
  - Graphs to visualize trends.

---

## Dependencies
Add these to `requirements.txt`:
```
pandas
requests
openpyxl
schedule
```
Install dependencies with:
```bash
pip install -r requirements.txt
```

---

## Future Enhancements
1. **Dashboard**:
   - Add a web-based UI using Flask/Django for real-time monitoring.
2. **Machine Learning**:
   - Implement predictive analytics for emerging threats.
3. **Integration with SIEM**:
   - Send processed data to Splunk or ELK for advanced correlation.
4. **Additional APIs**:
   - Incorporate more threat intelligence sources.

---

## License
This project is licensed under the Apache 2.0 License. See `LICENSE` for details.

---

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for improvements or bug fixes.

---
