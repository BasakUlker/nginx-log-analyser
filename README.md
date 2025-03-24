# Log Analyzer Script

## Overview

This Bash script analyzes an Nginx access log file and provides useful insights such as the most frequent IP addresses, requested paths, response status codes, and user agents.

## Features

- Displays the top 5 IP addresses with the most requests.

- Lists the top 5 most requested paths.

- Shows the top 5 response status codes.

- Identifies the top 5 user agents.

## Prerequisites

Linux/macOS with a Bash shell

Basic knowledge of shell scripting

## Usage

1. Download the log file:
```
wget -O nginx-access.log "https://gist.githubusercontent.com/kamranahmedse/e66c3b9ea89a1a030d3b739eeeef22d0/raw/77fb3ac837a73c4f0206e78a236d885590b7ae35/nginx-access.log"
```

2. Make the script executable:
```
chmod +x log_analyzer.sh
```

3. Run the script:
```
source log_analyzer.sh 
```

## Sample Output

Top 5 IP addresses with the most requests:
45.76.135.253 - 1000 requests
142.93.143.8 - 600 requests
178.128.94.113 - 50 requests
43.224.43.187 - 30 requests
178.128.94.113 - 20 requests

Top 5 most requested paths:
/api/v1/users - 1000 requests
/api/v1/products - 600 requests
/api/v1/orders - 50 requests
/api/v1/payments - 30 requests
/api/v1/reviews - 20 requests

Top 5 response status codes:
200 - 1000 requests
404 - 600 requests
500 - 50 requests
401 - 30 requests
304 - 20 requests

## Notes

This script uses commands such as awk, sort, uniq, and head.

Ensure the log file follows the standard Nginx access log format.

Related to: https://roadmap.sh/projects/nginx-log-analyser
