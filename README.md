# Lightning-API-Callout

Authorize the endpoint URL For Apex Callout.
For Authorize the endpoint URL -: http://data.fixer.io

<h2>How to:</h2>
From Setup, enter Remote Site Settings in the Quick Find box
Click on the Remote Site Settings.
Click New Remote Site.
For the remote site name, enter foreign_exchange_rates .
For the remote site URL, enter http://data.fixer.io  ,This URL authorizes all subfolders for the endpoint, like http://api.fixer.io/latest
Make sure your Active checkbox is Equal to True.
Click Save.

<h2>Summary</h2>
In apex class controller we have a getCalloutResponseContents @AuraEnabled class method with one parameter url as string type. 
The Return type is Map type where String is key and object as value of the Map.
In getCalloutResponseContents Method ,first we created a new HTTP object. and set the EndPoint url with url parameter.
In the url parameter we set url from lightning component js controller.
and when the HttpResponse come from callout, Deserialize the JSON string into the Map collection and return the map.
