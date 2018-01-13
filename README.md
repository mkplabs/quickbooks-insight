# quickbooks-insight
Developer Docs for the Quickbooks Insight AppExchange Application

# Post Installation Instructions
**Authentication**
- Click on Setup | Named Credentials
- Edit the Quickbooks Insight Named Credential
- Click Save, you will be prompted to authenticate into Quickbooks

**Adding the component to a Lightning Page**
- While on a Page, click the Gear at the top, then Edit Page
- Drag the lightning component to the desired spot on the page
- Modify the properties on the component
- Specify the correct Quickbooks Object
- Enter a comma separated string of Quickbooks Object Fields you want displayed

# API Usage
You can interact directly with Quickbooks via the API class
```sh
Map<String,Object> res = QBI.API.retrieveRecord(String objectName, String qbId);
Map<String,Object> res = createRecord(String resourceName, Map<String,Object> record);
Map<String,Object> res = updateRecord(String resourceName, Map<String,Object> record, Boolean sparse);
Map<String,Object> res = queryRecords(String queryString);
```
Object Definitions can be found at [https://developer.intuit.com/docs/api/accounting](https://developer.intuit.com/docs/api/accounting)

# Release Notes
1.2 : 2018-01-12
- Fix: Updated URL for Logo

1.1 : 2017-09-08
- Enhancement: Added public API methods

1.0 : 2017-09-01
- Enhancment: Lightning Component to view QB data
