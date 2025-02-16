
# 🔍 Whois Command Cheat Sheet

Whois is a query and response protocol used to retrieve information about domain names, IP addresses, and their ownership.

---

## 📘 Basic Commands

| Command | Description | Example |
|---------|-------------|---------|
| `whois example.com` | Retrieves WHOIS information for a domain, including registrar, status, and expiration date. | `whois google.com` |
| `whois 8.8.8.8` | Looks up WHOIS information for an IP address, showing ownership and geolocation details. | `whois 192.168.1.1` |
| `whois -h whois.verisign-grs.com example.com` | Queries a specific WHOIS server, useful for more accurate results for certain TLDs. | `whois -h whois.verisign-grs.com microsoft.com` |

---

## 🌐 Domain Specific Queries

| Command | Description | Example |
|---------|-------------|---------|
| `whois example.com \| grep 'Name Server'` | Extracts nameservers associated with the domain. | `whois yahoo.com \| grep 'Name Server'` |
| `whois example.com \| grep 'Registrar'` | Displays the domain registrar's name. | `whois amazon.com \| grep 'Registrar'` |
| `whois example.com \| grep -i 'Creation Date\|Expiration Date'` | Shows domain creation and expiration dates. | `whois netflix.com \| grep -i 'Creation Date\|Expiration Date'` |

---

## 🛠 Advanced Usage

| Command | Description | Example |
|---------|-------------|---------|
| `whois -r example.com` | Displays raw WHOIS data without any formatting. | `whois -r github.com` |
| `whois -R example.com` | Disables redirection to the authoritative WHOIS server. | `whois -R facebook.com` |
| `for domain in $(cat domains.txt); do whois $domain; done` | Checks WHOIS information for multiple domains listed in a text file. | `for domain in $(cat domains.txt); do whois $domain; done` |

---

## 🔗 Useful WHOIS Servers

| WHOIS Server | Description | Example Usage |
|--------------|-------------|---------------|
| `whois.verisign-grs.com` | For `.com` and `.net` domains. | `whois -h whois.verisign-grs.com example.com` |
| `whois.arin.net` | For IP addresses in North America. | `whois -h whois.arin.net 8.8.8.8` |
| `whois.ripe.net` | For IP addresses in Europe. | `whois -h whois.ripe.net 192.0.2.1` |
| `whois.apnic.net` | For IP addresses in the Asia-Pacific region. | `whois -h whois.apnic.net 203.0.113.1` |

---

## ⚙️ Install Whois

| OS | Command |
|----|---------|
| **Debian/Ubuntu** | `sudo apt update && sudo apt install whois` |
| **CentOS/RHEL** | `sudo yum install whois` |
| **macOS (Homebrew)** | `brew install whois` |

---

## 📜 Notes

- WHOIS data may vary by registrar and region.
- Some registrars limit the number of WHOIS queries.
- Use appropriate WHOIS servers for accurate results.

---
