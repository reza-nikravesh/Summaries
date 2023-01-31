##Types

* Tuple

* Literal Type
* Type Alias

*  Unknown Type

*  Never Type

##Compiler

* watch
* include
* exclude

##Class

### Define property tip:
	// use this
	class Person {
	  constructor(public name: string) {
	  }
	}
	// instead of this 
	class Person {
		name:string;
	 	 constructor( name: string) {
	 	 this.name=name;
	  }
	}
### Access modifiers:
* **public** : default for all properties and methods . 
* **private** : properties with this access modifier is not available out of the class
* **readonly** : you cannot change the value of variable or property after initialization . Like const.
* **protected** : If you use "private" access modifier the properties are not available out of the class including the extended classes . but if you use "Protected" you can use properties inside the extended classes .


### Static
You cannot use static property like this.property . 
if you wanna use it inside for example constructor function you should use the class name instead of this keywodr 

	class Person{
    static age:number;
	constructor(age:number){
	this.age=age; ❌
	Person.age=age; ✅
	 }
	 }
	 
	 
### Interface tip:
If you want to define a type for function you have to do like this:
	`type AddFn =(a:number)=>number`
But if you want to handle this using interface you can do this :
`interface AddFn{
	(a:number):number
}`	
this is an especial syntax for interface and not behave like object-form