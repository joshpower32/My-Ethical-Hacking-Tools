## Param Miner
<!-- Capture an endpoint that returns personal identifiable sensitive data.
Right click the request, go to “Extentions”, “Param Miner”, and then select the type of input/parameter you’d like to test for hidden inputs.  -->



If you selected “Guess Everything” on the “Attack Config” popup you’ll need to click “ok” a few times to close the popup. 

Param Miner will send a series of requests to the target, which you can see if the “Logger” tab, to see the results of the test select “Extensions” tab, go to “Param Miner” and check the “Output” section, this tab displays a log of the param miner’s targets run, including any hidden inputs identified in the request ex : 

	Completed 1/4 
	Identified parameter on example.com: category
	Identified parameter on example.com: x-original-url 
	Identified parameter on example.com: origin 
	Identified parameter on example.com: account_id

	Completed 4/4 

This allows you too test an endpoint for hidden inputs.  

-- 