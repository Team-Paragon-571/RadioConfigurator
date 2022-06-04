# Business Rules

## Radio Configuration

The Configurator will configure your router with the following settings:

* Static IP of 10.TE.AM.1
* Wired IP of 192.168.1.1 for future programming
* Bridge wired ports so that they may be used interchangeably
* 4Mb/s bandwidth limit on the outbound side of the wireless interface (optional; may be disabled for home use)
* QoS rules for internal packet prioritization
  * Robot Control and Status (UDP 1110, 1115, 1150)
  * Robot TCP & Network Tables (TCP 1735, 1740)
  * Bulk (All other traffic; disabled if bandwidth limit is disabled)
* DHCP Server Settings
  * Enabled
  * 10.TE.AM.11 - 10.TE.AM.111 on the wired side
  * 10.TE.AM.138 - 10.TE.AM.237 on the wireless side
  * Subnet Mask: 255.255.255.0
  * Broadcast address 10.TE.AM.255
* DNS server enabled.
* DNS server IP and domain suffix (.lan) are served as part of the DHCP.
* At Home Only:
  * No Bandwidth Limit
    * Disables bulk QoS rule
  * SSID may have "Robot Name" appended to team number
  * Firewall option may be enabled to mimic the field firewall rules (see game manual)
  * WPA Key
* All Modes:
  * Team Number
  * Radio Type
  * Mode
* Network configuration shall not be user modifiable, save for At-Home Only settings if configuration is being written in At-Home Mode.
* The Israeli teams use a special version of the OM5PAC firmware with restricted channels for use in Israel.
* The program can only interact with radios using an FRC-specific build of OpenWRT.
  * The program shall ship with the required firmware to program the OM5P-AN and OM5P-AC radios for use with the program.