# Mohd-Farid-bin-Johari
An API Key is used by the Campus API Gateway to authenticate a calling application and determine the permissions/access that application has to the APIs. The API Key (known as the Consumer Key in the Developer Portal) must passed as a header on every request, even on the requests which have no security limitations.

Security Overview Diagram

Where To Get It
You can find you API Key (Consumer Key) by following the instructions from the Creating Your First App example in the Getting Started guide.

Consumer Key

Usage
Every API Call requires that an ucsb-api-key header be included which contains your API Key.

Using the example Employees - Employee Map API, click on the Authorize button:

accessing the employee map API

Enter ucsb-api-key as the name and insert your app Consumer Key from your My First App page as the value and then click Authorize.

entering your consumer Key

Next, fill in the id value (example: 800000000) as required by the UCPath Employee Map API documentation. Finally, let's click on Send this request to perform the network request. If all went well and the id is valid, you should see a response from the UCPath Employee Map API like this:

[
  {
    "InputId": "800000000",
    "OutputId": "60000000",
    "errorMsg": {
      "Success": true,
      "Message": "Match found for this ID"
    }
  }
]
Note: The above response is fictitious because there isn't a valid crosswalk between 800000000 (ppsId) to 60000000 (ucpathId).

Note: If your API key is invalid or if you've entered it incorrectly, you'll see an error like this:

{
  "fault": {
    "faultstring": "Invalid ApiKey for given resource",
    "detail": {
      "errorcode": "oauth.v2.InvalidApiKeyForGivenResource"
    }
  }
}
