# Web-Security-Audit
This project provides a comprehensive suite of tools designed to audit the security of web applications. It consists of two main Python scripts: one for analyzing web security headers and another for performing in-depth security scans on a target domain.
Table of Contents
Features
Prerequisites
Required Tools
Python Packages
Operating System
Installation
Usage
Security Header Analyzer (security_header.py)
Web Audit Tool (web-audit.py)
Contributing
License
Features
1. Security Header Analyzer (security_header.py)
This script analyzes the HTTP security headers of a given website and grades it based on the presence and configuration of the following headers:

Strict-Transport-Security: Enforces secure (HTTPS) connections.
Content-Security-Policy: Mitigates the risk of XSS and other code injection attacks.
X-Content-Type-Options: Prevents MIME type sniffing.
X-Frame-Options: Protects against clickjacking.
X-XSS-Protection: Adds an extra layer of protection against XSS attacks.
Referrer-Policy: Controls how much referrer information is included with requests.
Permissions-Policy: Manages permissions for browser features.
2. Web Audit Tool (web-audit.py)
This script performs a series of security tests on a target domain using various security tools. It helps identify vulnerabilities and provides suggestions for remediation.

Vulnerability Classification: Issues are classified as critical, high, medium, low, or informational.
Interactive Scanning: Allows skipping tests or quitting the scan interactively.
Multiple Security Scanners: Utilizes tools like nmap, SSLyze, wafw00f, and more for comprehensive security checks.
Prerequisites
Required Tools
The web-audit.py script relies on several third-party security tools. Ensure these are installed and accessible in your system's PATH:

Nmap: Network exploration tool and security/port scanner.
SSLyze: Fast and comprehensive SSL/TLS configuration analyzer.
wafw00f: Web application firewall detection tool.
Uniscan: A vulnerability scanner and directory checker.
theHarvester: Email, subdomain, and name search tool.
DNSRecon: DNS reconnaissance tool.
dirb: Web content scanner and directory brute-forcing tool.
XSser: Cross-site scripting (XSS) vulnerability scanner.
You can install these tools on Ubuntu-based systems using:

sudo apt-get install nmap sslyze wafw00f uniscan theharvester dnsrecon dirb xsser
Python Packages
This project requires the following Python packages:

aiohttp: Asynchronous HTTP client/server framework.
termcolor: Utility for printing colored text to the terminal.
You can install the necessary Python packages using pip:

pip install -r requirements.txt
If a requirements.txt file is not available, you can install the packages individually:

pip install aiohttp termcolor
Operating System
This project is best suited for Unix-like operating systems, particularly:

Ubuntu 20.04+: Recommended for its ease of installation of required tools and packages.
Kali Linux: Ideal for penetration testing and security auditing, as it comes pre-installed with many required tools.
While the scripts may work on other operating systems, they are developed and tested primarily on Ubuntu and Kali Linux.

Installation
Clone the repository:

git clone https://github.com/srinivasan2003/Web-Security-Audit.git
cd Web-Security-Audit
Install the necessary dependencies:

sudo apt-get update
sudo apt-get install nmap sslyze wafw00f uniscan theharvester dnsrecon dirb xsser
pip install -r requirements.txt
Ensure that the required tools are in your system's PATH.

Usage
Security Header Analyzer (security_header.py)
This script analyzes the security headers of a single URL or multiple URLs listed in a file.

Analyze a Single URL
python3 security_header.py https://example.com
Analyze Multiple URLs from a File
python3 security_header.py --file urls.txt
The results will be saved to an output file and displayed in the terminal.

Web Audit Tool (web-audit.py)
This script performs a comprehensive security audit of a web domain using a variety of security scanners.

Basic Usage
python3 web-audit.py example.com
Skip Specific Tests
python3 web-audit.py example.com --skip dmitry --skip theHarvester
Disable Spinner/Loader
python3 web-audit.py example.com --nospinner
The tool will display a summary of findings along with recommendations for remediation.

Contributing
Contributions are welcome! If you have suggestions for new features or improvements, feel free to submit a pull request or open an issue.

License
This project is licensed under the MIT License. See the LICENSE file for more details.
About
No description, website, or topics provided.
Resources
 Readme
License
 MIT license
 Activity
Stars
 0 stars
Watchers
 1 watching
Forks
 1 fork
Report repository
Releases
No releases published
Packages
No packages published
Languages
Python
100.0%
Footer
© 2
