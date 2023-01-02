[<img src="https://www.intelgic.com/static/img/intelgic.png" width="200">](https://www.intelgic.com/ "Powered By Intelgic")
  

 📧 Accounts Automation
====================================

# :sparkler: Jira Worklog Invoice
This bot can be used to download project wise worklog from Jira account. It will calculate the total of worklog hours & billing amount on the basis of downloaded jira worklog and rate provided in "Active_Project_List" excel sheet. Bot will then generate the project invoice pdf and send email with attached invoice to specific client's email id provided in "Active_Project_List" excel sheet.

## 🔥 Features:
- Read Project name, ProjectURL, WorklogURL, Start date, Client name, Company name, Rate, email id from "Active_Project_List" excel sheet
- Download respective worklog from Jira account
- calculate total work hours & billing amount on the basis of downloaded jira worklog and rate provided in "Active_Project_List" excel sheet.
- Make the invoice and convert that to pdf.
- Send the invoice to specific email id provided in project details excel sheet

## :heavy_check_mark: How to use?
1. Import the script xml file to your working directory of Dwmaker. `Default: My Scripts`
2. Set full path to the directory where you have saved your "Active_Project_List.xlsx" file `(Line: 5) Default: C:\Intelgic\Active_Project_List.xlsx`.
        - ***Please note:*** *Sample of "Active_Project_List.xlsx" and "Invoice_Template_DemoProject.docx" is provided in the folder name "Intelgic".*
3. Set Jira credentials `(Line:28-29) `. 
4. Set the full path of worklog download file `(Line: 76) Default: C:\Users\Intelgic\Downloads`
5. Set the full path of invoice template document file `(Line: 172) default: C:\Intelgic\Invoice_Template\Invoice_Template_DemoProject.docx`
6. Set the directory path of generated invoice to be saved `(Line: 196) Default: C:\Intelgic`
7. Save the bot.
8. Run the bot.

# :sparkler: Quickbooks Credit Card Reconciliation
This bot can be used to reconcile credit card statements in QuickBooks Online.

## 🔥 Features:
- Pdf formats of Credit card statements need to be uploaded to User portal to extract the required data from the statements by AI Parser for reconciliation. 
                ***Please note:*** *For more information regarding User portal and AI Parsing of statements visit `https://intelgic.com/` or email us to `info@intelgic.com`.*
- After parsing the data from uploaded statements Bot will get all the required data for reconciliation.
- Login into QuickBooks Online.
- Nevigate to specific company page on the basis of data provided in "qb_data" excel sheet.
- Go to reconciliation page and set Ending Balance & Ending date.
- Compare the last reconcile date and Ending date to decide if it is already reconciled or not.
- Check for the difference amount.
- If difference amount is 0 then it will reconcile else it will close the reconcilation window without saving and through an email with discrepancy details.

## :heavy_check_mark: How to use?
1. Import the script xml file to your working directory of Dwmaker. `Default: My Scripts`
2. Set the directory path you would like the bot to save the downloaded credit card statement file  `(Line: 5) Default: C:\Intelgic\QuickBook\Download`.
3. Credit card statements need to be uploaded to User protal for parsing through AI parser and to go further with Reconciliation.
                ***Please note:*** *User portal and AI API url is needed for uploading Credit Card statements to be parsed through AI parser. An example of AI API url given in `(Line:11) example: https://intelgic_ai_api_url.com`. For more query about Bot portal and AI parsing of Credit card statements email use to `info@intelgic.com`*
4. Set Quickbooks credentials `(Line:13-14) `. 
5. Set the full path of "qb_data.xlsx" `(Line: 15) Default: C:\Intelgic\QuickBook\Datasource\qb_data.xlsx`
                - ***Please note:*** *Sample of "qb_data.xlsx" is provided in the folder name "Intelgic\QuickBook\Datasource".*
6. provide Email id to where the bot should send the discrepancy email. `(Line: 117) default: intelgic@abc.com`
7. Save the bot.
8. Run the bot.

# :sparkler: Invoice Processing via InforVisual desktop app
This bot can be used to process invoices of Purchase Orders from various vendors in Infor Visual Desktops.

## 🔥 Features:
- Pdf formats of Invoices need to be uploaded to User portal to extract the required data from the statements by AI Parser for reconciliation. 
                ***Please note:*** *For more information regarding User portal and AI Parsing of statements visit `https://intelgic.com/` or email us to `info@intelgic.com`.*
- After parsing the data from uploaded invoices Bot will get all the required data like PO numbers, Invoice numbers, amount, quantity etc. for Invoice Processing .
- Signin into Infor Visual Desktop with specific Database.
- Go to "purchase Order Receipt" window and retrive the purchase related data by entering PO number got from invoice after AI parsing.
- Go to reconciliation page and set Ending Balance & Ending date.
- Enter all required data like Amount, Invoice number, Invoice date etc.
- Delete all rows which are not matched to the invoices.
- Process the invoice and store the newly generated Voucher ID.
- Bot will send an email with all details of matched and unmatched data.

## :heavy_check_mark: How to use?
1. Import the script xml file to your working directory of Dwmaker. `Default: My Scripts`
2. Pdf of Invoices need to be uploaded to User protal for parsing through AI parser and to go further with Invoice processing.
                ***Please note:*** *User portal and AI API url is needed for uploading Invoices to be parsed through AI parser. An example of AI API url given in `(Line:5) example: https://intelgic_ai_api_url.com`. For more query about User portal and AI parsing of Invoices email use to `info@intelgic.com`*
3. Set Infor visual Username , Database name and Password in respective lines of code `(Line:40-42)`. 
4. Set the Tax GL code if applicable `(Line: 44)`
5. Set the Purchase Order Receipt Window's full name `(Line: 46) Default:Purchase Order Receipts - INT`
6. Set the directory path of "report_template.xlsx" `(Line: 48) Default:C:\Intelgic\InforVisual`
                 - ***Please note:*** *Sample of "report_template.xlsx" is provided in the folder name "Intelgic\InforVisual".*
7. provide Email id to where the bot should send the details email. `(Line: 464) default: intelgic@abc.com`
8. Save the bot.
9. Run the bot.

# :sparkler: QuickBooks Online Categorization
This bot can be used to categorize transactions of a specific company with various vendors in QuickBooks online.

## 🔥 Features:
- Retrieve the transaction list as per the start date and end date provided by the user with the help of a QuickBooks API call.
- Sign in to QuickBooks Online and navigate to a specific company's Banking page.
- Go to a specific Account as per the Account name provided by the user.
- Add categories to all the pending transactions.
- Bot will send an email with all details if any Category is not found.

## :heavy_check_mark: How to use?
1. Import the script XML file to your working directory of Dwmaker. `Default: My Scripts`
2. Set QuickBooks OAuth Refresh Token. `(Line:2)`
                ***Please note:*** *You can get your QuickBooks Refresh token both for the Sandbox account and the Production account. Here the default code is for production. To use it for the Sandbox environment change the Environment from 'Production' to 'Sandbox' in `line number 2`. To know more about the QuickBooks OAuth process please visit: `https://developer.intuit.com/app/developer/qbo/docs/develop/authentication-and-authorization/oauth-2.0`*
3. Set Company ID, Start date, and End date in respective lines of code. `(Line:5-7)`
4. Set Company name. `(Line:69) Default:Intelgic Innovations Inc`
5. Set the Account name. `(Line:70)`
6. Set QuickBooks Username/Email ID and Password in respective lines of code `(Line:74-75)`.
7. provide the Email id to where the bot should send the details email. `(Line: 181) default: intelgic@abc.com`
8. Save the bot.
9. Run the bot.

# :sparkler: QuickBooks Batch Transactions Entry
This bot can be used to enter batch transactions received from an API  to QuickBooks desktop.

## 🔥 Features:
- Retrieve the batch transaction list for multiple companies through an API call.
- Sign in to QuickBooks Desktop and navigate to a specific company's Banking page.
- Enter the batch transactions for that company.
- Enter debit transactions and credit transactions seperately.
- Close the company page when finished and move to next company.

## :heavy_check_mark: How to use?
1. Import the script XML file to your working directory of Dwmaker. `Default: My Scripts`
2. Set QuickBooks Desktop exe file path. `(Line:1)`
3. Pdf or Excel of statements need to be uploaded to User protal for parsing through AI parser and to go further with Invoice processing.
>***Please note:*** *User portal and AI API url is needed for downloading parsed statments. An example of AI API url given in `(Line:5) example: https://intelgic_ai_api_url.com`. For more query about User portal and AI parsing of Invoices email use to `info@intelgic.com`*
4. Set API url where the information about the last entered statement should be sent. `(Line:93)` This is required to let the portal know that this statement is done.
5. Save the bot.
6. Run the bot.
