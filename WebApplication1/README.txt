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
PART 4:
A class was added to the Model folder and named "movie.cs".
Next, within the Controllers folder, a New Scaffolded Item was added, opting for the movie option as the model class.
To obtain the Migration folder, the NuGet Package Manager was accessed from the Tools menu,
and the necessary command was executed within the Package Manager Console.
The app was then executed, the Movie App was chosen, and the data was modified.
Models serve to embody the data and business logic of an application.

2024-01-24
2200
PART 5:
Migration Code 20240125161633_InitialCreate
Connected SQL database
Added new data to database

2024-01-25
1200
PART 6:
Controller methods and views
Used scaffolding to generate code for editing movie data in the database
Used Tag Helpers and data annotations to streamline the HTML markup and validation logic.

2024-01-31
1830
PART 7:
To incorporate the search bar.
The index method within Controllers/MoviesController.cs was revised.
The parameter was altered to 'id' and all instances of 'searchString' were replaced with 'id'.
Subsequently, the index method was reverted to accept a parameter named 'searchString'.
The Views/Movies/Index.cshtml file was accessed, and the <form> markup was introduced utilizing the form tag helper.
This setup ensures that upon form submission, the filter string is posted to the Index action of the movies controller.

2024-01-31
1930
PART 8:
To incorporate a Rating Property into the Movie Model.
Added the rating property within Models/Movie.cs.
Updated the [Bind] attribute in MoviesController.cs for both the Create and Edit action methods to include the Rating property.
Edited the /Views/Movies/Index.cshtml file to include a Rating field.
Updated the /Views/Movies/Create.cshtml file with a Rating field.
Adjusted the SeedData by incorporating the rating division to ensure a value for the new column.
The application encountered issues until the database was updated; thus, the database was updated by executing the ADD MIGRATION command in PMC.

2024-01-31
2100
PART 9:
To implement validation.
Enhanced the Movie class to utilize built-in validation attributes like Required, StringLength, RegularExpression, Range, and the DataType formatting attribute.
Included Minimum Length and Regular Expression attributes to restrict character input.
An error occurred subsequently, which was resolved by assigning ratings to existing movies in the database.
The database was accessed by navigating through View > SQL Server Object Explorer > SQL Server > Databases > MvcMovie context > dbo.movie.

2024-02-01
1100
PART 10:
To analyze the Details and Delete methods.
Accessed the movie controller class to review the details method.
Referenced the segments defined in program.cs.
Inspected the delete and deleteconfirmed methods.
Named the [HttpPost] method responsible for data deletion as DeleteConfirmed, providing it with a distinct signature or name within the HTTP POST method.
