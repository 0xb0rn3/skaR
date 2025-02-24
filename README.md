# skaR

![License](https://img.shields.io/badge/license-MIT-green)
![Python Version](https://img.shields.io/badge/python-3.6%2B-blue)
![Version](https://img.shields.io/badge/version-1.0.3-brightgreen)

## FAST • ACCURATE • STEALTHY

skaR is a powerful yet user-friendly network scanning utility built as a Python wrapper around Nmap. It provides an intuitive interface for network reconnaissance, host discovery, and vulnerability scanning while maintaining the flexibility and power of Nmap.

## Features

- **Intuitive Command-Line Interface**: Navigate through scanning options with a simple menu-based system
- **Multiple Target Selection Methods**: Specify targets manually or discover hosts on your network
- **Flexible Scanning Profiles**: Choose from pre-configured scan types or create custom scans:
  - Quick Scan: Rapid overview of common ports
  - Standard Scan: Balanced scan with version detection
  - Deep Scan: Thorough analysis with OS detection and port enumeration
  - Stealth Scan: Low-profile SYN scanning to avoid detection
- **Live Host Discovery**: Automatically find active hosts on your specified network
- **Results Management**: Option to save scan results to files for later analysis
- **Automatic Dependency Management**: Required libraries are installed on first run

## Requirements

- Python 3.6 or higher
- Nmap (will be installed automatically if missing)
- Network access with appropriate permissions

## Installation

### Method 1: Direct Clone

```bash
git clone https://github.com/0xb0rn3/skaR.git
cd skaR
chmod +x skaR
sudo ./skaR
```

### Method 2: Pip Installation

```bash
pip install git+https://github.com/0xb0rn3/skaR.git
skaR
```

## Usage

Run the script to launch the interactive menu:

```bash
sudo ./skaR 
```

### Main Menu Options

1. **Set Target**: Define which hosts to scan
   - Manual input: Enter IP addresses or ranges directly
   - Discover on interface: Find active hosts on your network

2. **Set Scan Type**: Choose scanning methodology
   - Quick scan: Fast scan of common ports (`-T4 -F --version-light`)
   - Standard scan: Balanced scan with version detection (`-T3 -sV`)
   - Deep scan: Comprehensive scan with OS detection (`-T2 -A -p-`)
   - Stealth scan: Low-visibility SYN scan (`-sS -T2 --max-retries 1 --min-rate 100`)
   - Custom: Specify your own Nmap parameters

3. **Show Current Settings**: Display configured targets and scan options

4. **Run Scan**: Execute the scan with current settings
   - Results are displayed in the terminal
   - Option to save results to a file

5. **Exit**: Terminate the application

## Example Workflow

```
1. Set target -> Choose option 2 (Discover on interface) -> Enter network range
2. Select hosts from the discovery results
3. Set scan type -> Choose option 2 (Standard scan)
4. Show current settings to verify configuration
5. Run scan and view results
```


## Security Notes

- Network scanning without proper authorization may be illegal in many jurisdictions
- Only use skaR on networks you own or have explicit permission to scan
- Stealth scanning should be used responsibly and only in appropriate security testing contexts

## Troubleshooting

- If you encounter permission errors when running scans, try running the script with elevated privileges
- For network discovery issues, ensure you have the correct interface name and network range
- Dependencies are automatically installed but may require proper permissions

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


## Disclaimer

skaR is designed for legitimate network administration and security testing purposes only. The authors are not responsible for any misuse or damage caused by this program. Always ensure you have proper authorization before conducting network scans.

## Author

- [@0xb0rn3](https://github.com/0xb0rn3)
