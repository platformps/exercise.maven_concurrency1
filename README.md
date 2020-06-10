# Basic Concurrency


### Description
* **Objective** - To implement a synchronous and asynchronous structures, each with behavior dependent on defined synchronicity.
* **Purpose** - To establish familiarity with
    * concurrency operations
    * asynchronous operations
    * multithreading
    * race conditions

* **Details**
    * You are provided with a detailed list of specifications in the `README` below.
    * Fulfill each request of the `README` by creating a separate test-case for each of asks.
        * Test-cases _do not have to have assertions_, as the assignment only asks for _printing_.
    

    


### Part 0 - Getting Started
* Begin by _forking_ this project into a personal repository.
   * To do this, click the `Fork` button located at the top right of this page.
* Navigate to your github profile to find the _newly forked repository_.
* Clone the repository from **your account** into the `~/dev` directory.
* Open the newly cloned project in a code editor (Visual Studio Code, for example).




### Part 1 - Creating and joining threads
1. Write a Class, named `CreatingAndJoining`, that prints `Hello World` from an additional `Thread` using Java Thread API.
2. Modify the Class to print `Hello World` exactly 5 times.
    * Each print statement should be handled by a separate thread.
    * Ensure `String`s are not _interleaved_ in the output.
3. Modify the printing of the Class to include the thread-number. Ensure all threads have a unique thread-number


## Part 2 - Simple Synchronization
1. Write a Class, named `SimpleSchronization`, which creates two `Thread` objects, each incrementing a shared integer asynchronously, 1,000,000 times.
    * Print the integer's value at the end of program.
    * Run the program on a multicore system and attempt to exercise the potential race in the program.  
2. Modify the Class to make use of `synchronized` keyword, ensuring that increments on the shared integer are atomic.


## Part 3 - Guarded blocks
1. Write a Class, named `GuardedBlocks`, which creates two `Thread` objects.
    * The first thread should increment an integer 1,000,000 times.
    * The second thread should print the integer without waiting for the first `Thread` to finish
2. Modify the class to use a conditional signalling the completion of the task by the first `Thread` before the second `Thread` prints.
3. Modify the class to ensure that the second `Thread` prints the integer after waiting for the first `Thread` to complete.