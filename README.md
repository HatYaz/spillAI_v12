# spillAI_v12
This Python script is a graphical user interface (GUI) application for downloading, processing, and predicting oceanographic data using NetCDF files from Environment Canada’s WCPS model.

This Python script is a **graphical user interface (GUI) application** for downloading, processing, and predicting oceanographic data using **NetCDF** files from **Environment Canada’s WCPS model**. The application uses **Tkinter** for the GUI and **RandomForestRegressor** for predictions.

### **Key Features of the Code:**
1. **Downloading NetCDF Data**  
   - Fetches ocean currents (**SeaWaterVelocityX/Y**) and wind data (**WindU/V**) from the Government of Canada’s website.
   - Downloads files based on a user-defined time interval.
   - Saves data in a selected directory.

2. **Processing & Extracting Data**  
   - Reads NetCDF files to extract the nearest **latitude/longitude** values.
   - Converts longitude values to align correctly.
   - Handles missing/invalid values.
   - Organizes extracted data in a **Pandas DataFrame**.

3. **Machine Learning Prediction**  
   - Uses **Random Forest Regression** to predict future values of:
     - uwindsurf
     - vomecrty
     - vozocrtx
     - vwindsurf
   - Trains on historical data extracted from NetCDF files.

4. **Graphical User Interface (GUI)**
   - Allows users to **input latitude, longitude, and time interval**.
   - Provides **buttons to browse** data directories and save results.
   - Displays results in a **table (Treeview Widget)**.
   - Shows **download progress** and detected variables.

5. **Interactive Map for Location Selection**
   - Uses **Cartopy** and **Matplotlib** to plot a map.
   - Allows users to **click on a map** to select a geographic location.

6. **Data Visualization**
   - Generates **bar charts** to display predicted values.
   - Saves extracted data and predictions in an **Excel file**.

7. **Threading for Performance**
   - Uses **threading** to handle data processing and downloads without freezing the GUI.

### **Summary**
The script is a **comprehensive tool for oceanographic data analysis**, integrating **real-time data retrieval, machine learning predictions, and interactive visualization** in a **user-friendly** Tkinter-based application.
