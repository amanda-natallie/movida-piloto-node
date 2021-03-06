# Node.js Launcher Code Examples
This GitHub repo includes code example for both the DocuSign eSignature REST API as well as the DocuSign Rooms API. To use the Rooms API code example, modify the **exampleAPI** settings at the end of the appsettings.json file from eSignature to rooms.

**Note:** to use the Rooms API you must also [create your DocuSign Developer Account for Rooms](https://developers.docusign.com/docs/rooms-api/rooms101/create-account). 

### Github repo: [code-examples-node](../../)
## Introduction
This repo is a Node.js application that demonstrates:

## eSignature API

1. **Embedded Signing Ceremony.**
   [Source.](./eg001EmbeddedSigning.js)
   This example sends an envelope, and then uses an embedded signing ceremony for the first signer.
   With embedded signing, the DocuSign signing ceremony is initiated from your website.
1. **Send an envelope with a remote (email) signer and cc recipient.**
   [Source.](./lib/eSignature/eg002SigningViaEmail.js)
   The envelope includes a pdf, Word, and HTML document.
   Anchor text ([AutoPlace](https://support.docusign.com/en/guides/AutoPlace-New-DocuSign-Experience)) is used to position the signing fields in the documents.
1. **List envelopes in the user's account.**
   [Source.](./lib/eSignature/eg003ListEnvelopes.js)
1. **Get an envelope's basic information.**
   [Source.](./lib/eSignature/eg004EnvelopeInfo.js)
   The example lists the basic information about an envelope, including its overall status.
1. **List an envelope's recipients** 
   [Source.](./lib/eSignature/eg005EnvelopeRecipients.js)
   Includes current recipient status.
1. **List an envelope's documents.**
   [Source.](./lib/eSignature/eg006EnvelopeDocs.js)
1. **Download an envelope's documents.** 
   [Source.](./lib/eSignature/eg007EnvelopeGetDoc.js)
   The example can download individual
   documents, the documents concatenated together, or a zip file of the documents.
1. **Programmatically create a template.**
   [Source.](./lib/eSignature/eg008CreateTemplate.js)
1. **Send an envelope using a template.**
   [Source.](./lib/eSignature/eg009UseTemplate.js)
1. **Send an envelope and upload its documents with multpart binary transfer.**
   [Source.](./lib/eSignature/eg010SendBinaryDocs.js)
   Binary transfer is 33% more efficient than using Base64 encoding.
1. **Embedded sending.**
   [Source.](./lib/eSignature/eg011EmbeddedSending.js)
   Embeds the DocuSign web tool (NDSE) in your web app to finalize or update 
   the envelope and documents before they are sent.
1. **Embedded DocuSign web tool (NDSE).**
   [Source.](./lib/eSignature/eg012EmbeddedConsole.js)
1. **Embedded Signing Ceremony from a template with an added document.**
   [Source.](./lib/eSignature/eg013AddDocToTemplate.js)
   This example sends an envelope based on a template.
   In addition to the template's document(s), the example adds an
   additional document to the envelope by using the
   [Composite Templates](https://developers.docusign.com/esign-rest-api/guides/features/templates#composite-templates)
   feature.
1. **Payments example: an order form, with online payment by credit card.**
   [Source.](./lib/eSignature/eg014CollectPayment.js)
1. **Get the envelope tab data.**
   Retrieve the tab (field) values for all of the envelope's recipients.
   [Source.](./lib/eSignature/eg015EnvelopeTabData.js)
1. **Set envelope tab values.**
   The example creates an envelope and sets the initial values for its tabs (fields). Some of the tabs
   are set to be read-only, others can be updated by the recipient. The example also stores
   metadata with the envelope.
   [Source.](./lib/eSignature/eg016SetTabValues.js)
1. **Set template tab values.**
   The example creates an envelope using a template and sets the initial values for its tabs (fields).
   The example also stores metadata with the envelope.
   [Source.](./lib/eSignature/eg017SetTemplateTabValues.js)
1. **Get the envelope custom field data (metadata).**
   The example retrieves the custom metadata (custom data fields) stored with the envelope.
   [Source.](./lib/eSignature/eg018EnvelopeCustomFieldData.js)
1. **Requiring an Access Code for a Recipient**
   [Source.](./lib/eSignature/eg019AccessCodeAuthentication.js)
   This example sends and envelope that requires an access-code for the purpose of multi-factor authentication.
1. **Requiring SMS authentication for a recipient**
   [Source.](./lib/eSignature/eg020SmsAuthentication.js)
   This example sends and envelope that requires entering in a six digit code from an text message for the purpose of multi-factor authentication.
1. **Requiring Phone authentication for a recipient**
   [Source.](./lib/eSignature/eg021PhoneAuthentication.js)
   This example sends and envelope that requires entering in a voice-based response code for the purpose of multi-factor authentication.
1. **Requiring Knowledge-Based Authentication (KBA) for a Recipient**
   [Source.](./lib/eSignature/eg022KbaAuthentication.js)
   This example sends and envelope that requires passing a Public records check to validate identity for the purpose of multi-factor authentication.
1. **Requiring ID Verification (IDV) for a recipient**
   [Source.](./lib/eSignature/eg023IdvAuthentication.js)
   This example sends and envelope that requires the recipient to upload a government issued id.    
1. **Creating a permission profile**
   [Source.](./lib/eSignature/eg024CreatePermission.js)
   This code example demonstrates how to create a permission profile using the [Create Permission Profile](https://developers.docusign.com/esign-rest-api/reference/Accounts/AccountPermissionProfiles/create) method.
1. **Setting a permission profile**
   [Source.](./lib/eSignature/eg025PermissionSetUserGroup.js)
   This code example demonstrates how to set a user group's permission profile using the [Update Group](https://developers.docusign.com/esign-rest-api/reference/UserGroups/Groups/update) method. 
   You must have already created permissions profile and group of users.
1. **Updating individual permission settings**
   [Source.](./lib/eSignature/eg026PermissionChangeSingleSetting.js)
   This code example demonstrates how to edit individual permission settings on a permissions profile using the [Update Permission Profile](https://developers.docusign.com/esign-rest-api/reference/Accounts/AccountPermissionProfiles/update) method.
1. **Deleting a permission profile**
   [Source.](./lib/eSignature/eg027DeletePermission.js)
   This code example demonstrates how to delete a permission profile using the [Delete Permission Profile](https://developers.docusign.com/esign-rest-api/reference/Accounts/AccountPermissionProfiles/create) method.
1. **Creating a brand**
   [Source.](./lib/eSignature/eg028CreateBrand.js)
   This example creates brand profile for an account using the [Create Brand](https://developers.docusign.com/esign-rest-api/reference/Accounts/AccountBrands/create) method.
1. **Applying a brand to an envelope**
   [Source.](./lib/eSignature/eg029ApplyBrandToEnvelope.js)
   This code example demonstrates how to apply a brand you've created to an envelope using the [Create Envelope](https://developers.docusign.com/esign-rest-api/reference/Envelopes/Envelopes/create) method. 
   First, creates the envelope and then applies brand to it.
   Anchor text ([AutoPlace](https://support.docusign.com/en/guides/AutoPlace-New-DocuSign-Experience)) is used to position the signing fields in the documents.
1. **Applying a brand to a template**
   [Source.](./lib/eSignature/eg030ApplyBrandToTemplate.js)
   This code example demonstrates how to apply a brand you've created to a template using using the [Create Envelope](https://developers.docusign.com/esign-rest-api/reference/Envelopes/Envelopes/create) method. 
   You must have at least one created template and brand.
   Anchor text ([AutoPlace](https://support.docusign.com/en/guides/AutoPlace-New-DocuSign-Experience)) is used to position the signing fields in the documents.
1. **Bulk sending envelopes to multiple recipients**
   [Source.](./lib/eSignature/eg031BulkSendEnvelopes.js)
   This code example demonstrates how to send envelopes in bulk to multiple recipients using these methods:
   [Create Bulk Send List](https://developers.docusign.com/esign-rest-api/reference/BulkEnvelopes/BulkSend/createBulkSendList), 
   [Create Bulk Send Request](https://developers.docusign.com/esign-rest-api/reference/BulkEnvelopes/BulkSend/createBulkSendRequest).
   Firstly, creates a bulk send recipients list, and then creates an envelope. 
   After that, initiates bulk envelope sending.

## Rooms API 
**Note:** to use the Rooms API you must also [create your DocuSign Developer Account for Rooms](https://developers.docusign.com/docs/rooms-api/rooms101/create-account). 


1. **Create room with Data.**
   [Source.](./lib/rooms/eg001CreateRoomWithData.js)
   This example creates a new room in your DocuSign Rooms account to be used for a transaction.
1. **Create a room from a template.**
   [Source.](./lib/rooms/eg002CreateRoomFromTemplate.js)
   This example creates a new room using a template.
1. **Create room with Data.**
   [Source.](./lib/rooms/eg003ExportDataFromRoom.js)
   This example exports all the avialalble data from a specific room in your DocuSign Rooms account.
1. **Add forms to a room.**
   [Source.](./lib/rooms/eg004AddingFormToRoom.js)
   This example adds a standard real estate related form to a specific room in your DocuSign Rooms account.
1. **How to search for rooms with filters.**
   [Source.](./lib/rooms/eg005GetRoomsWithFilters.js)
   This example searches for rooms in your DocuSign Rooms account using a specific filter. 
1. **Create an external form fillable session.**
   [Source.](./lib/rooms/eg006CreateExternalFormFillSession.js)
   This example create an external form that can be filled using DocuSign for a specific room in your DocuSign Rooms account.


## Authentication types:

* Authentication with Docusign via [Authorization Code Grant flow](https://developers.docusign.com/platform/auth/authcode) .
When the token expires, the user is asked to re-authenticate.
The **refresh token** is not used in this example.

* Authentication with DocuSign via the [JSON Web Token (JWT) Grant](https://developers.docusign.com/platform/auth/jwt/).
When the token expires, it updates automatically.

## Installation

### Prerequisites
**Note: If you downloaded this code using Quickstart from the DocuSign Developer Center, skip steps 1 and 2 below as they're automatically performed for you.**

1. A DocuSign Developer Sandbox account (email and password) on [demo.docusign.net](https://demo.docusign.net).
   Create a [free account](https://go.docusign.com/sandbox/productshot/?elqCampaignId=16534).

1. A DocuSign Integration Key (a client ID). To use Authorization code grant, you will need the **Integration Key** itself, and its **secret**. To use JSON Web token, you will need the **Integration Key** itself, the **RSA Secret Key** and an API user ID for the user you are impersonating.  

   If you use this example on your own workstation,
   the Integration key must include a **Redirect URI** of `http://localhost:5000/ds/callback`

   If you will not be running the example on your own workstation,
   use the appropriate DNS name and port instead of `localhost`

1. Node.JS v8.10 or later and NPM v5 or later.
1. A name and email for a signer, and a name and email for a cc recipient.
   The signer and the cc email cannot be the same.

### Installation steps
1. Download or clone this repository to your workstation to directory **code-examples-node**
1. **cd code-examples-node**
1. **npm install**   
**Note: If you downloaded this code using Quickstart from the DocuSign Developer Center, skip steps 4 and 5 below as they're automatically performed for you.**

1. Copy the file **config/appsettings.example.json** into a file **config/appsettings.json** 
1. *Either:*

   * Update the file **config/appsettings.json** in the project's root directory
     with the Integration Key
     and other settings, *or*
   * Create and export environment variables for the settings.
     See the **config/appsettings.json** file
     for the names of the environment variables.

   **Note:** Protect your Integration Key and secret--If you update
   the config/appsettings.json file, then you
   should ensure that it will not be stored in your source code
   repository.

1. **npm start**
1. Open a browser to **http://localhost:5000**

### Configuring JWT

1. Create a developer sandbox account on developers.docusign.com if you don't already have one.
2. Create a new API key in the Admin panel: https://admindemo.docusign.com/api-integrator-key, take note of the public key.
3. Set a redirect URI of `http://localhost:5000/ds/callback` as mentioned in the installation steps above for the API key you make in step 2.
4. Generate an RSA keypair in the administrator console on the DocuSign developer sandbox and copy the private key to a secure location.
5. Create a new file in your repo source folder named **private.key**, and paste in that copied RSA private key, then save it.
6. Update the file **config/appsettings.json** and include the newly created API key from step 2 as well as your account user id GUID which is also found on the Admin panel: `https://admindemo.docusign.com/api-integrator-key`.

From there you should be able to run the launcher using **npm start** then selecting **JSON Web Token** when authenticaing your account.


#### Payments code example
To use the payments example, create a 
test payments gateway for your developer sandbox account. 

See the 
[PAYMENTS_INSTALLATION.md](./code-examples-node/blob/master/PAYMENTS_INSTALLATION.md)
file for instructions.
   
Then add the payment gateway account id to the **config/appsettings.json** file.

## Using the examples with other authentication flows

The examples in this repository can also be used with either the
Implicit Grant or JWT OAuth flows.
See the [Authentication guide](https://developers.docusign.com/esign-rest-api/guides/authentication)
for information on choosing the right authentication flow for your application.

## License and additional information

### License
This repository uses the MIT License. See the LICENSE file for more information.

### Pull Requests
Pull requests are welcomed. Pull requests will only be considered if their content
uses the MIT License.
