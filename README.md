# API Testing

Below are some test cases on https://petstore.swagger.io/v2 that I did for API Testing + screenshots from Postman

----------------------------

**Title:** Open an API on Postman website

**Description:** 
Test how an API is opened to be created/updated/deleted

** Steps to Reproduce:** 

1. Go to https://www.postman.com/
2. Log in with your credentials
3. Click on "Workspaces"
4. Click on "My Workspace"
5. Hit the "New" button 
6. Select "HTTP" request

**Expected results:** A new API is open to be created/updated/deleted

**Environment:** Safari

----------------------------
###### POST

**Title:** 
Create an API

**Description:** 
Add a new pet to the store (using Swagger website)

**Preconditions:** 
Open the Postman website: https://www.postman.com/ and log in with your credentials

**Steps to Reproduce:** 

1. Click on "Workspaces", then ""My Workspace"
2. Hit the "New" button 
3. Select "HTTP" request
4. Select "POST" from droplist
5. Copy base URL from Swagger website "petstore.swagger.io/v2"
6. Insert "https://" + paste "petstore.swagger.io/v2" in URL textbox
7. Add "/pet" after the new created URL "https://petstore.swagger.io/v2"
8. Click on "Body"
9. Select "raw" option
10. Select "JSON" from the blue droplist
11. Go to https://petstore.swagger.io/#/pet/addPet
12. Click on the second "POST" button from the pet section
13. Copy required body object from the black textbox
14. Paste on Postman the copied text in cell 1
15. Complete the textbox with details: id, name, status for the new pet
16. Hit the "Send" button

**Expected results:** 
The new pet has been successfully added with Status: 200 OK and all the details are displayed in the Body textbox.

**Test data:** 
id: 9910 & name: "Blue"

**Environment:** 
Safari

![Add a new pet : API](https://user-images.githubusercontent.com/113981640/222540779-9fe7bc24-81cb-4e3c-8a88-6441571a1671.png)

-------------------------------

###### PUT

**Title:**
Update an API

**Description:** 
Update an existing pet

**Preconditions:** 
Open the Postman website:https://www.postman.com/ and log in with your credentials

**Steps to Reproduce:** 

1. Open a new API: Workspaces/My Workspaces/ New/ Select "HTTP" request
2. Select "PUT" from droplist
3. Add https://petstore.swagger.io/v2/pet into requested URL textbox
4. Go to https://petstore.swagger.io/#/pet/updatePet and copy the required body
5. Paste it on Postman in Body/raw/json/cell 1
6. Update the "name" with "Blue Husky", id remain "9910"
7. Hit the "Send" button

**Expected results:** The new pet has been successfully updated and all the details are displayed into the Body textbox

**Environment:** Safari

![Update an API](https://user-images.githubusercontent.com/113981640/222541527-ed9b7e39-844f-43a7-a246-1ba8b439d278.png)

--------------------------------

###### GET

**Title:**
Find an API

**Description:** 
Find a pet by ID after the pet has been created 

**Preconditions:** 
Open the Postman website version: https://www.postman.com/ and log in with your credentials

**Steps to Reproduce:** 

1. Open a new API: Workspaces/My Workspaces/ New/ Select "HTTP" request
2. Select "GET" from droplist
3. Insert the POST URL created before for a new pet / https://petstore.swagger.io/v2/pet
4. According to the Swagger documentation add the petID at the end of the link: "/9910"
5. Click on "Send" button

**Expected results:** 
All the details about the pet are displayed

**Environment:** 
Safari

![Find a pet](https://user-images.githubusercontent.com/113981640/222542172-09d6f611-62a1-462d-8e48-9761a9ebe8a7.png)

----------------------------------

###### DELETE

**Title:**
Delete an existing API

**Description:** 
Delete a pet (already created and updated)

**Preconditions:** 
Open the Postman website version: https://www.postman.com/ and log in with your credentials

**Steps to Reproduce:

1. Open a new API: Workspaces/My Workspaces/ New/ Select "HTTP" request
2. Select "DELETE" from droplist
3. According to the documentation in this link: https://petstore.swagger.io/#/pet/deletePet add the id "9910" at the end of the copied URL https://petstore.swagger.io/v2/pet/
4. Click on the "Send" button

**Expected results:** 
The pet with id 1 was deleted and all the information has been erased. 

**Environment:** 
Safari

![Delete a pet](https://user-images.githubusercontent.com/113981640/222542910-d538530d-9213-4ad4-b0d1-5237668ef8a4.png)

![Delete a pet](https://user-images.githubusercontent.com/113981640/222542947-a65a4b89-d96c-4418-8ab4-9194ab1a0952.png)


------------------------------

**Title:**
Test if "DELETE" Request is working properly on Postman

**Description:** 
The user check if the existing API has been successfully deleted

**Preconditions:** 
Open the Postman website version: https://www.postman.com/ and log in with your credentials

**Steps to Reproduce:**

1. Open a new API: Workspaces/My Workspaces/ New/ Select "HTTP" request
2. Insert https://petstore.swagger.io/v2/pet/1 into the requested URL
3. Select "GET" from the droplist
4. Hit the "Send" button

**Expected results:** 
The message "Pet not found" with status 404 is displayed in the Body textbox

**Environment:** 
Google Chrome

![Delete functionality](https://user-images.githubusercontent.com/113981640/222542967-cf1eed88-7c3c-4c8a-92c2-692ddc134632.png)
