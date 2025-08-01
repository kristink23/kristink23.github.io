The artifact I selected for this portion of my capstone was the same Weight Loss Tracker application I used for the first enhancement. This project helps users track their daily weight, but originally it only stored and displayed the data without any analysis. There was no way for the user to understand whether they were trending up, down, or staying stable. 

I chose this artifact because it gave me an opportunity to show how I can apply algorithms and data structures to add real value to an application. In its original form, the app was missing any kind of meaningful feedback based on the stored data. By enhancing it, I was able to show that I can design and implement an algorithm to analyze weight trends and clearly display the results. To improve the artifact, I made several key changes: 

- I added a new function called calculateWeightTrend() in the ViewModel, which uses a simple linear regression algorithm to detect if the user is gaining weight, losing weight, or staying the same. 

  - This function processes the list of weight entries in chronological order, calculates the slope of the data, and then returns a message about the user’s current trend. 

- I updated the user interface to include a trend message TextView above the data entry area so the user can easily see the result of the calculation. 

- I wrote new unit tests for calculateWeightTrend() that check for all scenarios: gaining, losing, stable, and not enough data. These tests helped confirm that the algorithm works correctly. 

These enhancements align directly with the course outcome focused on algorithms and data structures (Outcome 3). They show that I can design and evaluate a computing solution using algorithmic principles and integrate it into an existing system. 

I believe I met my planned outcome coverage from Module One. The enhancement demonstrates my ability to implement an algorithm, use data structures like lists effectively, and validate my work with unit tests. There are no changes needed to my original outcome plan. 

Throughout this process, I learned how important it is to think about both performance and accuracy when analyzing data. Even though this algorithm is fairly simple, I had to ensure it would handle all possible edge cases, such as when there aren’t enough data points to calculate a trend. Another challenge was making the feature easy for the user to understand; the calculation is done behind the scenes, but the result has to be presented clearly. One challenge I faced was building unit tests for the algorithm and making sure the messages matched exactly, including punctuation and spacing. A small mismatch caused failed tests at first. Writing the tests helped me focus on the details and made the final feature more reliable. Overall, this enhancement added valuable functionality to the application and demonstrates my ability to apply algorithmic thinking to solve real-world problems. 
