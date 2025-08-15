## Burp Intruder 
<!-- Highlight the section you want to inject some potential parameters into and send it to intruder with a list of payloads -->




Capture an interesting endpoint that contains personal identifiable sensitive data, 

	ex. GET /api/users/{id} , GET /api/account/profile , GET /api/orders/{orderID} 


Target the parameter you want to test and highlight it, right click and send it to intruder. 

Notice intruder automatically adds the targeting symbols around your parameter, now simply go into payloads, create a list of potential testing points for your request, example : 

	ex. GET /api/account/profile/?$isAdmin$=true

The payloads I’d create for this endpoint would look like { 

	accessLevel 
	admin
	administrator
	Admin
	Administrator 
} 

This is an example of using intruder to automate testing for request endpoints, you can use intruder to automate the testing for multiple different scenario’s including : 

JSON Tampering : 
- Injecting different JSON parameters into your request body to try and gain admin access. (Content-type: application/json {“admin”: “true”, “customerId”: “Victim”}) etc… 

Fuzzing : 
- Injecting different parameters into your request URL to try and access another users account, or gain admin access (isAdmin=true, account_id=Victim) etc… 

	GET /api/account/personal/$$ 

	Create a payload for potential endpoints that may exist, /admin /admin/panel /admin/settings, use a common admin wordlist for fuzzing and inject it into intruder, see which requests respond with 200 OK, 404/403. 

Remember that all of this automated testing is very useful for getting a good overview of an applications endpoints, but all vulnerabilities must be manually testing to be confirmed. 

-- 