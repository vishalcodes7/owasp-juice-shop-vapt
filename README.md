# OWASP Juice Shop – Web Application VAPT

A practical Web Application Vulnerability Assessment and Penetration Testing (VAPT) project conducted on the intentionally vulnerable OWASP Juice Shop application in a controlled local lab environment.

## Project Overview

This project demonstrates practical web application security testing techniques, vulnerability identification, evidence collection, risk assessment, and remediation recommendations.

The assessment focuses on selected vulnerability categories from the OWASP Top 10:2021.

## Objectives

- Identify common web application security weaknesses.
- Perform controlled vulnerability testing.
- Analyze HTTP requests and responses.
- Validate security findings with practical evidence.
- Assess potential risks and recommend remediation.
- Document the assessment professionally.

## Tools and Technologies

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| OWASP Juice Shop | Intentionally vulnerable test application |
| Burp Suite | Intercepting and analyzing HTTP traffic |
| Nmap | Network and port scanning |
| cURL | HTTP request testing |
| Docker | Running the test application |
| Oracle VirtualBox | Virtual lab environment |

## Vulnerabilities and Observations

The following findings were documented during the assessment:

| No. | Finding | Preliminary Severity |
|---|---|---|
| 1 | SQL Injection | High |
| 2 | Cross-Site Scripting (XSS) | Medium |
| 3 | Broken Access Control | High |
| 4 | Public FTP Directory Listing | Medium |
| 5 | Sensitive Information Disclosure | Medium |
| 6 | Malware-Related Shortcut Exposure | Low |
| 7 | Public API Specification Exposure | Informational |

Severity ratings are preliminary and based on observations in the local lab. They are not formal CVSS scores.

## Testing Scope

**Target:** OWASP Juice Shop  
**Environment:** Local testing lab  
**Application URL:** `http://127.0.0.1:3000`

Testing included:
- Reconnaissance and port scanning.
- SQL Injection testing.
- Cross-Site Scripting testing.
- Broken access control testing.
- HTTP security header and CORS observations.
- Public directory and file exposure checks.
- API documentation and authentication checks.

## Key Observations

- SQL Injection testing demonstrated unauthorized administrator account access in the lab.
- XSS testing triggered a JavaScript alert in the browser.
- A basket API request exposed another user's basket data.
- A publicly accessible directory exposed file and folder listings.
- A document labelled confidential was accessible through the public directory.
- A malware-related shortcut reference was accessible; the executable was not downloaded or executed.
- The tested protected API endpoint rejected missing and invalid credentials with HTTP 401 Unauthorized.

## Remediation Recommendations

- Use parameterized SQL queries and prepared statements.
- Apply context-aware output encoding to prevent XSS.
- Enforce server-side authorization and resource ownership checks.
- Disable public directory listing.
- Remove confidential files from public directories.
- Restrict access to backup and quarantine directories.
- Review API documentation exposure and enforce API authentication.

## Project Limitations

- Testing was conducted only against a locally hosted OWASP Juice Shop instance.
- Only selected OWASP Top 10:2021 categories were assessed.
- This project does not claim complete OWASP Top 10 coverage.
- No production systems or real user accounts were tested.
- No malware was downloaded or executed.
- Public API documentation exposure was treated as informational; no API authentication bypass was confirmed.

## Project Documentation

The detailed VAPT report, supporting screenshots, and testing evidence will be organized in this repository.

## Disclaimer

This project was conducted for educational and cybersecurity skill-development purposes using an intentionally vulnerable application in a controlled local environment. Do not perform security testing on systems without explicit authorization.

## Author

**Vishal Bhambhana**  
BCA Student | Aspiring Cybersecurity Professional

