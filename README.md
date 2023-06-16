CVE-2017-7529 Vulnerability Checker

This GitHub repository contains a Python script that serves as a tool for checking the vulnerability status of web servers against CVE-2017-7529. The vulnerability, also known as Range Header DoS (Denial of Service), can lead to server unresponsiveness when exploited.
Description

The exploit.py script included in this repository utilizes the requests library to perform HTTP requests and the logging module for capturing relevant information. It offers a straightforward method to assess whether a specific web server is vulnerable to CVE-2017-7529.

The key features of the script are as follows:

    Sends an initial HTTP request to the provided URL to gather information about the server.
    Retrieves the Content-Length header from the response to determine the content size.
    Calculates a modified content_length value and constructs a custom 'Range' header for subsequent requests.
    Sends a second HTTP request using the custom header to determine if the server is vulnerable.
    Logs the results, including the server status code and the presence of the "Content-Range" header.

Usage

To use the tool, follow these steps:

    Clone the repository:

shell

git clone https://github.com/your-username/cve-2017-7529-vulnerability-checker.git

    Install the required dependencies:

shell

pip install requests

    Navigate to the repository's directory:

shell

cd cve-2017-7529-vulnerability-checker

    Execute the script, providing the target URL as a command-line argument:

shell

python exploit.py http://example.com

The script will perform the vulnerability check and display the results in the console.
Disclaimer

This tool is intended for educational and testing purposes only. Use it responsibly and only on systems you have permission to assess. The repository owners are not responsible for any misuse or damage caused by the tool.
