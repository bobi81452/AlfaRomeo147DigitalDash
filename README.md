# AlfaRomeo147DigitalDash
It is simple implementation of digital dashboard app for alfa romeo 147 from 2002 using kwp fast
# App6 – Android OBD Application

## What is this?
**App6** is an Android mobile application developed using **Xamarin.Android** in C#. It connects via Bluetooth to an OBD-II adapter to read data from a vehicle and display it using custom gauge views (dashboard-style meters).

 **Note:** This project is designed for vehicles using **K-Line protocol (KWP2000 Fast Init)**. As such, **only a limited number of OBD PIDs are supported**. It's intended for use with older cars that do not support full ELM327 PID ranges.

## Features
- Reads real-time vehicle data (RPM, speed, temperature, etc.)
- Sends standard OBD-II commands (e.g., `010C` for RPM)
- Connects to Bluetooth OBD-II adapters (like ELM327 clones)
- Displays data with custom-built gauge UI components

## Project Structure
- `MainActivity.cs` – The main activity that initializes the UI and connects to the OBD interface
- `ObdManager.cs` – Manages Bluetooth connection and OBD command execution
- `ObdProtocol.cs` – Parses and interprets OBD-II responses
- `GaugeView.cs` and `CustomGaugeView.cs` – Custom gauges that visualize sensor values
- `AndroidManifest.xml` – Android permissions and app settings

##  Technical Overview
- **Language:** C# (.NET / Xamarin.Android)
- **Platform:** Android API 21+
- **Bluetooth:** Uses `BluetoothSocket` and `BluetoothAdapter` for communication
- **IDE:** Visual Studio with Xamarin support (`App6.sln`)

##  Requirements
- Android device with Bluetooth
- K-Line compatible OBD-II Bluetooth adapter (e.g., ELM327)
- Vehicle with OBD-II support (older models, pre-CAN)

## How to Run
1. Clone this repository
2. Open `App6.sln` in Visual Studio
3. Deploy to an Android device (or emulator with mock Bluetooth)
4. Pair with an OBD-II adapter
5. View live data from the vehicle

## Ideas for Future Improvements
- Add logging and export features
- Graphical history of readings
- Support for more protocols and PID definitions
