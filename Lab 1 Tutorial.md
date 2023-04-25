# Lab Report 2

### Part 1 (String Server):
1. Below are two images which make up the coding that I wrote which enable my String server to work. The coding itself took a lot of inspiration from the lab code we had for lab 2 in which we created a number server but I modified a good chunk of it in order to meet the needs of adding strings/text rather than numbers.
2. The basic commands of my server are displaying the current List of strings implemented to the server which can be found by following the server link. Along with adding words to the list by writing `/add-message?s=` into the address bar of my string server. If anything else other than the two basic calls of my server then the user is prompted with a `404 Not Found!` screen.
    ![Code_Part_1](https://user-images.githubusercontent.com/130005453/233888785-23dbae42-9420-4990-ae10-c7ae99b2e78a.png)
    ![Code_Part_2](https://user-images.githubusercontent.com/130005453/233888706-0a5c6347-0ef6-48ae-bda0-446794f96e76.png)

* Infrmation on server
* Below is an image of the server when it is simply opened up (before any words are added to the list)
![Starter_server](https://user-images.githubusercontent.com/130005453/233889762-f73091cc-1818-4c93-9007-9ff44f7e286c.png)






* The following image is an example call which usses `/add-message?s=` to add a word onto my list (Note: To view entire list of words I would need to edit the url so it is the same as the previous image rather than the one below)
![Cake_Added_Word_Example](https://user-images.githubusercontent.com/130005453/233890070-3fea9f06-a41a-48ae-ab93-daaa86cf809d.png)
Methods called for the image above:
* `format()` 
    * Arguments: Takes in new `String`(in our case `cake`) and adds it to `"Word added was "` before displaying it to the user

* `println()`
    * Arguments: takes `URL` (more specifically the path of the `URL`) to add it to the string `"Path: "` before displaying it on the terminal the server is running on

* `getpath()`
    * Arguments: takes in no argument but returns the path of the current `URL` before proceeding onto the next step of code

* `getQuery()` 
    * Arguments: Takes in no argument but returns a shortened version of the path of the `URL` with everything after the `"?"` in the path (returned this information into the system before proceeding with the rest of the code)
 
* `split()` 
    * Arguments: Takes in `String` (in our case `"="`) and looks for that in the shortened `URL` querry in order to create 2 smaller strings consisting of `s` and `what ever the user inputed`

* `contains()` 
    * Arguments: takes in a `String` (in this case `"/add-message"`) and checks the path of the `URL` to see if the `URL` is trying to add new words to the `String` list for the server. If it does it produces true and if not it produces false

* `equals()` 
    * Arguments: Takes in a `String` (`"s"`)and checks to see if it is the same as the querry formed through the `URL` link to add a word on our list. If it's true then it proceeds with the rest of the code to add a word onto the list.

* `HandleRequest()` 
    * Arguments: Takes in a `URL` and affects the server/webpage based on the pathway of the `URL`. If the `URL` only has a "/" for the pathway then the page displays the current `String` list. If the `URL` has "/add-message" (in sthis case: `"/add-message?s=cake"`) it checks to see if it'll add a new string to the list.
Relevant value that the image above produces: `cake` being the key difference between the `URL` differences of the last image and the one coming up. (One `URL` ended in `cake` while the other ended in `pie`)

The values that get changed in the image above and below are:
* `String` (that holds all the strings of the server. In other words the list of strings the user has added previously) The `String` gets changed because a new string is added to our server string.
* `URL`/ `URI` (the weblink itself) gets changed so that our code recognizes different commands of displaying the list of strings or adding a new string to our list
** It basically gets slightly changed everytime a user wants to add a new word to the list because the end of the `URL/URI` is alteered to show what word the user wants to add to the list.



The image below is another example of when I `add-message` to my `String` of words
![pie_add](https://user-images.githubusercontent.com/130005453/234161762-0dd95032-d2f4-4aa3-a1b9-c2b83fa4a1bf.png)
Methods called for the image above:

* `format()` 
    * Arguments: Takes in new `String`(in our case `pie`) and adds it to `"Word added was "` before displaying it to the user

* `println()`
    * Arguments: takes `URL` (more specifically the path of the `URL`) to add it to the string `"Path: "` before displaying it on the terminal the server is running on

* `getpath()`
    * Arguments: takes in no argument but returns the path of the current `URL` before proceeding onto the next step of code

* `getQuery()` 
    * Arguments: Takes in no argument but returns a shortened version of the path of the `URL` with everything after the `"?"` in the path (returned this information into the system before proceeding with the rest of the code)
 
* `split()` 
    * Arguments: Takes in `String` (in our case `"="`) and looks for that in the shortened `URL` querry in order to create 2 smaller strings consisting of `s` and `what ever the user inputed`

* `contains()` 
    * Arguments: takes in a `String` (in this case `"/add-message"`) and checks the path of the `URL` to see if the `URL` is trying to add new words to the `String` list for the server. If it does it produces true and if not it produces false

* `equals()` 
    * Arguments: Takes in a `String` (`"s"`)and checks to see if it is the same as the querry formed through the `URL` link to add a word on our list. If it's true then it proceeds with the rest of the code to add a word onto the list.

* `HandleRequest()` 
    * Arguments: Takes in a `URL` and affects the server/webpage based on the pathway of the `URL`. If the `URL` only has a "/" for the pathway then the page displays the current `String` list. If the `URL` has "/add-message" (in sthis case: `"/add-message?s=pie"`) it checks to see if it'll add a new string to the list.
Relevant value that the image above produces: `pie` being the key difference between the `URL` differences of the last two images. (One `URL` ended in `cake` while the other ended in `pie`)


* Lastly here is an my server's list of strings having added a few more examples
![Final_example_of_server](https://user-images.githubusercontent.com/130005453/233890401-2aa81fb1-2359-4050-9223-a81c6c45d2cb.png)

### Part 2 (Bug Checking): Reverse method for arrays
(Note: This is the starting code below)
![start](https://user-images.githubusercontent.com/130005453/233908915-9b7f37ae-2c1e-4cc7-ba0e-23f9719e646f.png)
* Failure inducing input: Any input array that consists of numbers (The image below shows an example array of `[1,2,3]` being put through a junit for the reverse in which it failed to giver the output `[3,2,1]`)
* Symptom: Returning an array that consists of only `0's`
![failed_junit](https://user-images.githubusercontent.com/130005453/233911309-5381c714-ea9c-4c78-b96e-f453e6dfd3cd.png)
* An input that doesn't procude an input: An empty array (ex. `[ ]`) or an array with only 0 values (ex: `[0,0,0]`) (Picture below shows the code of junit tests that passed although the code is still buggy)
![exception_to_buggy_code](https://user-images.githubusercontent.com/130005453/233910708-044754f0-8b37-45f5-8a70-3f329e01635d.png)

* Bugs before fix: \
`static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
    arr[i]  = newArray[arr.length - i - 1];
    }
    return arr;
  }` \
  (or as the image below)
![image](https://user-images.githubusercontent.com/130005453/233913718-40a54863-b0bc-4e7e-b7de-3db345366234.png)

* Fixed code: \
`static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[arr.length - i - 1] = arr[i];
    }
    return newArray;
  }` \
  (or as the image below)
![No_Bug_Code](https://user-images.githubusercontent.com/130005453/233908124-3c92c30a-a8c9-4208-b788-d35c00098c4b.png)
The code above fixes the code because instead of replacing the starting array (`arr`) with the 0 values of the `newArray`, the code would now fill in the 0's of the `newArray` with the values of the `arr` but placing them in the reverse order (the first element in `arr` would be placed as the last element of `newArray`). The fixes also return the newly created array instead of the starting array.

### Part 3 (Things learned):
* Something I learned from labs 2 and 3 was the idea of servers being more than just a videogame thing which allows for larger quantities of people to use a specific program.
* Originally: I knew the concept of a server since games often use this to funnel a finite number of players into spaces which the computer system could handle rather than having every person all in one server.
* Now: I know that even the websites we use and probably other applications of servers allows for larger quantities of people to use the same system/program while also ensuring that the server works as it's intended (Without crashing or slowing down too bad).
