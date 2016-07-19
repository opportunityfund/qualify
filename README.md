# qualify
Web API project to prequalify borrowers for Opportunity Fund

We will provide a public web services API for pre-qualifying potential borrowers.  The Web API can be called directly by partners such as lending club, or can be called by our own web pages.

The root URL of all api calls will be:

    https://api.opportunityfund.org/v1

The qualify api will start with

   /qualify

Issuing a GET to /qualify will return a schema of the expexted fields and their types.

Issuing a POST to the same url will run our prequalify logic.  The input parameters will be stored in a database, and we will provide secured web UI for authenticated Opportunity Fund personel to change those parameters.  For audiability purposes, the change model will be multiple inserts, with the most recent inserting being deemed current.  

# Persistance
All data will be persisted in our small business CRM database (MS-SQL Server), potentally using side tables for this purpose.

# Web UI 
The web UI will be built using Angular or a similar java script / CSS framework.  

# Web API
The web API / web services stack can be build with either C# or Node.js, TBD

# Fields 

The fields will collect are:

fieldName type required caption
First Name
Last Name
Language Preference
Business Name
Business Zip Code
Business Type
Business Email
Mobile Phone
Business Start Date
Loan Amount
Loan Use
Monthly Sales Revenue
AcceptRunCreditCheck

## Check for Exiting
We will first check for existing records in our CRM by name, business name, email, and phone number.  




