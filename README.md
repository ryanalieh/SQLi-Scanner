# Advanced SQL Injection Scanner

## Overview

An SQL Injection Scanner that is a sophisticated, Python-based tool developed for automating the detection of SQL Injection vulnerabilities in web applications by sending different SQLi payloads to specified URLs and analyzing the responses for signs of injectable parameters.

## Files

### 1. `SQL-is.py`
This script performs SQL Injection testing on URLs and HTML forms. It uses various payloads to identify potential vulnerabilities and outputs the results.

**Usage:**
```bash
python SQL-is.py [URL] [OPTIONS]
```

**Options:**
- `--payloads`: File containing custom SQLi payloads (one per line)
- `--timeout`: Request timeout in seconds (default: 10)
- `--verbosity`: Increase output verbosity (0 = minimal, 1 = detailed, 2 = debug)

**Default SQLi Payloads:**
- A set of common SQLi payloads to test for vulnerabilities, including:
  - `' OR '1'='1' --`
  - `' UNION SELECT NULL, NULL, NULL--`
  - `' OR EXISTS(SELECT * FROM users) --`
  - And many more...

**Default Error Indicators:**
- A list of default error indicators to identify SQLi vulnerabilities in the response.

## Contributing

Feel free to submit issues or pull requests if you have suggestions or improvements.
