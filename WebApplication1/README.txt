Sharu Joseph John (0847821)

2024-01-11
1500

Installed Visual Studio Enterprise Edition successfully.

Followed the instructions provided in the tutorial:

ASP.NET Core MVC Tutorial: https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-mvc-app/start-mvc?view=aspnetcore-8.0&tabs=visual-studio

Ensured all prerequisites for ASP.NET Core MVC are installed.

Created a new project named WebApplication1.

Selected .NET 8.0 (Long Term Support) and followed the provided instructions.

While running the app, a Warning popup appeared; selected Yes for the SSL and CA warning.

Started debugging, redirected to Microsoft Edge.

Created an "img" folder inside "wwwroot".

Drew an image using Paint and saved it as png format inside the "img" folder.

Added the housejpg image after the Welcome heading:

<p><img src="~/img/house.png" /> </p>


2024-01-17
2000

Part 2: Adding a Controller

Added a controller named HelloWorldController.cs
Replaced the contents of Controllers/HelloWorldController.cs with the provided code.

Appended "/HelloWorld" to the path in the address bar; the Index method returned a string:
https://localhost:7092/HelloWorld

Modified the code in HelloWorldController.cs:

Added a Welcome method that accepts parameters and provides encoded output.
Tested the app with the URL: https://localhost:7092/HelloWorld/Welcome?name=Rick&numtimes=6
Modified the Welcome method in HelloWorldController.cs:

Updated the parameter name and added a default value.
Tested the app with the URL: https://localhost:7092/HelloWorld/Welcome/6?name=Rick


2024-01-17 
1000

Part 3: Modifying the HelloWorldController class to use Razor Syntax Views.

Replaced the Index method in HelloWorldController.cs with:

public IActionResult Index()
{
    return View();
}
The Index method now calls the controller's View method and returns an IActionResult or a class derived from ActionResult.

Right-click on the Views/HelloWorld folder, and then Add > New Item.

In the Add New Item dialog select Show All Templates.

In the Add New Item - MvcMovie dialog:

In the search box in the upper-right, enter view
Select Razor View - Empty
Keep the Name box value, Index.cshtml.
Select Add

2024-01-24
2030
PART 4: add a model to an ASP.NET Core MVC app
In Model folder added class and named file as movie.cs
Then under Controllers folder Added New Scaffolded Item and selcted movie option under the model class
To get Migration folder, selected NuGet Package Manager From the Tools menu and gave required command under Package Manager Console 
Then Run the app and selected the Movie App and modified the data
Models represent the data and business logic of an application.

2024-01-24
2200
Migration Code 20240125161633_InitialCreate
Added new data to database
