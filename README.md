The requirements and goals for this application, was to make a way for the user track daily weights
and set goals. The app would then send a message to the user when they reach their goal. 

The app required the use of Android's local sql lite to store user login credentials and goal / daily weights.

For this application I used two screens, one to act as the login page and the other as the table to display the user's daily and goal weights. 
I kept the UI uncluttered and simple, only having what was needed for displaying the proper information and nothing extra. It's because of this that the design works, I especially think that the login screen is the best of the two screens in terms of design. 

When coding the application I grouped the functionality of the application into different classes, and grouped my classes based on the screen they were used. 
I also followed a MVP pattern when coding. The xml files acted as the View, while the classes like Account and Weight acted as the model. The activity classes acted as the controller or I made seperate controller classes that inflated parts of the UI

When testing, I ran my code often and interacted with the application to determine that the app behaved in the way that I desired and there were no bugs. Either that caused the application to crash or that cause the application to behave in a strange way.
This is important because one doesn't know if their code works as intended or is error free unless it's tested. Throughout my testing, it revealed errors in my code and logic that I was able to correct to make my application work. 

One big part of the project that I had to innovate was during the development of the database. I had used the Room persistence library that android provides to create my database. 
I wanted my database to run only on background threads. I had an example from the course material that I used, but when I had to query from the database, the example only showed how to use LiveData objects to get information from the repository. 
Because I had also used the Executor Service object to run the other database operations, I looked into how threading worked and how I could get a calculation or result from a worker thread. I then was able to find out about callable objects, which I created custom classes that implemented Callable.
I was then able to use the submit method on the Executor Service and a Future object to get the result of the operation after it was completed and return it to the main application thread. 

I think that the Login component implementation was very successful and displayed my skills the best. I think it especially showed how well object composition is when making the code simpler and easier to read and maintain. 


