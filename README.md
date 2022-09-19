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

### 2. Authorize
* One last step before we can access and make use of the endpoints is to authorize using the token created. Click on "Authorize".

![authorize](https://user-images.githubusercontent.com/81962930/189092651-7ff63cc5-3bf1-4dca-899d-56e5abe68b3b.PNG)

* Then a prompt to enter the token will appear. To enter the token - the user should type in "Bearer" then space and then paste the copied token and hit "Authorize".

![authorizing](https://user-images.githubusercontent.com/81962930/189093041-b45fe5a5-8d29-4014-b6d1-8415c6294cdc.PNG)

* Notice the endpoints have unlocked and can be used.

## Endpoints available in the API
The following section lists the endpoints that are available in the API. 

### 1. Category Endpoints:
* The first GET method retrieves all Category entries from the database.
* The second GET method retrieves one Category from the database based on the ID parsed through.
* The POST method creates a new Category entry on the database.
* The DELETE method deletes an existing Category entry on the database.

![unlockedEndpoints](https://user-images.githubusercontent.com/81962930/189093311-d487b04c-8ff6-4a59-a684-a3f78f023af9.PNG)

### 2. Devices Endpoints:
* The first GET method retrieves all Devices entries from the database.
* The second GET method retrieves one Devices from the database based on the ID parsed through.
* The POST method creates a new Devices entry on the database.
* The DELETE method deletes an existing Devices entry on the database.

![devices](https://user-images.githubusercontent.com/81962930/189098624-45a682da-4f28-4eaa-a449-5a1a374e57c6.PNG)

### 3. Zones Endpoints:
* The first GET method retrieves all Zones entries from the database
* The second GET method retrieves one Zones from the database based on the ID parsed through.
* The POST method creates a new Zones entry on the database.
* The DELETE method deletes an existing Zones entry on the database.

![zones](https://user-images.githubusercontent.com/81962930/189098559-a276f247-a22d-4ab7-b6d0-89b96fa86864.PNG)

## API Manager EndPoints

![endpoints1](https://user-images.githubusercontent.com/81962930/189645707-28146317-bb1e-4bdf-9c8a-3507c678b0d3.PNG)

![endpoints2](https://user-images.githubusercontent.com/81962930/189645761-6e178549-68ac-4b72-99f5-9b70b53ed058.PNG)

![endpoints 3](https://user-images.githubusercontent.com/81962930/189645845-1c648a9e-ef9d-4f29-a39d-bc71ebd16057.PNG)
