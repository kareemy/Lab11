## Your Name:


# Extra CreditLab 12: Professor Web App Redux: Scaffolding and Related Data

In this lab exercise you will perform scaffolding, add a second entity class to your project, and connect that class with your existing one. This process is known as connecting related data.

## Step 0: Prepare Your Environment

1. Open your completed Lab 11 in Visual Studio Code

## Step 1: Scaffolding

1. Bring in the required packages and tools for scaffolding:
```
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design
dotnet tool install --global dotnet-aspnet-codegenerator
```
2. Run the scaffolding command. Refer to the slides for the correct command. Note: You will have to make changes to the command to match your project.
3. Once scaffolding is complete, run your project and visit the newly scaffolded pages.
        * Look at the Index page and ensure you have a list of all the professors.
        * Click “Create New” and make a new professor. Ensure that it is added to your list.
        * Click “Edit” and edit a professor. Ensure that your changes worked.
        * Click “Details” and see the details of a professor.
        * Click “Delete” and delete a professor. Ensure that the professor is removed.

## Step 2: Connect Related Data

1. Add a Course entity class. 
        * Each course should have a CourseId and a Description property.
        * Each course is taught by ONE professor, and a professor may teach MANY courses. Put in the correct navigation properties.
        * Add the DbSet<Course> property to your DbContext class.
2. Modify your SeedData class:
        * One professor should teach one course.
        * Another professor should teach at least two courses.
        * A third professor should teach no courses.
        * Delete your Migrations/ folder and your database.db file. Re-run your migrations.
3. **PAUSE**. Run your project. If you see build errors, debug! You should not see any changes on your website yet. Just make sure that it runs and looks OK.

## Step 3: Display your courses (Read part of CRUD)
