# JavaScript-Class-Inheritance

Inheritance is a key aspect seen in JavaScript Class

Inheritance allows the defining of classes taking all of the functionality from a parent class

and allowing the addition of more functionalities

Inheritance is an essential concept allowing code reusability in programming

The below illustrations shows Inheritance in JavaScript with examples:

<pre>
<code>

// parent class
class Person {
    constructor(name, location, age, maritalStatus) {
        this.name = name;
        this.location = location;
        this.age = age;
        this.maritalStatus = maritalStatus;
    }
    // defining a Method() greet
    greet(){
        console.log(`Hello ${this.name}, I have been told you are from ${this.location} and you are ${this.age}
         Years Old and your Marital Status is ${this.maritalStatus}. Welcome to Our Company.`);
    }
}
// Inheriting parent class
class Student extends Person {

}
// Now there is creating an object student1 to access the greet() method and Student {} class
let Student1 = new Student('Danny Votes King', 'Nairobi, Kenya', 23 , 'Married');
Student1.greet();
// Here, we are creating an object student1 to access the greet() method and Student {} class
let Student2 = new Student ('Lizzie', 'Amsterdam', 25, 'Single');
Student2.greet();


// Using the super() keyword in denoting the parent class
// Example
// Parent class

class People {
    constructor (theName, theAge, theLocation) {
        this.theName = theName;
        this.theAge = theAge;
        this.theLocation = theLocation;
    }
    theGreeting() {
        console.log(`Hello ${this.theName}, I see you are from ${this.theLocation} and you are ${this.theAge} Years. Welcome`);
    }
}
// Inheritng parent class
class theStudent extends People {
    constructor(theName, theAge, theLocation){;
    console.log("Creating theStudent Class");
    // call the super class constructor and pass in the name of the parameter
    super(theName, theAge, theLocation);
    }
}
let theStudent1 = new theStudent('Danny Votes King', 23, 'London');
theStudent1.theGreeting();


// Overriding Method or Property
// If a child class has the same Method or Property name as the parent class
// It will use the method and property of the child class
// This concept is called overriding

// Parent class
class ThePerson {
    constructor(ourName) {
        this.ourName = ourName;
        this.occupation = "Employed";
    }
    ourGreeting(){
        console.log(`Hello ${this.name}.`);
    }
}
// Inheriting parent class
class OurStudent extends ThePerson {
    constructor(ourName) {
        // call the super class constructor and pass in the name parameter
        super(ourName);

        // overriding occupation property
        this.occupation = 'Business Owner';
    }
    // overriding ThePerson's method
    ourGreeting() {
        console.log(`Hello Success ${this.ourName}.`);
        console.log(`Occupation: ` + this.occupation);
    }
}
let h = new OurStudent('Danny Votes King');
h.ourGreeting();



// The occupation property and the ourGreeting() method are present in parent ThePerson class and child OurStudent class
// Hence, the OurStudent class overrides the occupation property and the ourGreeting() method

// USES OF INHERITANCE

// 1.   Allows for code resuability as the child class can inherit all functionalitoes of the parent class
// 2.   Allows for cleaner code and easier maintanance as once functionality is developed, one can simply inherit it. No need for reinventing the wheel
// 3. Allows for adding one's [own] functionalities as part of Child class
// 4. Allows one to inherit only useful functionalities and also define other useful or required functionalities
</code>
</pre>
// OUTPUTS

<pre>
Hello Danny Votes King, I have been told you are from Nairobi, Kenya and you are 23
         Years Old and your Marital Status is Married. Welcome to Our Company.
Hello Lizzie, I have been told you are from Amsterdam and you are 25
         Years Old and your Marital Status is Single. Welcome to Our Company.
Creating theStudent Class
Hello Danny Votes King, I see you are from London and you are 23 Years. Welcome
Hello Success Danny Votes King.
Occupation: Business Owner
</pre>
