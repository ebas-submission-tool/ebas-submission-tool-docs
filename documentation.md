> **Pay attention**:
> - Make sure that your file is encoded using UTF-8

The EBAS Data Submission Tool
============

##About
This page contains information about the EBAS data submission and validation tool (The tool that helps you validate and submit files using the EBAS NASA ames format) which we will refer to as the EBAS-submit-tool. In addtion we give you information on how to plot your data as well as how to best troubleshoot validation errors, including information on how to encode your file in the UTF-8 format.

**So where do I start looking?**:

- If you are in a hurry to submit your data to EBAS you can look at **section 1.** Quick Start.

- If you want a more thorugh understanding of the tool please have a look at **section 2.** In depth tutorial of the EBAS-submit-tool.

- If you have a file you would like to plot, please see **section 3.**

- If you have problems with validating your file plases see the [EBAS-submit-tool troubleshooting docs](http://ebas-submit-tool.nilu.no/troubleshooting), for parsing issues see section 2.3. 

- If you have data submission specific issues, please see the [EBAS data submission Manual](http://ebas-submit-tool.nilu.no/troubleshooting) or contact us at <ebas@nilu.no>. 

- If you would like to contribute to our troubleshooting docs you can check out **section 4**. 

- For syntactical help related to the files themselves, take a look at **section 5**.

- If you are wondering when we schedule the next release, see **section 6**.

- And if you are interested in knowing more about our tech-stack, take a look at **section 7**.

###1. Quick Start- File validation

1. Go to http://ebas-submit-tool.nilu.no/
2. Press "Select file..." and select the NASA ames file you want to validate
3. Then press "Upload and check"
4. If your file is encoded using UTF-8, you should be getting the metadata header information in the top text-box. If not check your encoding and make sure that your header data follows the same syntax as the templates listed at [ebas-submit.nilu.no](http://ebas-submit.nilu.no/SubmitData/RegularAnnualDataReporting.aspx).
5. The application will prompt the number of errors and warnings (if you have any), you can hover over with your mouse pointer in order to get more information regarding the errors and warnings. 
6. You can edit the information in your browser by double-clicking the respective lines in the online editor (As mentioned above, the session will automatically timeout after 30 minutes regardless of activity, therefore we highly encourage you to  save your file whenever a change has been made, so that you do not loose any changes, or edit the file in a seperate text-editor). You can also get file related errors listed in your browser, below the file header error console. Note that these ones you cannot edit in the browser, you must open a seperate text-editor if you see data your data contains errors or warnings.
7. When you have eleminated all errors, you are able to press the "Submit file" button. Pressing this button will result in sending the data to the EBAS team for internal QA-check. The data-submitter listed in the file should recieve an e-mail confirming the submission.

###2. In depth tutorial of the EBAS data validation and submission tool

####2.1 The purpose of this tool
The EBAS Data Submission Tool is an online file format checker and a data submission system. It is designed to give the data submitters direct feedback on the formatted NASA Ames files and to deliver files through online data submission.

The tool aims at supporting data submitters from all projects and programs submitting data to EBAS who want to: 

- Check the consistency of their NASA Ames file 

- Upload data to EBAS
should use the tool.

All measurement principles registred in the EBAS portal, with online formatting templates available at <http://ebas-submit.nilu.no> and <http://gaw-wdca.org/SubmitData.aspx>, are supported by this tool. 

####2.2 How to use the tool
Go to [http://ebas-submit-tool.nilu.no/](http://ebas-submit-tool.nilu.no/)

Make sure that the file is a NASA Ames 1001 EBAS formatted file, as described from the templates at [http://ebas-submit.nilu.no/](http://ebas-submit.nilu.no/) or [http://www.gaw-wdca.org](http://www.gaw-wdca.org). 

	Please note, that for the time being, 
	the system does not handle complete particle number size distribution files, 
	This is due to size limitations in the set-up during test phase of the system. 
	It is, however, possible to check file headers for these files.

> Press the **Select file** button to select file from local directory

![Select file](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/select_file.png "Select file")

> Check file against the EBAS database tables by pressing the **Upload and check** button. Depending on the file size, this might take up to 1 minute.

![Upload and check](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/upload_check.png "Upload and check")

> The number of header errors and warnings, and data errors and warnings, are separated in two different windows.

![Errors and warnings](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/error_warning.png "Errors and warnings")

> Errors and warnings are marked in red and orange, respectively.

![Errors and warnings are marked in red and orange, respectively.](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/red_orange.png "Errors and warnings are marked in red and orange, respectively.")

> Pointing the mouse pointer on the highlighted line will show the error/warning message

![error/warning message](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/error_warning_message.png "error/warning message")

> Errors in file header can be corrected directly in the online browser. It is possible to correct all errors in one batch before re-checking the file (but be aware that the session might time out, see chapter on session timeouts). When done with the corrections, press the **Recheck file** botton. 

![Recheck file button](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/recheck_file.png "Recheck file button")

> Errors in the data part must be corrected locally on the user’s PC. Before the local modifications take place, it is possible to save and store the file modified in the web-tool to the local disc to include the modified header in the locally modified file. This is achieved by pressing the **Save file** button. The file is then downloaded to the data submitter’s local computer and can be opened there for editing. The figure below gives an example of a file with errors in the datapart.

![Save file button](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/save_file.png "Save file button")

> **Reset the system. Select file. Upload and check.**

> If/when file is correct, the statusbar will turn green and the **Submit file** button is activated. Upon submit, the file is sent to the EBAS FTP system, and an auto-email is sent to the data submitter. After entering the FTP system, the NASA Ames file is forwarded to manual inspection at NILU. 

![Submit file button](https://raw.githubusercontent.com/ebas-submission-tool/ebas-submission-tool-docs/master/images/submit_file.png "Submit file button")

--------  -----------------------
**Post-processing inside NILU:** 
Before the data can be uploaded to EBAS, the submitted file will need manual inspection by the database team. If the file is correctly formatted, data will be available in EBAS within a few working days. The data submitter will be informed when this is done. He/she will also be contacted in case of problems with, or questions to, the submitted file.
--------  -----------------------

####2.3. Issues with parsing the data
If you are trying to upload a dataset pressing the "Select file..." button, but experience that you are getting an error similar to "Internal Server Error 500" or "Requested JSON parse error", we suspect that you have not encoded your file in the proper encoding format. 

To find our wich encoding your file uses you can either use a text-editor and select save as, then most editors will likely show you which file encoding your file currently is going to be saved as. 

You can also use a web-browser to check the file format. With Firefox for example you can check this by Open firefox. Go to File-> Open File and then select your nasa-ames file. Then go to View -> Text Encoding and see what type of encoding you file is using. If you e.g. see that you are using "Western" encoding, switch to Unicode. If you have invalid charachters these will likely look something like this, e.g. -40�C instead of -40°C or H�rger instead of Hörger. The character encoding should be set to Unicode or UTF-8.

If you still are getting the same error, please contact us at <ebas@nilu.no>, or submit an issue using our issue tracker at github <https://github.com/ebas-submission-tool/troubleshooting/issues>.

###3. Plotting data 
The EBAS-submission-tool also comes with plotting capabilities. This is in order to make it easier for the users to validate their files and inspect their data before submission. This is especially usefull when you want to check for unusall values in your dataset and to double check that you have flagged all of these values. The community could also request to contribute to this tool by sending a request to ror@nilu.no.

> Currently you can only plot data that has a one year resolution, we expect to have fixed this in the next release

####3.1 Chrome users
If you are using Google Chrome, your select box might only show the first column in the selected dataset. To enable selecting all of the columns, you have to change some of your default settings in Google Chrome.
First go to Edit -> Preferences. Then at the bottom of the settings page (chrome://settings) press "Show advanced settings...". Scroll down until you see "Use hardware acceleration when available". Make sure this box is checked. This should work and if not, Firefox should be a safe choice.  

###4. Contributing to the troubleshooting document

For the EBAS-submit-tool troubleshooting document, Git is used as a version controll system, and github is the platform hosting these document. In order to contribute, you could fork the repository, and then we will look throught the proposed changes, and then commit these changes if we find that they are valuable to the project.

###5. The EBAS-file-submission and validation issue tracker
At the moment we are experimenting with online support of our ebas-submission-tool platform. If you check out our [issue tracker](https://github.com/ebas-submission-tool/troubleshooting/issues), you will get a list of errors reported from users trying to upload files using the ebas submission tool. We are doing this in order for our users to look through errors and see if any of the users previously has submitted errors similar to you (if you ever experienced one). Instead of us helping each and one of you directly, we want to have a forum where everybody can take part. You will have to have a registered Github account to submit issues (this is free of charge) and comment on issues reported. But if you do not have a user, you could still browse the issues submited via the [issue tracker](https://github.com/ebas-submission-tool/troubleshooting/issues).

###6. Releases
**Next release, version 1.1 is scheduled for 20th of June, 2016**

This will include bug fixes for:
* Plotting data with resoultion more than 1 year
* Session is deleted after 30 minutes

###7. Tech Stack
The EBAS-submit-tool is utilizes an open source technology stack.

![Python-flask](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/flask.png "Flask")
###<http://flask.pocoo.org/>

![Python](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/python.png "Python")
###<https://www.python.org/>

![Bootstrap](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/bootstrap.png "Bootstrap")
###<http://getbootstrap.com/>

![Git](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/git.png "Git")
###<https://git-scm.com/>

![Github](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/github.png "Github")
###<https://github.com/>

![Gitlab](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/gitlab.png "Gitlab")
###<https://about.gitlab.com/>

![Markdown](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/markdown.png "Markdown")
###<http://daringfireball.net/projects/markdown/>

![Bokeh](https://raw.githubusercontent.com/richard-olav/docs-ebas-data-submission-tool/master/images/tech_stack/bokeh.png "Bokeh")
###<http://bokeh.pydata.org/en/latest/>
