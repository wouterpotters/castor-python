# castorapi
Python API wrapper for Castor EDC to fetch data from you clinical study.

## Usage
First, make sure that save the client and secret from your Castor account in 
seperate *client* and *secret* files (without line endings) in a private 
folder on your PC. Do not share these files with anyone.    

See also https://data.castoredc.com/api and https://helpdesk.castoredc.com/article/124-application-programming-interface-api

## Example code
    import castorapi
    c = CastorApi("/path/to/folder/with/secret_client")
    c.select_study_by_name("<castor_name_of_your_study>")
    
    # export data - fast method
    data = c.request_study_export_data() 
    
    # export data - slow method, but required if you have many records
    # or if you get a error 500 
    data = c.records_reports_all()

## NOTE
I am not affiliated with Castor EDC in any way. Use this software at your own risk.

## TODO
- implement POST endpoints of the api
- implement PATCH endpoints of the api