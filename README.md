# gptUseCase2App API
Welcome to the `gptUseCase2App` API, a robust solution designed to retrieve country-related information tailored to your requirements.
Whether you need a comprehensive list, specific country details, or even populations within a range, this API has got you covered. 
You can fetch countries based on names, order the list in ascending or descending fashion, filter based on population, or even limit the number of results you get.
The API is driven by query parameters, allowing users to tailor the output based on their needs.

## How it works:
+ **No Query Parameters: Simply fetches the entire list of countries without any filter or sorting logic.**

_Example_ : `GET /restcountries`


+ **Use the name query parameter to filter countries containing the provided name substring.**

_Example_: `GET /restcountries?name=est`

This will retrieve countries with names containing 'est', like Estonia.

+ **Use the population query parameter. The filter searches for countries where the population is less than the provided number, in millions.**

_Example_: `GET /restcountries?population=10`

Retrieves countries with a population of fewer than 10 million people. Remember, if the population parameter equals 0, no filtering occurs.

+ **Use the order query parameter. You can sort countries in ascending or descending order based on their names.**

 _Example_: `GET /restcountries?order=ascend`

Lists countries in ascending order of their names.

 _Example_: `GET /restcountries?order=ascend`

Lists countries in descending order of their names.

+ **Use the totalNumber query parameter to limit the number of countries returned.**

_Example_: `GET /restcountries?totalNumber=5`

Returns only the first five countries.

### You can also combine these functions

+ **Name and Population Filters Combined**

_Example_: `GET /restcountries?name=est&population=2`

Fetches countries with names containing 'est' and with a population less than 2 million.

+ **Sorting and Pagination Combined**

_Example_: `GET /restcountries?order=descend&totalNumber=3`

Returns the first three countries when sorted in descending order.

+ **All Functions Combined**

_Example_: `GET /restcountries?name=us&population=50&order=ascend&totalNumber=2`

Filters countries containing 'us', with populations less than 50 million, list them in ascending order, and then only display the first two of the resultant list.

## Recently the new endpoint was added!
_Example_: `GET /restcountries/Africa` 

 Fetch details about countries by selected Region, in this case, fetch all countries located in Africa

### _Experiment and combine as needed! Our API is designed to give you the utmost flexibility in retrieving the country data you need._

## How to run the application locally?

**Running the API**:

     Right-click on the project in the Package Explorer.
    
     Select Run As > Mule Application.
    
     Studio will build and deploy the project to the embedded Mule runtime.
    
     Look for the console message like: Started app "gpt-1use-case-app" - this indicates your API is up and running.
    
 **Testing the API**:
 
     Once the API is running, you can test it by accessing the endpoints. If you're unsure of the URL, it's typically printed in the console during the startup. For example: 
    http://localhost:8081/api/restcountries.
    
     Use tools like Postman or simply your browser to send GET requests to the provided URLs.
    
 **Stopping the API**:
 
     When you want to stop the API, go to the Console tab at the bottom, select the running process, and click on the red square button (Stop) on the top right of the console.
     
 **Troubleshooting**:
 
     If you run into port conflicts (e.g., "Address already in use"), it's likely that the default port (like 8081) is already in use. You'll need to update the configuration in your project to use another port.
     If there are issues related to project dependencies or configurations, they will typically be displayed in the console. Reading these error logs can give insights into what needs fixing.

### _Useful links_:
+ [Exchange](https://anypoint.mulesoft.com/exchange/4af9c84b-ab45-49f9-9cc2-9764f985bec1/gpt-1use-case-api/minor/1.0/)
+ [Public Portal](https://anypoint.mulesoft.com/exchange/portals/softserve-inc-62/4af9c84b-ab45-49f9-9cc2-9764f985bec1/gpt-1use-case-api/)
+ [Implementation Url](http://gpt-1use-case-app.us-e2.cloudhub.io/api/restcountries)
   + API is secured by Basic Authentication
