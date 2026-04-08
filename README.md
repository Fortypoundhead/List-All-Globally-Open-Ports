# List-All-Globally-Open-Ports

A Windows VBScript utility that queries and displays all globally open firewall ports on your system.

## Overview

This script leverages Windows Firewall's COM interface to retrieve detailed information about all ports that are configured to be globally open in your Windows Firewall policy. It's useful for auditing your firewall configuration and identifying which ports are exposed to network traffic.

## What It Does

The script performs the following:

1. **Connects to Windows Firewall**: Accesses the local Windows Firewall manager using the HNetCfg.FwMgr COM object
2. **Retrieves Current Policy**: Gets the active firewall policy for the current profile
3. **Queries Open Ports**: Fetches the list of all globally open ports configured in the firewall
4. **Displays Detailed Information**: For each open port, outputs the following details:
   - **Port Name**: The friendly name of the port configuration
   - **Port Number**: The network port number
   - **IP Version**: Whether it applies to IPv4 or IPv6
   - **Protocol**: TCP or UDP
   - **Scope**: Network scope (local subnet, any, or specific addresses)
   - **Remote Addresses**: Which remote addresses can access the port
   - **Enabled**: Whether the port exception is currently enabled
   - **Built-in**: Whether it's a built-in Windows exception

## How to Use

1. Save the script on your Windows machine
2. Open Command Prompt or PowerShell as Administrator
3. Run the script with: `cscript ListAllGloballyOpenPorts.vbs`
4. The script will output all globally open ports and their properties to the console

## Requirements

- Windows operating system with Windows Firewall
- Administrator privileges to access firewall settings
- Windows Script Host (included with Windows) 
