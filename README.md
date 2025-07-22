# **Interactive Data Viz Dashboard with AI Nudging**

This Gemini prompt generates a dynamic, single-page web application for visualizing data from CSV files. Powered by Apache ECharts, the application allows users to upload their data, switch between various chart types, and use conversational commands to interactively refine the visualizations.

## **Table of Contents**

* [App Setup](#app-setup)
* [Important Note on Generation](#important-note-on-generation)  
* [How to Use](#how-to-use)  
  * [Initial View](#1-initial-view)  
  * [Uploading Your Own Data](#2-uploading-your-own-data)  
  * [Interacting with the Charts](#3-interacting-with-the-charts)

## **App Setup**

To generate the visualization dashboard, please follow these steps:

1. **Download Files**: From the repository, download the `prompt.txt` file and an example `.csv` file from the /data directory (or use your own).  
2. **Upload to Gemini**: In a new Gemini chat (or a Gem), upload both the `prompt.txt` and the `.csv` file.  
3. **Provide the Prompt**: Use the exact prompt provided in `prompt.txt`.
4. **Enable Canvas Output**: Optional, but will ensure Gemini creates a Canvas response with a preview as opposed to code output.
5. **Generate the App**: Please allow a few minutes for the application to be fully generated.

## **Important Note on Generation**

**A Note on AI Generation:** Due to the non-deterministic nature of generative AI, there can be variances in the output app. If you find that an internal function of the generated application is not working as expected (e.g., uploading a new CSV, nudging a chart), please use the **"Fix errors"** button. This will often resolve any inconsistencies from the generation process.

## **How to Use**

### **1\. Initial View**

When you first use the generated tool, it will load with a default placeholder dataset. You will immediately see the four chart types populated with this data.

### **2\. Uploading Your Own Data**

* Locate the **"Upload New CSV"** button in the header.  
* Select a CSV file from your local machine.  
* The tool will automatically parse the file, infer the data columns, and re-render all four charts with your data.

**Important Note on CSV Format:** Your CSV **must** have a header row (e.g., Category,Value1,Value2). The application relies on this header to identify data columns correctly.

### **3\. Interacting with the Charts**

For each of the four charts, you have several interaction options:

* **Toggle Theme**: Use the **"Toggle Theme"** button in the header to switch the entire page and all charts between light and dark modes.  
* **Rate a Chart**:  
  * Click the **✅** button to approve a chart. This indicates you find it useful and enables the "Nudge" and "Download" options.  
  * Click the **❌** button to mark a chart as not useful.  
* **Nudge a Chart with AI**:  
  1. First, approve a chart by clicking **✅**. The **"Nudge Chart"** button will appear.  
  2. Click **"Nudge Chart"** to open a modal window.  
  3. In the text box, type a command in plain English. For example:  
     * `"Change the chart type to a pie chart."` 
     * `"Make the bars for 'Category A' and 'Category C' taller."`  
     * `"Use a red color for the 'Value1' series."`  
  4. Click **"Submit Nudge"**. The application will send the current chart settings and your request to the Gemini API and update the chart with the AI-generated modifications.  
* **Download a Chart**:  
  1. First, approve a chart by clicking **✅**. The **"Download SVG"** button will appear.  
  2. Click **"Download SVG"** to save a high-quality vector version of the chart.  
  3. You can also use the built-in ECharts toolbar (at the bottom of each chart) to **save** the **chart as a PNG image**.
