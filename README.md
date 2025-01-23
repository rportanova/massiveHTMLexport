Export Safari Tabs as HTML Files

This AppleScript is designed to save the content of all open Safari tabs as individual HTML files. The files are saved in a folder named ExportedHTML located on the desktop.

Features
	•	Exports All Open Tabs: Retrieves the URL, title, and source HTML content of each tab in the active Safari window.
	•	Safe File Naming: Sanitizes tab titles to create valid file names, replacing characters that are invalid in file names.
	•	Organized Output: Creates an ExportedHTML folder on the desktop (if it doesn’t already exist) and saves each tab’s content as a separate .html file.

How to Use
	1.	Open Safari:
	•	Ensure that the tabs you want to export are open in the frontmost Safari window.
	2.	Run the Script:
	•	Open the script in Script Editor (or your preferred AppleScript editor).
	•	Run the script.
	3.	Check the Output:
	•	Navigate to your desktop.
	•	Open the ExportedHTML folder to find the exported .html files.

Script Details

Workflow:
	1.	Folder Setup:
	•	Creates the ExportedHTML folder on your desktop if it doesn’t already exist.
	2.	Tab Processing:
	•	Iterates through all tabs in the active Safari window.
	•	Extracts the URL, title, and HTML source of each tab.
	3.	File Naming:
	•	Sanitizes the tab titles to ensure file names are valid by replacing problematic characters with underscores (_).
	4.	HTML File Creation:
	•	Saves each tab’s HTML source as a .html file in the ExportedHTML folder.

Key Components:
	•	set saveFolder:
	•	Specifies the path to the output folder on the desktop.
	•	URL of tab and source of tab:
	•	Retrieves the tab’s URL and HTML source, respectively.
	•	do shell script:
	•	Handles folder creation, file name sanitization, and saving content using shell commands.

Notes
	•	File Name Sanitization:
	•	The script uses sed to remove invalid characters from tab titles. If a title contains characters like "\ / : * ? < > |", they will be replaced with underscores.
	•	Compatibility:
	•	Designed to work with macOS and Safari.

Troubleshooting
	•	No Tabs Exported:
	•	Ensure Safari is running and there are tabs open in the frontmost window.
	•	Output Folder Not Found:
	•	Confirm that the script has permission to create folders on the desktop.

Customization
	•	Change Output Folder:
	•	Modify the set saveFolder line to specify a different folder location.
	•	File Format:
	•	Adjust the script to save in other formats (e.g., .txt) if needed by replacing the .html extension in the filePath.
