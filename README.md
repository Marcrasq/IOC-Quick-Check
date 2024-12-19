# IOC-Quick-Check
Chrome extension for rapid analysis of potential Indicators of Compromise (IOCs) using VirusTotal API. Supports URLs, IPs, domains, and file hashes.

## Features

- Real-time IOC analysis
- Multiple IOC types supported (URLs, IPs, domains, file hashes)
- Offline mode with caching
- Respect API quotas rate limit
- Draggable results panel

## Installation

1. Clone this repository
2. Open Chrome and navigate to `chrome://extensions`
3. Enable "Developer mode"
4. Then click Load unpacked and select the extension directory

## Configuration

1. Get a VirusTotal API key from [VirusTotal](https://www.virustotal.com/)
2. Go to the extension icon, click on it and insert your API key.
3. It is now ready to use

## Usage

1. Choose any of the potential IOC text on a webpage.
2. Clicking on the file, right click and select “Check IOC with VirusTotal”
3. See analysis results in the popup panel.

## Architecture

The extension consists of:
- Background script: Handles API calls and caching
- Content script: Manages UI overlay
- Popup: Handles configuration
- Error boundary: It also provides error handling.
- Offline support: Queues requests when offline

## Error Codes

- VT001: API key not configured
- VT002: Rate limit exceeded
- VT003: Network error
- VT004: Invalid IOC format
- VT005: Offline mode active

## License

see LICENSE for more information
