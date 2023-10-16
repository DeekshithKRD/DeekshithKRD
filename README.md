To perform the equivalent requests in Postman, you can follow these steps:

1. **Install Postman**: If you don't already have Postman installed, download and install it from the [official website](https://www.postman.com/).

2. **Create a New Request**:

    a. Open Postman.

    b. Click the "New" button to create a new request.

3. **Setting the Request Method**:

    a. In the request tab, select the HTTP method as "POST."

4. **Setting the Request URL**:

    a. In the URL field, enter the URL for the first request: `https://app.processunity.net/token`.

5. **Setting Headers**:

    a. Click the "Headers" tab.

    b. Add the headers to the request:

       - Key: `Host`, Value: `app.process`
       - Key: `Content-Type`, Value: `application/x-www-form-urlencoded`

6. **Setting Request Body**:

    a. Click on the "Body" tab.

    b. Select the "x-www-form-urlencoded" option for the request body.

    c. Add the key-value pairs for your payload. For example, you can add the following key-value pairs:

       - Key: `grant_type`, Value: `password`
       - Key: `username`, Value: `directwebservice`
       - Key: `password`, Value: `YourPasswordHere` (replace with the actual password)
       - Key: `processunityUserName`, Value: `Pro_inter`
       - Key: `processunityPassword`, Value: `YourPasswordHere` (replace with the actual password)

7. **Handling Proxies (if required)**:

    a. If you need to configure proxies as in your original code, you can set them up in Postman.

    b. In the Postman app, go to File > Settings > Proxy and configure your proxy settings there.

8. **Sending the Request**:

    a. Click the "Send" button to send the POST request.

    b. You will receive a response in the lower part of the Postman window.

9. **Extracting the Access Token**:

    a. You can extract the "access_token" from the response body and use it for the next request.

10. **Creating the Second Request**:

    a. Click the "New" button again to create a new request.

    b. Set the request method to "POST."

    c. In the URL field, enter the URL for the second request, e.g., `https://app.processunity.net/api/importexport/Export/7653457`.

    d. In the "Headers" tab, set the "Host" and "Content-Type" headers as in your original code.

    e. In the "Authorization" header, use the "Bearer" token you extracted from the first request:

       - Key: `Authorization`, Value: `Bearer YourAccessTokenHere` (replace with the actual access token)

    f. Click the "Send" button to send the second request.

    g. You will receive the response, and you can view the "Data" in the response body.

These steps should allow you to replicate the two POST requests in Postman. Make sure to configure the request headers, body, and tokens according to your specific requirements.
