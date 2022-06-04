# System Design

## Types

### QoS Rules

* Robot Control and Status: UDP list
* Robot TPC and Network Tables: TCP list
* Bulk: Discriminated Union
  * Disabled
  * 4 Mb/s

### DHCP Server Settings

* Wired IP Address Range
* Wireless IP Address Lanes
* Subnet Mask
* Broadcast Address
* DNS Server IP
* Domain Suffix

### At Home Settings

* Robot Name
* Firewall Mimic
* WPA Key

### Radio Settings

* Selected Radio
* Radio Mode
  * 2.4GHz
  * 5GHz
* Static IP: IP Address
* Wired IP: IP Address
* Bridge Wired Ports: bool
* QoS Rules
* DNS Settings
* At Home Settings (optional)

## Command Workflows

* Update Firmware
  * Select Network Interface
    * Ethernet Only
  * Must be OpenMesh Radio
  * Load Firmware
    * Refer to flashing utility instructions

* Update Radio Configuration
  * Select Radio Type
  * Select Operating Mode
  * At-Home?
    * True:
      * Set Robot Name
        * If OpenMesh Radio:
          * Set FRC Field Firewall Emulation
          * Set Bandwidth Limit
    * Set WPA Key (optional)
  * Configure Radio
        