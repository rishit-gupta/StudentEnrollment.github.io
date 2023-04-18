# Student_Enrollment_Form_Login2Explore_Project

<p align="center">
  <img src="https://user-images.githubusercontent.com/83339859/232839880-f4e06903-eede-472a-abc8-a78b21b6f69d.png" />
</p>

## Description
It is a student registration form that stores the user's data in JSONPowerDB. It supports REST APIs and serverless technology. Students can be added, updated based on their roll number. In this form, the roll number is automatically checked and by the help of API, the data entered into other input fields sothat the user can update accordingly. The application uses AJAX requests for smooth and fast interaction. All kinds of data can be stored, such as numbers, strings, dates, etc.

## Benefits of using JsonPowerDB
- Can store structured / semi-structured and unstructured data along with other types of files and big-data.
- Dynamic relational constraints while using CRUD operations. i.e. Relational data can be managed without pre-defining PK, FK, UK, databases, tables etc.
- Free from technology constraints - Low-Code and easy to use from any technology via HTTP Rest AP
- Minimum learning curves, builds faster, cuts time to market, reduces the development cost.
- Helps developers in managing their databases using various tools and techniques.

## Use cases:
   - All RDMS use cases.
   - All key-value use cases.
   - All document use cases.
   - Time series/geospatial analytics.
   - Real time application for data analytics.
   - Live working HTML templates.
   - Any software application that needs backend DB. (Dynamic web-apps/Mobile/Desktop Apps)

## Technology Used:
client:
  - HTML
  - CSS
  - Javascript
 
Server:
  - JsonPowerDB (As Database)

## JsonPowerDB
Version: 2.0

## Execute API
```ruby
var baseUrl = "http://api.login2explore.com:5577";
function executeCommand(reqString, apiEndPointUrl) {
    var url = baseUrl + apiEndPointUrl;
    var jsonObj;
    
    $.post(url, reqString, function (result) {
        jsonObj = JSON.parse(result);
    }).fail(function (result) {
        var dataJsonObj = result.responseText;
        jsonObj = JSON.parse(dataJsonObj);
    });
    return jsonObj;
}l
```
### Create a PUT Request String
```ruby
function createPUTRequest(connToken, jsonObj, dbName, relName) {
    var putRequest = "{\n"
            + "\"token\" : \""
            + connToken
            + "\","
            + "\"dbName\": \""
            + dbName
            + "\",\n" + "\"cmd\" : \"PUT\",\n"
            + "\"rel\" : \""
            + relName + "\","
            + "\"jsonStr\": \n"
            + jsonObj
            + "\n"
            + "}";
    return putRequest;
}
```

### Features
- Simple to Use
- Fast Response
- Detailed User Interface

## Screenshots
### Student Enrollment Form:
![image](https://user-images.githubusercontent.com/83339859/232830315-2e8662c2-3657-4cfb-b98e-d323546b7c92.png)

### Database:

![image](https://user-images.githubusercontent.com/83339859/232832030-c9d50e9e-36f3-405d-b3cc-d191bcaddbf0.png)

## Illustrations:
- UPDATE : when student roll number is already present in database then student information is fetched from database and filled in respective feild then user can                  UPDATE student information
- SAVE : If student roll number is not existed in database then we can fill other field and save in database
- clear : By this we can clear all field of form and with this except first field (roll-no) other field are disabled until user enter any roll number
- Alert : This website uses disposable Alter prompt using bootstrap

## Steps To Use:

- Initially
![image](https://user-images.githubusercontent.com/83339859/232833071-9be14ccd-05e1-44db-b193-4ea4690a6ef0.png)

We need to enter a roll number
If roll number is valid and that roll number is existnig in database
- When User Write 1 in Roll number and Press Enter It automatically Fill the Google form or Extract the Info from database.
Bsically it Fetching student data using roll number If student already present in database, then all field filled with that student information

![image](https://user-images.githubusercontent.com/83339859/232830717-48242f65-24a6-4213-8182-0faa5ab8977a.png)

otherwise, other fields are enabled after user input roll number

![image](https://user-images.githubusercontent.com/83339859/232835665-7ef86860-5e58-4426-822b-22370be18b76.png)

- Updation of student details In order to update student details input roll number, and then we can update the student data
- Adding new student data

Enter new roll number and then all other fields are enabled and then after filling student information we can save this data into database only if input is valid

![image](https://user-images.githubusercontent.com/83339859/232834292-c8aab5ae-41b8-4d27-adff-f66495c51a8c.png)

## Sources

Introduction to JsonPowerDB - V2.0 course on https://careers.login2explore.com/

Bootstrap

## Demo

https://user-images.githubusercontent.com/83339859/232842745-39ace747-372c-4602-88be-4e374562ec78.mp4

