# Reconnaissance and Fingerprinting

Passive and active reconnaissance against hackthissite.org, a legal cybersecurity training platform. Demonstrates the information gathering phase of an ethical penetration test.

## Skills Demonstrated
OSINT and Google dorking, domain intelligence gathering, internet wide asset discovery, network scanning and service enumeration, web technology fingerprinting.

## Tools
Kali Linux, Nmap 7.99, Whois, Shodan, Wappalyzer

## Target
hackthissite.org, authorized for ethical hacking and security testing. No exploitation performed.

---
## Process

## Google Dorks

![Google dork filetype:pdf results](Project_Figures/google_dork_pdf.png)

![Google dork inurl:admin results](Project_Figures/google_dork_admin.png)

Indexed PDFs and articles publicly accessible on mirror.hackthissite.org.

---

## WHOIS Lookup

![WHOIS output](Project_Figures/whois.png)

Registrar: Porkbun LLC, Created: 2003-08-10, Expires: 2026-08-10, Nameservers: buddyns.com

---

## Shodan Search

![Shodan results](Project_Figures/shodan.png)

7 results, Top ports: 443 and 6697, Location: Dunkerque France, TLSv1.2, SSL: HARICA DV TLS RSA

---

## Nmap Port Scan

![Nmap -sS scan](Project_Figures/nmap_ss.png)

Port 22 closed, Port 80 open (http), Port 443 open (https), IP: 137.74.187.102

---

## Service Detection

![Nmap -sV scan](Project_Figures/nmap_sv.png)

Port 80 and 443 running HAProxy 1.3.1 to 1.9.0, Device identified as load balancer

---

## Wappalyzer Fingerprinting

![Wappalyzer output](Project_Figures/wappalyzer.png)

Cloudflare (CDN/Security), jQuery (JavaScript Library)

---

## Summary

| Technique | Tool | Finding |
|---|---|---|
| Google Dorks | Google | Indexed PDFs and OSINT articles publicly accessible |
| WHOIS | whois | Registrar: Porkbun LLC, Created: 2003-08-10 |
| Shodan | Shodan | 7 results, ports 443 and 6697, TLSv1.2 |
| Port Scan | Nmap sS | Port 22 closed, ports 80 and 443 open |
| Service Detection | Nmap sV | HAProxy 1.3.1 to 1.9.0, load balancer |
| Web Fingerprint | Wappalyzer | Cloudflare, jQuery |

## Full Report
See Project1_Recon_Fingerprinting.docx for the complete write up with screenshots and references.

## Ethics
All activity was performed against a platform explicitly authorized for security testing. No scanning or access attempts were made against any system outside this scope.

## References
Lyon, G. (n.d.). Nmap: The network mapper. https://nmap.org
Shodan. (n.d.). Shodan search engine. https://www.shodan.io
Wappalyzer. (n.d.). Wappalyzer: Technology profiler. https://www.wappalyzer.com
Wilhelm, T., & Engebretson, P. (2026). The basics of hacking and penetration testing (3rd ed.). Syngress.
