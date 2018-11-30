# Global





* * *

## Class: contacts


### contacts.add(contact) 

Adds a Contact [BBCore.contact](#bbcore.contact) to Contacts collection

**Parameters**

**contact**: `contact`, Adds a Contact [BBCore.contact](#bbcore.contact) to Contacts collection

**Returns**: `contacts`

### contacts.find(fieldName, value) 

Returns the first matched contact from

**Parameters**

**fieldName**: `string`, Name of the field to search for the value

**value**: `string`, Value to search for in the contacts

**Returns**: `* | BBCore.contact`


## Class: video


### video.add(video) 

Adds a Video to the collection

**Parameters**

**video**: `video`, Adds a Video to the collection

**Returns**: `videos`


## Class: BBCore


**resumeStoredSession**:  , DEPRECATED - Use validateSession
### BBCore.login(uid, pwd, success) 

Authenticates a user using their Email Address (User Id) and Password

**Parameters**

**uid**: `string`, Authenticates a user using their Email Address (User Id) and Password

**pwd**: `string`, Authenticates a user using their Email Address (User Id) and Password

**success**: `responseSuccess`, Authenticates a user using their Email Address (User Id) and Password


### BBCore.credentialsSaved() 

Returns bool for whether or not a prior authentication is stored locally

**Returns**: `boolean`

### BBCore.saveCredentials(uid, pwd) 

Save credentials to local storage (not recommended)

**Parameters**

**uid**: `string`, User ID/Email Address

**pwd**: `string`, Password


### BBCore.validateSession(onSuccess, onError) 

Authenticates from previously stored credentials

**Parameters**

**onSuccess**: `responseSuccess`, Authenticates from previously stored credentials

**onError**: `responseSuccess`, Authenticates from previously stored credentials


### BBCore.validateAccessToken(onSuccess) 

**Parameters**

**onSuccess**: 


### BBCore.isAuthenticated() 

Returns bool for authentication state

**Returns**: `boolean | *`

### BBCore.invalidateSession() 

Invalidates and clears the active session, similar to logout

**Returns**: `boolean | *`

### BBCore.verifyKey(key, complete) 

Validates the given key

**Parameters**

**key**: `string`, Validates the given key

**complete**: `responseSuccess`, Validates the given key


### BBCore.storeKey(key) 

Stores the give session key, typically used so a session can be resumed later on.

**Parameters**

**key**: , Stores the give session key, typically used so a session can be resumed later on.


### BBCore.verifyJsonWebToken(key, complete) 

Validates the given key

**Parameters**

**key**: `string`, Validates the given key

**complete**: `responseSuccess`, Validates the given key


### BBCore.storeOAuthTokens(key) 

Stores the OAuth Token for API calls

**Parameters**

**key**: , Stores the OAuth Token for API calls


### BBCore.getOAuthPayload() 

**Returns**: `string`

### BBCore.validateOAuthCode(authCode, onSuccess, onError) 

**Parameters**

**authCode**: 

**onSuccess**: 

**onError**: 


### BBCore.refreshOAuthToken() 


### BBCore.storeJsonWebToken(key) 

Stores the give session key, typically used so a session can be resumed later on.

**Parameters**

**key**: , Stores the give session key, typically used so a session can be resumed later on.


### BBCore.getValidJsonWebTokenAsync(callback) 

Attempts to always return a valid JWT which makes an async verification request

**Parameters**

**callback**: , handler given a valid JWT.  If the JWT is null then the useris NOT authenticated.


### BBCore.getServerUrl() 

**Returns**: `BBCore.apiServer | * | BBCore.CONFIG.SERVER_API_URL`

### BBCore.getRequestUrl() 

Returns the fully qualified URL for BB API

**Returns**: `string`

### BBCore.sendRequest(method, params, success, error) 

Sends a request to the specified method of the [BombBomb API](//bombbomb.com/api)

**Parameters**

**method**: `string`, The method name to call

**params**: `requestParameters`, The parameters to send with the request

**success**: `responseSuccess`, A callback when the request succeeds

**error**: `responseSuccess`, A callback when the request fails


### BBCore.getLists(success) 

Retrieves Contact Lists

**Parameters**

**success**: `responseSuccess`, Retrieves Contact Lists


### BBCore.createList(listName, success) 

Creates a Contact List and returns the Guid

**Parameters**

**listName**: `string`, Creates a Contact List and returns the Guid

**success**: `responseSuccess`, Creates a Contact List and returns the Guid


### BBCore.getContact(contactId, success) 

Retrieves a Contact

**Parameters**

**contactId**: `string`, Retrieves a Contact

**success**: `responseSuccess`, Retrieves a Contact


### BBCore.getListContacts(listId, success) 

Retrieves Contacts from a Contact List

**Parameters**

**listId**: `string`, Retrieves Contacts from a Contact List

**success**: `responseSuccess`, Retrieves Contacts from a Contact List


### BBCore.addContact(contact, success) 

Adds a Contact to a Contact List

**Parameters**

**contact**: `contact`, Adds a Contact to a Contact List

**success**: `responseSuccess`, Adds a Contact to a Contact List


### BBCore.bulkAddContacts(opts, success) 

Adds a batch of Contacts

**Parameters**

**opts**: `object`, Adds a batch of Contacts

**success**: `responseSuccess`, Adds a batch of Contacts


### BBCore.updateContact(opts, success) 

**Parameters**

**opts**: `object`

**success**: `responseSuccess`


### BBCore.getImportAddressesByType(opts, success) 

Retrieves an Import Address by a Type

**Parameters**

**opts**: , Retrieves an Import Address by a Type

**success**: `responseSuccess`, Retrieves an Import Address by a Type


### BBCore.addContactImportAddress(opts, success) 

Retrieves an Import Address by a Type

**Parameters**

**opts**: `object`, Retrieves an Import Address by a Type

**success**: `responseSuccess`, Retrieves an Import Address by a Type


### BBCore.getClientRecentInteractions(opts, success) 

Retrieves a list of re

**Parameters**

**opts**: `getClientInteractionOptions`, Retrieves a list of re

**success**: `responseSuccess`, Retrieves a list of re


### BBCore.getEmails(success) 

Retrieves a list of Emails from the current authenticated session

**Parameters**

**success**: `responseSuccess`, Retrieves a list of Emails from the current authenticated session


### BBCore.sendCustomVideoEmail(opts, success) 

**Parameters**

**opts**: `customVideoEmailOptions`

**success**: `function`


### BBCore.getDrips(opts, success) 

**Parameters**

**opts**: `object`

**success**: `responseSuccess`


### BBCore.getForms(opts, success) 

**Parameters**

**opts**: `object`

**success**: `responseSuccess`


### BBCore.getClientIntegrations(opts, success) 

**Parameters**

**opts**: 

**success**: 


### BBCore.getEmbeddedRecorderUrl(options, onComplete) 

**Parameters**

**options**: `Object`

**onComplete**: `function`


### BBCore.getVideoRecorder(opts, onComplete) 

**Parameters**

**opts**: `object`

**onComplete**: `function`


### BBCore.saveRecordedVideo(title, videoId, videoFilename, success) 

**Parameters**

**title**: `string`

**videoId**: `string`

**videoFilename**: `string`

**success**: `function`



## Class: videoOptions


**vid_id**: `string` 
### videoOptions.saveRecording(options) 

**Parameters**

**options**: `Object`


### videoOptions.deleteVideo(videoId, success) 

Deletes a Video

**Parameters**

**videoId**: `string`, Deletes a Video

**success**: `responseSuccess`, Deletes a Video


### videoOptions.videoQuickSend(opts, onSuccess) 

**Parameters**

**opts**: `object`

**onSuccess**: `responseSuccess`


### videoOptions.responseSuccess(responseObject, jqXHR) 

reponseSuccess

**Parameters**

**responseObject**: , reponseSuccess

**jqXHR**: , reponseSuccess




# BBCore





* * *

## Class: contact
Contact Object

**email**: `string` , Email Address
**firstname**: `string` , First Name
**lastname**: `string` , Last Name
**phone_number**: `string` , Phone Number
**address_line_1**: `string` , Address 1
**address_line_2**: `string` , Address 2
**city**: `string` , City
**state**: `string` , State
**country**: `string` , Country`
**postal_code**: `string` , Postal Code
**company**: `string` , Company
**position**: `string` , Position
**comments**: `string` , Comments
**listlist**: `string` , Array of List Ids the Contact is subscribed to
**id**: `string` , Contact Id

## Class: video


**vid_id**: `string` 
**title**: `string` 
**filename**: `string` 


* * *










