<h1>Generating OAuth Access token for Safaricom’s Daraja platform</h1>

First  [create an app at Safaricom Devs](https://developer.safaricom.co.ke/user/915/apps/add)

Click on the app you just created to get consumer key and consumer secret. You will need them when generating Basic Auth string.
![where to find keys](https://github.com/kmacharia/darajaaccesstoken/blob/master/consumer-and-secret-keys.png)

The Basic Auth string is a base64 encoded string of your app’s consumer key and consumer secret. You can generate base64 encoded string at https://www.base64encode.org/ by concatenating your ConsumerKey, full colon and ConsumerSecret.

Once you have Auth string, make a GET request to:

`https://sandbox.safaricom.co.ke/oauth/v1/generate?grant_type=client_credentials`

![sample access token request](https://github.com/kmacharia/darajaaccesstoken/blob/master/generate-access-token-request.png)
