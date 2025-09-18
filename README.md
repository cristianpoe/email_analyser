**Email Analysis Tool**
This is a self-contained, local web application for performing forensic analysis of raw email files (.eml). It is designed to run completely offline, providing a secure environment to inspect email headers, content, and attachments without transmitting data to any external services.

The tool provides a user-friendly web interface where you can upload an .eml file and receive a detailed, organized report.

**Features**
Header Analysis: Extracts and organizes critical email headers, including From, To, Subject, and Date.

Authentication Checks: Provides a summary of SPF, DKIM, and DMARC authentication results.

Network Hop Tracing: Parses "Received" headers to trace the path an email took through various servers, including originating IPs and rDNS.

URL and IP Extraction: Identifies and "defangs" URLs and IP addresses found within the email body.

Attachment Analysis: For each attachment, the tool calculates MD5, SHA-1, and SHA-256 hashes and scans for known malicious file signatures. Downloads a .zip file copy.

Content Viewer: Renders a clean preview of the email's HTML and plaintext content, and allows you to view the raw source.

PDF Export: Generates a print-friendly PDF report of the analysis for easy sharing or archival.

**Getting Started**
Installation and Usage
Download the binary: Download the latest "email_analyser" binary

Make the binary executable: Open a terminal, navigate to the directory where you downloaded the file, and make it executable with the chmod command:
chmod +x email_analyser

Run the application: Launch the binary from your terminal. By default, it runs on port 5000. You can specify a different port using the -p option:
./email_analysis -p 8080

Open in browser: Open your web browser and navigate to http://127.0.0.1:5000 (or the port you specified) to access the tool.

Analyze your file: Use the "Upload a raw email file" section to select a .eml file from your computer and click "Analyze Email" to generate the report.
