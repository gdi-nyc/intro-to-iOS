### Agenda 

# Day 1

- Know your tools. Intro to XCode. What is Xcode and how to use it

- What is IOS

- Learning to Program with Swift and IOS

	- Quick overview of Variables

	- Swift Data Structures: Arrays, Dictionaries

	- Object Oriented Programming - What is a Class

	- Enumerations - Also a type of Class

	- Some of my most favorite and cool things in Swift



### Day 1 Continued 

- The MVC Paradigm

	- What is The Model

	- What is the View

	- What is the Controller

	- Tie them together

- Practicing Swift with Playgrounds

- Getting ready for Day-2. Write your own IOS App



### Agenda: Day 2

Demo: We are going to write an IOS App. The App will be a task Management App.

- Introduction to the Story Board

- What is a View Controller

- Using Auto-Layout

- Create our TableView Controller

- Populate our Data

- Add, Remove rows

- Complete your demo

- Bonus if we can put it on our phones!

- WHOHOO!! were App Developer's



# What is XCODE

XCode is what is known as an IDE. You will use XCODE to design, develop and test your app. It is a complete eco-system unto itself.

Apple Developer has great documentation on this. We will be using Apple Developer a lot going forward.

[Learn More](https://developer.apple.com/xcode/ide/). 



# What is IOS

IOS is the Operating System that the Iphone runs on. It contains core Foundation Classes, Networking classes, Security and OS Classes. IOS handles security, FileIO and all the things that an OS usually takes care of. 

[Learn More](https://en.wikipedia.org/wiki/IOS)



# Apple Developer Account

It is a really good idea to sign up for an Apple Developer Account. You will need it if you are going to program in IOS and want to put your app on your Iphone.

Apple Developer Account is free for Development. If you want to buy a license for your company it is a $100.00 as of now-a-days.

[Learn More]([Xcode](https://developer.apple.com/)



# Introduction to Swift

Swift is Apple's new language. Mobile Development on IOS was previously done in Objective-C. Swift has brought modern programming techniques and efficiencies to Iphone Programming. [The Swift Book](https://itunes.apple.com/us/book/the-swift-programming-language-swift-3-1/id881256329?mt=11) Can be found here. 

It is for *Free* so please do not buy it. Get it for free :)



### Lets Begin to write Code!!! 

#### What is a Variable

A variable is a location in memory that holds data. Usually you assign a value to a variable that can be used later.

A variable is just a holder. The value in a variable can change. Hence it is known as a variable.

	your_name = 'radhika' //LHS is the variable. RHS is the data

	your_name = 'bumlebee'

	print(your_name) //will now print bumblebee because thats the last thing the variable was assigned

Swift also has constants. A constant is a variable that cannot be modified.
More on that soon.




#### Variables and Types

Open up Playgrounds.

	var name = "radhika" // Is a String. The Type is String

	var number = 10 // Is a number. The Type is a Integer

	var digit = 100.99 //Is a float. The Type is a Float

	var name: String! //Is an Optional String. Aha! Got you. What is an optional?

In Swift you assign a value with the = sign

Swift is a strongly typed language and is a compiled language. The compiler needs to know the type before it can be used.

It is also uses type inference so you do not need to define the type before hand. It can infer the type when it is used for the first time.



### More on Variables and Types

- Strings 

- Integers

- Floats and Double

- Boolean

- Optionals

- Custom Type ( Your Own )

- Enumerations

A variable has strict naming conventions. It cannot contain spaces, numbers or special characters. Try to keep the name meaningful.



### Constants and Optionals

Swift has the concept of a constant. A constant is when the value in a variable cannot be modified.

	let PI = 3.214

	func circle(radius: Integer) -> area {
		return PI * radius * radius
	}

	//Above it makes sense to make PI a constant. This is good programming form. 
	//Unless you create your own country with a different PI, PI is always the same.

Also notice the let above. Not var. Thats swift way of creating a constant

	PI = 99999 //will throw an error. You cannot change the LHS PI



### Practice Excercise

Lets open up playgrounds.

1. Create the following variables:
	
	name, age, date of birth, address, and phone number

2. Use the print statement and print out the values in these variables

3. Create a constant. Assign a value and then try and modify the values.



### Arrays and Loops - Collection Types 

What is an array? How can we create one in Swift?

	var array_of_names = ['Radhika', 'Karthika', 'Aria', 'Sally', 'John', 'Mindy']

	for name in array_of_names:
		print("Hello \(name)! How are you doing today?")

So we created an Array and we looped over each item in the array

	var array_for_future = Array<String>()

	array_for_future.append("Radhika")
	array_for_future.append("Aria")

Another way to add items into an Array. Read more on Arrays when you have time.



### Dictionaries - Another Collection Type

A dictionary is a Key:Value pair. It is a great way of looking up a specific item without having to traverse the entire data structure

as we would have to do in an array. There are times when Dictionaries are very useful.

	var name_of_integers = [Int : String]()
	name_of_integers[1] = "One"
	name_of_integers[10] = "Ten"
	name_of_integers[20] = "Twenty"

	var airports = [String: String]()

	airports["YYZ"] = "Toronto Pearson Intl. Airport"
	airports["JFK"] = "John F Kennedy Intl. Airport"

	print("The airports dictionary contains \(airports.count) items

	for (airportCode, airportName) in airports {
    	print("\(airportCode): \(airportName)")
	}

	for airportName in airports.values {
    	print("Airport name: \(airportName)")
	}




### Practice Excercises

Create an array of fruits. Then loop over the array and print them.

Create a dictionary of your friends' name and birthday.

print the above.


### Homework and Reading ( If you wish )

- Read the chapter on Collection Types in the Swift Book. 

- Arrays

- Dictionaries

- Classes

- Work out the examples



### OOP - What is a Class? What is an Object? Why do we need this?

- Swift is an Object Oriented Language

- A class is a blueprint, a template

- It bundles data and functionality together

- This is important to understand because IOS and the GUI is class based



### Lets create a class

[Swift Class](https://developer.apple.com/library/content/documentation/Swift/Conceptual/Swift_Programming_Language/ClassesAndStructures.html#//apple_ref/doc/uid/TP40014097-CH13-ID82)

	class Shape {

		func init(name: String)
		self.name = name

		func What_am_I() -> String {
			print("I am a \(self.name)")
			return self.name
		}

	}

	//main program

	var circle = Shape(name: "Circle")
	circle.What_am_I()

	var square = Shape(name: "Square")
	square.What_am_I()

	//notice how each variable maintains its own data




### Using Classes

- We will see how everything in IOS is a class. The Buttons, dropdowns, Controllers are all pre-created classes for us.

- We are given instructions ( Documentation ) on how to use and access these classes

- There are *functions* on how to put data into variables and how to fetch them

- Enumerations is also a type of class. But we wont get into it today.



### Example - A Calculator Class

	class Calculator {
    var operations =  Dictionary<String,String>()
    
    init() {
        self.operations["+"] = "Add"
        self.operations["-"] = "Subtract"
    }

    func operate_on(_ number_1: Int, _ number_2 : Int, action: String) -> Int {
        var operation = self.operations[action]
        if operation == "Add" {
            return number_1 + number_2
        }
        else if operation == "Subtract" {
            return number_1 - number_2
        }
        else { return   0 }
    }

   } //end class



### Continued

	var c = Calculator()

	var res = c.operate_on(10, 20, action: "+")

	print(res)

	var diff = c.operate_on(50,10, action: "-")

	print(diff)

	//pass data into the class. 
	//The class handles the functionality. We provide documentatation on how to do the work

Create this class in Playgrounds



### MVC - The Model View Controller Paradigm

- The Model controls the data

- The View controls the display

- The Controller handles the logic and brains of the program

Example: In the Calculator class. 

The Model is your dictionary which holds on to the data ie when you get an operation, you need to take some action

The View is how you display the result. It can be print() or with decimals etc.

The Controller is the brains. It decides the logic. If the data recieved is "+" then lets add the numbers, else lets do something else.



### MVC - Continued

- MVC is modular. The Model should not worry about display and vice versa

- Display should not care how the model is created. It gets data and all it does is show it

- The Controller does care about the Model and the display. It is the middle man.



### Let the fun and games begin!  Demo Begins.

- We shall start with how to create a Story Board

- All the code will be available on GIT. Going forward no more slides.

- Links to the code [HERE] After we are done.
	



### Day 2: Story Boards

- The StoryBoard is the main UI of the IOS App

- This is where you create your scenes, buttons and all user interactions

- Behind the scenes these are nothing but Classes which we interact with

- Now lets get familiar with XCode. The Design assistant, StoryBoard and How to Build the app.



### XCode

- Create a Single View Application. Open up Xcode and select New Project.

- Save it in a place you will remember or you usually put your code in.

- Choose Swift. Leave everthing else blank

- Enter your (fake) Company name etc into Xcode to create a new Project. 
	


### Building our Todo List App

- Lets remove the existing View Controller File

- Create a new file - of class Tableview Controller

- Remove the existing View controller file in Story board

- Add a new Tableview Controller scene to our story board

- Hook up the file to the new TblView Controller scene.



### Create our Models

- Remember data should live in a model. The design does not care about where we store this.

- We will use an Array to store out todo-list. So yeah, its a simple model. An array.

- Later on we can create more complicated models - but for our purpose this is fine.

- We will store out todo items in an array. reminder of array:

        items = ['Go to the gym', 'Visit Grandma', 'Do laundry', 'Dont forget to chill!']


### Hook up the Model to the UI

- So once we have our data the rest is easy peasy!

- We just need to hook up our model ie data to the UI right. 

- The TableViewController is a Class in IOS Core. Which means we have certain functions given
to us to do this.

- The rows in a Tableview are actually an array. The first row starts at 0... and goes on.

- So if we store our data in an array, our first item, goes in the first row



### IndexPath and Rows

- Each indexpath is a row

- So to populate data we get the indexpath and row and use that to pull out our data from the model

- Lets do that on the Tableview Controller

- The method we will use is :

        func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell

- Like magic - our data is automatically populated in our Tableview



### Add, and Delete operations

- Of course to be a useful app we need to add certain functionality

- We will see how we can Add rows and Delete rows. Edit is more complicated. We can do that another time.



### What is a Segue

- Segues are how you travel between one scene to another scene and send and recieve data back

- To add a row we need to create a View Controller that can accept data. A Text Box. 

- When we hit "SAVE" it should come back to our main parent but with our newly added todo item.

- Again these are functions provided to us by IOS. We need to use them correctly and most of the work is done already.

- We will create a new View Controller to Add data. Lets do it!!


### Adding Data


- Create a new Cocoa Touch File, Choose View Controller and name it appropriately.

- In your storyboard lets create a new View Controller.

- Lets Hook them up together.

- OK - We have our data entry detail scene.


### Save data and Add to the todo list

- We will work on Adding the data to the model.

- Displaying the newly added data onto the screen.



### Next: Delete data from the todo.

- Reverse of add. Remove data from the model

- Display new data structure ( without above ) on the screen.



### Lets run and put this on our phone

Run and install on Phone.

Congrats!!! You have an Iphone App. 