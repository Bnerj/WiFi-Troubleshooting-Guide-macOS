## WiFi Troubleshooting Guide for macOS

Having issues connecting to WiFi-network on your Mac? This guide outlines detailed steps to diagnose and fix common WiFi issues.

## Introduction 
Wi-Fi connectivity issues can be fustrating, especially on macOS where some troubleshooting steps differ from other operating systems. This guide provides a clear, step-by-step process for diagnosing and resolving common Wi-fI problems on Macs, using both built-in macOS tolls and advanced Terminal commands.

Whether your mac is experiencing slow speeds, frequencgt disconnections, or trouble connecting to networks, this guide will help you identify the cause and apply safe, effective solutions, all while keeping your system settings backup and intact. It's designed aspecifically for macOS users, ensuring that each steps matches the unique behavior and utilities of Apple devices. 

## Operating System
- macOS (Monterey, Venture, or later).

## Steps 
- This guide focuses on macOS systems. Steps may vary slightly depending on your macOS version (Monterey, Ventura, or later.

## Step 1. Check the WiFi Menu 
1. Click the WiFi icon in the top-right menu bar on your macbook.

2. Ensure the wifi is turned on.

3. Verify that your network is listed and selectable.

<img width="301" height="270" alt="Wifi_menu" src="https://github.com/user-attachments/assets/e0430822-31ba-4425-9c2b-917adcaf1091" />

## Step 2. Forget and Reconnect to Network
1. Open **System Settings** located on the dock of your macbook.

2. Open **Network**, then **WiFi**.

<img width="706" height="902" alt="System_Settings" src="https://github.com/user-attachments/assets/ab5312a5-69c6-402b-9bc0-8b88516ce8f0" />

3. Select your network and click on **Forget**.

<img width="591" height="213" alt="forget_connect" src="https://github.com/user-attachments/assets/11324d29-fe47-488d-8bf1-90d247dd2df5" />

4. Reconnect to network by selecting it and entering the password. 

<img width="512" height="343" alt="Restart_wifi" src="https://github.com/user-attachments/assets/f9ad5342-582b-4141-923a-c40f74df89ad" />


## Step 3. Restart WiFi 
1. Click the WiFi icon, turn off WiFi, wait 5 seconds, then turn WiFi back on.

<img width="706" height="856" alt="Turn_Off_WiFi" src="https://github.com/user-attachments/assets/b3fd9f6d-3419-49aa-9d69-8d6ddded71e7" />

2. Check if the network recconnects automatically. 

<img width="466" height="313" alt="Restart_wifi_2" src="https://github.com/user-attachments/assets/f355fd09-6486-44cc-9cd3-a86ec691f535" />


## Step 4. Diagnoise Connection 
1. If reconnection fails, click **System Settings**, **Network**, **WiFi**,  **Advanced**, and finally **Diagnostics**.

<img width="707" height="861" alt="Advanced_Diagnostic" src="https://github.com/user-attachments/assets/deab8ef7-f805-48a7-a11d-39fe84db32ca" />

2.  Follow the prompts to diagnose the issue.

## If you have a modern macOS, the diagnostic process is a bit different.

1.  Hold down the **option (⌥) key** on your keyboard.

2. While holding **option**, click the WiFi icon in the menu bar (top-right).

<img width="418" height="33" alt="WiFi_Menu" src="https://github.com/user-attachments/assets/ac6c4733-8902-44ec-9821-439e88a6f5f3" />

3. Select **Open Wireless Diagnostics** from the hidden menu.

<img width="294" height="76" alt="Open_Wireless" src="https://github.com/user-attachments/assets/6f242502-e9b8-46ec-99d8-134728daa8f7" />

4. The **Wireless Diagnostics App** will launch. Click **Continue** and follow the on-screen instructions.

<img width="617" height="435" alt="Diagnostic_Continued" src="https://github.com/user-attachments/assets/6ae7759f-ae0e-47d6-bcb8-bd0a55dbdee8" />

5. Once diagnostic are complete, close the app.

## macOS Version Notes

- **macOS Monterey (12.x) and Big Sur (11.x)**: All Terminal commands and Wireless Diagnostics steps are fully supported.

- **macOS Ventura (13.x)**: The steps remain the same; however, some Wi-Fi menu locations have moved slightly in System Settings.

- **macOS Sonoma (14.x)**: The `airport` command-line utility has been deprecated. Use `system_profiler SPAirPortDataType` or Wireless Diagnostics for similar information. Some menu labels may differ from earlier versions.

- **General advice**: If a step does not match your macOS version, consult [Apple’s Wireless Diagnostics guide](https://support.apple.com/guide/mac-help/use-wireless-diagnostics-mchlf4de377f/mac) for updated instructions.

**Note:** macOS updates may change menu paths or command-line utilities. If a step does not match your version, consult Apple’s Wireless Diagnostics guide or the GitHub Issues page for updates.

## Maintenance Plan 
- The steps in this guide are verified for macOS 11-14 (Big sur to Sonoma).

- Guide will be reviewed and updated quarterly, or when Apple releases major updates affecting Wi-Fi settings or command-line utilities.

- Users are encouraged to report any issues via GitHub Issues page to help keep this guide current.

## Backup & Warning 

⚠️ **Warning:** Some troubleshooting steps may remove saved Wi-Fi networks, VPN profiles, or custom settings. Always back up before making changes. 

### Backing up Wi-Fi Preferences 

1. Open Terminal and run:
```bash
mkdir -p ~/WiFi_Backup
cp /Library/Preferences/SystemConfiguration/com.apple.airport.preferences.plist ~/WiFi_Backup/
cp /Library/Preferences/SystemConfiguration/com.apple.network.identifcation.plist ~/WiFi_Backup/
cp /Library/Preferences/SystemConfiguration/NetworkInterfaces.plist ~/WiFi_Backup/
cp /Library/Preferences/SystemConfiguration/preferences.plist ~/WiFi_Backup/
```

## Additional Resources

- [Apple Support: Wireless Diagnostics on your Mac](https://support.apple.com/en-lamr/guide/mac-help/mchlf4de377f/mac?utm_source=chatgpt.com)

- [Apple Support: WiFi Network Troubleshooting on Mac](https://support.apple.com/en-lamr/guide/mac-help/mchlp1185/mac?utm_source=chatgpt.com)

- [Apple Support: macOS Release Notes](https://developer.apple.com/documentation/macos-release-notes)
  

