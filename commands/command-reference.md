# Command Reference

This reference outlines the standard tools and commands used during the controlled assessment. It serves an educational purpose and documents the parameters supported by the historical evidence.

## iw / iwconfig
These tools are used to query and configure wireless network interfaces in Linux.
- **Usage in Assessment:** `iw list` was used to query the capabilities of the wireless adapter, specifically confirming support for monitor mode. `iw dev` was used to verify the interface type.

## airmon-ng
A script from the Aircrack-ng suite used to enable monitor mode on wireless interfaces.
- **Usage in Assessment:** Executed via `sudo airmon-ng start wlan0` to transition the interface from managed mode to monitor mode, a prerequisite for capturing raw 802.11 frames.

## airodump-ng
A packet capture tool for 802.11 frames. It is used to discover wireless networks and identify connected clients.
- **Usage in Assessment:** Used to passively observe the wireless environment, identify the target authorized WLAN, and isolate the authorized client device for testing.

## aireplay-ng
A tool used to inject 802.11 frames, such as deauthentication packets, into a wireless network.
- **Usage in Assessment:** Used to transmit directed deauthentication frames to the specific authorized client device to observe the impact on its network connectivity. The syntax used in the assessment included specifying the attack type (`--deauth`), the number of frames, the target BSSID (`-a`), and the specific client MAC address (`-c`).
