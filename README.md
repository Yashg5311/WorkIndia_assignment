## WorkIndia Assignment

# When an admin registers first time
![Screenshot (646)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/41d7c74f-f109-47fb-a4ea-3f8612afe414)

Database Screenshot:
![Screenshot (648)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/2dfd7ea6-eb42-4765-9e68-978adced7c06)


# When an admin logs in
![Screenshot (651)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/4226a113-9d13-4d76-a1fc-04bf1a7a4b7e)


Wrong Password Case:
![Screenshot (653)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/d6e3290e-50d2-4790-a415-47465182e87c)

# When an admin adds the train
![Screenshot (656)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/b2d70a28-af98-46e7-bfaa-d300be4184ca)

Admin has to enter floowing fields:
![Screenshot (655)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/73e5a611-8bd5-44da-a331-6af78a015c26)

If admin enters wrong admin key:
![Screenshot (659)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/4091c03f-c819-4507-bdfb-33f49bbba2ec)

If token is wrong:
![Screenshot (660)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/f0320037-34d9-4da0-a3c5-74dbf4554c22)


Train database:
![Screenshot (661)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/0958d9a3-028c-4e91-a16d-9c57e53b1aa0)

# Admin wants to edit train details
![Screenshot (663)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/f971ece7-e911-41fc-b60e-feb2a4255288)

![Screenshot (665)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/6c71e038-1eb3-4c48-9b2d-8f0badf4b7e8)


# If a normal users tries to add the train:
![Screenshot (668)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/4f98f55c-1ce5-4cf2-8230-f31bf08c6329)


# Normal User when wants to fetch the train between source and destination
![Screenshot (669)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/c3ce0d62-c97b-4417-80c0-913b0682c9f7)

# Normal User when tries to book a train
![Screenshot (678)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/a2b6c03b-bc8f-4208-8768-50b7f2709333)

When books an empty train:
![Screenshot (676)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/9915bbdd-b806-4f58-84aa-ac3355178b6e)

# Normal user when wants to fetch a detail of a particular booking

![Screenshot (674)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/c7326194-6d00-4d1d-b551-69c694ce24fa)

![Screenshot (673)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/87ab0127-42e8-4bec-b2d0-d35b76b7bec7)


# Booking Table:
![Screenshot (672)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/aa410fd0-5dbd-47ba-a1fd-f9661e1da6f5)

# Users  Table
![image](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/067fd7bc-ff90-41c4-853f-74291339e285)

# Trains Table:
![Screenshot (680)](https://github.com/Yashg5311/WorkIndia_assignment/assets/91370994/eb3105af-be84-4f65-8efa-72c4cbd421a6)

## API EndPoints

 # Users Registers: http://localhost:3000/api/users/register\n

 {
  "username": "yash",
  "email": "yash@gmail.com",
  "password": "12345",
  "role": "normal"
}
 <br/>
 Response:
 {
    "message": "User registered successfully"
}
<br/>
 # Users Log in:  http://localhost:3000/api/users/login
 {
    "email": "yash@gmail.com",
  "password": "12345"
}
<br/>
Response:
{
    "message": "User logged in successfully",
    "success": true,
    "data": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VySWQiOjI2LCJyb2xlIjoibm9ybWFsIiwiaWF0IjoxNzE3MTM3NTkwLCJleHAiOjE3MTcyMjM5OTB9.L8xlXL_imKlDxrb1ewL59Q7O3Sfp0NZQBnb0NQj6DUA"
}
<br/>
# Admin when tries to add a Train: http://localhost:3000/api/admin/trains
<br/>
{
  "trainName": "Shatabdi",
  "trainId": "SH125",
  "source": "Banglore",
  "destination": "Mumbai",
  "totalSeats": 0
}
<br/>
response:
{
    "message": "Train added successfully",
    "success": true,
    "data": {
        "id": 9,
        "trainName": "Shatabdi",
        "trainId": "SH125",
        "source": "Banglore",
        "destination": "Mumbai",
        "totalSeats": 0,
        "updatedAt": "2024-05-31T06:39:37.640Z",
        "createdAt": "2024-05-31T06:39:37.640Z"
    }
}
<br/>

# admin whwn tries to update Train Details: http://localhost:3000/api/admin/trains/SH123
<br/>
{
"destination":"New Mumbai",
"totalSeats":60
}
<br/>
Response:
{
    "message": "Train details updated successfully",
    "success": true,
    "data": {
        "id": 8,
        "trainName": "Shatabdi",
        "trainId": "SH123",
        "source": "Banglore",
        "destination": "New Mumbai",
        "totalSeats": 60,
        "createdAt": "2024-05-31T06:26:19.000Z",
        "updatedAt": "2024-05-31T06:28:58.662Z"
    }
}
<br/>
# User whwn tries to fetch train between source and destination : http://localhost:3000/api/trains?source=Banglore&destination=New Mumbai

{
    "message": "Trains fetched successfully",
    "success": true,
    "data": [
{
            "trainName": "Shatabdi",
            "trainId": "SH123",
            "source": "Banglore",
            "destination": "New Mumbai",
            "totalSeats": 60,
            "createdAt": "2024-05-31T06:26:19.000Z",
            "updatedAt": "2024-05-31T06:28:58.000Z"
        }
    ]
}
<br/>
# Users when tries to book a train: http://localhost:3000/api/bookings/book
<br/>
{
  "source": "Banglore",
  "destination": "New Mumbai",
  "trainId": "SH123"
}
<br/>
{
    "status": "SUCCESS",
    "bookingId": "be38b8c9-3793-4a54-9fd0-2479343c83c0"
}
<br/>
# users when tries to fetch  a partcular booking: http://localhost:3000/api/bookings/886f4acb-1270-47a3-8996-434e456a3931
<br/>
{
    "status": "SUCCESS",
    "bookingDetails": {
        "trainName": "Shatabdi",
        "trainId": "SH123",
        "status": "booked"
    }
}
<br/>

## Steps to set up locally
We use NodeJS , ExpressJS and MySQL for Database Connection

1. Clone the repository
2. Add the .env file in root directory
3. Provide the following fields for Database connection:
   PORT=
DB_HOST=
DB_USER=
DB_PASSWORD=
DB_NAME=
JWT_SECRET=
ADMIN_API_KEY=

4. Install all dependency: using npm i
5. Start the server using node app.js
6. Open postman and test all the API endpoints


## Race Condition Handle
Row-Level Locking: When a user tries to book a seat, the row corresponding to the specific train is locked for the duration of the transaction. This prevents other transactions from accessing and modifying the same row until the current transaction is completed (either committed or rolled back).
Transactional Integrity: All operations (finding the train, updating seat count, and creating booking) are performed within a single transaction. This ensures that either all operations are successfully completed, or none of them are, maintaining database integrity.
Example Scenario:
1. User A begins a booking transaction and locks the train row.
2. User B attempts to book the same train while User A's transaction is active:
User B's request will wait until User A's transaction is complete because the row is locked.
Once User A's transaction commits or rolls back, User B's request can proceed.
If User A booked the last available seat, User B will find no available seats and receive a "No available seats" error.
This mechanism ensures that two users cannot book the same seat simultaneously, effectively preventing race conditions.




