How to use EBAS Data Submission Tool application
============

> This is a quick introductory manual for the ebas-submit-tool as well as the plotting tool offered. This document also contains an how-to on how to contribute to the troubleshooting documentation as well as the manual itself. Please fork the ebas-submit-tool user-manual repository to contribute to the documentation. [https://github.com/richard-olav/docs-ebas-data-submission-tool](https://github.com/richard-olav/docs-ebas-data-submission-tool). For data submission specific issues, please see the [EBAS data submission Manual](http://ebas-submit.nilu.no/). 

##The EBAS Data submission Tool

Go to [http://ebas-submit-tool.nilu.no/](http://ebas-submit-tool.nilu.no/)

Make sure that the file is a NASA Ames 1001 EBAS formatted file, as described from the templates at [http://ebas-submit.nilu.no/](http://ebas-submit.nilu.no/) or [http://www.gaw-wdca.org](http://www.gaw-wdca.org). 

	Please note, that for the time being, 
	the system does not handle complete particle number size distribution files, 
	This is due to size limitations in the set-up during test phase of the system. 
	It is, however, possible to check file headers for these files.

> Press the **Select file** button to select file from local directory

![Select file](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/select_file.png "Select file")

> Check file against the EBAS database tables by pressing the **Upload and check** button. Depending on the file size, this might take up to 1 minute.

![Upload and check](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/upload_check.png "Upload and check")

> The number of header errors and warnings, and data errors and warnings, are separated in two different windows.

![Errors and warnings](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/error_warning.png "Errors and warnings")

> Errors and warnings are marked in red and orange, respectively.

![Errors and warnings are marked in red and orange, respectively.](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/red_orange.png "Errors and warnings are marked in red and orange, respectively.")

> Pointing the mouse pointer on the highlighted line will show the error/warning message

![error/warning message](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/error_warning_message.png "error/warning message")

> Errors in file header can be corrected directly in the online browser. It is possible to correct all errors in one batch before re-checking the file. When done with the corrections, press the **Recheck file** botton. 

![Recheck file button](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/recheck_file.png "Recheck file button")

> Errors in the data part must be corrected locally on the user’s PC. Before the local modifications take place, it is possible to save and store the file modified in the web-tool to the local disc to include the modified header in the locally modified file. This is achieved by pressing the **Save file** button. The file is then downloaded to the data submitter’s local computer and can be opened there for editing. The figure below gives an example of a file with errors in the datapart.

![Save file button](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/save_file.png "Save file button")

> **Reset the system. Select file. Upload and check.**

> If/when file is correct, the statusbar will turn green and the **Submit file** button is activated. Upon submit, the file is sent to the EBAS FTP system, and an auto-email is sent to the data submitter. After entering the FTP system, the NASA Ames file is forwarded to manual inspection at NILU. 

![Submit file button](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/submit_file.png "Submit file button")

--------  -----------------------
**Post-processing inside NILU:** 
Before the data can be uploaded to EBAS, the submitted file will need manual inspection by the database team. If the file is correctly formatted, data will be available in EBAS within a few working days. The data submitter will be informed when this is done. He/she will also be contacted in case of problems with, or questions to, the submitted file.
--------  -----------------------

##Plotting data
The EBAS-submission-tool also comes with plotting capabilities. This is in order to make it easier for the users to validate their files and inspect their data before submission. This is especially usefull when you want to check for unusall values in your dataset and to double check that you have flagged all of these values. The community could also request to contribute to this tool by sending a request to ror@nilu.no.

##Contributing to the manual and the troubleshooting document

###The EBAS team <3 contributions!
For the EBAS-submission-tool manual and the troubleshooting document, git is used as a version controll system, and github is the platform hosting these documents. In order to contribute, you could fork the repository, and then we will look throught the proposed changes, and then commit these changes if we find that they are valuable to the project.

##The ebas-file-submission issue tracker
At the moment we are experimenting with online support of our ebas-submission-tool platform. If you go the the issue tracker via the main menu, you will get a list of errors reported from users trying to upload files using the ebas submission tool. We are doing this in order for our users to look through errors and see if any of the users previously has submitted errors similar to you (if you ever experienced one). Instead of us helping each and one of you directly, we want to build a repository where everybody can take part. You will have to have a registered Github account to submit issues (this is free of charge) to submit issues and comment on issues reported. If you do not have a userr, you could still browse the issues submited via the issue tracker.
