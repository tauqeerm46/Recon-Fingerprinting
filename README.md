# Web Application Penetration Testing

Hands-on penetration testing against DVWA (Damn Vulnerable Web Application), a deliberately vulnerable environment designed for security training. Identifies and exploits common vulnerabilities from the OWASP Top 10.

## Skills Demonstrated
SQL injection exploitation, cross site scripting detection, insecure file upload testing, CSRF vulnerability identification, HTTP request manipulation, and vulnerability assessment documentation.

## Tools
Kali Linux, DVWA, Burp Suite Community Edition, Firefox, Apache2, MariaDB, PHP

## Target
DVWA deployed locally on Kali Linux. Security level set to Low. No external systems accessed.

---

## Environment Setup

![DVWA security set to Low](dvwa_security.png)

![Burp Suite Intercept on](burp_intercept.png)

---

## SQL Injection

![Burp Suite intercepted request](sqli_burp.png)

![SQL injection results](sqli_results.png)

Payload `1' OR '1'='1` bypassed authentication and dumped all database records.

---

## Cross Site Scripting (XSS)

![XSS alert popup](xss_alert.png)

Payload `<script>alert('XSS')</script>` executed in browser confirming reflected XSS.

---

## File Upload

![Shell upload success](fileupload_success.png)

PHP web shell (`shell.php`) uploaded with no file type validation in place.

---

## CSRF

![CSRF password change form](csrf_form.png)

Password change form confirmed to have no CSRF token.

---

## Findings

| Vulnerability | Severity | Status | Remediation |
|---|---|---|---|
| SQL Injection | Critical | Exploited | Use prepared statements |
| XSS Reflected | High | Exploited | Sanitize and encode user input |
| File Upload | Critical | Exploited | Validate file type and content |
| CSRF | Medium | Identified | Implement CSRF tokens |

## Ethics
All testing performed against a locally deployed deliberately vulnerable application. No external systems targeted.

## References
DVWA Project. (n.d.). Damn Vulnerable Web Application (DVWA). https://dvwa.co.uk  
OWASP Foundation. (2025). OWASP Top 10:2025. https://owasp.org/Top10/  
Stuttard, D., & Pinto, M. (2011). The web application hacker's handbook. John Wiley & Sons.  
Weidman, G. (2014). Penetration testing: a hands-on introduction to hacking. No Starch Press.
