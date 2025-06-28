# Comprehensive Server Hardware Reporting Tool for Linux Servers

![GitHub release](https://img.shields.io/github/release/JustLeo123/server-hw-report.svg)
[![Download Releases](https://img.shields.io/badge/Download%20Releases-%20%F0%9F%93%96%20%F0%9F%93%9A%20-blue)](https://github.com/JustLeo123/server-hw-report/releases)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Supported Environments](#supported-environments)
- [Configuration Options](#configuration-options)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Overview
The **server-hw-report** tool collects and stores detailed hardware and kernel configuration reports from both physical and cloud-based Linux servers. This tool is designed for sysadmins, IT professionals, and anyone who needs to audit, diagnose, or manage hardware configurations across various environments. The reports generated provide valuable insights into server performance, inventory, and overall health.

## Features
- **Comprehensive Reporting**: Gather detailed information on hardware components, kernel configurations, and system resources.
- **Multi-Environment Support**: Works seamlessly on bare-metal servers and cloud-based platforms.
- **Easy to Use**: Simple commands to generate and store reports.
- **Audit Ready**: Generate reports that meet auditing standards.
- **Asset Inventory**: Maintain an accurate inventory of hardware across your infrastructure.

## Getting Started
To get started with **server-hw-report**, download the latest release from the [Releases section](https://github.com/JustLeo123/server-hw-report/releases). You will find the executable file there, which you need to download and execute.

### Prerequisites
- A Linux-based server (physical or cloud).
- Basic command-line knowledge.

### Installation
1. Download the latest release from the [Releases section](https://github.com/JustLeo123/server-hw-report/releases).
2. Make the downloaded file executable:
   ```bash
   chmod +x server-hw-report
   ```
3. Move it to a directory in your PATH, such as `/usr/local/bin`:
   ```bash
   sudo mv server-hw-report /usr/local/bin/
   ```

## Usage
To use the **server-hw-report** tool, simply run the following command in your terminal:
```bash
server-hw-report
```
This command will generate a report and save it to the current directory. You can specify options to customize the report.

### Command Options
- `--output <file>`: Specify a filename for the report.
- `--format <json|yaml|txt>`: Choose the format for the report.
- `--include <component>`: Include specific hardware components (e.g., CPU, RAM, Disk).
- `--exclude <component>`: Exclude specific hardware components.

### Example Command
To generate a JSON report of the server's hardware and save it as `report.json`, use:
```bash
server-hw-report --output report.json --format json
```

## Supported Environments
**server-hw-report** supports various Linux distributions, including:
- Ubuntu
- CentOS
- Debian
- Fedora
- Arch Linux

It is also compatible with cloud platforms such as:
- AWS
- Google Cloud
- OVH
- Azure

## Configuration Options
The tool can be configured through a configuration file located at `~/.server-hw-report/config.yml`. You can set default options for output format, included components, and more. Below is an example configuration:

```yaml
output:
  format: json
  file: report.json
include:
  - cpu
  - memory
exclude:
  - disk
```

## Contributing
Contributions are welcome! If you would like to improve the **server-hw-report**, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch and create a pull request.

Please ensure your code adheres to the project's coding standards and includes tests where applicable.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- Thanks to the contributors who have helped improve this tool.
- Special thanks to the open-source community for their support and resources.
- Inspired by various system auditing tools that provide valuable insights into hardware configurations.

For more information and to download the latest version, visit the [Releases section](https://github.com/JustLeo123/server-hw-report/releases).