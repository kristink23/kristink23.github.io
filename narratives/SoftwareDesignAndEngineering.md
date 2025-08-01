The artifact I selected for this portion of my capstone was a Weight Loss Tracker application built in Android Studio using Java. I created this project during a previous course to help users track their daily weight using a simple user interface and a local SQLite database. It worked, but the original version mixed too many responsibilities in one file. This meant it was handling the UI, storing data, and validating input all in one place. 

I chose this artifact because it gave me a perfect chance to show how my software design skills have improved. Originally, the code did not follow many best practices, which made it hard to test, hard to update, and not very flexible. By enhancing it, I was able to show that I have learned how to write cleaner, more maintainable code using principles like separation of concerns and modular design. To improve the app, I made several key changes: 

- I refactored the code to follow the MVVM (Model-View-ViewModel) architecture. This split the UI, data, and logic into separate layers. 

- I moved database access into its own class (DatabaseHelper) and created a new ViewModel to manage background tasks and LiveData updates. 

- I replaced the old TableLayout with a RecyclerView, which is more efficient and flexible for showing multiple items. 

- I made the app easier to test by adding a second constructor to the ViewModel, which lets me pass in a mock database helper during unit tests. 

- I also added basic unit testing using JUnit and Mockito, which wasn’t possible with the old version. 

- Finally, I added comments to explain the code better and followed modern Android design patterns to make everything easier to maintain. 

These enhancements showcase my ability to write clean, testable, and maintainable code, as well as my understanding of modern Android development practices. They also demonstrate adherence to the Single Responsibility Principle and Separation of Concerns, which are important concepts within software engineering.  

These enhancements align with the course outcome focused on software engineering and design. I believe I exceeded my original plan in several ways: 

- I introduced unit testing using JUnit, Mockito, and InstantTaskExecutorRule. 

- I implemented constructor-based dependency injection for better testability. 

- I improved input validation and error handling for a more robust user experience. 

There are no changes needed to my planned outcome coverage, but I feel confident that these enhancements provide a more complete demonstration than originally proposed. 

Throughout this process, I learned how much easier it is to update and improve an app when it's built using a solid structure. Refactoring the app to use MVVM and LiveData helped me separate the UI from the backend logic, which made the code cleaner and easier to manage. Writing unit tests also taught me to think more carefully about how the app was built, especially around constructors and working with background threads. It helped me better understand how Java handles concurrency and how Android manages its lifecycle. 

One of the biggest challenges was testing the ViewModel because it originally created the database helper directly. To fix this, I added a second constructor that let me use a mock database for testing, which also made the code more flexible. I also had to make sure the background tasks had time to finish in the tests, so I used Thread.sleep() to simulate waiting for them. 
