# Towhid-Projects
Networking Automation Projects

Here’s a professional GitHub project description / README-style post you can use for your repository:

# 🚀 Meraki Event Log Automation using Python & Meraki Dashboard API

## 📌 Overview

This project automates the collection of event logs from the Cisco Meraki Dashboard using Python and the Meraki Dashboard API.

The script retrieves daily network event logs, processes the data, converts timestamps to IST, and stores the results in structured CSV reports automatically.

The automation is designed to run daily using Windows Task Scheduler without manual intervention.

---

# ⚙️ Features

✅ Automated Meraki event log retrieval
✅ Fetches previous 24-hour logs automatically
✅ Handles API pagination (1000+ events)
✅ Converts UTC timestamps → IST
✅ Extracts detailed `eventData` information
✅ Creates structured CSV reports
✅ Prevents file overwrite using date-based filenames
✅ Automatically creates monthly log folders
✅ Supports Task Scheduler automation

---

# 🛠️ Technologies Used

* Python
* Cisco Meraki Dashboard API
* CSV & JSON Processing
* Windows Task Scheduler

---

# 📂 Project Structure

```text id="nqjw0u"
C:\MerakiLogs\
    └── 2026-05\
            ├── meraki_logs_2026-05-01.csv
            ├── meraki_logs_2026-05-02.csv
            ├── meraki_logs_2026-05-03.csv
```

---

# 📊 CSV Output Fields

The generated CSV reports contain:

* Time (IST)
* Event Type
* Description
* Client Name
* Client MAC
* Device Name
* Category
* Severity
* Event Data

---

# 🔑 Prerequisites

Before running the script:

1. Install Python 3.x
2. Install Meraki SDK

```bash id="8pc1n4"
pip install meraki
```

3. Enable API access in Meraki Dashboard
4. Generate a Meraki API Key
5. Obtain Network ID

---

# ▶️ Running the Script

```bash id="l6lqk8"
python meraki_daily.py
```

---

# ⏰ Task Scheduler Setup

Recommended Schedule:

* Daily
* 12:05 AM

Task Scheduler Configuration:

* Program/script → python.exe
* Add arguments → meraki_daily.py
* Start in → Script folder path

---

# 🧠 Challenges Solved

* Meraki API pagination handling
* Historical event retrieval
* CSV overwrite prevention
* Timezone conversion
* Automated daily reporting

---

# 🚀 Future Improvements

* Microsoft Teams integration
* Email reporting
* SIEM integration
* Real-time webhook alerts
* Dashboard visualization

---

# 📌 Learning Outcomes

This project helped strengthen knowledge in:

* API automation
* Network monitoring
* Python scripting
* Event log analysis
* Task scheduling
* Scalable automation workflows

---

# 🔥 Use Case

This solution is useful for:

* IT Administrators
* Network Engineers
* SOC Teams
* NOC Monitoring
* Event Auditing & Troubleshooting

---

# 📜 License

This project is for educational and automation purposes.
