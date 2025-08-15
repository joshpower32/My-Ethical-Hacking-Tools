## Autorize 
<!-- Copy the Victims Injected URL/JSON Parameter and put it into Autorize, Then Perform Requests with Attacker and compare results. -->


- Intercept requests from Repeater 

// Every time you use repeater it will send the request with authorize swell and insert whatever you’ve given it into the request and display the results. 


- Cookie: Insert=injected; cookie=or; 
Header: here 

// “Victims Cookie or JSON”, perform crud functions in your attacker account, and authorize will take your Attacker request’s “Original” and modify whatever Victim cookie or JSON parameters you want to inject from the Victim into the Attackers request and see the result 200 OK (potential IDOR), 404/403 (SECURE). 

This automated testing is only for checking potential weak endpoints, all Cookie/JSON testing must be manually verified. 


- Replace query params

// If you want to inject parameters into requests and see the result, Take Victim A’s parameter values or ID’s (customer_Id, user_id, account_id, etc… ) and then perform requests in your Attackers account and Authorize will inject the Victims parameters into your Attackers requests and display the results. 

This automated testing is only for checking potential weak endpoints, all Parameter testing must be manually verified. 

-- 