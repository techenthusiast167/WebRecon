# WebRecon Pro 

**Advanced OSINT Web Reconnaissance Tool with Relationship Graph Visualization**

![WebRecon Pro](https://img.shields.io/badge/WebRecon-Pro-brightgreen)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![OSINT](https://img.shields.io/badge/OSINT-Advanced-red)
![Graph](https://img.shields.io/badge/Relationship-Graphs-purple)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Reconnaissance-orange)

## Overview

**WebRecon Pro** is an advanced Open Source Intelligence (OSINT) web reconnaissance tool designed for cybersecurity professionals, penetration testers, and security researchers. This major update introduces comprehensive relationship graph visualization, tabular reporting, enhanced image downloading, and sophisticated data correlation capabilities.

Unlike traditional reconnaissance tools, WebRecon Pro focuses on understanding the **relationships between discovered entities** - emails, social media profiles, technologies, domains, and people - creating an interactive visual map of organizational digital footprints.


## WebRecon Features 



- **Relationship Graph Visualization**: Interactive network graphs showing connections between entities
  
- **Comprehensive Tabular Reporting**: Structured data tables with source tracking

- **Enhanced Image Intelligence**: Smart image downloading with metadata extraction

- **Data Correlation Engine**: Intelligent relationship discovery between findings
  
- **Multi-format Export**: JSON, HTML, CSV, and interactive visualizations


### Enhanced Capabilities

- **Advanced False Positive Filtering**: Improved email and image pattern detection
  
- **Source Tracking**: Every finding traced back to its source URL

- **Interactive HTML Reports**: Browser-based exploration of findings

- **Network Analysis Metrics**: Centrality, clustering, and relationship strength calculations
  
- **Professional Output**: Enterprise-ready reports and visualizations
  

# Key Features

### Intelligent Web Crawling

- Configurable depth and breadth crawling (1-5 levels)

- Robots.txt and sitemap.xml parsing
  
- JavaScript source extraction
  
- Login page detection
  
- Cloud storage discovery (AWS S3, Azure, GCP)


### Advanced Email Harvesting

- Intelligent pattern matching with false positive filtering
 
- Domain-based email grouping
  
- Source URL tracking for each email
  
- Image filename exclusion
 
- Corporate vs personal email classification
  

### Social Media Intelligence

- Platform-specific pattern matching (LinkedIn, Twitter, Facebook, etc.)
  
- Username extraction and correlation
  
- Profile validation to avoid share buttons and widgets
  
- Organizational vs personal profile detection

### Image Intelligence Suite

- **Smart Image Downloading**: Filters placeholders and icons
  
- **Metadata Extraction**: EXIF data, dimensions, file types
  
- **Thumbnail Generation**: Automatic resizing for analysis

- **HTML Gallery Creation**: Visual browsing of collected images

- **Size Filtering**: Configurable minimum/maximum file sizes

### Technology Stack Detection

- 50+ technology patterns (CMS, frameworks, servers, analytics)
  
- Header and content-based detection
  
- Marketing tag identification (GA, GTM, Facebook Pixel)
  
- CDN and hosting provider detection

### DNS & Network Intelligence

- Comprehensive DNS record enumeration (A, MX, TXT, NS, CNAME)
  
- Domain IP resolution and reverse DNS lookup
  
- Subdomain discovery from crawled content
  
- Automated DNSDumpster browser integration

### Document & File Discovery

- File type detection (PDF, DOC, XLS, PPT, CSV, etc.)
  
- Configuration file discovery (.config, .conf, .ini)
  
- Log file identification (.log)
  
- Database file detection (.sql)

### Relationship Graph System

- **Interactive Network Visualization**: Drag, zoom, explore relationships
  
- **Entity Categorization**: Automatic classification of nodes
 
- **Intelligent Relationship Discovery**: Same-domain emails, shared usernames, etc
  
- **Network Metrics**: Centrality, density, clustering coefficients

- **Export Formats**: HTML interactive, JSON data, analysis reports

### Comprehensive Reporting

- **Tabular Data Presentation**: Organized category-based tables
  
- **Source Tracking**: Every finding linked to its discovery URL

- **Multi-format Export**: JSON, HTML, CSV, Text

- **Executive Summaries**: High-level overviews with statistics

- **Detailed Findings**: Complete data with context and sources



# Relationship Graph Visualization 

### Graph Features

- **Interactive HTML Graphs**: Drag nodes, zoom, hover for details

- **Entity Categories**: Color-coded nodes (emails, domains, social, tech, etc.)
  
- **Intelligent Layout**: Force-directed graph algorithms
  
- **Relationship Types**: Different line styles for different connections

- **Network Analysis**: Metrics and insights about the discovered network

### Node Categories & Colors

- 🔵 **Domains**: Target and related domains
  
- 🔴 **Emails**: Discovered email addresses
  
- 🟢 **Social Media**: Profiles and accounts

- 🟡 **IP Addresses**: Network infrastructure

- 🟣 **People/Organizations**: WHOIS and contact information

- 🟠 **Documents/Files**: Discovered files
  
- 🔶 **Technologies**: Detected tech stack

- ⚫ **URLs**: Web pages and endpoints

### Relationship Types

- **Solid Blue Lines**: Direct domain relationships
  
- **Red Lines**: Same email domain connections

- **Purple Lines**: Same username across platforms

- **Dashed Gray Lines**: Found-on-page relationships

- **Green Dashed Lines**: Technology usage relationships

### Graph Output Files

```
webrecon_output/graphs/
├── relationship_graph_domain_timestamp.html  # Interactive graph
├── graph_data_domain_timestamp.json          # Raw graph data
└── graph_analysis_report.txt                 # Network metrics
```

# Output Structure

### Default Output Directory

```
webrecon_output/
├── comprehensive_report_TIMESTAMP.json       # Complete JSON data
├── comprehensive_report_TIMESTAMP.html       # Interactive HTML report
├── comprehensive_report_TIMESTAMP.txt        # Text summary
├── images_DOMAIN_TIMESTAMP/                  # Downloaded images
│   ├── raw/                                  # Original images
│   ├── thumbnails/                           # Resized thumbnails
│   ├── extracted/                            # Metadata and extracted data
│   ├── gallery.html                          # Image gallery
│   ├── metadata.json                         # Image metadata
│   └── images_summary.csv                    # CSV summary
├── graphs/                                   # Relationship graphs
│   ├── relationship_graph_DOMAIN_TIMESTAMP.html
│   ├── graph_data_DOMAIN_TIMESTAMP.json
│   └── graph_analysis_report.txt
└── webrecon_DOMAIN_TIMESTAMP.json            # Legacy JSON format
```

# Installation

### Prerequisites

- Python 3.8 or higher
  
- pip package manager
  
- 500MB+ free disk space (for images and graphs)

### Quick Installation

**Direct Download using Wget**

    wget -O WebRecon.py https://gist.githubusercontent.com/techenthusiast167/47c8f8c94a520c8d96a1495b7c9a1fcb/raw/42e8dacea162de67c8377682aea3907349aa6c9d/WebRecon.py

# Make Executable (Optional)

    chmod +x WebRecon.py

# Verify Installation

    python3 WebRecon.py --help


# Install Dependencies

    pip install requests beautifulsoup4 colorama tabulate tldextract dnspython python-whois pillow networkx pyvis lxml html5lib pysocks urllib3

**Note**: For the most stable installation, it is highly recommended to use a **Python virtual environment**. This prevents conflicts with your system's global Python packages.
    

# Verification

### Test installation

    python3 WebRecon.py --help

    

### Expected output should show v6.0 features including:

**--no-graphs              Disable relationship graph generation**
**--table-only             Display only tabular output**
**--detailed-tables        Show detailed tables for all categories**


# Usage Examples

### Basic Usage

### Comprehensive reconnaissance with all features

    python3 WebRecon.py https://example.com


### With custom output directory

    python3 WebRecon.py https://example.com --output ./my_report.json

### Limited crawling

    python3 WebRecon.py https://example.com --max-pages 50 --max-depth 2


# Advanced Reconnaissance

### Enterprise reconnaissance with full graph visualization
 
    python3 WebRecon.py https://target-company.com --max-pages 200 --max-depth 3

### Stealth reconnaissance through Tor

    python3 WebRecon.py https://target.com --proxy socks5://127.0.0.1:9050

### Technology-focused reconnaissance

    python3 WebRecon.py https://tech-company.com --no-images --no-dnsdumpster


# Feature Control

### Disable specific modules

    python3 WebRecon.py https://example.com \

  --no-images \          # Disable image downloading
  --no-graphs \          # Disable relationship graphs
  --no-dns \            # Disable DNS reconnaissance
  --no-whois \          # Disable WHOIS lookup
  --no-wayback \        # Disable Wayback Machine
  --no-builtwith \      # Disable BuiltWith analysis
  --no-dnsdumpster      # Disable DNSDumpster

### Table-only output mode

    python3 WebRecon.py https://example.com --table-only

### Detailed tabular output

    python3 WebRecon.py https://example.com --detailed-tables


# Output Customization

### Custom proxy configuration

    python3 WebRecon.py https://example.com --proxy http://proxy:8080

### Specific crawl limits

    python3 WebRecon.py https://large-site.com --max-pages 500 --max-depth 4

### Save to specific location

    python3 WebRecon.py https://example.com --output /path/to/report.json


# Command Line Arguments

### Basic Arguments

| Argument | Description | Default |
|----------|-------------|---------|
| `url` | Target URL for reconnaissance | **Required** |
| `--max-pages` | Maximum pages to crawl | 100 |
| `--max-depth` | Maximum crawl depth | 2 |
| `--output` | Custom output file path | Auto-generated |
| `--proxy` | HTTP/SOCKS proxy URL | None |

### Feature Control Arguments

| Argument | Description | Default |
|----------|-------------|---------|
| `--no-dns` | Disable DNS reconnaissance | Enabled |
| `--no-whois` | Disable WHOIS lookup | Enabled |
| `--no-wayback` | Disable Wayback Machine | Enabled |
| `--no-builtwith` | Disable BuiltWith analysis | Enabled |
| `--no-dnsdumpster` | Disable DNSDumpster domain IP analysis | Enabled |
| `--no-images` | Disable image downloading | Enabled |
| `--no-graphs` | Disable relationship graph generation | Enabled |

### Output Control Arguments 

| Argument | Description | Default |
|----------|-------------|---------|
| `--table-only` | Display only tabular output (no JSON) | Disabled |
| `--detailed-tables` | Show detailed tables for all categories | Disabled |

# Using the Relationship Graphs

### Accessing Graph Output

After running WebRecon Pro, open the generated HTML graph file:

### On Linux/Mac

    xdg-open webrecon_output/graphs/relationship_graph_example_20240101_120000.html

### Or simply navigate to the file in your file browser and open it


### Graph Navigation

1. **Zoom**: Mouse wheel or touchpad pinch
  
2.  **Pan**: Click and drag background
   
3. **Node Interaction**:
   - **Hover**: See detailed information
   - **Click**: Highlight connections
   - **Drag**: Reposition nodes
     
4. **Controls** (top-right panel):
   - **Fit View**: Auto-arrange graph
   - **Toggle Physics**: Enable/disable node movement
   - **Spring Length**: Adjust connection tension

### Graph Legend (Draggable)

- Located top-left, can be moved anywhere
  
- Shows node color meanings
  
- Shows relationship line meanings
  
- Click `×` to hide/show

### Interpreting the Graph

- **Node Size**: Larger nodes = more connections
  
- **Node Color**: Indicates entity type (see legend)
  
- **Line Thickness**: Thicker = stronger relationship
  
- **Line Style**: Solid/dashed indicates relationship type
  
- **Clusters**: Groups of tightly connected nodes

### Graph Analysis Report

Check `graph_analysis_report.txt` for:

- Network density and clustering metrics
 
- Most connected entities (hubs)
  
- Key bridge entities (connectors)
  
- Relationship clusters and patterns
  
- Strategic insights and recommendations



# Use Cases

### Enterprise Security Teams

- **Attack Surface Management**: Continuous monitoring of digital assets
  
- **Third-Party Risk Assessment**: Vendor and partner security evaluation
  
- **M&A Due Diligence**: Pre-acquisition security assessment
  
- **Brand Protection**: Monitoring unauthorized use of assets

### Penetration Testers & Red Teams

- **Pre-engagement Reconnaissance**: Comprehensive target intelligence
  
- **Attack Path Discovery**: Relationship mapping for privilege escalation
  
- **Social Engineering Intelligence**: Employee and organizational mapping
  
- **Password Spray Research**: Email domain and pattern analysis

### Cybersecurity Researchers

- **Threat Actor Tracking**: Infrastructure and persona mapping
  
- **Campaign Analysis**: Understanding attacker infrastructure relationships
  
- **Vulnerability Research**: Technology stack analysis for exploit research
  
- **Academic Studies**: Large-scale web intelligence research

### Law Enforcement & Investigators

- **Digital Forensics**: Evidence collection and relationship mapping
  
- **Cybercrime Investigations**: Tracking illicit infrastructure
  
- **Person of Interest Profiling**: Digital footprint analysis
  
- **Network Investigation**: Understanding complex organizational structures

### Corporate Intelligence

- **Competitive Analysis**: Technology stack and online presence comparison
  
- **Market Research**: Understanding industry digital footprints
  
- **Executive Protection**: Monitoring exposed executive information
  
- **Risk Intelligence**: Proactive threat identification

## Legal & Ethical Considerations

### Permitted Usage

- Security testing on systems you own or have written authorization to test
  
- Educational and academic research with proper oversight
  
- Corporate security assessments on owned assets
  
- Bug bounty programs with explicit permission
  
- Law enforcement investigations with proper legal authority

### Prohibited Usage

- Unauthorized scanning of systems you don't own
  
- Privacy violation or harassment of individuals
  
- Commercial exploitation without permission
  
- Network disruption or denial of service
  
- Any activities violating applicable laws

### Compliance Requirements

1. **Always obtain proper authorization** before scanning
   
2. **Respect robots.txt** and terms of service
   
3. **Follow responsible disclosure** practices
   
4. **Comply with local laws** and regulations (GDPR, CFAA, etc.)
   
5. **Use rate limiting** to avoid overwhelming target systems
   
6. **Store collected data securely** and delete when no longer needed

## Security & Privacy Features

### Built-in Protections

- **Rate Limiting**: Configurable delays between requests
  
- **User-Agent Rotation**: Standard browser user agents
  
- **Error Handling**: Graceful failure without crashing
  
- **Memory Management**: Efficient processing of large datasets
  
- **Data Anonymization**: Option to anonymize reports

### Privacy Considerations

- **Local Processing**: All analysis happens on your machine
  
- **No Data Sharing**: No telemetry or external calls (except target)
  
- **Configurable Retention**: Automatic cleanup of temporary files
  
- **Selective Collection**: Disable modules that collect sensitive data

## Troubleshooting

### Common Issues & Solutions

**Issue**: `ModuleNotFoundError` for networkx or pyvis

**Solution**: Install graph dependencies: `pip install networkx pyvis`

**Issue**: SSL certificate verification errors

**Solution**: Tool automatically handles SSL issues, but ensure system certs are updated

**Issue**: DNS resolution failures
**Solution**: Check network connectivity or use `--no-dns` flag

**Issue**: Graph not generating

**Solution**: Ensure minimum 2 findings exist and graph libraries are installed

**Issue**: Image downloading blocked

**Solution**: Some sites block image scraping; use `--no-images` flag

### Performance Tips

1. **Limit crawl depth** for faster reconnaissance
   
2. **Use `--no-images`** to significantly speed up scans
   
3. **Increase timeouts** for slow sites: Modify config.py
   
4. **Use proxy** for distributed or slower scanning
   
5. **Monitor memory usage** for very large sites


### Community Contributions

- Submit bug reports and feature requests via GitHub Issues
  
- Share your graph analysis techniques
  
- Develop specialized detection modules
  
- Contribute to false positive pattern databases


## Contributing

I welcome contributions from the security community!

### How to Contribute

1. **Fork the repository**
   
2. **Create a feature branch**: `git checkout -b feature/AmazingFeature`
  
3. **Commit your changes**: `git commit -m 'Add some AmazingFeature'`
   
4. **Push to the branch**: `git push origin feature/AmazingFeature`
   
5. **Open a Pull Request**

### Contribution Areas

- **Detection Patterns**: New technology or platform patterns
  
- **False Positive Filters**: Improved filtering algorithms
  
- **Graph Algorithms**: Better relationship detection
  
- **Output Formats**: Additional report formats
  
- **Performance**: Speed and memory optimizations

## Disclaimer

**WebRecon Pro is designed for legitimate security research and authorized testing only.**

### LEGAL DISCLAIMER:

1. The authors are not responsible for misuse of this tool
   
2. Users must ensure they have proper authorization before scanning
   
3. This tool should only be used in accordance with applicable laws
   
4. Educational purposes only - use at your own risk
   
5. Always respect privacy and comply with data protection regulations

### By using this tool, you agree to:

- Use it only for authorized security testing
  
- Respect all applicable laws and regulations
  
- Not use it for malicious purposes
  
- Accept full responsibility for your actions


### Reporting Issues

**When reporting issues, please include**:

1. Command used and target URL (or similar test case)
   
2. Error messages or unexpected behavior
   
3. Your environment (OS, Python version, installed packages)
   
4. Steps to reproduce the issue

## Educational Value

WebRecon Pro is not just a tool but an educational platform for understanding:

1. **Web Infrastructure Mapping**: How modern websites are structured
   
2. **Digital Footprint Analysis**: What organizations expose online
   
3. **Relationship Analysis**: How entities connect in the digital world
   
4. **Data Correlation**: Finding meaningful patterns in large datasets
   
5. **Visual Intelligence**: Presenting complex data in understandable ways

## Version History

- **v7-6.0** (Current): Relationship graphs, tabular reporting, enhanced intelligence
  
- **v5.0**: Image downloading, comprehensive reporting, false positive filtering
  
- **v4.0**: Modular architecture, proxy support, multi-format output
  
- **v3.0**: Technology detection, social media intelligence, DNS integration
  
- **v2.0**: Basic crawling, email harvesting, JSON reporting
  
- **v1.0**: Initial release with core crawling capabilities

---

**Made with ❤️ for the security community by D4rk_Intel**

**Remember**: With great power comes great responsibility. Always use this tool ethically, legally, and with proper authorization.

---

*Last Updated: January 2026| License: Educational Use Only*
