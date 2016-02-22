# Exercise-Cocoapods-0

In this exercise you will learn to use **Cocoapods**, **AFNetworking** and **Grand Central Dispatch**.

## Tips
1. Make sure a server is running locally:
  - Open the `Terminal` application.
  - Use the command `cd` to navigate to the location of you `.json` file.
  - Execute the command `json-server file.json --watch`.
2. The JSON server is running at this location: **http://localhost:3000**
3. When adapting the JSON file manually, it's sometimes required to reboot the JSON server. Use `CTRL+C` to stop the server and `↑` to recall the last used command.

## Tasks
1. Create a new project for this exercise.
2. Make a `.json` file and fill it with some objects. The choice is yours ;-) Place the file in the folder **project_name/project_name**.
3. Configure Cocoapods:
  - Open the `Terminal` application.
  - Use the command `cd` to navigate to your project. Make sure you inside the folder **project_name**, on the same level as the Xcode project (this is the file with the extension `.xcodeproj`).
  - Execute the command `pod init`. This command will create the Podfile.
  - Open the Podfile and add the pod `AFNetworking`. Use the slides as reference if needed.
  - Execute the command `pod install`.
  - Close the Xcode project. From now on you should always open the **workspace** instead of the project. Go ahead and open the workspace.
  - The pod is now available in the same way as any other class. Wherever you need the pod, import the header file where needed.
4. Create a subclass of `AFHTTPSessionManager`. This class will perform all requests to the web service. In this class you should make use of the following methods:
  - `GET:parameters:success:failure:` to perform a Get request
  - `POST:parameters:success:failure:` to perform a POST request
  - `PUT:parameters:success:failure:` to perform a PUT request
  - `DELETE:parameters:success:failure:` to perform a DELETE request
5. The subclass of `AFHTTPSessionManager` is responsible for:
  - Parsing the response of the web service: when the request has returned you should convert the response to objects of your model. Create the models you need and do your magic to convert the response into a **(NSArray *)** of your custom objects.
  - Notifying when done: when the request has returned and the parsing is done, this class should indicate somehow the results are ready to use. Write your own delegate protocol to use the results when done.
6. Add a `UITableViewController` to the storyboard, create your own subclass of `UITableViewController` and set it as its custom class.
7. Use this `UITableViewController` to display the results of the request.
8. Extend your model by adding a relation. E.g.: you are building an app to view hotels, add reviews for some of the hotels.
  - Change your `.json` file as needed.
  - Change your custom models as needed.
  - Extend the functionality of your subclass of `AFHTTPSessionManager` to download, parse, etc.
9. Make sure you can insert new records of your model by using your application (e.g.: adding reviews).
  - You will have to use the correct web service to persist the changes to your database.
10. Make sure you can edit records of your model by using your application (e.g.: editing a review).
  - You will have to use the correct web service to persist the changes to your database.

## Solutions
The solutions are available in the **Demo-Cocoapods** repository.
