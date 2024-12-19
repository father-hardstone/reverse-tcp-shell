
# Reverse TCP Shell
## Overview
This project demonstrates the implementation of a Reverse TCP Shell using Python and a Raspberry Pi Pico configured as a Rubber Ducky for payload delivery. It is designed for educational purposes to explore network security concepts, ethical hacking, and the importance of securing systems.

> **Disclaimer**: This project is strictly for educational use. Unauthorized use or distribution for malicious purposes is prohibited.


## Features
- Reverse TCP Shell implemented in Python.
- Uses a Raspberry Pi Pico as a Rubber Ducky for automated payload delivery.
- Establishes a TCP connection for remote command execution.
- Provides insights into network vulnerabilities and secure coding practices.
- Includes visual indicators (e.g., blinking Caps Lock light) for payload status.
## Payload Description
One component of this project is a Rubber Ducky payload written to deliver a reverse TCP shell on a Windows machine. Below is an overview of how the payload works:

## Payload Initiation:

The Rubber Ducky script launches PowerShell in a hidden mode (powershell -w hidden).
## TCP Client Setup:

The script establishes a TCP connection to the attacker's machine at a specified IP (192.168.100.93) and port (4444).
A socket is created to send and receive TCP traffic.
## Command Execution:

Commands from the attacker are processed, executed on the target machine, and the results are sent back via the TCP stream.
The prompt is updated dynamically with the current working directory.
## Feedback Mechanism:

The Caps Lock light blinks three times upon payload completion, serving as a visual indicator.
## Setup and Usage
### Prerequisites
A Raspberry Pi Pico configured as a Rubber Ducky.
Python 3.x installed on the attacker machine.
Network setup with the correct IP address and open port for listening.
### Steps
Configure the Raspberry Pi Pico with the provided Ducky script in the lib/ folder.
Run the Python server script on the attacker machine to listen for incoming  connections.
Connect the Raspberry Pi Pico to the target machine, where it will execute the payload.
### Folder Structure

reverse-tcp-shell/
├── lib/
│   ├── ducky-payload.txt   # The main payload script
│   ├── helpers.py          # Helper functions for the project
├── server.py               # The Python script for the attacker machine
├── requirements.txt        # Python dependencies
├── LICENSE                 # Open-source license
└── README.md               # Project documentation

This project is licensed under the MIT License.

# Contributing
Contributions are welcome! Please fork the repository and create a pull request.

