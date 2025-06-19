# insightly-demo
public data files

## Description of routes and roles for accessing these. 


| Routes  				| Protected 	|	Roles 							|
|--						|--				|--									|
| / 					| partial 		| all 								|
|/authorize/*			|		yes		|	creator 						|	
|/profiles				|		partial	|	all 							|		
|/profiles/profileid	|		partial	|	creator, client, admin, staff 	|	
|/login					|		no  	|	all 							|	
|/signup				|		no		|	all 							|
|/cookie-information	|		no		|	all 							|
|/terms-of-service		|		no		|	all 							|
|/privacy-policy		|		no		|	all 							|
													

### Roles

**visitor**:	
 - reads unprotected routes
 - reads public parts of protected routes
 - can apply to sign up

**creator**: 	
 - creates and uses account 
 - shares their platform data with the insightly app
 - selects what to share with whom
 - reads all of own data
 - reads public parts of any creator 


**client**:	
 - creates and uses account
 - reads public parts of any creator
 - requests access to protected creator data

			
**admin**: 	

 - uses account
 - handles all other accounts, ie Creates, Reads, Updates, Deletes (CRUD)
 - reads all routes
 - can act in other roles (for test purposes)
 - cannot act as other user

**staff**:	

 - accepts/rejects accounts
 - reads public parts of protected routes
