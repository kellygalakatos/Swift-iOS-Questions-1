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
A: 
### Q7: Explain forced unwrapping.
A: 
### Q8: What problems does delegation solve?
A: 
### Q9: What is the difference between a delegate and an NSNotification?
A: 
### Q10: How is an inout parameter different from a regular parameter?
A: 
### Q11: Explain View Controller lifecycle events order? What are the events and in what order do they occur?
A: 
### Q12: What is downcasting? Provide an example.
A: 
### Q13: What is upcasting? Provide an example.
A: 
### Q14: What is the nil coalescing operator and when do you use it?
A: 
### Q15: What is optional chaining and when do you use it?
A: 
### Q16: Explain subscripts.
A: 
### Q17: What is DispatchGroup?
A: 
### Q18: What is the difference ANY and ANYOBJECT?
A: 
### Q19: What is the difference between the filter and map functions?
A: 
### Q20: When do you use optional chaining vs. if let or guard?
A: 
### Q21: Describe the different ways to pass data in Swift.
A: 
### Q22: What is an “app ID” and a “bundle ID”?
A: 
### Q23: Explain what a property observer is and how/when it is used.
A: 
### Q24: What is URLSession?
A: 
### Q25: Explain rethrows keyword.
A: 
### Q26: Explain type inference.
A: 
### Q27: Explain @objc inference.
A: 
### Q28: What is the “mutating” keyword?
A: 
### Q29: What is the difference the Stack and the Heap?
A: 
### Q30: Explain tuples.
A: 
### Q31: What’s the difference between the frame and the bounds?
A: 
### Q32: What is a raw value for an enum and give an example of how it can be used.
A: 
### Q33: What is the difference between synchronous and asynchronous tasks?
A: 
### Q34: What are the states of an iOS App?
A: 
### Q35: What is a UIStackView and how is it used?
A: 
