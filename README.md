# CMPG-323-Project-2---33526966
This a CRUD RESTful API that will connect to a database storing IoT device data which contains endpoints called over HTTP, invoking application code to update a database. 

## Getting Started
This CRUD RESTFUL API is hosted on [Azure](https://azure.com). If you have access to the API, [click here](https://apiproject2.azurewebsites.net/swagger/index.html). This link should redirect the user to the page shown below:

![first page](https://user-images.githubusercontent.com/81962930/189060433-2b80bb10-3c58-423d-bc56-3a273d9baa49.PNG)

## How to use the API?
This web API has been secured with JWT authentication, therefore the user needs to be registered as an admin to make use of the endpoints within the API. 

### 1. Authenticate
* Firstly, click on "POST (/api/Authenticate/register-admin)" and then click on "try it out".

![try out](https://user-images.githubusercontent.com/81962930/189084375-17fcc5aa-8fcc-4db7-84c1-8b81b3a4564c.PNG)

* Then, you need to enter your credentials. Ensure that the password used is strong (Contains uppercase, lowercase, digits and a character). Then hit "execute".

![execute](https://user-images.githubusercontent.com/81962930/189084740-6a69865c-3a32-4afc-a6af-51702244ebf3.PNG)

* Next, we're required to get a token form the API by logging in. Click "POST (/api/Authenticate/login)" and enter the credentials created on the previous step:

![Login](https://user-images.githubusercontent.com/81962930/189087868-76fa582d-f996-4d0a-97e1-cf83b17bcefa.PNG)

And then hit "excute". You should receive a token down below in the "Response body" section:

![token](https://user-images.githubusercontent.com/81962930/189086634-fe29449c-1e7b-4b24-b43a-e01cc71f57fa.PNG)

We have now created a token from the API which will be used to authorise the user when attempting to use the endpoints. However, this token has a lifetime which it will be valid to be used. After the "expiration" time the user will need to login again. Note that the user need not to re-register - as their credentials are stored in the database.
