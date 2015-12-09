# codeacademyangular1

So far this is our typical workflow when making an AngularJS app:

Create a module, and use ng-app in the view to define the application scope.
Create a controller, and use ng-controller in the view to define the controller scope.
Add data to $scope in the controller so they can be displayed with expressions in the view.

Great! The product price changed from a number to a formatted currency. How does it work?

AngularJS gets the value of product.price.
It sends this number into the currency filter. The pipe symbol (|) takes the output on the left and "pipes" it to the right.
The filter outputs a formatted currency with the dollar sign and the correct decimal places.

In this way, filters help to separate the content in the controller from its presentation in the view.

A module contains the different components of an AngularJS app
A controller manages the app's data
An expression displays values on the page
A filter formats the value of an expression

Well done! You got both books in $scope.products to show up in the view. How does it work?

In the controller, we used products to store an array containing two objects.
Then in the view, we added <div ng-repeat="product in products">. Like ng-app and ng-controller, the ng-repeat is a directive. It loops through an array and displays each element. Here, the ng-repeat repeats all the HTML inside <div class="col-md-6"> for each element in the products array.

In this way, ng-repeat shows both products in the $scope.products array. Instead of writing the same HTML twice as before, we just use ng-repeat to generate the HTML twice.

We've used a few directives so far - ng-app, ng-controller, ng-repeat, and ng-src. What can we generalize about directives?

Directives bind behavior to HTML elements. When the app runs, AngularJS walks through each HTML element looking for directives. When it finds one, AngularJS triggers that behavior (like attaching a scope or looping through an array).

So far we've made a static AngularJS app by adding properties in the controller and displaying them in the view. AngularJS is a framework for building dynamic web apps, so let's start to make this app interactive.

Great! Each time you click on the number of likes, the number goes up. How does it work?

The ng-click is a directive. When <p class="likes"> is clicked, ng-click tells AngularJS to run the plusOne() function in the controller.
The plusOne() function gets the index of the product that was clicked, and then adds one to that product's likes property.

Notice that the plusOne() doesn't interact with the view at all; it just updates the controller. Any change made to the controller shows up in the view.

Congratulations! You built an AngularJS app from scratch. What can we generalize so far?

A user visits the AngularJS app.
The view presents the app's data through the use of expressions, filters, and directives. Directives bind new behavior HTML elements.
A user clicks an element in the view. If the element has a directive, AngularJS runs the function.
The function in the controller updates the state of the data.
The view automatically changes and displays the updated data. The page doesn't need to reload at any point.
