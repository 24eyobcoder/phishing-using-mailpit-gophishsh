# phishing-using-mailpit-gophishsh

# 🎯 Phishing Simulation Lab with Gophish and Mailpit

This project demonstrates how to simulate a phishing attack in a safe lab environment using [Gophish](https://getgophish.com/) and [Mailpit](https://github.com/axllent/mailpit).

---

## 🛠 Tools Used
- Gophish (for sending and tracking phishing emails)
- Mailpit (as a fake SMTP/email server)
- HTML (email templates)
- Linux terminal (Bash)

---

## 📦 Installation & Configuration

### 1. Install Mailpit

```bash
sudo bash < <(curl -sL https://raw.githubusercontent.com/axllent/mailpit/develop/install.sh)
mailpit

Mailpit will start:

SMTP: localhost:1025

Web: http://localhost:8025

Download & run Gophish:

bash
Copy
Edit
wget https://github.com/gophish/gophish/releases/download/v0.12.1/gophish-v0.12.1-linux-64bit.zip
unzip gophish-*.zip
cd gophish
nano config.json   # Set "listen_url": "0.0.0.0:8080"
./gophish

Access:

Admin UI: https://localhost:3333

Campaign tracker: http://localhost:8080

3. Configure Gophish
Sending Profile: SMTP Server: localhost, Port: 1025

Email Template: Include {{.URL}} and {{.Tracker}}

Landing Page: A basic fake login page (or redirect)

Users & Groups: Target your own local test inbox

Campaign: Launch and track from the dashboard

