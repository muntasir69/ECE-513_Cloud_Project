ECE513 Project (Server Side) - Team 4
======

The following is the server-side code for the ECE513 project. This project focuses on developing a cloud-based heart rate monitoring system tailored for both patients and physicians. It enables patients to effortlessly configure their devices for seamless data upload to the server. Additionally, physicians can conveniently review the generated reports, enhancing the overall monitoring and management of patient health.

**Team members:**

- Md Muhtasim Alam Chowdhury
- Chris Mastrangelo
- Muntasir Mamun

Videos:
---------
Pitch Video: [(https://youtu.be/pKrdHhLNEM4)]
User Experience and Code Implements:[https://youtu.be/-8ff1xErOiU]

Let's Get Started
---------
Using node.js to run the server
```
node app.js
```
If the event is successful then it will run the server, you will see the "Listening on port: 3000" message.  
Then anyone can check the application on their web browser using http://localhost:3000

Require Modules
----------

| Module | Description |
| ------ | ----------- |
| [Exrpress](https://expressjs.com/) | Web application framework |
| [mongoose](https://mongoosejs.com/) | MongoDB object modeling for node.js |
| [moment](https://momentjs.com/) | Parse, validate, manipulate, and display dates and times in JavaScript. |
| [http-errors](https://www.npmjs.com/package/http-errors) | Create HTTP errors |
| [cookie-parser](https://www.npmjs.com/package/cookie-parser) | Parse Cookie header and populate req.cookies with an object keyed by the cookie names. |
| [morgan](https://www.npmjs.com/package/morgan) | HTTP request logger middleware for node.js |
| [body-parser](https://www.npmjs.com/package/body-parser) | Node.js body parsing middleware. |

APIs
----------

- Data API – Route: /api/\*

|APIs|Description|HTTP Method|
| :- | :-        | :-        |
|readAll|Read out all sensor data|GET|
|read\_patient\_data|Return all data from a patient|POST|
|weekly\_patient\_data|Return one week data from a patient|POST|
|Daily\_patient\_data|Return one day data from a patient|POST|
|Particle\_data|For receive data from Particle webhook|POST|

- Patient API – Route: /patient/\*

|APIs|Description|HTTP Method|
| :- | :-        | :-        |
|create|Sing up a patient|POST|
|logIn|Log in to a patinet|POST|
|status|For check the authorization|GET|
|update\_device|Update a device name and device SN|POST|
|update\_info|Update the user info|POST|

- Physician API – Route: /patient/\*

|APIs|Description|HTTP Method|
| :- | :-        | :-        |
|create|Sing up a physician|POST|
|logIn|Log in to a physician|POST|
|status|For check the authorization|GET|
|read\_all\_patient|Return all patient name and ID|GET|
|update\_info|Update the user info|POST|
