# power-automate-bim360-projects-to-onedrive

A Power Automate Flow to export BIM 360 Project data from a selected BIM 360 Account to a CSV file in OneDrive

[![PowerAutomate](https://img.shields.io/badge/Power-Automate-blue.svg)](http://flow.microsoft.com/)
[![License](http://img.shields.io/:license-mit-blue.svg)](http://opensource.org/licenses/MIT) 
[![OAuth2](https://img.shields.io/badge/OAuth2-v2-green.svg)](http://forge.autodesk.com/)
[![BIM360](https://img.shields.io/badge/BIM360-v1-green.svg)](http://forge.autodesk.com/)

## Description

This is a flow package for [Microsoft Power Automate](https://flow.microsoft.com/) that shows how to use [Autodesk Forge APIs](https://forge.autodesk.com/developer/documentation) to export project profiles from a [Autodesk BIM 360 Account](https://admin.b360.autodesk.com/login) to a CSV file in Microsoft OneDrive. 

## Setup
#### 1. Create Autodesk Forge App.
* Visit the [Forge Developer Portal](https://developer.autodesk.com) and sign up for an account
* [Create an App](https://developer.autodesk.com/myapps/create). Callback URL is not being used by this script. When asked for the 'callback URL', you can use any URL
* Take note of the **Client ID** and **Client Secret**.

#### 2. Add Custom Integration to BIM 360 Account
* Login to your BIM 360 Account Admin site, https://admin.b360.autodesk.com/
* Go to “SETTINGS” tab then to “Custom Integrations” tab
* Click on “Add Custom Integration” button to register your app for this specific account
* Take note of the **BIM 360 Account ID**.

#### 3. Add "OneDrive for Business" Connection to Power Automate
* Login to Power Automate site, https://flow.microsoft.com/
* In the navigation panel on the left, select **Data > Connections**
* At the top of the page, select **New connection**
* In the list of available connections, choose **OneDrive for Business** connection
* Follow the steps to enter your credentials to configure the connection

#### 4. Import Flow ".zip Package"
* Download [ExportBIM360ProjectstoOneDrive.zip](ExportBIM360ProjectstoOneDrive.zip)
* In Power Automate, select **My flows** from the navigation panel on the left, then click on **Import**
* In the Import Package page, click on the **Upload** button and select the **.zip package** downloaded earlier, then click on **Import**
* Scroll down to **Related resource**, click on **Select during import**, select **OneDrive for Business** connection from **step 3**, and click on **Import**
* When Import is completed, select **My flows**, look for **Export BIM 360 Projects to OneDrive** flow, and click on it. It should look like this: [bim360-projects-to-onedrive.pdf](bim360-projects-to-onedrive.pdf)

## Execute
#### 1. Run Flow
* In Power Automate, select **My flows** from the left panel, select the **Export BIM 360 Projects to OneDrive** flow, and click on **Run**
* Input **Client ID**, **Client Secret**, and **BIM 360 Account ID** from steps 1 & 2 in Setup and click **Run Flow**

![](ExportBIM360ProjectstoOneDrive%20RunFlow.jpg)

#### 2. Check OneDrive
* When Run is completed, a CSV file named **YYYY.MM.DD_hh_mm BIM 360 Projects.CSV** will be created in the root folder of your OneDrive for Business

![](ExportBIM360ProjectstoOneDrive%20OneDrive%20CSV.jpg)

## License

This sample is licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT).
Please see the [LICENSE](LICENSE) file for full details.

## Written by

Sam Nseir, P.E. [@samnseirpe](https://www.linkedin.com/in/samnseirpe/)
