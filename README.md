# Capaccino UI
## Introduction

Capaccino is designed to manage and visualize sensor data through a dashboard. The tool aims to simplify tasks like device configuration and data logging, which often require manual coding or separate software. By integrating these functions into a single interface, Capaccino aims to streamline the process of sensor data management for a variety of applications.

### Key Features

- 📊 **Real-time Visualization:**  
The dashboard displays sensor readings in real-time, providing immediate feedback and allowing for effective monitoring of various data points.

- ⚙️ **Configuration Interface:**  
The UI allows users to adjust device parameters directly, negating the need to modify the source code for simple configuration changes.
  
- 💾 **Data Logging:**  
Users have the option to create logs based on sensor data. The logging frequency can be adjusted as needed, offering flexibility in data capture for later analysis.

- 🔄 **Automatic Updates:**  
Automatic app updates as well as Over-The-Air (OTA) firmware upgrades are supported, allowing for straightforward updates to add features or address bugs.

## Getting Started

1. **Downloading the Latest Release:** Begin by downloading the most recent version of Capaccino-UI. You can find the latest release by visiting [this link](https://github.com/APSP-AG/Capaccino-UI/releases/latest). Download and install the application on your computer.
    
2. **Connecting the Capaccino Board:** Once the application is installed, connect the Capaccino board to your computer using a USB port. The Capaccino-UI app is designed to automatically recognize the device as soon as it's connected.
    
3. **Verifying the Connection:** To confirm that the Capaccino board is successfully connected, look for the USB icon located at the bottom left corner of the Capaccino-UI interface. This icon serves as an indicator of the connection status between the app and your Capaccino board.

## Data Logging & Visualization

### Dashboard Overview

The Dashboard is your central hub for real-time data visualization. It offers an easy-to-understand interface, complete with chart and download options. To access this feature, navigate to the "Dashboard" section in the sidebar.
#### Data Storage and CSV Export

- **Local Storage:** Every data point received from the sensors is stored locally in a database. This data is persistent between sessions.
- **CSV Export:** Clicking the "Save" button will loop through all stored data points and export them into a CSV file. 
- **Database Clearance:** The "Clear" button will erase all stored data points in the local database.

> [!WARNING]
> **CDC Parameter Caveats:** The CDC parameters are not stored with individual data points. When you export the CSV file, the CDC parameters are gathered and assumed to be the same across all data points. They will reflect the state that is active at the time of the export.

### Typical Workflow for Data Logging

To commence a fresh data logging session, begin by clicking the "Clear" button. This action will clear out any existing data points from the local database, ensuring that your new session starts with a clean slate. Once you have cleared the database, the app will automatically start logging new data points from your sensors.

When you're ready to conclude your session and save the accumulated data, simply click the "Save" button. This will export all the stored data points into a CSV file, capturing the entire range of data from your session. Remember, the CDC parameters active at the time of export will be applied uniformly across all data points in the CSV file.
### Setting Logging Frequency

To adjust how often data is logged:

1. Navigate to "Settings" in the sidebar.
2. Select the "Logging" subsection.
3. Here, you can adjust the frequency settings as per your requirements.

> [!WARNING]
> **Logging Frequency Caveats:** The maximum achievable logging frequency depends on the resolution and multiplier settings. Incompatible settings can lead to stale data in measurements. Refer to the indicator on the CDC parameters card.

## CDC Configuration Interface

### Adjusting Device Parameters

In the Capaccino interface, you'll find several options for configuring the CDC (Capacitive-to-Digital Converter). Each option controls a specific aspect of how the CDC behaves, affecting the precision, speed, and type of measurements you get. 

Instead of settings these parameters manually, you can use the suggest range slider to automatically determine suitable parameters.

> [!WARNING]
> It's important to choose the settings carefully to optimize sensor performance. Incorrect settings can produce readings that appear accurate but are actually invalid. 

## Automatic Updates

If there are any App or Firmware updates available, you will receive a notification. Simply follow the on screen instructions.
