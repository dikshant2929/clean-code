# clean-code
JavaScript coding standards to keep your code clean

Keep your #CleanCode while working with JavaScript. Here are some points on which developer should focus upon:

## For Comparison 
✓ : === <br>
✗ : ==  

## Declare Variable
✓ : let | const<br>
✗ : var

## Always use semi-colon at line end
✓ : (;)

## Naming Convention:
let  : camelCase (ex. firstName)<br>
const : UPPER_CASE_SNAKE_CASE | camelCase (Depends on use editable or non-editable) (ex. GOOGLE_API_KEY, userInformation)<br>
Class Name: PascalCasing (ex. MyClass)<br>
Function Name: camelCase (ex. findById)<br>

## Contacting Strings:
✗ : let fullName = firstName + " " + lastName;<br>
✓ : let fullName = `${firstName} ${lastName}`   ||  firstName.concat(lastName);<br>

## Use Arrow Function (where it's possible):
✓ : const multiply = (a, b) => a * b;<br>
✗ : var multiply = funtion(a,b){ return a*b; };

## Always use curly braces around control statement:
✓ : if(yourBooleanValue){<br>
		doSomething();<br>
	}<br>
✗ : if(yourBooleanValue) doSomething();

## Start curly braces from same line:
✗ : if(yourBooleanValue) <br>
	{<br>
		doSomething();<br>
	}<br>
✓ : if(yourBooleanValue){<br>
		doSomething();<br>
	}<br>

## Use Ternary Operation where ever you can
✓ : return isValid ? buy() : error()     ||    return (isValid ? buy : error)(); <br>
✓ : if(!isValid){           //If you don't want to use ternary <br>
		return error();<br>
	}<br>
	return buy();<br>
✗ : if(isValid){<br>
		return buy();<br>
	}else{<br>
		return error();<br>
	}<br>

## Avoid unneeded ternary statements:
✓ : const boo = a || b;<br>
✗ : const boo = a ? a : b;<br>

## Max Line length in function or in file:
✓ : files make not more than 80 lines of code<br>
✓ : functions make of 15 lines of code<br>

## Use Default Parameters:
✓ : const sum = (a = 0, b = 0) => a + b; <br>
✗ : var sum = function(a,b){ return a + b; }<br>

## Switch Statement
✓ : Should use break in each case<br>
✓ : Should use default<br>

## Use short hand code for Boolean
✓ : if(isValid) {}   ||   if(!isValid) {}<br>
✗ : if(isValid === true) {}  ||   if(isValid === false) {}<br>

## Only use one variable per declaration
✓ : let firstName = 'John';<br>
    let lastName = 'Doe';<br>
✗ : let firstName = 'John', lastName = 'Doe';<br>
