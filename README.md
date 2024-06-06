# Travel Management
The travel management app provides users with a streamlined platform to manage their travel plans efficiently.
All data is stored in MongoDB, with a React Native front end and a Python Flask back end.

Author: Yu-Wei Wu
Update: June 6, 2024

## Target Audience
Individuals and families seeking a convenient and efficient solution for planning and organizing travel arrangements.

## Current Features
- User Registration: Simple sign-up process to create an account.
- Log In/Log Out: Secure authentication for accessing personalized travel plans.
- Create Travel Plan: Users can create detailed travel plans.
- Edit Travel Plan: Modify existing travel plans to accommodate changes.
- Delete Travel Plan: Remove outdated or unwanted travel itineraries.

## Potential Features
- Expense Tracking: Effortlessly monitor and manage travel-related expenses, helping users stay within budget during their trips.
- Plan Sharing: Share travel plans with family members or friends, facilitating coordination and collaboration on trip details.
- Photo Album: Create and maintain a digital photo album within the app, capturing and preserving memories from each trip for future enjoyment.
- Travel Journal: Document and share travel experiences through a built-in journal feature, enabling users to reflect on their adventures and share their stories with others.
- Weather Forecast: Check the weather forecast for the travel destination, helping users pack appropriately and plan activities accordingly.

# Screenshots
## Log in process
![1717620361022](https://github.com/yuwei-3206/Travel-mng/assets/122844465/89274399-4770-4acf-9bc4-0f91717b09b1)


## Register Account
Before register, the database only has 1 user
![1717620520681](https://github.com/yuwei-3206/Travel-mng/assets/122844465/64c4e1c2-43ef-4c66-8cbf-ff9519104c68)

## Error Handling
![1717620644509](https://github.com/yuwei-3206/Travel-mng/assets/122844465/54685332-5321-4295-b2a1-f897fa7d02d4)
![1717620744808](https://github.com/yuwei-3206/Travel-mng/assets/122844465/9965df4e-c11d-42ac-876a-89d596c928cc)

## Create travel plan
![1717620777808](https://github.com/yuwei-3206/Travel-mng/assets/122844465/8af153f3-1cfa-4db8-a100-c7136ae73532)
![1717620795701](https://github.com/yuwei-3206/Travel-mng/assets/122844465/116d3c71-019d-4f5c-a59c-3cab99edd83f)
![1717620843695](https://github.com/yuwei-3206/Travel-mng/assets/122844465/37d71664-8588-40e1-94c4-3de34521f04e)

# API
There are two blueprints: users and travel_plans. Users has 3 routes, while travel_plans has 4 routes. Below are examples of 2 routes.

### User Register
Endpoint: users/register<br>
Method: POST<br>
Parameters:<br>
firstName (string): First name of the user.<br>
lastName (string): Last name of the user.<br>
username (string): Username of the user.<br>
password (string): Password of the user.<br>
Example Request Body: {<br>
  "firstName": "John",<br>
  "lastName": "Doe",<br>
  "username": "johndoe@example.com",<br>
  "password": "password123"<br>
}<br>
Server Response (Example): {"message": "User registered successfully. You can now login."}<br>
![1717620676681](https://github.com/yuwei-3206/Travel-mng/assets/122844465/f37c297d-9690-45fb-8392-7e3ab3d4635a)

### List travel plans
Endpoint: /list/<string:user_id><br>
Method: GET<br>
Parameters:<br>
user_id (string): ID of the user.<br>
Server Response (Example):<br>
{<br>
  "travel_plans": [<br>
    {<br>
      "id": "user_id",<br>
      "location": "Philadelphia",<br>
      "days": 5<br>
    },<br>
    {<br>
      "id": "user_id",<br>
      "location": "New York",<br>
      "days": 7<br>
    }<br>
  ]<br>
}<br>
![1717620395993](https://github.com/yuwei-3206/Travel-mng/assets/122844465/e5db5f35-e6df-4bb4-b3c7-afc9165b7e7e)
![1717620812201](https://github.com/yuwei-3206/Travel-mng/assets/122844465/f2237241-7b3a-4dac-901f-bc64bdb8eade)
