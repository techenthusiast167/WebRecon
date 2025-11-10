# WebRecon
WebRecon is an advanced Open Source Intelligence (OSINT) web reconnaissance tool designed for cybersecurity professionals, penetration testers, and security researchers. It automates the process of gathering intelligence from target websites through comprehensive crawling, data extraction, and analysis.


**Advanced OSINT Web Reconnaissance Tool**

![WebRecon Pro Banner](https://img.shields.io/badge/WebRecon-Pro-brightgreen)
![Python](https://img.shields.io/badge/Python-3.6%2B-blue)
![OSINT](https://img.shields.io/badge/OSINT-Tool-orange)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Reconnaissance-red)

## Table of Contents

- Overview
- Key Features
- Importance in Cybersecurity & OSINT
- Installation
- Usage
- Advanced Usage Examples
- Output & Reports
- Use Cases
- Legal & Ethical Considerations
- Contributing
- Disclaimer


## Key Features

### Core Capabilities

- **Advanced Web Crawling** - Configurable depth and page limits
- **Email Harvesting** - Intelligent email extraction with false positive filtering
- **Social Media Discovery** - Automated profile detection across platforms
- **Technology Stack Detection** - Comprehensive technology fingerprinting
- **DNS Intelligence** - DNS record enumeration and analysis
- **WHOIS Lookup** - Domain registration information gathering
- **Historical Analysis** - Wayback Machine integration

### Data Extraction

- **Cloud Storage Discovery** - AWS S3, Azure Blob, GCP Storage detection
- **File Enumeration** - PDF, documents, configuration files, and more
- **Marketing Tags** - Google Analytics, Facebook Pixel, Hotjar detection
- **IP Address Discovery** - Public IP extraction from content
- **HTML Comments** - Hidden comment analysis
- **JavaScript Analysis** - JS source mapping and analysis

### Advanced Features

- **Proxy Support** - HTTP/SOCKS proxy integration
- **Automated Browser Integration** - BuiltWith, Wayback Machine auto-launch
- **PDF Search Automation** - Google Dork integration for document discovery
- **JSON Reporting** - Comprehensive structured output
- **Custom Configuration** - Flexible scanning parameters

## Importance in Cybersecurity & OSINT

### Cybersecurity Applications

- **Attack Surface Mapping** - Identify all exposed assets and endpoints
- **Vulnerability Assessment** - Discover sensitive files and information leaks
- **Threat Intelligence** - Gather intelligence on target infrastructure
- **Penetration Testing** - Pre-engagement reconnaissance and intelligence gathering
- **Incident Response** - Investigate compromised assets and exposed data

### OSINT Intelligence Value

- **Digital Footprint Analysis** - Map organizational online presence
- **Brand Protection** - Monitor unauthorized use of company assets
- **Competitive Intelligence** - Analyze competitor technology stacks
- **Due Diligence** - Investigate business partners and acquisitions
- **Security Research** - Academic and professional security analysis

## Installation

### Prerequisites

- Python 3.6 or higher
- pip (Python package manager)

### Quick Manual installation

**Visit the link below to get the script, then use nano to install it**

**https://gist.github.com/techenthusiast167/d675163c3c941bb6184ca36f20b511bf**

**Step-by-Step**:

- Click on the link below to access the script
- Copy the script content
- Use nano to create and install the tool


# Manual Dependency Installation

    pip install requests beautifulsoup4 colorama tldextract python-whois dnspython lxml

# Basic Usage

    python3 webrecon.py https://example.com

# Advanced Options

### Custom crawl limits

    python3 webrecon.py https://example.com --max-pages 50 --max-depth 3

# With proxy and custom output

    python3 webrecon.py https://example.com --proxy socks5://127.0.0.1:9050 --output results.json

# Minimal reconnaissance (crawling only)

    python3 webrecon.py https://example.com --no-dns --no-whois --no-wayback --no-builtwith


# Command Line Arguments

### Argument	Description	Default

  url	Target URL for reconnaissance	Required
--max-pages	Maximum pages to crawl	100

--max-depth	Maximum crawl depth	2

--output	Custom output file path	Auto-generated

--proxy	HTTP/SOCKS proxy URL	None

--no-dns	Disable DNS reconnaissance	Enabled

--no-whois	Disable WHOIS lookup	Enabled

--no-wayback	Disable Wayback Machine	Enabled

--no-builtwith	Disable BuiltWith analysis	Enabled


# Advanced Usage Examples

Corporate Security Assessment


# Comprehensive corporate reconnaissance

    python3 webrecon.py https://target-company.com --max-pages 200 --max-depth 3


# Penetration Testing Engagement


### Stealth reconnaissance with Tor

    python3 webrecon.py https://target.com --proxy socks5://127.0.0.1:9050 --max-pages 50

# Competitive Intelligence


### Technology stack analysis only

    python3 webrecon.py https://competitor.com --no-dns --no-whois --output tech_report.json

# Academic Research

### Large-scale data collection

    python3 webrecon.py https://research-target.edu --max-pages 500 --max-depth 4

# Output & Reports

### JSON Report Structure


{
  "crawled_links": ["url1", "url2", ...],
  "emails": ["email1@domain.com", "email2@domain.com", ...],
  "social_media": {
    "facebook": ["profile_urls"],
    "twitter": ["profile_urls"],
    ...
  },
  "technologies": {
    "detected": ["WordPress", "jQuery", "Cloudflare", ...]
  },
  "dns_info": {
    "a_records": ["IPs"],
    "mx_records": ["mail_servers"],
    ...
  },
  "whois_info": {
    "registrar": "Registrar Name",
    "creation_date": "2020-01-01",
    ...
  }
}


# Report Location

- **Default: webrecon_output/webrecon_domain_timestamp.json**

- **Custom: User-specified path with --output flag**

# Use Cases

## Enterprise Security

- **Attack Surface Management** - Continuous monitoring of digital assets

- **Third-Party Risk Assessment** - Vendor security evaluation

- **M&A Due Diligence** - Pre-acquisition security assessment


# Government & Law Enforcement

- **Cyber Crime Investigation** - Digital evidence gathering

- **Threat Actor Profiling** - Adversary infrastructure mapping

- **National Security** - Critical infrastructure protection



# Legal & Ethical Considerations


### Permitted Usage

- Security research on systems you own

- Authorized penetration testing

- Academic research with proper consent

- Corporate security assessments on owned assets

- Bug bounty programs with explicit permission


# Prohibited Usage

- Unauthorized scanning of systems

- Privacy violation or harassment

- Commercial exploitation without permission

- Any illegal activities

- Network disruption or denial of service


# Compliance Notes

- Always obtain proper authorization before scanning

- Respect robots.txt and terms of service

- Follow responsible disclosure practices

- Comply with local laws and regulations


# Contributing

Contributions from the security community!


# How to Contribute

- Fork the repository

- Create a feature branch (git checkout -b feature/AmazingFeature)

- Commit your changes (git commit -m 'Add some AmazingFeature')

- Push to the branch (git push origin feature/AmazingFeature)

- Open a Pull Request





# Disclaimer


**WebRecon is designed for legitimate security research and authorized testing only**

- The author is not responsible for misuse of this tool

- Users must ensure they have proper authorization before scanning

- This tool should only be used in accordance with applicable laws

- Educational purposes only - use at your own risk






**Made with ❤️ for the security community**

**Remember**: With great power comes great responsibility. Always use this tool ethically.


