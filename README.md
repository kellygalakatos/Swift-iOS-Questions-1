# Swift-iOS-Questions-1

### Q1: What is the difference “strong” and “weak”?
A: Swift's memory management system is Automated Reference Counting, and memory is disposed of, or deallocated, when there are no strong references to it. Having a strong reference prevents the object from getting eliminated on compile time. Strong reference increases the reference count, and weak decreases it and allows an object to become nil.
### Q2: Explain the “lazy” keyword.
A: Making a lazy property means that the value is not initialized until the property is first used. Therefore, it eliminates the need for allocating memory to the property if it is never used.
### Q3: What are benefits of “guard”?
A: Guard allows you to execute code if a set of conditions are not met. Upon the first variable that is not assigned successfully or any one of the conditions for the code to run successfully is false, it immediately goes into the block of code which you can return or print error messages, or the like.
### Q4: What is the difference non-escaping and escaping closures ?
A: In non-escaping closures, the closure is passed into the function, it executes, and then it is returned in a normal chronological order. However, escaping closures allow the code to "escape" the body of the function and return to it later. This is common in asychronous calls when a dispatch queue needs to hold on to the closure and have it exist elsewhere in memory until it is ready to execute.
### Q5: What is ARC?
A: ARC is Automatic Reference Counting which is Swift's memory management tool. It provides memory for new instances and frees up the memory when it is no longer needed. The way that it tracks whether or not the memory is needed is by if anything is referencing it. There needs to be at least one strong reference to an object for it to not be freed of its memory space. If it is nil upon execution, the memory will be deallocated.
### Q6: How does memory management work in Swift?
A: ARC is Automatic Reference Counting which is Swift's memory management tool. It provides memory for new instances and frees up the memory when it is no longer needed. The way that it tracks whether or not the memory is needed is by if anything is referencing it. If something references it, the type gets incremented, and if something dereferences it, the type gets decremented within ARC.
### Q7: Explain forced unwrapping.
A: Force unwrapping an Optional means that you are extracting its value, whether or not it is nil. This can potentially cause errors if it is equal to nil, which is why force unwrapping should only be done with caution.
### Q8: What problems does delegation solve?
A: Delegation is a design pattern that enables a class or structure to hand off (or delegate) some of its responsibilities to an instance of another type. It helps to add functionality without carrying the burden.
### Q9: What is the difference between a delegate and an NSNotification?
A: Delegates hand out responsibilities and communicate with the protocols that are aiding in functionality for them; however NSNotification is more of a one-way messaging system used to broadcast data.
### Q10: How is an inout parameter different from a regular parameter?
A: All parameters passed into a Swift function are constants, so you can’t change them. If you pass in a parameter as inout, they can be changed inside your function, and those changes reflect in the original value outside the function.
### Q11: Explain View Controller lifecycle events order? What are the events and in what order do they occur?
A:   1.	init(coder:)
2.	(void) loadView
3.	(void) viewDidLoad
4.	(void) viewWillAppear
5.	(void) viewDidAppear
6.	(void) didReceiveMemoryWarning
7.	(void) viewWillDisappear
8.	(void) viewDidDisappear
### Q12: What is downcasting? Provide an example.
A: Downcasting is the (fundamentally unsafe) act of casting an object as one of its subclasses in an attempt to invoke methods or read members that only exist on that subclass. Ex: if let pet = pet as? Cat 
### Q13: What is upcasting? Provide an example.
A: Upcasting is the act of casting an object as one of its superclasses. It usually works if what you are upcasting is a subtype of the latter. Ex. if let pet = cat as? Pet
### Q14: What is the nil coalescing operator and when do you use it?
A: The nil-coalescing operator (a ?? b) unwraps an optional a if it contains a value, or returns a default value b if a is nil. Ex. var colorNameToUse = userDefinedColorName ?? defaultColorName
### Q15: What is optional chaining and when do you use it?
A: Optional chaining is a process that allows you to run blocks of code if the value of the variable/method/etc. is not nil. You would use it if you are unsure of whether or not the optional will contain nil at that time.
### Q16: Explain subscripts.
A: It would be essentially the index of an array, the key in a dictionary, or something that helps you immediately access a particular item in a list. 
### Q17: What is DispatchGroup?
A: Allows you to run a group of processes asynchronously so that it is more efficient.
### Q18: What is the difference ANY and ANYOBJECT?
A: ANY can reference any type at all, including optionals, but ANYOBJECT, quite literally can only reference class instances, or objects.
### Q19: What is the difference between the filter and map functions?
A: Map allows you to perform the same operation to every element of an array, while filter allows you to filter the array based on set criteria.
### Q20: When do you use optional chaining vs. if let or guard?
A: Optional chaining executes a block of code if the value is not nil, but an if let or guard sets you up to handle the “else” statement if it is nil 
### Q21: Describe the different ways to pass data in Swift.
A: Passing data between view controllers can happen if you do the prepare(for: segue…) function and then perform the segue. You can also instantiate an instance of the next view controller and assign its attributes, and then push the view controller on top of the current one. You can have separate external files that can be referenced from all view controllers.
### Q22: What is an “app ID” and a “bundle ID”?
A: The app ID identifies me as a developer, while the bundle ID identifies my specific project.
### Q23: Explain what a property observer is and how/when it is used.
A: You can write blocks of code to execute when a property is set, such as Will Set and Did Set, to monitor a property and to see when the value was changed.
### Q24: What is URLSession?
A: It allows for an app to create one session in which you are interacting with the URL, such as uploading and downloading data, in the background asynchronously with other tasks occurring.
### Q25: Explain rethrows keyword.
A: This allows a function to throw an error, not based on the content of the actual function, but based on one or more of the function’s parameters.
### Q26: Explain type inference.
A: Type inference in Swift is nice because you can assign a value to a variable without specifying what type it is, and Swift will infer what it is.
### Q27: Explain @objc inference.
A: When you use @objc inference, it allows you to run some objective C code inside of your Swift file.
### Q28: What is the “mutating” keyword?
A: It modifies the properties of the struct when it is placed in front of a function inside of a struct.
### Q29: What is the difference the Stack and the Heap?
A: Heaps are more fluid and flexible as they handle dynamic memory allocation, but stacks are more precise and restricted, but much faster because they handle static memory allocation.
### Q30: Explain tuples.
A: A tuple is a group of values that acts as one. It is one way to return multiple items from a function.
### Q31: What’s the difference between the frame and the bounds?
A: Both are expressed as a location in (x,y) and size in height and width, but the bounds are relative to its own View, while the frame is relative to the superView it is contained within.
### Q32: What is a raw value for an enum and give an example of how it can be used.
A: The raw value is the number associated with each member of the enum, so if there is an enum: enum Car: Int {
     case red, yellow, green, blue
} you can reference the green car by just calling 2.
### Q33: What is the difference between synchronous and asynchronous tasks?
A: Synchronous implies sequential order, while asynchronous tasks can all run as the same time because they are not dependent upon on another and increase efficiency.
### Q34: What are the states of an iOS App?
A: Not running, suspended, background, inactive, and active
### Q35: What is a UIStackView and how is it used?
A: UIStackView is an interface method of laying out a collection of methods in a nice, uniform manner that adjusts well to all devices.
