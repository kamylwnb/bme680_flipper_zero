BME680 Sensor Application for Flipper Zero
Overview
This is a comprehensive environmental monitoring application for Flipper Zero that interfaces with the BME680 sensor via I2C. The BME680 is a high-precision environmental sensor that measures temperature, humidity, barometric pressure, and air quality (gas resistance).

Features
Sensor Measurements
Temperature: Accurate temperature readings in Celsius
Barometric Pressure: Local atmospheric pressure in hPa with sea-level pressure calculation
Humidity: Relative humidity percentage
Gas Resistance: Air quality indicator via VOC (Volatile Organic Compounds) detection
Dew Point: Automatically calculated using the Magnus formula
User Interface
Main Screen: Scrollable card-based interface displaying all sensor readings with custom icons
Settings Menu: Configure sensor parameters and application preferences
Dark Mode: Optional dark theme for better visibility in low-light conditions
Legend Screen: Interactive help screen with 2D panning that explains all icons and displays creator information
Configuration Options
I2C Address Selection: Toggle between 0x76 and 0x77 to match your sensor
Gas Sensor Control: Enable/disable the heater element for VOC measurements
Altitude Compensation: Set your altitude (0-5000m) for accurate sea-level pressure calculation
Persistent Settings: All configurations are automatically saved to /ext/apps_data/bme680/config.bin and restored on startup
Technical Features
Forced Mode Operation: Sensor operates in forced mode for optimal power efficiency
I2C Communication: Robust I2C interface with timeout protection
Thread-Safe: Uses mutex protection for concurrent data access
Error Handling: Comprehensive error checking and logging
Non-blocking UI: Sensor readings don't freeze the user interface
Automatic Directory Creation: Creates necessary directories for configuration storage
Icons
Custom 10x10 pixel XBM icons for each measurement:

🌡️ Thermometer for temperature
📊 Gauge for pressure
💧 Drop for humidity/dew point
🔥 Flame for gas/heater status
Navigation
Main Screen: Use Up/Down to scroll through measurements, OK to enter settings, Back to exit
Settings: Use Up/Down to navigate, Left/Right to adjust values, OK to select, Back to exit app
Legend Screen: Use arrow keys to pan the content, OK/Back to return to settings
Configuration File
Settings are stored in binary format with:

Magic number validation (0x42534D45 "BSME")
Version checking for compatibility
Automatic backup and restore
Creator
Dr. Mosfet
