# clean-code
JavaScript coding standards to keep your code clean

Keep your #CleanCode while working with JavaScript. Here are some points on which developer should focus upon:

## For Comparison 
✓ : === <br>
✗ : ==  

## Declare Variable
✓ : let | const
✗ : var

## Always use semi-colon at line end
✓ : (;)

## Naming Convention:
let  : camelCase (ex. firstName)
const : UPPER_CASE_SNAKE_CASE | camelCase (Depends on use editable or non-editable) (ex. GOOGLE_API_KEY, userInformation)
Class Name: PascalCasing (ex. MyClass)
Function Name: camelCase (ex. findById)

## Contacting Strings:
✗ : let fullName = firstName + " " + lastName;
✓ : let fullName = `${firstName} ${lastName}`   ||  firstName.concat(lastName);

## Use Arrow Function (where it's possible):
✓ : const multiply = (a, b) => a * b;
✗ : var multiply = funtion(a,b){ return a*b; };

## Always use curly braces around control statement:
✓ : if(yourBooleanValue){
		doSomething();
	}
✗ : if(yourBooleanValue) doSomething();

## Start curly braces from same line:
✗ : if(yourBooleanValue) 
	{
		doSomething();
	}
✓ : if(yourBooleanValue){
		doSomething();
	}

## Use Ternary Operation where ever you can
✓ : return isValid ? buy() : error()     ||    return (isValid ? buy : error)(); 
✓ : if(!isValid){           //If you don't want to use ternary
		return error();
	}
	return buy();
✗ : if(isValid){
		return buy();
	}else{
		return error();
	}

## Avoid unneeded ternary statements:
✓ : const boo = a || b;
✗ : const boo = a ? a : b;

## Max Line length in function or in file:
✓ : files make not more than 80 lines of code
✓ : functions make of 15 lines of code

## Use Default Parameters:
✓ : const sum = (a = 0, b = 0) => a + b; 
✗ : var sum = function(a,b){ return a + b; }

## Switch Statement
✓ : Should use break in each case
✓ : Should use default

## Use short hand code for Boolean
✓ : if(isValid) {}   ||   if(!isValid) {}
✗ : if(isValid === true) {}  ||   if(isValid === false) {}

## Only use one variable per declaration
✓ : let firstName = 'John';
	  let lastName = 'Doe';
✗ : let firstName = 'John', lastName = 'Doe';
