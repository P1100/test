# PROGRAMMING LANGUAGE SYNTAX COMPARISON
> A syntax summary, which also compares the differences between each programming language.
* List of languages
  * Python, Javascript, Ruby, Java, C#, C/C++
## Table of Contents
- [Interpreted Language](#interpreted-language)
- [Compiled Language](#compiled-language)
- [Hello World](#hello-world)
- [Comments](#comments)
- [Variable declaration int](#variable-declaration-int)
- [Variable declaration float](#variable-declaration-float)
- [Variable declaration None](#variable-declaration-none)
- [Strings](#strings)
- [Boolean](#boolean)
- [Arithmetic Operators](#arithmetic-operators)
- [Comparison Operators](#comparison-operators)
- [Logical Operators](#logical-operators)
- [Getting Input](#getting-input)
- [Bitwise Operators](#bitwise-operators)
- [Increment](#increment)
- [Arrays and Lists](#arrays-and-lists)
- [Conditional Statement](#conditional-statement)
- [Loops](#loops)
- [Instantiation](#instantiation)
- [Functions](#functions)
- [Higher order functions](#higher-order-functions)
- [Hash Tables](#hash-tables)
- [Destructuring](#destructuring)
- [Spread Operator](#spread-operator)
- [Rest parameters](#rest-parameters)
- [Class](#class)
- [Importing Libraries](#importing-libraries)
- [Type Conversions](#type-conversions)
- [Find Data Type](#find-data-type)
- [String Concatenation](#string-concatenation)
- [JSON](#json)
- [Program Entry Point](#program-entry-point)
- [Swapping values](#swapping-values)
- [Error Handling](#error-handling)
- [Custom Error](#custom-error)
- [Asynchronous](#asynchronous)
- [Math](#math)
- [Date and Time](#date-and-time)
- [Access modifier](#access-modifier)
- [Properties](#properties)
- [File System](#file-system)
- [Language Specific](#language-specific)

## Interpreted Language
### Dynamically-typed Language: resolution of types, members, properties, methods are done at run-time
#### lose compile-time checking, have to write more unit tests to ensure app behaves properly at run-time
* python, javascript, ruby
## Compiled Language
### Statically-typed Language: resolution of types, members, properties, methods are done at compile-time
#### trying to access a method that is not defined in an object when compiling the app will get an immediate error feedback
* java: compiled to bytecode then interpreted by Java virtual machine into machine code
* c#: compiled to an Intermediate Language (IL), which is then translated by the Common Language Runtime (CLR) into machine code
  * from .NET 4, dynamic capability was added to improve interoperability with COM & Dynamic languages
* c++: compiled into machine code
## Hello World
### python 2
```python
print "Hello World"
```
### python 3
```python
print("Hello World")  # "Hello World\n"
print("Hello", "World", sep="/")  # "Hello/World"
print("Hello World", end="")  # "Hello World"
```
### javascript
```javascript
console.log("Hello World");
```
### Java
```java
public class HelloWorld {
  public static void main(String args[]) {
    System.out.println("Hello World");
  }
}
```
### c#
```c#
public class HelloWorld {
  public static void Main() {
    System.Console.WriteLine("Hello World");  // adds new line after printing
    System.Console.Write("Hello World");  // no new line is added after printing
  }
}
```
### c++
```c++
#include <iostream>

int main() 
{
    std::cout << "Hello, World!";
    return 0;
}
```
[back to top](#table-of-contents)
## Comments
### python 2 & 3
```python
# Single line comment
    
"""
multi-line comments
"""
```
### javascript
```javascript
// Single line comment

/*
multi-line comments
*/
```
### Java
```java
// Single line comment

/*
multi-line comments
*/
```
### c#
```c#
// Single line comment

/*
multi-line comments
*/
```
### c++
```c++
// Single line comment

/*
multi-line comments
*/
```
[back to top](#table-of-contents)
## Variable declaration int
* integer ...-2, -1, 0, 1, 2...
### python 2 
```python
# int: -2147483648 ~ 2147483647
integer_name = 123
# long: -9223372036854775808L ~ 9223372036854775807L
long_name = 123L  # int beyond int size will automatically be converted to long
```
### python 3
```python
# python 3: int and long are combined into int
integer_name = 123
```
### javascript ES5
```javascript
// method 1
var integer_name;
integer_name = 123;  // accessible within the function

// method 2
var integer_name = 123;
```
### javascript ES6
```javascript
// method 1
let integer_name;
integer_name = 123;  // accessible only within the block {}

// method 2
let integer_name = 123;

// method 3
const integer_name = 123;  // variable value cannot be reassigned
```
### Java
```java
// public/private/protected static final byte/short/int/long integer_name = 123;
/* 
public: visible to all classes
protected: visible to class they belong and any subclasses
private (most restricted): visible only to class they belong
static: can be accessed without creating a class instance
final: constant value, value cannot be changed
*/

// byte: -128 ~ 127, 8 bits
byte byte_name = 123;

// short: -32768 ~ 32767, 16 bits
short short_name = 123;

// int: -2147483648 ~ 2147483647, -2_147_483_648 ~ 2_147_483_647, 32 bits
int integer_name; integer_name = 123;
int integer_name = 123;  // default is visible within the same package

// long: -9223372036854775808L ~ 9223372036854775807L, can use _ same as int, 64 bits
long long_name = 123l;
long long_name = 123L;
```
### c#
```c#
// var can be used to handle declarations when the data type is unknown
// once a variable is declared with var, the variable cannot be reassigned to a different data type
var variableName = 123;
variableName = "123";  // error CS0029: Cannot implicitly convert type `string' to `int'

// byte: -128 ~ 127, 8 bits
byte byteName = 123;  // type Byte
System.Byte byteName2 = 123;

// short: -32768 ~ 32767, 16 bits
short shortName = 123;  // type Int16
System.Int16 shortName2 = 123;

// int: -2,147,483,648 ~ 2,147,483,647
int integerName1 = 123;  // type Int32
int integerName2 = int.MaxValue;  // 2147483647
System.Int32 integerName3 = 123;

// Add const before variable declaration to make it a constant
const int integerName3 = 123;

// long: -9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807
long longName1 = 123;  // type Int64
long longName2 = long.MaxValue;  // 9223372036854775807
System.Int64 longName3 = 123;

// decimal: max value 79,228,162,514,264,337,593,543,950,335
decimal decimalName1 = 123;  // type Decimal
decimal decimalName2 = 123m;
decimal decimalName3 = decimal.MaxValue;  // 79228162514264337593543950335
System.Decimal decimalName4 = 123;

// use System.Numerics.BigInteger for larger values (need add references to System.Numerics.dll)
```
### c++
```c++
// const unsigned char/short/int/long/long long integer_name = 123;
/* 
const: constant value, value cannot be changed
integer are signed by default: can assign both positive & negative values
unsigned integer (use when dealing with bit values): 0 ~ ...
  e.g. char: -128 ~ 127
  e.g. unsigned char: 0 ~ 255  // 128 + 127 = 255
*/

// char: 1 byte, -128 ~ 127, use C code to print "#include＜stdio.h＞ printf("%d", char_name);"
// 1 char has 8 bits
char char_name;
char_name = 123;

// similar to the rest of int variable declaration

// short/short int: 16 bits, 2 bytes, -32768 ~ 32767
short short_name;
short_name = 123;

short int short_name; short_name = 123;

// similar to the rest of int variable declaration

// int: 16 bits, 4 bytes, -2147483648 ~ 2147483647
int integer_name;
integer_name = 123;  // uninitialized

int integer_name = 123;  // C-like initialization

int integer_name (123);  // Constructor initialization

int age {123};  // C++11 list initialization syntax

// long/long int: 32 bits, 4 bytes, -2147483648 ~ 2147483647 bytes
long long_name;
long_name = 123;

long int long_name;
long_name = 123;

// similar to the rest of int variable declaration

// long long/long long int: 64 bits, 8 bytes, -9223372036854775808 ~ 9223372036854775807
long long long_name;
long_name = 123;

long long int long_name; long_name = 123;

// similar to the rest of int variable declaration
```
[back to top](#table-of-contents)
## Variable declaration float
* float, double
### python 2 & 3
```python
float_name = 1.123
float_name = 0.1123e1  # equals to 1.123
float_name = 0.1123E1  # equals to 1.123
float_name = 1123e-3  # equals to 1.123
float_name = 1123E-3  # equals to 1.123
```
### javascript ES5
```javascript
var float_name = 1.123;
```
### javascript ES6
```javascript
let float_name = 1.123;
const float_name = 1.123;
```
### Java:
```java
// float: 32 bits, 4 bytes
float float_name = 1.123f;  // have 7 decimal digits
float float_name = (float) 1.123;

// double: 64 bits, 8 bytes
double double_name = 1.123d;  // have 16 decimal digits
double double_name = 1.123;
```
### c#
```c#
// float: 32 bit max value with 7 decimals of precision 3.402823E+38
float floatName1 = 1.123f;  // type Single
float floatName2 = float.MaxValue;  // 3.402823E+38
System.Single floatName3 = 1.123f;

// double: 64 bit max value with 15 decimals of precision 1.79769313486232E+308
double doubleName1 = 1.123d;  // type Double
double doubleName2 = 1.123;  // all floats are double by default
double doubleName3 = double.MaxValue;  // 1.79769313486232E+308
System.Double doubleName4 = 1.123;
```
### c++
```c++
// float: 4 bytes
float float_name;
float_name = 1.123;  // have 7 decimal digits

// similar to the rest of int variable declaration

// double: 8 bytes
double double_name;
double_name = 1.123;  // have 15 decimal digits

// similar to the rest of int variable declaration

// long double: 12 bytes
long double double_name;
double_name = 1.123;  // have 19 decimal digits

// similar to the rest of int variable declaration
```
[back to top](#table-of-contents)
## Variable declaration None
### python 2 & 3
```python
variable_name = None

# nan in python
import math
math.inf - math.inf  # nan
```
### javascript
```javascript
// undefined is reserved for variables whose values have not yet been set.
let variable_name; // undefined

//null is reserved for variables whose values are explicitly nothing — instead of just “not yet defined.”
let variable_name2 = null;

// NaN is a special numeric value meaning “Not a Number”
let variable_name3 = NaN;
```
### Java
### c#
```c#
string stringName = null;
string stringName2 = String.Empty;

// method 1: use the nullable method
Nullable<int> integerName1 = null;

// method 2: value type requires ? during declaration
int? integerName2 = null;
```
### c++
[back to top](#table-of-contents)
## Strings
### python 2 & 3
```python
string_name = "string"
string_name = 'string'
# back slash not required, but will produce a new line if not given
string_name = """multi-line \
string\
"""

# raw strings (ignore escape characters)
string_name = r"\n raw string"  # "\n raw string"

len(string_name)  # 6

# Character unicode point
# only accepts 1 character
ord("b")  # 98

# reverse string
string_name = string_name[::-1]  # "gnirts"

string_name = string_name.upper()  # "GNIRTS"
string_name = string_name.lower()  # "gnirts"

# capitalize string
string_name = string_name.title()  # "Gnirts"

# Replace string in string, string_name.replace(old, new, max)
string_name = string_name.replace("G", "xxx")  # "xxxnirts"
string_name = string_name.replace("x", "g", 1)  # "gxxnirts"

# Find character or string in string and return the index of the 1st character, return -1 if not found
string_name.find("x")  # 1
string_name.find("v")  # -1

# string slicing
# extract characters from a string, from start position to but not including end position
new_string_name = string_name[1:4]  # "xxn"

# Split strings, string_name.split(separator, max)
string_name = string_name.split()  # ["gxxnirts"]  only works for string without spaces
string_name = "test string"
string_name1 = string_name.split()  # ["test", "string"]
string_name2 = string_name.split("s")  # ["te", "t ", "tring"]
string_name3 = string_name.split("s", 1)  # ["te", "t string"]

# Split string into an array of letters
string_name4 = list(string_name)  # ['t', 'e', 's', 't', ' ', 's', 't', 'r', 'i', 'n', 'g']

# Remove empty spaces
string_name = "    string    "
# remove all left spaces
string_name1 = string_name.lstrip()  # "string    "
# remove all right spaces
string_name2 = string_name.rstrip()  # "    string"
# remove all spaces
string_name3 = string_name.strip()  # "string"

# Check if string has alphabet and integer characters
string_name3.isalnum()  # False
string_name = "123"
string_name.isalnum()  # True
string_name = "s 123"
string_name.isalnum()  # False
string_name = "s123"
string_name.isalnum()  # True

# Check if string has all alphabet characters
string_name3.isalpha()  # True
string_name = "A e"
string_name.isalpha()  # False
string_name = "a2"
string_name.isalpha()  # False

# Check if string has all digit characters
string_name = "123"
string_name.isdigit()  # True
string_name = "12 3"
string_name.isdigit()  # False
string_name = "12d"
string_name.isdigit()  # False

# Join an array of string elements
arr = ["a", "b"]
"_".join(arr)  # "a_b"
```
### javascript ES5
```javascript
var stringName = "string";
var stringName = 'string';
// back slash required
var stringName = "multi-line \
string";

stringName.length;  // 6

// Character unicode point
string.charCodeAt(stringIndex)
"abc".charCodeAt(1)  // 98

// reverse string
stringName.split("").reverse().join("");  // "gnirts"

stringName = stringName.toUpperCase();  // "GNIRTS"
stringName = stringName.toLowerCase();  // "gnirts"

// capitalize string
stringName = stringName.charAt(0).toUpperCase() + stringName.slice(1);  // "Gnirts"

// replace string with string, stringName.replace(old, new)
stringName = stringName.replace("G", "xxx");  // "xxxnirts"

// extract characters from a string, from start position to but not including end position
newStringName = stringName.substring(1, 4); // "xxn"
    
// Split string into arrays
stringName = "test string"
stringName1 = stringName.split()  // ["test string"]
stringName2 = stringName.split("")  // ['t', 'e', 's', 't', ' ', 's', 't', 'r', 'i', 'n', 'g']
stringName3 = stringName.split("s")  // ["te", "t ", "tring"]
```
### javascript ES6  // Almost all of ES5 are included in ES6
```javascript
// back slash not required, but will produce a new line if not given
var stringName = `multi-line \
string`;
let stringName = "string";
const stringName = "string";

// raw strings (ignore escape characters)
String.raw`\n raw string`;  // "\n raw string"
```
### Java
```java
// character: 16 bits, 2 bytes, only 1 letter or symbol, must use single quotes ''
char charName = 'a';
char charName = '\u0061';  // unicode character for the letter a

// strings: must use double quotes ""
String stringName = "string";
String stringName = "multi-line " +
                     "string";
```
### c#
* Strings (immutable)
    * each operation that appears to be modifying a string is actually creating a new string
    * modifying a string repeatedly can cause a significant performance penalty
    * when to use string
        * when number of changes that your app will make to a string is small
            * string builder might offer negligible or no performance improvement
        * when performing a fixed number of concatenation operations is required
            * compiler might combine the concatenation operations into a single operation
        * when performing extensive search operations while building a string is required
            * string builder lacks search methods (IndexOf, StartsWith)
            * thus will need to convert string builder to a string for these operations
            * this can negate the performance benefit from using string builder
```c#
// character: 16 bits
char charName1 = 'a';  // type Char
char charName2 = '\u0061';  // unicode character for the letter a
System.Char charName3 = 'a';

// strings
string stringName = "string";  // type String
System.String stringName2 = "string";

// multiline strings
// method 1
string multilineString1 = "multi-line\n"
+ "string";
// method 2
string multilineString2 = @"multi-line
string";
// method 3
string multilineString3 = System.String.Join(
  System.Environment.NewLine,
  "multi-line",
  "string"
);


// raw strings (ignore escape characters
string rawString = @"\n raw string";  // "\n raw string"


// check if string is empty
String.IsNullOrEmpty(stringName);  // False
String.IsNullOrEmpty("");  // True

// check for white space or empty
String.IsNullOrWhiteSpace(stringName); // False
String.IsNullOrWhiteSpace("  "); // True
String.IsNullOrWhiteSpace(""); // True
String.IsNullOrWhiteSpace(" test "); // False


// get length of a string
stringName.Length;  // 6


// get index of the 1st character or word in a string
stringName.IndexOf("s");  // 0
stringName.IndexOf("unknown");  // -1


// convert string to uppercase
stringName.ToUpper();  // "STRING"


// convert string to lowercase
stringName.ToLower();  // "string"


// split string to an array of characters
stringName.ToCharArray();  // ['s', 't', 'r', 'i', 'n', 'g']


// split string into an array of strings (must have separator)
stringName.Split('r');  // ["st", "ing"]


// get substring from a string (if length is not declared, the entire string from startIndex onwards will be returned)
int startIndex = 0;
int length = 2;
stringName.Substring(startIndex, length);  // "str"


// replace string with another string, stringName.Replace(old, new);
stringName.Replace("test", "newTest");  // "  newTest  "


// comparing strings
string s1 = "test";
string s2 = "test";
string s3 = "test1".Substring(0, 4);
object s4 = s3;
Console.WriteLine("{0} {1} {2}", object.ReferenceEquals(s1, s2), s1 == s2, s1.Equals(s2));  // True True True
Console.WriteLine("{0} {1} {2}", object.ReferenceEquals(s1, s3), s1 == s3, s1.Equals(s3));  // False True True
Console.WriteLine("{0} {1} {2}", object.ReferenceEquals(s1, s4), s1 == s4, s1.Equals(s4));  // False False True


// check if a string starts with a character or words
string sampleString = "some random words";
sampleString.StartsWith("some");  // True

// check if a string ends with a character or words
sampleString.EndsWith("words");  // True


// remove white spaces from both left and right
string stringName3 = "  test  ";
stringName3.Trim();  // "test"
// remove white spaces from left
stringName3.TrimStart();  // "test  "
// remove white spaces from right
stringName3.TrimEnd();  // "  test"


// string slicing from start index
// count is the number of characters to delete from the start index
int startIndex = 3;
int count = 3;
stringName.Remove(startIndex, count);  // "str"
stringName.Remove(startIndex);  // "str"
stringName.Remove(startIndex, 2);  // "strg"
```
* String builder (muttable)
    * maintains a buffer to accommodate expansions to the string
    * new data is appended to the buffer if room is available
        * otherwise, a larger buffer is allocated
        * data from the original buffer is copied to the new buffer
        * then the new data is appended to the new buffer
    * when to use string builder
        * when expecting an unknown number of changes to a string at design time (when using a loop to concatenate a random number of strings that contain user input)
        * when expecting to make a significant number of changes to a string
```c#
// Declaration
// method 1
System.Text.StringBuilder builder = new System.Text.StringBuilder();  // ''
// method 2
using System.Text;  // import the prefix
var builder2 = new StringBuilder();  // ''
// method 3
var builder3 = new StringBuilder("starting string");  // "starting string"


// check if string builder is empty
// method 1
if (builder == 0) System.Console.WriteLine("true");  // "true"
// method 2
if (System.String.IsNullOrEmpty(builder.ToString())) 
  System.Console.WriteLine("true");  // "true"


// append an array of similar characters
builder.Append('-', 3);  // "---"

// append a new line in string
builder.AppendLine();  // new line is counted as 1 character

// append a string
builder.Append("Header");
/*
"---
Header"
*/


// replace a character with a new character or a string with new string
builder.Replace('-', '+');
builder.Replace("er", "ing");
/*
"+++
Heading"
*/


// remove characters from startIndex for totalCharacters
int startIndex = 0;
int totalCharacters = 3;
builder.Remove(startIndex, totalCharacters);
/*
"
Heading"
*/


// insert an array of similar characters at index
builder.Insert(startIndex, new string('+', 4));
/*
"++++
Heading"
*/


// get character of string builder at index
builder[0];  // '+'
```
### c++
```c++
// character: only have 1 character, must use single quotes ''
char charName;
charName = 'a';

char charName = 'a';
char charName ('a');
char charName {'a'};

// strings
// C-style strings: an ARRAY of characters, must use double quotes ""
// THIS IS NOT A TRUE STRING, IT IS AN ARRAY OF CHARACTERS!!!!!!!
char * stringName = "string";
const char * stringName = "string";  // const is normally used
char stringName[] = "string";  // creates array of 7 chars, last char is null "\0"
char stringName[7] = "string";  // need give 7 slots for chars and null char
char stringName[7] = {'s', 't', 'r', 'i', 'n', 'g', 0};  // no 0 = error
char stringName[7] = {'s', 't', 'r', 'i', 'n', 'g', '\0'};  // no '\0' = error

//C++ strings: must add at the top "#include＜string＞", must use double quotes ""
#include＜string＞
std::string stringName;
stringName = "string";

// back slash not required, but can use if want to
std::string stringName = "multi-line"
                          "string";
std::string stringName ("string");
```
[back to top](#table-of-contents)
## Boolean
### python 2 & 3
* boolean_name = True
* boolean_name = False
* not True  # False
* not False  # True
### javascript ES5
* var boolean_name; boolean_name = true;
* var boolean_name = false;
* !true  // false
* !false  // true
* truthy: "xxx", 1, -1, 2.5, true
* falsey: false, 0, "", null, undefined, NaN
### javascript ES6
* let boolean_name; boolean_name = true;
* let boolean_name = false;
* const boolean_name = true;
### Java
* boolean boolean_name = true;
* boolean boolean_name = false;
### c#
* // type Boolean
* bool booleanName = true;  // displayed as True when printed
* bool booleanName = false;  // displayed as False when printed
* System.Boolean booleanName = false;
### c++: 8 bits
* bool boolean_name; boolean_name = true;  // produces a 1 output
* bool boolean_name = false;  // produces a 0 output
* bool boolean_name (true);
* bool boolean_name {false};

[back to top](#table-of-contents)
## Arithmetic Operators
### python 2
* addition: +
* subtraction: -
* multiplication: *
* division: 3.0/2  # output 1.5, 3/2 output 1
* modulus: %
* exponent: **
* floor division: 3//2  # output 1
### python 3
* division: 3/2  # output 1.5
* floor division: 3//2  # output 1
### javascript
* addition: +
* subtraction: -
* multiplication: *
* division: 3/2  // output 1.5
* modulus: %
* exponent: **
* floor division: Math.floor(3/2)  // output 1
### Java
* addition: +
* subtraction: -
* multiplication: *
* division: double double_name = 3.0/2;  // output 1.5, 3/2 output 1
* modulus: %
* exponent: Math.pow(3, 2);  // output 9
* floor division: int integer_name = 3/2;  // output 1
### c#
* addition: +
* subtraction: -
* multiplication: *
* division: 3.0/2;  // output 1.5, 3/2 output 1
* modulus: %
* exponent: Math.Pow(3, 2);  // output 9
* floor division: 3/2;  // output 1
### c++
* addition: +
* subtraction: -
* multiplication: *
* division: double double_name = 3.0/2  // output 1.5, 3/2 output 1
* modulus: %
* exponent:
    * must add this to the top "#include＜cmath＞"
    * int integer_name = pow(3, 2);  // output 9
* floor division: 3/2  // output 1

[back to top](#table-of-contents)
## Comparison Operators
### python 2 & 3
* ==  # condition is True if both operand have equal contents
```python
list1 = []
list2 = []
list1 == list2  # True
```
* is  # condition is True if both operand points to the same identical object
```python
list1 = []
list2 = []
list1 is list2  # False

list1 = None
list2 = None
list1 is list2  # True
```
* !=  # condition is True if both operand do not have equal contents
* is not  # condition is True if both operand do not points to the same identical object
* ＜＞ # py2 only, condition is True if both operands do not equal contents
* ＞  # condition is True if right operand is less than left operand
* ＜  # condition is True if left operand is less than right operand
* ＞=  # condition is True if right operand is less than or equal to left operand
* ＜=  # condition is True is left operand is less than or equal to right operand
### javascript
* ==  // string or int will be automatically converted before comparison, only checks the value
    * var x = 5;
        * x == 5;  // is true
        * x == "5"  // is also true
* ===  // string or int will NOT be converted before comparison, checks both the value and type
    * var x = 5;
        * x === 5;  // is true
        * x === "5"  // is false
* !=
* !==
* ＞
* ＜
* ＞=
* ＜=
### Java
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=
### c#
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=
### c++
* ==
* !=
* ＞
* ＜
* ＞=
* ＜=

[back to top](#table-of-contents)
## Logical Operators
### python 2 & 3
* and
* or
* not
### javascript
* &&  // and
* ||  // or
* !  // not
* truthy and falsey examples
    * truthy1 && truthy2  // truthy2
    * falsey && truthy  // falsey
    * truthy && falsey  // falsey
    * falsey1 && falsey2  // falsey1
    * truthy1 || truthy2  // truthy1
    * truthy || falsey  // truthy
    * falsey1 || falsey2  // falsey2
### Java
### c#
* &&  // and
* ||  // or
* ^  // exclusive or
* !  // not
### c++
[back to top](#table-of-contents)
## Getting Input
### python 2
```python
raw_input("What's your name?")

# input must be the same data type as xxx else return an error
input(xxx)
```
### python 3
```python
input("What's your name?")
```
### javascript
```javascript
// install readline-sync package locally via npm i readline-sync
var readlineSync = require('readline-sync'); // import package
var getInput = readlineSync.question("What's your name?");
```
### Java
### c#
```c#
// print question
System.Console.WriteLine("What's your name?");
// get input
string name = System.Console.ReadLine();
```
### c++
[back to top](#table-of-contents)
## Bitwise Operators
### python 2 & 3
```python
# Each digit is 1 bit, all bitwise operators converts to signed 32-bit integers, except for zero-fill right shift which results to unsigned 32 bit integer
a = 60  # 60 = ...0011 1100
b = 13  # 13 = ...0000 1101
c = 9  # 9 = ...0000 1001
# & is binary AND, return 1 if both a and b are 1
a & b  # 12 = ...0000 1100

# | is binary OR, return 1 if either a and or b HAVE a 1
a | b  # 61 = ...0011 1101

# ^ is binary XOR, return 1 if both a and b are not 1 or 0
a ^ b  # 49 = ...0011 0001

# ~ is binary ones complement, invert everything, 1 change to 0 and vice versa
~a  # -61 = ...1100 0011

# << is binary left shift, shift everything to the left by n digit(s)
a << 2  # 240 = ...1111 0000

# >> is binary right shift, shift everything to the right by n digit(s)
a >> 2  # 15 = ...0000 1111
c >> 2  # 3 = ...0000 0010, count the 1s
c = -9  # -9 = ...1111 0111
c >> 2  # -3 = ...1111 1101, count the 0s

# Zero fill right shift, shift everything to the right by n digits(s), leftmost will add n 0s
def zero_fill_right_shift(val, n):
    return (val >> n) if val >= 0 else ((val + 0x100000000) >> n)
zero_fill_right_shift(9, 2)  # 2 = ...0000 0010, count the 1s
c = -9  # -9 = ...1111 0111
zero_fill_right_shift(-9, 2)  # 1073741821 = 0011...1111 1101, count the 0s
```
### javascript
```javascript
// Each digit is 1 bit, all bitwise operators converts to signed 32-bit integers, except for zero-fill right shift which results to unsigned 32 bit integer
let a = 60  // 60 = ...0011 1100
let b = 13  // 13 = ...0000 1101
let c = 9  // 9 = ...0000 1001
// & is binary AND, return 1 if both a and b are 1, count the 1s
a & b  // 12 = ...0000 1100
    
// | is binary OR, return 1 if either a and or b HAVE a 1
a | b  // 61 = ...0011 1101
    
// ^ is binary XOR, return 1 if both a and b are not 1 or 0
a ^ b  // 49 = ...0011 0001
    
// ~ is binary ones complement, invert everything, 1 change to 0 and vice versa, count the 0s
~a  // -61 = ...1100 0011
    
// << is binary left shift, shift everything to the left by n digit(s)
a << 2  // 240 = ...1111 0000
    
// >> is Sign-propagating right shift, a binary right shift, shift everything to the right by n digit(s)
a >> 2  // 15 = ...0000 1111
c >> 2  // 3 = ...0000 0010, count the 1s
c = -9  // -9 = ...1111 0111
c >> 2  // -3 = ...1111 1101, count the 0s
    
// >>> is Zero fill right shift, shift everything to the right by n digits(s), leftmost will add n 0s
c >>> 2  // 2 = ...0000 0010, count the 1s
c = -9  // -9 = ...1111 0111
c >>> 2  // 1073741821 = 0011...1111 1101, count the 0s
```
### Java
### c#
```c#
// & is binary AND, return 1 if both a and b are 1, count the 1s
a & b  // 12 = ...0000 1100
    
// | is binary OR, return 1 if either a and or b HAVE a 1
a | b  // 61 = ...0011 1101
```
### c++
[back to top](#table-of-contents)
## Increment
### python 2 & 3
* x = x + 1  # increment
* x += 1
### javascript
* x = x + 1;  // add 1 now
* x += 1;  // add 1 now
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
### Java
* x = x + 1;
* x += 1;
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
### c#
* x = x + 1;
* x += 1;
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again
### c++
* x = x + 1;
* x += 1;
* ++x;  // preincrement, add 1 now
* x++;  // postincrement, display without addition now then add 1 later when called again

[back to top](#table-of-contents)
## Arrays and Lists
### python 2 & 3
```python
# Empty list
list_name = []
# List with elements
list_name = [1, "one", True]
# Nested lists
list_name = [1, ["two", 3]]


# Find list size
len(list_name)


# Get index of element, return ValueError if element does not exist
list_name.index(element)


# Add element to list (left to right)
list_name.append(element)

# Add element to list at index
list_name.insert(index, element)

# Extends list by appending elements from the iterable
list_name = [1, 2]
list_name.extend([3, 4])  # [1, 2, 3, 4]


# Access an element
list_name[index]

# Modify an element
list_name[index] = element


# Remove element from list (right to left)
list_name.pop()

# Remove element from list at index
list_name.pop(index)

# Remove any element from list at element
list_name.remove(element)

# Method 1: remove all elements
del list_name[:]
# Method 2: remove all elements
list_name = []
# Method 3: remove all elements, only in python 3
list_name.clear()


Slice notation
# items start through stop-1
list_name[start:stop]

# items start through the rest of the array
list_name[start:]

# items from the beginning through stop-1
list_name[:stop]

# a copy of the whole array
list_name[:]

# start through not past stop, by step
list_name[start:stop:step]
list_name = [1, 2, 3, 4, 5]
list_name[::2]  # [1, 3, 5]

# last item in the array
list_name[-1]

# last two items in the array
list_name[-2:]

# everything except the last two items
list_name[:-2]

# all items in the array, reversed
list_name[::-1]

# the first two items, reversed
list_name[1::-1]

# the last two items, reversed
list_name[:-3:-1]

# everything except the last two items, reversed
list_name[-3::-1] 


# Reverse an array
list_name.reverse()


# Merge 2 or more arrays together
new_list = list_name + list_name2


# Sort an array in ascending order
list_name = [2, 3, 1, 4]
# method 1
list_name2 = sorted(list_name)  # [1, 2, 3, 4]
# method 2
list_name.sort()  # [1, 2, 3, 4]

# sort an array of dictionaries in ascending order
dict_name = [{"key_name": value1}, {"key_name": value2}]
# sort by value
dict_name2 = sorted(dict_name, key=lambda k: k["key_name"])


# Sort an array in descending order
# method 1
list_name2 = sorted(list_name2, reverse=True)  # [4, 3, 2, 1]
# method 2
list_name.sort(reverse=True)  # [4, 3, 2, 1]

# sort an array of dictionaries in descending order
# sort by value
dict_name2 = sorted(dict_name, key=lambda k: k["key_name"], reverse=True)
```
### javascript
```javascript
// Method 1: empty list
var list_name = [];
// Method 2: empty list
var list_name = new Array();
// create list of empty elements
var list_name = new Array(3); // [empty, empty, empty]
// List with elements
var list_name = [1, "one", true];
var list_name = new Array(3).fill("-") // ["-", "-", "-"]
// Nested lists
var list_name = [1, ["two", 3]];
var list_name = new Array(3).fill(new Array(2).fill("-")) // [["-", "-"], ["-", "-"], ["-", "-"]]
    
    
// Modify an element
list_name[index] = element;
    
// Access an element
list_name[index];
    
    
// Remove element from list (right to left)
list_name.pop();
// Remove element from list (left to right)
list_name.shift();
// Remove number of elements (left to right) from index and insert new elements (left to right)
list_name.splice(index, number_of_element);

    
// Add element to list (left to right)
list_name.push(element);
// Add element to list (right to left)
list_name.unshift(element);
// Add element to list at index (left to right)
list_name.splice(index, 0, new_element1, new_element2...);
// Add & Remove elements to & from list at index (left to right)
list_name.splice(index, number_of_element, new_element1, new_element2...);
    
    
// Return the selected elements in an array, as a new array object
list.name.slice();
// Return the elements starting at the given 1st argument,
// and ends at, but does not include, the given 2nd argument
list_name.slice(1, 3);
list_name.slice(1);  // if 1 argument is given, return all elements from array from the 1st argument index
    
    
// Find list size
list_name.length;
// Remove all elements
list_name = [];
    
    
// Merge 2 or more arrays together
list_name1 = [1, 2, 3];
list_name2 = [4, 5, 6];
new_list = list_name1.concat(list_name2);
    
    
// Get index of element, return -1 if not present
list_name = ["element1", "element2", "element1"]
list_name.indexOf("element1")  // returns index of 0
list_name.indexOf("element1", 1);  // returns index of 2
list_name.indexOf("element1", 2);  // also returns index of 2
list_name.indexOf("element1", 0);  // returns index of 0
    
    
// Sort array in ascending order
list_name = [2, 3, 1, 4];
list_name.sort();  // [1, 2, 3, 4]
    
// Sort array in descending order
list_name.sort((a, b) => (b - a));  // [4, 3, 2, 1]
// use .reverse() if elements are strings
list_nameStr = ["a", "b", "c"];
list_nameStr.reverse(); // ["c", "b", "a"]
    
    
// Determine whether an array contains a specified element
list_name = ["a", "b", "c", "a"]
console.log(list_name.includes("b"))  // true
    
// Determine whether an array contains a specified element from starting index
console.log(list_name.includes("b", 2)  // false
console.log(list_name.includes("a", 2)  // true

// Flatten nested arrays
list_name = [1, 2, [3, 4]];
list_name.flat() // [1, 2, 3, 4]

// Check if all elements in array pass the conditional check
function helper(currentValue) {
 return currentValue < 3;
}
list_name = [1, 2, 3, 4];
list_name.every(helper); // false
list_name = [1, 2];
list_name.every(helper); // true
```
### Java
```java
// Arrays: can only have 1 data type: string, int, etc.
// Empty string array of desired array size
String[] string_array = new String[length_of_desired_array];
// New string array with elements inside
String [] string_array = new String [] {string1, string2,...};  // Method 1
String[] string_array = {string1, string2,...};  // Method 2

// Add string array element, limited to array size
// Modify string array element value
string_array[index] = element;

// Access an element
string_array[index];

// Find array size
string_array.length;


// Arraylists: can only have 1 data type: string, int, etc.
import java.util.ArrayList;  // Must import to use

// Empty string arrayList
ArrayList<String> string_arrayList = new ArrayList<String>();

// Add string element to string arrayList (left to right)
string_arrayList.add(element);

// Modify an element at index
string_arrayList.set(index, element);

// Access an element
string_arrayList.get(index);

// Remove element from arrayList at index
string_arrayList.remove(index);

// Find arrayList size
string_arrayList.size();

// Remove all elements
string_arrayList.clear();
```
### c#
* Arrays: can only have 1 data type: string, int, etc. (size cannot be modified after declaration)
```c#
// Empty string array of desired array size
string[] stringArray = new string[lengthOfDesiredArray];
// New string array with elements inside
string [] stringArray2 = new string [] {string1, string2, ...};  // Method 1, size is determined by number of elements declared
string [] stringArray2 = new string [2] {string1, string2};  // Method 2, size is determined by the array size declared
string[] stringArray3 = {string1, string2, ...};  // Method 3, size is determined by number of elements declared
string[] stringArray5 = new[] {string1, string2, ...};  // Method 4
var stringArray6 = new[] {string1, string2, ...};  // Method 5, use var to auto determine data type

// Multi-dimensional Rectangular Arrays
int[] rectArray = new int[3, 5];
int[] rectArray2 = new int[3, 5] {
  {1, 2, 3, 4, 5},
  {6, 7, 8, 9, 10},
  {11, 12, 13, 14, 15}
};

// Multi-dimensional Jagged Arrays
int[] jaggedArray = new int[3][];  // create an array of 3 empty arrays
jaggedArray[0] = new int[4];  // create an array of size 4
jaggedArray[1] = new int[5];  // create an array of size 5
jaggedArray[2] = new int[3];  // create an array of size 3

// Add string array element, limited to array size
// Modify string array element value
stringArray[index] = element;


// Access an element
stringArray[index];
rectArray2[index1, index2];
jaggedArray[0][0];


// Find array size
string[] strArr = {"a", "b", "c"};
strArr.Length;  // 3


// Find index of an element in an array
string element = "a";
int index = System.Array.IndexOf(strArr, element);  // 0


// Clear the element in the array (0 for int, false for bool, null for other objects), exclude the endIndex value
int startIndex = 0;
int endIndex = 1;
System.Array.Clear(strArr, startIndex, endIndex);


// Copy the elements into a new array
int firstFewElem = 3;
string[] copiedStrArr = new string[3];
System.Array.Copy(strArr, copiedStrArr, firstFewElem);


// Sort (ascending order)
System.Array.Sort(strArr);


// Reverse (only works on sorted arrays)
System.Array.Reverse(strArr);  // ["c", "b", "a"]
System.Array.Reverse(strArr);  // ["a", "b", "c"]


// Join elements of an array into a string
System.String.Join("", strArr);  // "abc"
System.String.Join(",", strArr);  // "a,b,c"
```
* List (dynamic array)
```c#
// Empty int array of desired array size
System.Collections.Generic.List<int> intList = new System.Collections.Generic.List<int>();  // empty list
System.Collections.Generic.List<int> intList2 = new System.Collections.Generic.List<int>() {1, 2, 3, 4};  // list with values
// import to write less code when declaring
using System.Collections.Generic;
List<int> intList3 = new List<int>();  // empty list
List<int> intList4 = new List<int>() {1, 2, 3, 4};  // list with values


// Add 1 new element to the list (left to right)
intList4.Add(5);  // [1, 2, 3, 4, 5]

// Add a range of elements to the list with an array
intList4.AddRange(new int[3] {6, 7, 8});  // [1, 2, 3, 4, 5, 6, 7, 8]


// Find index of an element in a list (return -1 if element is not found)
intList4.IndexOf(2);  // 1

// Find last index of elements with similar values in a list
int[] intList5 = new List<int>() {1, 2, 1, 3};
intList5.LastIndexOf(1);  // 2


// Get length of list
intList4.Count;  // 8


// Remove an element at element in list
intList4.Remove(2);  // [1, 3, 4, 5, 6, 7, 8]


// Remove an element at index of list
intList4.RemoveAt(0);  // [3, 4, 5, 6, 7, 8]


// Remove all elements from the list
intList4.Clear();  // [];
```
* ArrayList (dynamic list of multiple data types, does not offer the best performance)
```c#
// Empty array list
System.Collections.ArrayList list = new System.Collections.ArrayList();  // empty list


// Add 1 new element to the list (left to right)
list.Add(1);  // [1]
list.Add("abc")  // [1, "abc"]

// methods are similar to List
```
### c++
```c++
// Arrays
// Empty int array of desired array size
int int_array[length_of_desired_array];
// New int array with elements inside
int int_array [length_of_desired_array] {element1, element2,...};  // size declared
int int_array[] = {element1, element2,...};  // size automatically calculated

// Assign int element, limited to array size
// Modify int element value
int_array[index] = element;

// Access an element
int_array[index];

// Find array size: size of array (bytes) / size of an element of an array (bytes)
sizeof(int_array) / sizeof(int_array[0]);


// Vectors: a type of dynamic array
#include <vector>  // Must import to use

// Empty int vector of desired vector size, each element of 0 value will automatically be included
std::vector <int> int_vector (length_of_desired_array);
// New int vector with elements inside
std::vector <int> int_vector {element1, element2,...};
// New int vector with length of desired array and all value in parameter
// Method 1
std::vector <int> int_vector (length_of_desired_array, constant_value_for_all_elements);
// Method 2
std::vector <int> int_vector;
int_vector.assign(length_of_desired_array, constant_value_for_all_elements);

// Assign int element
int_vector[index] = element;

// Access an element
int_vector[index];
int_vector.at(index);

// Add element to vector (left to right), vector size will automatically increase
int_vector.push_back(element);
// Add element to vector at index
std::vector<int>::iterator it;  // Must create iterator for inserting or emplacing to work
it = int_vector.begin()  // Set it at index 0
// insert method: copies or moves the elements into the container by calling copy constructor or move constructor
int_vector.insert(it + index, element);  // Add element at index
// emplace method: elements are constructed in place, no copy or move operations are performed (better performance)
int_vector.emplace(it + index, element);  // Add element at index

// Remove element from vector at index
std::vector<int>::iterator it;  // Must create iterator for erase to work
it = int_vector.begin()  // Set it at index 0
int_vector.erase(it + index)  // Remove element at index
int_vector.erase(it + index, it + index)  // Remove a range of elements in the vector
// Remove element from vector (right to left)
int_vector.pop_back();  // does not return value

// Find vector size
int_vector.size();

// Resize vector
int_vector.resize(length_of_desired_array);

// Remove all elements
int_vector.clear();
```
[back to top](#table-of-contents)
## Conditional Statement
### python 2 & 3
```python
# If else statement
if condition_a:
    do_A
elif condition_b:
    do_B
else:
    do_something_else


# Ternary operator
do_A if condition_a else do_B


# Switch Statement is not available in python, but can create similar function
def switch(choice):
    case = {
        1: do_A,
        2: do_B,
    }
    case.get(choice, do_something_else)
    
 
# comparing between 2 objects (array, dictionaries, etc.) is allowed
x = [1, 2, 3]
y = [1, 2, 3]
x == y  # returns True
```
### javascript
```javascript
// If else statement
if (condition_a) {
    do_A;
} else if (condition_b) {
    do_B;
} else {
    do_something_else;
}


// Ternary operator
condition_a ? do_A : do_B;


// Switch statement
switch(choice) {
    case choice_A:
        do_A;
        break;
    case choice_B:
        do_B;
        break;
    default:
        do_something_else;
}

// comparing between 2 objects (array, object, etc.) is NOT allowed
var x = [1, 2, 3]
var y = [1, 2, 3]
x === y ? true : false;  // returns false
// solution: use JSON.stringify()
JSON.stringify(x) === JSON.stringify(y) ? true : false  // return true
```
### Java
```java
// If else statement
if (condition_a) {
    do_A;
} else if (condition_b) {
    do_B;
} else {
    do_something_else;
}


// {} not required if statement is a single line
if (condition_a)
    do_A;  // Single line statement
else if (condition_b)
    do_B;  // Single line statement
else
    do_something_else;  // Single line statement


// Ternary operator
condition_a ? do_A : do_B;


// Switch statement
switch(choice) {
    case choice_A:
        do_A;
        break;
    case choice_B:
        do_B;
        break;
    default:
        do_something_else;
        break;  // not required, but good to have in Java
}
```
### c#
```c#
// If else statement
if (condition_a) {
    do_A;
} else if (condition_b) {
    do_B;
} else {
    do_something_else;
}


// Ternary operator
condition_a ? do_A : do_B;


// Switch statement
switch(choice) {
  case choiceA:
    doA;
    break;
  case choiceB:
    doB;
    goto doSomethingSpecial;  // go to a special case that is written outside the switch statement and run it (not advised to use it
  default:
    do_something_else;
    break;
}

doSomethingSpecial:
  doingSomething;
```
### c++
```c++
// If else statement
if (condition_a) {
    do_A;
} else if (condition_b) {
    do_B;
} else {
    do_something_else;
}


// {} not required if statement is a single line
if (condition_a)
    do_A;  // Single line statement
else if (condition_b)
    do_B;  // Single line statement
else
    do_something_else;  // Single line statement


// Ternary operator
condition_a ? do_A : do_B;


// Null coalescing operator
return_this_variable_value_if_not_null ?? else_return_this_value


// Switch statement
switch(choice) {
    case choice_A:
        do_A;
        break;
    case choice_B:
        do_B;
        break;
    default:
        do_something_else;
}
```
[back to top](#table-of-contents)
## Loops
### python 2
```python
# While loop
# declare_initial_conditional_value
i = 0
# Set condition
while i<5:  # Start from 0 to 4
    do_this
    # Include condition_increment_or_decrement
    i += 1
    # Can use break, continue, and pass statements to add additional functionality, or not use any
    break  # Breaks out of the current closest enclosing loop
    continue  # Goes to the top of the closest enclosing loop
    pass  # Does nothing at all


# For loop
# range() creates a list in python 2
# Looping with xrange()
for i in xrange(5):  # Starts from 0 to 4 (5 - 1)
    do_this
    # Can use break, continue, and pass statements to add additional functionality, or not use any
    break  # Breaks out of the current closest enclosing loop
    continue  # Goes to the top of the closest enclosing loop
    pass  # Does nothing at all
    
# Looping with xrange() and multiple parameters
for i in xrange(0, 5, 2):  # Start from 0 to 4 at every 2 steps (0,2,4)
    do_this
    
# Reverse loop
for i in xrange(4, -1, -1):  # Start from 4 to 0 at every -1 steps
    do_this


# Looping and getting each value
for value in list_name:  # [i1_value, i2_value, i3_value,...]
    print value


# Looping and getting index and value
for index, value in enumerate(list_name):
    print index, value  # output index, value
```
### python 3
```python
# For loop
# Looping with range()
for i in range(5):  # Starts from 0 to (5 - 1)
    do_this
    # Can use break, continue, and pass statements to add additional functionality, or not use any
    break  # Breaks out of the current closest enclosing loop
    continue  # Goes to the top of the closest enclosing loop
    pass  # Does nothing at all
    
# Looping with range() and multiple parameters
for i in range(0, 5, 2):  # Start from 0 to 4 at every 2 steps (0,2,4)
    do_this
    
# Reverse loop
for i in range(4, -1, -1):  # Start from 4 to 0 at every -1 steps
    do_this


# Looping and getting each value
for value in list_name:  # [value1, value2, value3,...]
    print(value)


# Looping and getting index and value
for index, value in enumerate(list_name):
    print(index, value)  # output index, value
```
### javascript ES5
```javascript
// While loop
// declare_initial_conditional_value
var i = 0;
// Set condition
while (i<5) {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}

// Do While loop
var i = 0;
do {
  do_this;
  i++;
} while (i<5);

// For loop
for (var i=0; i<5; i++) {  // Start from 0 to 4
    do_this;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}

// Reverse loop
for (var i=4; i>=0; i--) {  // Start from 4 to 0
    do_this;
}

// forEach loop
// Looping through a list while calling a function
list_name.forEach(function(value, index, list){  // do not need to include all 3 parameters, but must be in order
    console.log(index, value, list);  // outputs index value list
});
```
### javascript ES6: Use let in loops when declaring
```javascript
// For of loop
// Looping and getting each value
for (let value of list_name) {  // [value1, value2, value3,...]
    console.log(value);  // output value
}
// Looping and getting index and value
for (let index_and_value of list_name.entries()) {
    console.log(index_and_value);  // output a list [index, value]
}

// For in loop
for (let index in list_name) {
    console.log(list_name[index]);
}
// For in loop normally used to get values from objects (hash table, dictionaries) than to arrays
// object = {key1:value1, key2:value2,...}
for (let key in object) {
    console.log(object[key]);  // outputs value, normally calling this way will not output value from objects
}
```
### Java
```java
// While loop
// declare_initial_conditional_value
int i = 0;
// Set condition
while (i<5) {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}

// Do while loop: execute first before setting conditions
// declare_initial_conditional_value
int i = 0;
do {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
// Set condition
} while (i<5);

// For loop
for (int i=0; i<5; i++) {  // Start from 0 to 4
    do_this;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}
// Reverse loop
for (int i=4; i>=0; i--) {  // Start from 4 to 0
    do_this;
}
```
### c#
```c#
// While loop
// declare_initial_conditional_value
int i = 0;
// Set condition
while (i<5) {  // Start from 0 to 4
  do_this;
  // Include condition_increment_or_decrement;
  i++;
  // Can use break or continue to add additional functionality, or not use any
  break;  // Breaks out of the current closest enclosing loop
  continue;  // Goes to the top of the closest enclosing loop
}


// Do while loop: execute first before setting conditions
// declare_initial_conditional_value
int i = 0;
do {  // Start from 0 to 4
  do_this;
  // Include condition_increment_or_decrement;
  i++;
// Set condition
} while (i<5);


// For loop
for (int i=0; i<5; i++) {  // Start from 0 to 4
  do_this;
  // Can use break or continue to add additional functionality, or not use any
  break;  // Breaks out of the current closest enclosing loop
  continue;  // Goes to the top of the closest enclosing loop
}
// Reverse loop
for (int i=4; i>=0; i--) {  // Start from 4 to 0
  do_this;
}


// For each loop: cycles through every item in an array or collection (List)
// Modifications of an array or collection is not allowed, need to use normal loops
string stringName = "a random string of characters";

foreach(char c in stringName) {
  do_this;
}
```
### c++
```c++
// While loop
// declare_initial_conditional_value
int i = 0;
// Set condition
while (i<5) {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}

// Do while loop: execute first before setting conditions
// declare_initial_conditional_value
int i = 0;
do {  // Start from 0 to 4
    do_this;
    // Include condition_increment_or_decrement;
    i++;
// Set condition
} while (i<5);

// For loop
for (int i=0; i<5; i++) {  // Start from 0 to 4
    do_this;
    // Can use break or continue to add additional functionality, or not use any
    break;  // Breaks out of the current closest enclosing loop
    continue;  // Goes to the top of the closest enclosing loop
}
// Reverse loop
for (int i=4; i>=0; i--) {  // Start from 4 to 0
    do_this;
}

// Range-based for loop
// Looping and getting each value
for (int value : int_array) {
    cout << value << endl;  // output value per line
}
// Use auto to automatically detect array data type
for (auto value : array_name) {
    cout  << value << endl;
}

// Infinite for loops
for (;;)
    cout << "This will print forever" << endl;
```
[back to top](#table-of-contents)
## Instantiation
### python 2 & 3
```python
t = Thing()  # everything
```
### javascript
```javascript
v = getValue();  // plain function
t = new Thing();  // instantiation
```
### Java
### c#
```c#
// method 1
ClassName t = new ClassName();  // instantiation
ClassName t = new ClassName(argument);  // instantiation with arguments
// method 2
var t = new ClassName();  // instantiation
var t = new ClassName(argument);  // instantiation with arguments


public class Person {
  public int Age;
}

public class Program {
  public static void Main() {
    Person person = new Person() {Age=20};  // instantiation & assigning value
    increment(person);
    System.Console.WriteLine(person.Age);
  }

  public static void increment(Person person) {
    person.Age += 10;
  }
}
```
### c++
[back to top](#table-of-contents)
## Functions
### python 2 & 3
* Function returns None by default if return statement is not declared
```python
# Normal function, use return to return values
def myFunction():
    do_something

# Normal function with parameters
def myFunction(a):
    do_something_with_a
    
# Default parameters
def myFunction(a=value):
    do_something_with_a
    
# Lambda function: a small anonymous function
# can take any number of arguments, but can only have 1 expression
myFunction = lambda a : do_something_with_a
myFunction = lambda a, b : do_something_with_a_and_b

# Function annotation (python 3)
def get_sum(num1: int, num2: int):
    return num1 + num2
    
# Function annotation with default parameters (python 3)
def get_sum(num1: int=1, num2: int=2):
    return num1 + num2
```
### javascript ES5
* Function returns undefined by default if return statement is not declared
```javascript
// Normal function, use return to return values
function myFunction() {
    do_something;
}
// Normal function with parameters
function myFunction(a) {
    do_something_with_a;
}

// Function expression
let myFunction = function() {
    do_something;
}
// Function expression with parameters
let myFunction = function(a) {
    do_something_with_a;
}

// Arrow function: do not have their own "this" keyword
// 1 line arrow function
let myFunction = () => do_something;  // () at (do_something) not necessary if on single line
// 1 line arrow function with arguments
let myFunction = (a) => (
    do_something_with_a
);
// arrow function, must use return keyword
let myFunction = () => {
    return do_something
};
// arrow function with arguments
let myFunction = (a) => {
    return do_something_with_a
};

// Immediately Invoked Function Expressions (IIFE)
// method 1
(function() {
    do_something;
})();
// method 2
(function() {
    do_something;
}());
// method 3: no returning of value
!function() {
    do_something;
}();
```
### javascript ES6
```javascript
// Default parameters
function myFunction(a=value) {
    do_something_with_a;
}
```
### Java
### c#
```c#
// Normal functions
public static void MyFunction() {
  do_something
}


// Normal function with parameters
public static void MyFunction(dataType a){
  do_something_with_a
}


// Normal function with default parameters
public static void MyFunction(dataType a=value) {
  do_something_with_a;
}


// Lambda  expression
public static void MyFunction() => do_something;


// Lambda expression with parameters
public static void MyFunction(dataType a) => do_something_with_a;

// () not required if single input, use {} if have multi-lines
var MyFunction = (dataType a) => do_something_with_a;
var MyFunction = dataType a => do_something_with_a;
var MyFunction = (dataType a) => { do_something_with_a; };
var MyFunction = dataType a => { do_something_with_a; };

// dataType not required if data type is obvious
var MyFunction = a => do_something_with_a;
var MyFunction = a => { do_something_with_a; };

// Lambda expression with default parameters
public static void MyFunction(dataType a=someValue) => do_something_with_a;
```
### c++
[back to top](#table-of-contents)
## Higher order functions
### python 2
```python
# Map: applies a given function to each item of an iterable (list, tuple etc.) and returns a list of the results
# map(function, iterable, ...)
arr = [1, 2, 3]
def add(n):
    return n + n
map(add, arr)  # return <map object at 0x10473e518>
list(map(add, arr))  # return [2, 4, 6]


# Filter: filter and return a new array based on the conditions
# filter(function, iterable)
arr = [1, 2, 3]
def condition(n):
    if n < 3:
        return n
filter(condition, arr)  # return <filter object at 0x10473e550>
list(filter(condition, arr))  # return [1, 2]


# Reduce: executes a function on each element, resulting in a single output value
arr = [1, 2, 3]
def compute(n, m):
    return n * m
reduce(compute, arr)  # return 6

# Zip: combines 2 arrays or tuples into an array of tuples
arr1 = [1, 2, 3]
arr2 = ["1", "2", "3"]
zpp(arr1, arr2)  # [(1, '1'), (2, '2'), (3, '3')]
```
### python 3
```python
# Reduce: executes a function on each element, resulting in a single output value
arr = [1, 2, 3]
def compute(n, m):
    return n * m
from functools import reduce  # requires import in python 3
reduce(compute, arr)  # return 6

# Zip: must call a list() or tuple() on the zip method
list(zip(s, t))  # [(1, '1'), (2, '2'), (3, '3')]
tuple(zip(s, t)) # ((1, '1'), (2, '2'), (3, '3'))
```
### javascript
```javascript
// Map: create a new array from a current array
// array.map(element, currentIndex, originalArray)
const companies = [
    {name: "company1", category: "industry1"},
    {name: "company2", category: "industry2"}
];
// callback method
const companyNames = companies.map(function(company) {
    return company.name;
}
// arrow function method
const companynames = companies.map((company) => company.name);


// Filter: creates a new array with all elements that pass the condition implemented by the provided function
// array.filter(element, currentIndex, originalArray)
const ages = [age1, age2, age3];
// callback method
const canDrink = ages.filter(function(age) {
    if (condition) {
        return true;
    }
}
// arrow function method
const canDrink = ages.filter(age => condition);


// Reduce: executes a function on each element of the array, resulting in a single output value
// array.reduce(function(accumulator, currentValue){ do_something }, initialValue)
let arr = [1, 2, 3];
// no initial value
arr.reduce(function(accumulator, currentValue) {
    return accumulator + currentValue;
});  // returns a value of 6
/*
accumulator | currentValue | returned value
    1       |       2      |        3
    3       |       3      |        6
*/

// initial value included
arr.reduce(function(accumulator, currentValue) {
    return accumulator + currentValue;
}, 10);  // returns a value of 16
/*
accumulator | currentValue | returned value
    10      |       1      |        11
    11      |       2      |        13
    13      |       3      |        16
*/


// Sort: sorts the elements of an array in place and returns the sorted array
// array.sort(compareFunction)
// if compareFunction is not used, all sorted elements will be sorted based on it's string value
let array = ["1", 30, 4, 21, 100000];
array.sort();  // returns ["1", 100000, 21, 30, 4]

// sort in ascending order
array.sort((a, b) => a - b);  // returns ["1", 4, 21, 30, 100000]

// sort in descending order
array.sort((a, b) => b - a);  // returns [100000, 30, 21, 4, "1"]

// Zip is not available in Javascript, use Maps instead
const arr1 = [1, 2, 3];
const arr2 = ["1", "2", "3"];
function zip(arrays) {
    return arrays[0].map(function(_,i){
        return arrays.map(function(array){return array[i]})
    });
}
zip([arr1, arr2]);  // [[1, '1'], [2, '2'], [3, '3']]
```
### Java
### c++
[back to top](#table-of-contents)
## Hash Tables 
* Hash Tables, Dictionaries, Objects
### python 2 & 3
```python
# Create dictionary
newDict = {}

# Create dictionary and assign key value pairs
# method 1
newDict = {
    "key1": "value1",
    "key2": 123,
    "key3": True,
    "key4": myFunction
}
# method 2
newDict = dict(key1="value1", key2="value2")

# Add or reassign key value pair
newDict["Key"] = "Value"  # method 1
newDict.update({"key": "value"})

# Set multiple keys with a similar value
newKeys = ("key1", "key2", "key3")
newValue = value
newDict = dict.fromkeys(newKeys, newValue)

# Return value of the item with the specified key
# If the key does not exist, insert the key, with the specified value
newVariable = newDict.setdefault("key", "newValue")

# Get value
newDict["key"]  # method 1 # return KeyError if key does not exist
newDict.get("key")  # method 2 # return None if key does not exist

# Get list of keys
list(newDict.keys())

# Get list of values
list(newDict.values())

# Get list of key value tuples
list(newDict.items())

# Loop through Dictionary and get each key
# method 1
for key in newDict:
    print(key)
# method 2
for key in newDict.keys():
    print(key)
    
# Loop through Dictionary and get each value
# method 1
for key in newDict:
    print(newDict[key])
# method 2
for value in newDict.values():
    print(value)
    
# Loop through both keys and values
for key, value in newDict.items():
    print(key, value)
    
# Check if key exists
if "key" in newDict:
    return True
    
# Get dictionary length
len(newDict)

# Copy dictionary
# cannot copy just from dict2 = dict1 as it is just referencing to dict1
# method 1
newDict2 = newDict.copy()
# method 2
newDict2 = dict(newDict)

# Remove items
newDict.pop("key")  # method 1
del newDict["key1"]  # method 2

# Remove last inserted item
newDict.popitem()

# Delete entire dictionary
del newDict  # method 1
newDict.clear()  # method 2
```
### javascript ES5
```javascript
// Objects
// Create object
let newObj = new Object();  // method 1
let newObj = {};  // method 2, literal notation

// Create object and assign values
// keys can only be strings without quotes
let newObj = {
    key1: "stringValue",
    key2: 123,
    key3: true,
    key4: ["array", "array2"],
    key5: {anotherKey: anotherValue},
    key6: function(arg){return do_something_with_arg}
};

// Creates a new object, using an existing object as the prototype of the newly created object
let newObj2 = Object.create(newObj);  // method 1
let newObj2 = Object.assign({}, newObj);  // method 2

// Assign and Reassign values
newObj["key1"] = "newString";  // method 1, bracket notation
newObj.key1 = "newString2";  // method 2, dot notation

// Copy the values of all enumerable own properties from one or more source objects to a target object
// return the target object
const target = { a: 1, b: 2 };
const source = { b: 4, c: 5 };
const newObj = Object.assign(target, source);  // newObj, target = { a: 1, b: 4, c: 5 }

// Get value
newObj["key1"];  // method 1
newObj.key1;  // method 2

// Get an array of keys
Object.keys(newObj);

// Get an array of values
Object.values(newObj);

// Loop through all key value pairs
// must be (key, value)
for (let [key, value] of Object.entries(newObj)) {console.log(`Key: ${key}, Value: ${value}`);}

// Defines a new property directly on an object, or modifies an existing property on an object, and returns the object
// Object.defineProperty(obj, propertyName, descriptor)
Object.defineProperty(newObj, property1, {value: "123", writable: true});  // newObj.property1 = 123

// Seals an object
// prevent addition of properties, however defined properties still can be changed
Object.seal(newObj);

// Freeze an object
// makes the object immutable, meaning no change to defined property allowed, unless they are objects.
Object.freeze(newObj);
```
### javascript ES6
```javascript
// Maps or Hash tables
// Create new Map or hash table
const newDict = new Map();

// Add key value pair data
// keys does not need to be strings, can be numbers, booleans, etc.
newDict.set(key1, value1);
newDict.set(key2, value2);

// Get all keys
newDict.keys();

// Get all values
newDict.values();

// Iterate over Maps to get each key
for (let key of newDict.keys()) {
    console.log(key);
}

// Iterate over Maps to get each value
for (let value of newDict.values()) {
    console.log(value);
}

// Get value
newDict.get(key);

// Get hash table size
newDict.size;

// Check if key value pair exist with key input
newDict.has(key);

// Loop through all key value pairs
// method 1, must be (value, key)
newDict.forEach((value, key) => console.log(`Key: ${key}, Value: ${value}`));
// method 2, must be (key, value)
for (let [key, value] of newDict.entries()) {console.log(`Key: ${key}, Value: ${value}`);}

// Delete key value pair
newDict.delete(key);
// Delete all key value pairs
newDict.clear()


// WeakMap: similar to Map, but all keys must be objects
// Create new weak map
const newDict = new WeakMap();

// Add key value pair data
// key MUST be and Object
newDict.set(obj1, value1);
newDict.set(obj2, value2);

// Get value
newDict.get(obj);

// Delete key value pair
newDict.delete(obj);

// Check if key value pair exist with key input
newDict.has(obj);
```
### Java
### c#
```c#
// method 1 (can be used within a method)
System.Collections.Generic.Dictionary<string, string> _dictionary = new System.Collections.Generic.Dictionary<string, string>();  // declaration
_dictionary["name"] = "xyz" // assigning key value pairs
System.Console.WriteLine(_dictionary["name"]);  // getting value with key


// method 2: indexer (need to create a class)
public class Person {
  private readonly System.Collections.Generic.Dictionary<string, string> _dictionary = new System.Collections.Generic.Dictionary<string, string>();
 
  public string this[string key] {  // this keyword is required
    get { return _dictionary[key]; }
    set { _dictionary[key] = value; }  // value is a keyword
  }
}

class MainClass {
  public static void Main() {
    Person p = new Person();
    p["name"] = "xyz";
    System.Console.WriteLine(p["name"]);  // "xyz"
  }
}
```
### c++
[back to top](#table-of-contents)
## Destructuring
### python 2 & 3
```python
# Tuples
xVariable, yVariable = (xValue, yValue)

# Arrays
xVariable, yVariable = [xValue, yValue]

# String
xVariable, yVariable = "xy"

# Dictionaries
xKey, yKey = {"xKey": xValue, "yKey": yValue}
```
### javascript ES6
```javascript
// Arrays
const [xVariable, yVariable] = [xValue, yValue];

// Objects
const obj = {
    xKey: xValue,
    yKey: yValue
}
// declaring variables
const {xKey, yKey} = obj;  // variable names must be the same as object key names

// assigning different variable names
const {xKey: xNewKey, yKey: yNewKey} = obj;
```
### Java
### c++
[back to top](#table-of-contents)
## Spread Operator
### python 2 & 3
```python
# *args (splat)
# Takes an array and transform (unpacks) it into single values
# Must utitlize all of the element of the array to work
myFunction(a, b, c)  # normal method
myFunction(*Tuple)  # (a, b, c)
myFunction(*List)  # [a, b, c]
myFunction(*String)  # "abc"
myFunction(*Dict)  # {"a": value1, "b": value2}  only utilize the keys

# **kwargs
myFunction(**Dict) # {"a": value1, "b": value2}  utilize both keys and values
```
### javascript ES6
```javascript
// Takes an array and transform (unpacks) it into single values
// Must utitlize all of the element of the array to work
let arr = [a, b, c];
myFunction(a, b, c);  // normal method
myFunction.apply(null, arr)  // using the apply() method
myFunction(...arr);  // spread method

// join multiple arrays together
let arr1 = [a, b, c];
let arr2 = [d, e, f];
let totalArr = arr1.concat(arr2);  // concat method
let totalArr = [...arr1, ...arr2];
```
### Java
### c++
[back to top](#table-of-contents)
## Rest parameters
### python 2 & 3
```python
# *args
# Receive a couple of single values and transform them into an array
def myFunction(*args):
    newArr = args  # args is an array of arugments

# **kwargs
# Receive a couple of keys and values and transform them into a dictionary
def myFunction(**kwargs):
    newDict = kwargs  # kwargs is a dictionary of keys and values
# calling example
myFunction(var1=value1, var2=value2)
```
### javascript ES6
```javascript
// Receive a couple of single values and transform them into an array
function myFunction(...args) {
    let argsArr = args;  // args is an array of arguments
}
```
### Java
### c#
```c#
// hard coded method
public class Calculator1 {
  public in Add(int n1, int n2){
    return n1 + n2;
  }
  public in Add(int n1, int n2, int n3){
    return n1 + n2 + n3;
  }
}


// dynamic method
public class Calculator2 {
  public in Add(int[] numbers){
    int result = 0;
    foreach (int num in numbers)
      result += num
    return result;
  }
}

class MainClass {
  public static void Main(string[] args) {
    Calculator cal = new Calculator2();
    int result = cal.Add(new int[]{1, 2});  // need to initialize a new array
  }
}


// Using Params Modifier
public class Calculator3 {
  public in Add(params int[] numbers){  // add params keyword
    int result = 0;
    foreach (int num in numbers)
      result += num
    return result;
  }
}

class MainClass {
  public static void Main(string[] args) {
    Calculator cal = new Calculator3();
    int result = cal.Add(new int[]{1, 2});  // method 1: initialize a new array
    int result2 = cal.Add(1, 2);  // method 2: only possible if used params keyword
  }
}
```
### c++
[back to top](#table-of-contents)
## Class
### python 2
``` python
class MathClass:
    def __init__(self, arg1, arg2):
        self.arg1 = arg1
        self.arg2 = arg2
        self.total = self.outterAdd(arg1, arg2)
        
    def innerAdd(self, arg3):
        return self.arg1 + self.arg2 + arg3
        
    # Static method knows nothing about the class and just deals with the parameters
    def outterAdd(number1, number2):
        return number1 + number2
    outterAdd = staticmethod(outterAdd)
    
    
test = MathClass(2, 4)
print (test.total)  # 6
print (test.innerAdd(2))  # 8
print (test.outterAdd(3, 7))  # 10
print (MathClass.outterAdd(4, 5)  # 9
```
### python 3
```python
class MathClass:
    def __init__(self, arg1, arg2):
        self.arg1 = arg1
        self.arg2 = arg2
        self.total = self.outterAdd(arg1, arg2)
        
    def innerAdd(self, arg3):
        return self.arg1 + self.arg2 + arg3
        
    # Static method knows nothing about the class and just deals with the parameters
    @staticmethod
    def outterAdd(number1, number2):
        return number1 + number2
    
    
test = MathClass(2, 4)
print(test.total)  # 6
print(test.innerAdd(2))  # 8
print(test.outterAdd(3, 7))  # 10
print(MathClass.outterAdd(4, 5))  # 9


# Using classmethod: method 1
class Person:
    name = "Default name"
    
    @classmethod
    def change_name(clas, new_name):
        cls.name = new_name
        
        
person1 = Person()
print(person1.name)  # Default name
person1.change_name("New name")
print(person1.name)  # New name


# Using classmethod: method 2
class Person2:
    def __init__(self, name):
        self.name = name
    
    @classmethod
    def use_default_name(cls):
        return cls("Default name")
        
     
person2 = Person2("My name")
print(person2.name)  # My name
person3 = Person2.use_default_name()
print(person3.name)  # Default name


# Inheritance
class Employee:  # parent
    raise_amt = 1.04
    
    def __init__(self, first, last, pay):
        self.first = first
        self.last = last
        self.pay = pay
        
    def apply_raise(self):
        self.pay = int(self.pay * self.raise_amt)


class Developer(Employee):  # child
    raise_amt = 1.1
    
    def __init__(self, first, last, pay, prog_lang):
        super().__init__(first, last, pay)  # method 1: implement parent class init method
        Employee.__init__(self, first, last, pay)  # method 2: implement parent class init method
        self.prog_lang = prog_lang


dev = Developer("abc", "xyz", 5000, "Python")
print(dev.pay)  # 5000
dev.apply_raise()
print(dev.pay)  # 5500
```
* python magic method guide
  * https://rszalski.github.io/magicmethods/
### javascript ES5
```javascript
// Constructor
var MathClass = function(arg1, arg2) {
  this.arg1 = arg1;
  this.arg2 = arg2;
}

// Instantiation
var test = new MathClass(2, 4);

// Add method
MathClass.prototype.innerAdd = function(arg3) {
  return this.arg1 + this.arg2 + arg3;
}

test.innerAdd(2);  // 8
```
### javascript ES6
```javascript
// Case 1: normal javascript way
class MathClass {
  constructor(arg1, arg2) {
    this.arg1 = arg1;
    this.arg2 = arg2;
    this.total = this.constructor.outterAdd(arg1, arg2);
  }
  
  innerAdd(arg3) {
    return this.arg1 + this.arg2 + arg3;
  }
  
  // Static method knows nothing about the class and just deals with the parameters
  static outterAdd(number1, number2) {
    return number1 + number2;
  }
}
const test = new MathClass(2, 4);
console.log(test.total);  // 6
console.log(test.innerAdd(2));  // 8
console.log(test.constructor.outterAdd(3, 7));  // 10
console.log(MathClass.outterAdd(4, 5));  // 9

// Case 2: event handlers in React
class MathClass {
  constructor() {
    this.arg1 = 2;
    this.arg2 = 4;
    this.innerAdd = this.innerAdd.bind(this);  // this is required to prevent TypeError
  }
  
  innerAdd(arg3) {
    return this.arg1 + this.arg2 + arg3;
  }
}
const test = new MathClass();
console.log(test.innerAdd(2));  // 8


// Inheritance
class Employee {  // parent
  raiseAmt = 1.04;
    
  constructor(first, last, pay) {
    this.first = first;
    this.last = last;     
    this.pay = pay;
  }
        
  applyRaise() {
    this.pay = parseInt(this.pay * this.raise_amt);
  }
}


class Developer extends Employee {  // child
  raiseAmt = 1.1;
    
  constructor(first, last, pay, progLang) {
    super(first, last, pay)  // implement parent class init method
    this.progLang = progLang;
  }
}


const dev = new Developer("abc", "xyz", 5000, "Javascript")
console.log(dev.pay)  // 5000
dev.applyRaise()
console.log(dev.pay)  // 5500
```
### Java
### c#
* Struct vs Class
  * https://github.com/reshinto/Basic_technologies_revision/blob/master/c%23_summary.md#classes-vs-structs
* Stuct (structures)
```c#
public struct Math {
  public int arg1;
  public int arg2;
  public int total;
  
  // constructor (must have the same name as class name, must have parameters)
  public Math(int arg1, int arg2) {
    // this keyword is not a must, however, variable name must be different from the parameter
    this.arg1 = arg1;
    this.arg2 = arg2;
    this.total = OuterAdd(arg1, arg2);
  }
  
  public int InnerAdd(int arg3) {
    return this.arg1 + this.arg2 + arg3;
  }
  
  public static int OuterAdd(int number1, int number2) {
    return number1 + number2;
  }
}

class MainClass {
  public static void Main() {
    Math test = new Math(2, 4);
    System.Console.WriteLine(test.total);  // 6
    System.Console.WriteLine(test.InnerAdd(2));  // 8
    System.Console.WriteLine(Math.OutterAdd(4, 5));  // 9
  }
}
```
* Class
```c#
public class Math {
  public int arg1;
  public int arg2;
  public int total;
  
  // constructor (must have the same name as class name, no return data type)
  public Math(int arg1, int arg2) {
    // this keyword is not a must, however, variable name must be different from the parameter
    this.arg1 = arg1;
    this.arg2 = arg2;
    this.total = OuterAdd(arg1, arg2);
  }
  
  public int InnerAdd(int arg3) {
    return this.arg1 + this.arg2 + arg3;
  }
  
  public static int OuterAdd(int number1, int number2) {
    return number1 + number2;
  }
}

class MainClass {
  public static void Main() {
    Math test = new Math(2, 4);
    System.Console.WriteLine(test.total);  // 6
    System.Console.WriteLine(test.InnerAdd(2));  // 8
    System.Console.WriteLine(Math.OutterAdd(4, 5));  // 9
  }
}
```
* Inheritance
```c#
public class Employee {  // parent
  protected float raiseAmt = 1.04f;  // use protected to allow modification from other classes
  protected string first;
  protected string last;
  public int pay;  // only public allows display of value externally
    
  public Employee(string first, string last, int pay) {
    this.first = first;
    this.last = last;     
    this.pay = pay;
  }
        
  public void applyRaise() {
    this.pay = System.Convert.ToInt32(this.pay * this.raiseAmt);
  }
}

public class Developer : Employee {  // child
  private string progLang;
    
  public Developer(string first, string last, int pay, string progLang) : base(first, last, pay) { // base initiates the parent's constructor
    raiseAmt = 1.1f;  // this will modifiy the base variable value in the parent class
    this.progLang = progLang;
  }
}

class MainClass {
  public static void Main(string[] args){
    Developer developer = new Developer("abc", "xyz", 5000, "c#");
    System.Console.WriteLine(developer.pay);  // 5000
    developer.applyRaise();
    System.Console.WriteLine(developer.pay);  // 5500
    
    
    // Upcasting: reduce the methods avaliable to only the parent class
    Empoyee employee = developer;
    
    // Downcasting: add methods avaliable to the child class
    Developer developer2 = (Developer) employee;  // return an exception if cannot be converted
    
    // use "as" keyword if not sure about the runtime type of the object
    Developer developer3 = employee as Developer;  // return a null if cannot be converted
    if (developer3 != null) {
      do_something;
    }
    
    // use "is" keyword to check
    if (employee is Developer) {
      Developer developer4 = (Developer) e;
    }
  }
}
```
* Composition
```c#
public class Employee {  // parent
  protected float raiseAmt;
  protected string first;
  protected string last;
  public int pay;

  public Employee(string first, string last, int pay, float raiseAmt = 1.04f) {
    this.first = first;
    this.last = last;
    this.pay = pay;
    this.raiseAmt = raiseAmt;
  }

  public void applyRaise() {
    this.pay = System.Convert.ToInt32(this.pay * this.raiseAmt);
  }
}

public class Developer {  // child
  private string progLang;
  public readonly Employee _employee;

  public Developer(Employee employee, string progLang) {
    _employee = employee;
    this.progLang = progLang;
  }
}

class MainClass
{
  public static void Main(string[] args)
  {
    Developer d = new Developer(new Employee("abc", "xyz", 5000, 1.1f), "c#");
    Console.WriteLine(d._employee.pay);  // 5000
    d._employee.applyRaise();
    Console.WriteLine(d._employee.pay);  // 5500
  }
}
```
* Polymorphism
```c#
public class Subject {
  public string subjName;
  
  public virtual void Study() {
    System.Console.WriteLine("Study all subjects");
  }
}

public class Math : Subject {
  public string mathName;
  
  public override void Study() {
    System.Console.WriteLine("Study Maths");
  }
}

class MainClass {
  public static void Main() {
    Subject s = new Subject();
    s.Study();  // "Study all subjects"
    s.subjName;  // accessible
    
    // polymorphism
    Subject sm = new Math();  // create a Subject object but override the Study method with the Math object
    sm.Study();  // "Study Maths"
    sm.subjName;  // only subjName is accessible, mathName is not
  }
}
```
* Interfaces
  * it is similar to a class but with abstract methods
  * use of "interface" keyword is required
  * does not have implementations (similar to abstract methods)
  * does not have access modifiers (eg: public, private, etc) in methods
  * interface is for building loosely-coupled extensible and testable apps
    * enable easy modifications with less or 0 impact on other components
  * has polymorphism behavior
```c#
public interface IFeatureName {  // in .net all interfaces start with "I" convention
  int Method1 { get; set; }
  void Method2();
  void Method3(int arg);
}

public class ProductName : IFeatureName {  // similar to inheritance, but different because methods have to be declared
  public int Method1 { get; set; }
  
  public void Method2() {
    do_something;
  }
  
  public void Method3(int arg) {
    do_something
  }
}

class MainClass {
  public static void Main() {
    ProductName p = new ProductName();
    if (p is IFeatureName) {  // check if IFeatureName exists
      p.Method2();
    }
  }
}


// Multiple Interfaces
public interface IFeatureName1 {
  void MethodName1();
}

public interface IFeatureName2 {
  void MethodName2();
}

public class ProductName : IFeatureName1, IFeatureName2 {
  public void MethodName1() {
    do_something;
  }
  
  public void MethodName2() {
    do_something;
  }
}
```
### c++
[back to top](#table-of-contents)
## Importing Libraries
### python 2 & 3
```python
# import module from libraries
import module_name  # must call module_name to use

# Using alias
import module_name as mn  # must call mn to use

# import class or function from a module
from module_name import function_name


# Absoute imports within the same project (file extensions not required)
from folder1 import module1  # example 1
from folder1.module2 import function1  # example 2
from folder2 import class1  # example 3
from folder2.subfolder1.module5 import function2  # example 4


# Relative imports (dot feature is similar to terminal)
from .module1 import class1  # example 1
from ..folder2 import function1 # example 2
from . import class2 # example 3
```
### javascript ES5
```javascript
// Before a module can be imported, it has to be exported first
var objectName.functionName = function();
module.exports = objectName;  // can be an object of functions
// alternative exports, import rules also change
exports.moduleName = objectName;  // preset a name to the module

// importing a module
// moduleName can be path too
var mn = require("moduleName");  // must call mn to use
var {function1, function2} = require("moduleName");  // importing multiple functions from a module
// import for alternative export
var mn = require("moduleName").moduleName;
```
### javascript ES6
```javascript
// Before a module can be imported, it has to be exported first
export default objectName;  // exporting a single or nested functions or class

// {} must be used when importing
// method 1
export {functionName};  // export only 1 class or function (can be used for importing multiple functions or classes
// method 2, can be function, class, objects, etc.
export const functionName = () => {do_something}


// import class or function from module
import "moduleName";  // import module
import name from "moduleName";  // name can be anything if only have 1 export
import * as name from "moduleName";  // import multiple exports as name
import {function1} from "moduleName";  // import a function from a module of multiple exports
import {function1 as f1} from "moduleName";  // import a function with alias
import {function1, function2} from "moduleName";  // import multiple functions
import name, {function1} from "/modules/path/moduleName"; // function1 can be used directly or via name.function1
```
### Java
### c++
[back to top](#table-of-contents)
## Type Conversions
### python 2 & 3
```python
# Convert to Integer, floats will round down
int(type_to_convert)

# Convert to floats
float(type_to_convert)

# Convert to strings
str(type_to_convert)

# Convert to arrays
list(type_to_convert)  # cannot be a number

# Convert to tuples
tuple(type_to_convert)  # cannot be a number

# Convert to sets
set(type_to_convert)  # cannot be a number
```
### javascript
```javascript
// number to string
let num = 123;
let str = String(num); // "123"

// string to integer (remove all non numbers automatically)
str = "12 kg";
num = parseInt(str); // 12

// string to float (remove all non number automatically)
str = "12.5 kg";
num = parseFloat(str) // 12.5

//string to integer or float (return NaN if non number in string)
str = "12"
num = Number(str) // 12
str = 12.5";
num = Number(str) // 12.5
str = "12.5 kg";
num = Number(str); // NaN
```
### Java
### c#
```c#
// implicit type conversion (small value to big only)
byte b = 1;
int i = b;
float f = i;


// casting
// explicit type conversion (can convert big value to small, however, data loss will occur)
float pi = 3.14f;
int intPi = (int) pi;  // 3

int num = 256;
byte b = (byte) num; // 0 (surplus value will assigned if converting big data type value to smaller data type value)

int num2 = 255;
byte b2 = (byte) num2; // 255


// convert non-compatible types
// string to integer
string s = "1";
// method 1
int i = Systen.Convert.ToInt32(s);  // returns 0 if string is null
// method 2
int j = int.Parse(s);  // returns an exception if string is null

/* other methods
ToByte()
ToInt16()  // short
ToInt32()  // integer
ToInt64()  // long
*/


// convert number to strings
// convert to normal string
int i = 1234;
string str = i.ToString();  // "1234"
// convert to currency with decimal places
string floatCurrency = i.ToString("C");  // "$1,234.00"
// convert to currency without decimal places
string currency = i.ToString("C0");  // "$1,234"

/* Format strings
format specific | description | example
c or C          | currency    | 123456 (C) -> $123,456
d or D          | decimal     | 1234 (D6) -> 001234
e or E          | exponential | 1052.0329112756 (E) -> 1.052033E+003
f or F          | fixed point | 1234.567 (F1) -> 1234.5
x or X          | Hexadecimal | 255 (X) -> FF
*/
```
### c++
[back to top](#table-of-contents)
## Find Data Type
### python 2 & 3
```python
# Get data type
num = 123
type(num)  # int

# Get boolean value
isinstance(num, int)  # True
isinstance(num, str)  # False
```
### javascript
```javascript
// Get data type: "number", "string", "boolean", "object", "undefined", "function"
// null and arrays are classified as object
// classes and methods are classfied as function
let num = 123;
typeof num;  // "number"

let array = [1, 2, 3];
typeof array;  // "object"
```
### Java
### c#
* typeof: takes a type name (which you specify at compile time)
* GetType: gets the runtime type of an instance
* is: returns true if an instance is in the inheritance tree
```c#
public class Animal { }
public class Dog : Animal { }

public class MainClass {
  public static void Main() {
    Dog spot = new Dog();
    PrintTypes(spot);
    int num = 123;
    System.Console.WriteLine(num.GetType());  // System.Int32
    System.Console.WriteLine(num.GetTypeCode());  // Int32
    System.Console.WriteLine(num.GetType() == typeof(int));  // true (System.Int32 == System.Int32)
  }

  public static void PrintTypes(Animal a) {
    System.Console.WriteLine(a.GetType() + " " + typeof(Animal));  // Dog Animal
    System.System.Console.WriteLine(a.GetType() == typeof(Animal));  // false
    System.Console.WriteLine(a is Animal);  // true  (Dog is Animal)
    System.Console.WriteLine(a.GetType() + " " + typeof(Dog));  // Dog Dog
    System.Console.WriteLine(a.GetType() == typeof(Dog));  // true
    System.Console.WriteLine(a is Dog);  // true (Dog is Dog)
  }
}
```
### c++
[back to top](#table-of-contents)
## String Concatenation
### python 2
```python
string_name = "string1" + "string2"  # "string1string2"

# String formatting
# % string operator: old style, soon to be deprecated
string_name = "%s %s" % ("string1", "string2")  # "string1 string2"

# {} operator: python 2.6 and above
# method 1
string_name = "{} {}".format("string1", "string2")  # "string1 string2"
# method 2
string_name = "{0} {1}".format("string1", "string2")  # "string1 string2"
```
### python 3
```python
# f string: python 3.6 and above
string1 = "string1"
string2 = "string2"
string_name = f"{string1} {string2}"  # "string1 string2"
```
### javascript ES5
```javascript
// javascript allows data type mashups, numbers will be converted to strings when concatenated with a string.
let stringName = "string1" + "string2" + 123;  // "string1string2123"
```
### javascript ES6
```javascript
let string1 = "string 1 value";
let string2 = "string 2 value";
let stringName = `${string1} ${string2} 123`;  // "string 1 value string 2 value 123"
```
### Java
### c#
```c#
string string1 = "string 1 value";
string string2 = "string 2 value";

// method 1
string stringName1 = string1 + string2;  // "string 1 value string 2 value"
// method 2
string stringName2 = String.Format("{0} {1}", string1, string2);  // "string 1 value string 2 value"
// method 3
string stringName3 = $"{string1} {string2}";  // "string 1 value string 2 value"
```
### c++
[back to top](#table-of-contents)
## JSON
### python 2 & 3
```python
import json  # must import to use

# python objects that can be converted: dict, list, tuple, string, int, float, True, False, None
# Convert JSON to python
json.loads(json_object)

# Convert python to JSON
json.dumps(python_object)
```
### javascript
```javascript
// JSON (JavaScript Object Notation): a lightweight, text-based data format that's based on JavaScript.
// convert js to JSON
let objName = {title: 'Black Panther'};
objName = JSON.stringify(objName);

// convert JSON to js
let objName = {"title": "Black Panther"};
objName = JSON.parse(objName);
```
### Java
### c++
[back to top](#table-of-contents)
## Program Entry Point
### python 2 & 3
```python
if __name__ === "__main__":
    # do something
```
### javascript
```javascript
// only works in node js
if (require.main === module) {
  // do something
}
```
### Java
### c#
```c#
class MainClass {
  public static void Main(string[] args) {
    // do something
  }
}
```
### c++
[back to top](#table-of-contents)
## Swapping values
### python 2 & 3
```python
a, b = 1, 2
# method 1
temp = a
a = b
b = temp

# method 2
a, b = b, a
```
### javascript ES5
```javascript
let a = 1;
let b = 2;
const temp = a;
a = b;
b = temp;
```
### javascript ES6
```javascript
[a, b] = [b, a];
```
### Java
### c++
[back to top](#table-of-contents)
## Error Handling
### python 2 & 3
* try: lets you test a block of code for errors
* except: except block lets you handle the error
  * covers all error types
    > except:
  * define exception type (can write multiple except statements)
    > except NameError:
  * save error to variable e
    > except ValueError as e:
  * list of important error types
    * AssertionError, AttributeError, EOFError, FloatingPointError, GeneratorExit, ImportError, IndexError, KeyError
    * KeyboardInterrupt, MemoryError, NameError, NotImplementedError, OSError, OverflowError, ReferenceError, RuntimeError
    * StopIteration, SyntaxError, IndentationError, TabError, SystemError, TypeError, UnboundLocalError, UnicodeError
    * UnicodeEncodeError, UnicodeDecodeError, UnicodeTranslateError, ValueError, ZeroDivisionError
* else: code to be executed if no errors were raised
* finally: if specified, will be executed regardless if the try block raises an error or not
  * useful to close objects and clean up resources
```python
# similar to if else
try:  # must start with try
    do_something
except:  # must have to handle errors
    do_something_if_error_occurs
else:  # not required
    do_something_if_no_error
finally:  # not required
    do_something_when_try_&_except_or_else_is_completed
```
### javascript
* try: lets you test a block of code for errors
* catch: lets you handle the error
* finally: lets you execute code, after try and catch, regardless of the result
```javascript
try {
  doSomething;
} catch(error) {
  doSomethingIfErrorOccurs;
} finally {
  doSomethingWhenTryAndCatchIsCompleted;
}
```
### Java
### c#
* try: lets you test a block of code for errors
* catch: lets you handle the error
  * use "Exception" keyword to catch all exception types
  * use specific exception types to catch that specific exception
  * catch block can be chained (specific exception with highest priority should come first)
* finally: lets you execute code, after try and catch, regardless of the result
  * very important for closing a file when an opened file in the try block triggered an exception
```c#
try {
  doSomething;
} catch(Exception ex) {  // ex is an arg (not mandatory), ex can be used to print general or more detailed error
  doSomethingIfErrorOccurs;
} finally {
  doSomethingWhenTryAndCatchIsCompleted;
}
```
* Create custom exception
```c#
public class NewExceptionName : System.Exception {
  public NewExceptionName(string message, System.Exception innerException)
    : base(message, innerException)
    {}
}
```
### c++
[back to top](#table-of-contents)
## Custom Error
### python 2 & 3
```python
# raise generic exception
raise Exception("custom message")

# raise specific exception
raise ValueError("custom message")
```
### javascript
```javascript
throw "custom message"; // throw a text

throw 123; // throw a number
```
### Java
### c#
```c#
// raise generic exception
throw new System.Exception("custom message");


// raise specific exception
throw new SpecificExceptionName("custom message");
```
### c++
[back to top](#table-of-contents)
## Asynchronous
* Handling asynchronous code (making it synchronous)
### python
### javascript ES5
```javascript
var posts = [{title: "Post 1", body: "body of post 1"}, {title: "Post 2", body: "body of post 2"}];

// callback is required if need getPost to display data after createPost is called
// reason is because createPost takes longer time to complete compared to getPost
function createPost(post, callback) {
  setTimeout(() => {
    posts.push(post);
    callback();
  }, 2000);
}

// method 1
// callback function
function getPosts() {
  setTimeout(() => {
    var output = "";
    posts.forEach((post, index) => {
      output += post.title;
    });
    console.log(output);
  }, 1000);
}
createPost({title: "Post 3", body: "body of post 3"}, getPosts);

// method 2:
// Using anonymous callback function can lead to callback hell if over used
createPost({title: "Post 3", body: "body of post 3"}, function() {
  setTimeout(() => {
    var output = "";
    posts.forEach((post, index) => {
      output += post.title;
    });
    console.log(output);
  }, 1000);
});
```
### javascript ES6
```javascript
// Change createPost to return a Promise
function createPost(post) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (post) {
        posts.push(post)
        resolve();
      } else {
        reject("error")
      }
    }, 2000);
  });
}

// method 3
// use .then() instead of callback
createPost({title: "Post 3", body: "body of post 3"})
.then(getPosts) // can chain multiple promises by adding .then(do_something)
.catch(error => console.log(error));

// method 4
// use Promise.all
Promise.all([ // can chain multiple promises
  createPost({title: "Post 3", body: "body of post 3"}),
])
.then(values => {
  getPosts();
  console.log(values) // output array of results e.g [promise1_output, promise2_output, ...]
});
```
### javascript ES8
```javascript
// method 5
// use async / await when calling functions
async function init() {
  await createPost({title: "Post 3", body: "body of post 3"});
  getPosts();
}
init();
```
### Java
### c#
```c#
class MainClass {
    public static void Main(string[] args) {
        System.Console.WriteLine("Starting");
        Worker worker = new Worker();
        worker.DoWork();  // since this is any async function, add this to stack then move on
        while (!worker.IsComplete) {
            System.Threading.Thread.Sleep(100);
            System.Console.Write(".");
        }
        System.Console.WriteLine("Done");
    }

    public static System.Threading.Tasks.Task DelayOperation() {
        return System.Threading.Tasks.Task.Factory.StartNew(() => {
            System.Threading.Thread.Sleep(2000);
        });
    }
}

public class Worker { 
    public bool IsComplete { get; private set; }

    public async void DoWork() {  // add async to make function an async 
        this.IsComplete = false;
        System.Console.WriteLine("Doing work");
        await LongOperation();  // wait for the function to finish before proceeding
        IsComplete = true;
        System.Console.WriteLine("Work completed");
    }

    private System.Threading.Tasks.Task LongOperation() {
        return System.Threading.Tasks.Task.Factory.StartNew(() => {
            System.Console.WriteLine("Working!");
            System.Threading.Thread.Sleep(2000);
        });
    }
}
```
### c++
[back to top](#table-of-contents)
## Math
### python 3
```python
import math

print("abs(-1) ", abs(-1))  # abs(-1)  1
print("max(5, 4) ", max(5, 4))  # max(5, 4)  5
print("min(5, 4) ", min(5, 4))  # min(5, 4)  4
print("pow(2, 2) ", pow(2, 2))  # pow(2, 2)  4
print("ceil(4.5) ", math.ceil(4.5))  # ceil(4.5)  5
print("floor(4.5) ", math.floor(4.5))  # floor(4.5)  4
print("round(4.5) ", round(4.5))  # round(4.5)  4
print("exp(1) ", math.exp(1))  # e**x  # exp(1)  2.718281828459045
print("log(e) ", math.log(math.exp(1)))  # log(e)  1.0
print("log(100) ", math.log(100, 10))  # Base 10 Log  # log(100)  2.0
print("sqrt(100) ", math.sqrt(100))  # sqrt(100)  10.0
print("sin(0) ", math.sin(0))  # sin(0)  0.0
print("cos(0) ", math.cos(0))  # cos(0)  1.0
print("tan(0) ", math.tan(0))  # tan(0)  0.0
print("asin(0) ", math.asin(0))  # asin(0)  0.0
print("acos(0) ", math.acos(0))  # acos(0)  1.5707963267948966
print("atan(0) ", math.atan(0))  # atan(0)  0.0
print("sinh(0) ", math.sinh(0))  # sinh(0)  0.0
print("cosh(0) ", math.cosh(0))  # cosh(0)  1.0
print("tanh(0) ", math.tanh(0))  # tanh(0)  0.0
print("asinh(0) ", math.asinh(0))  # asinh(0)  0.0
print("acosh(pi) ", math.acosh(math.pi))  # acosh(pi)  1.811526272460853
print("atanh(0) ", math.atanh(0))  # atanh(0)  0.0
print("hypot(0) ", math.hypot(10, 10))  # sqrt(x*x + y*y)  # hypot(0)  14.142135623730951
print("radians(0) ", math.radians(0))  # radians(0)  0.0
print("degrees(pi) ", math.degrees(math.pi))  # degrees(pi)  180.0

# infinity value
math.inf

import random
# random integer
random.randint(1, 3)  # any number from 1 to 3
```
### javascript
### Java
### c#
```c#
double number1 = 10.5;
double number2 = 15;

System.Console.WriteLine("Math.Abs(number1) " + (Math.Abs(number1)));  // Math.Abs(number1) 10.5
System.Console.WriteLine("Math.Ceiling(number1) " + (Math.Ceiling(number1)));  // Math.Ceiling(number1) 11
System.Console.WriteLine("Math.Floor(number1) " + (Math.Floor(number1)));  // Math.Floor(number1) 10
System.Console.WriteLine("Math.Max(number1, number2) " + (Math.Max(number1, number2)));  // Math.Max(number1, number2) 15
System.Console.WriteLine("Math.Min(number1, number2) " + (Math.Min(number1, number2)));  // Math.Min(number1, number2) 10.5
System.Console.WriteLine("Math.Pow(number1, 2) " + (Math.Pow(number1, 2)));  // Math.Pow(number1, 2) 110.25
System.Console.WriteLine("Math.Round(number1) " + (Math.Round(number1)));  // Math.Round(number1) 10
System.Console.WriteLine("Math.Sqrt(number1) " + (Math.Sqrt(number1)));  // Math.Sqrt(number1) 3.24037034920393

Random rand = new Random();
System.Console.WriteLine("Random Number Between 1 and 10 " + (rand.Next(1,11)));
```
### c++
[back to top](#table-of-contents)
## Date and Time]
### python
### javascript
### Java
### c#
```c#
// Set date (time set to default at 12:00:00 AM)
System.DateTime newDate = new System.DateTime(2015, 1, 1);


// Get current date (time set to default at 12:00:00 AM)
System.DateTime todayDate = System.DateTime.Today;  // 1/14/2020 12:00:00 AM


// Get current date and time
System.DateTime now = System.DateTime.Now;  // 1/14/2020 10:19:54 AM


// Add or reduce days
now.AddDays(1);  // add 1 day
now.AddDays(-10;  // reduce 1 day


// Display formats
System.Console.WriteLine(now);  // 1/14/2020 10:23:09 AM
System.Console.WriteLine(now.ToLongDateString());  // Tuesday, January 14, 2020
System.Console.WriteLine(now.ToShortDateString());  // 1/14/2020
System.Console.WriteLine(now.ToLongTimeString());  // 10:23:09 AM
System.Console.WriteLine(now.ToShortTimeString());  // 10:23 AM
System.Console.WriteLine(now.ToString());  // 1/14/2020 10:23:09 AM
System.Console.WriteLine(now.ToString("yyyy-MM-dd"));  // 2020-01-14
System.Console.WriteLine(now.ToString("yyyy-MM-dd HH:mm"));  // 2020-01-14 10:26
```
### c++
[back to top](#table-of-contents)
## File System
### python
### javascript
### Java
### c#
```c#
// Create or Save file
string filename = @"/my/file/path/fileFolder/filename.txt";
string textString = "data to save in file";
System.IO.File.WriteAllText(filename, textString);  // existing file will be overwritten

// Copy file
bool overwrite = true;  // overwrite file if exist, else return an File already exists exception
string toBeCopiedFile = @"/my/file/path/fileFolder/filename.txt";
string toPasteFile = @"/my/file/path/fileFolder/filenameCopied";
// method 1
System.IO.File.Copy(toBeCopiedFile, toPasteFile, overwrite);
// method 2
System.IO.FileInfo file = new System.IO.FileInfo(toBeCopiedFile);
file.CopyTo(toPasteFile, overwrite);


// Check if file exists
// method 1
System.IO.File.Exists(toPasteFile);  // true
// method 2
file.Exists;  // true


// Get text from file
string content = System.IO.File.ReadAllText(toPasteFile);


// Delete file
System.IO.File.Delete(toPasteFile);  // method 1
file.Delete();  // method 2 (deletes toBeCopiedFile)


// Create new folder
string folder = @"/my/file/path/folderName";
System.IO.Directory.CreateDirectory(folder);  // does not overwrite if folder already exists


// Get file in folder
// method 1
string searchPattern = "*.*";  // eg. get only .jpg files -> "*.jpg"
string[] filesArray = System.IO.Directory.GetFiles(folder, searchPattern, SearchOption.AllDirectories);
// method 2
System.IO.DirectoryInfo dirInfo = new System.IO.DirectoryInfo(folder);
System.IO.FileInfo[] filesArray2 = dirInfo.GetFiles("*", SearchOption.AllDirectories);


// Get folders in folder
string[] foldersArray = System.IO.Directory.GetDirectories(folder, searchPattern, SearchOption.AllDirectories);
System.IO.DirectoryInfo[] foldersArray = dirInfo.GetDirectories();


// Check if folder exists
System.IO.Directory.Exists(folder);  // true


// Get filename of a file from path
Path.GetFileName(toBeCopiedFile);  // "filename.txt"


// Get file extension of a file from path
Path.GetExtension(toBeCopiedFile);  // ".txt"


// Get filename without file extension of a file from path
Path.GetFileNameWithoutExtension(toBeCopiedFile);  // "filename"


// Get directory name of a file from path
Path.GetDirectoryName(toBeCopiedFile);  // "fileFolder"


// Open file (not in app)
System.Diagnostics.Process.Start(filename);
```
### c++
[back to top](#table-of-contents)
## Properties
### python
### javascript
### Java
### c#
* Properties is a kind of class member that is used for providing access to fields of a class
* best practive to declare fields as private & create public properties to provide access to them
* a property encapsulates a get and a set method
```c#
// method 1
public class Person {
  private string _name;
  
  public void SetName(string name) {
    this._name = name;
  }
  
  public string GetName() {
    return _name;
  }
}

class MainClass {
  public static void Main() {
    Person p = new Person();
    p.SetName("xyz");
    System.WriteLine(p.GetName());  // "xyz"
  }
}


// method 2: using setter and getter properties
public class Person {
  private string _name;
  
  public string name {
    get { return _name; }
    set { _name = value; }  // value is a keyword
  }
}

class MainClass {
  public static void Main() {
    Person p = new Person();
    p.name = "xyz";
    System.WriteLine(p.name);  // "xyz"
  }
}


// method 3: using auto-implemented properties (does not work if logic is involved in get or set method, use method 2 instead)
public class Person {
  public string name { get; set; }
}

class MainClass {
  public static void Main() {
    Person p = new Person();
    p.name = "xyz";
    System.WriteLine(p.name);  // "xyz"
  }
}


// method 4: using auto-implemented properties with private set method
public class Person {
  public string name { get; private set; }  // if private keyword is used, need constructor to set
  
  public Person(string inputName) {  // constructor
    name = inputName;
  }
}

class MainClass {
  public static void Main() {
    Person p = new Person("xyz");
    System.WriteLine(p.name);  // "xyz"
  }
}
```
### c++
[back to top](#table-of-contents)
## Access modifier
* use to hide the implementation details of a class
### python
### javascript
### Java
### c#
* 6 types
  * public: accessible from everywhere in project, no accessibility restrictions
```c#
class NumberClass
{
    public int number = 10;
}
 
class MainClass
{
    static void Main(string[] args)
    {
        NumberClass num = new NumberClass();
        System.Console.WriteLine(num.number);  // This is OK. The number variable has the public access modifier.
    }
}
```
  * private: accessible only from inside a class or a structure, can't access them outside the class they are created
```c#
class NumberClass
{
    private int number = 10;
}
 
class MainClass
{
    static void Main(string[] args)
    {
        NumberClass num = new NumberClass();
        System.Console.WriteLine(num.number);  // Error. We can't access the number variable because 
        // it has the private access modifier and its only accessible in the NumberClass class
    }
}
```
  * protected: object is accessible inside the class and in all classes that derive from that class
```c#
class NumberClass
{
    protected int number = 10;  // we can access this variable inside this class
}
 
class DerivedClass: NumberClass  // this is inheritance. DerivedClass derives from the NumberClass class
{
    void Print()
    {
        System.Console.WriteLine(number);  // we can access it in this class as well because it derives from the NumberClass class
    }
}
 
class MainClass
{
    void Print()
    {
        NumberClass num = new NumberClass();
        System.Console.WriteLine(num.number);  // Error. The number variable is inaccessible due to its protection level. 
        // The Program class doesn't derive from the NumberClass
    }
}
```
  * internal: object is accessible only inside its own assembly (project) but not in other assemblies (projects)
```c#
//First Project (ASSEMBLY)
public class NumberClassInFirstProject
{
    internal int number = 10;  // we can access this variable inside this class
}
 
class Program1
{
    public static void Main()
    {
        NumberClassInFirstProject num = new NumberClassInFirstProject();
        System.Console.WriteLine(num.number);  // This is OK. Anywhere in this project (assembly) 
        // we can access the number variable.
    }
}


//Second project (ASSEMBLY)
class Program2
{
    public static void Main()
    {
        NumberClassInFirstProject num = new NumberClassInFirstProject();
        System.Console.WriteLine(num.number);  // Error. The number variable is inaccessible due to its protection level. 
        // The Program class in second project can't access the internal members from another project
    }
}
```
  * protected internal: a combination of protected and internal, can access the protected internal member only in the same assembly (project) or in a derived class in other assemblies (projects)
```c#
//First Project (ASSEMBLY)
public class NumberClassInFirstProject
{
    protected internal int number = 10;  // we can access this variable inside this class
}
 
class Program1
{
    public static void Main()
    {
        NumberClassInFirstProject num = new NumberClassInFirstProject();
        System.Console.WriteLine(num.number);  // This is OK. Anywhere in this project (assembly) we can access the number variable.
    }
}
 
//Second project (ASSEMBLY)
class Program2: NumberClassInFirstProject  // Inheritance
{
    public static void Main()
    {
        System.Console.WriteLine(number);  // This is OK as well. The class Program derives from the NumberClassInFirstProject class.
    }
}
```
  * private protected: a combination of private and protected, can access members inside the containing class or in a class that derives from a containing class, but only in the same assembly (project)
### c++
[back to top](#table-of-contents)
## Language Specific
### python
```python
# List comprehension
# original method
arr = []
for i in range(5):
 arr.append(i)
print(arr)  # [0, 1, 2, 3, 4]

# List comprehension method
arr = [i for i in range(5)]
print(arr)  # [0, 1, 2, 3, 4]

# List comprehension with conditional statement
arr = [i for i in range(5) if i < 3]
print(arr)  # [0, 1, 2]

# Tuples (similar to list, but are immutable)
tuple1 = (1, 2, "3")

# Sets (only have unique values)
# create set
set1 = set([1, 2])  # method 1
set2 = {1, 2}  # method 2

# join 2 sets together
set3 = set1 | set2  # {1, 2}

# add element to set
set1.add(3)  # {1, 2, 3}

# add set2 to set1
set1 |= set2  # {1, 2, 3}

# remove element from set from element
set1.discard(2)  # {1, 3}

# Get intersection of 2 sets
set1.intersection(set2)  # {1}

# Get unique value from the 2 sets
set1.symmetric_difference(set2)  # {2, 3}

# Get values from set1 that set2 does not have
set1.difference(set2)  # {3}

# delete all values from set
set1.clear()  # set()

# Create a set that cannot be modified
set_fixed = frozenset([1, 2, 3])
```
### javascript
* Explicit Binding
  * choose what we want the context of "this" to be by using call, apply or bind
  * by refering to the call, apply, or bind methods, you can determine the value of "this"
  * can only be used on FUNCTIONS
```javascript
/*
NAME OF METHOD  | PARAMETERS                | INVOKE IMMEDIATELY?
    CALL        |   thisArg,a,b,c,...       |       Yes
    APPLY       |   thisArg,[a,b,c,...]     |       Yes
    BIND        |   thisArg,a,b,c,...       |       No

CALL args can be set to anything and can have infinite arguments, function is immediately invoked
APPLY only takes 2 args, the 2nd arg is an array of infinite arguments, function is immediately invoked
BIND can have infinite arguments, and is a method that returns a function definition
*/
var foo = {
  firstName: "Foo",
  say: function() {
    return "Hi " + this.firstName;
  },
  add: function(a, b, c) {
    return this.firstName + " just calculated " + (a + b + c);
  }
}
var bar = {
  firstName: "Bar"
}
// Call: allow this to be referenced to bar instead of foo, all arguments must not be undefined
foo.say() // returns "Hi Foo"
foo.say.call(bar) // returns "Hi Bar"
foo.add.call(bar, 1, 2, 3); // returns "Bar just calculated 6"

// Apply: simlar to Call for the 1st argument, 2nd argument has to be an array of values, all arguments must not be undefined
foo.say.apply(bar) // returns "Hi Bar"
foo.add.apply(bar, [1, 2, 3]); // returns "Bar just calculated 6"

// Bind: returns the function, then requires it to be called
// all agruments need not be defined upfront, but must provide remaining arguments when calling
var say = foo.say.bind(bar);
say(); // returns "Hi Bar"
var add = foo.add.bind(bar, 1, 2);
add(3); // returns "Bar just calculated 6"

// Bind is commonly used when dealing with asynchronous code
var foo = {
  firstName: "Foo",
  say: function() {
    setTimeout(function() {
      console.log("Hi " + this.firstName;
    }.bind(this), 1000);
  }
}
foo.say(); // prints "Hi Foo", if without bind(this), prints "Hi undefined"
```
### Java
### c#
* Overloading
  * having multiple similar methods with different signatures
  * allows multiple different input data types for the same feature
```c#
// Overloading constructors
// overloaded constructors are separate 
public class Print {
  public Print() {
    System.Console.Write("test");
  }
  
  public Print(string x) {
    System.Console.Write(x);
  }
}

class MainClass {
  public static void Main(string[] args) {
    Print print = new Print();  // "first"
    Print print2 = new Print("second");  // "second"
  }
}


// overloaded constructors are linked
public class Print {
  public Print() {
    System.Console.Write("first");
  }
  
  public Print(string x) : this() {  // add ": this()" to link with default constructor
    System.Console.Write(x);
  }
}

class MainClass {
  public static void Main(string[] args) {
    Print print = new Print("second");  // "firstsecond"
  }
}


// Overloading methods
public class Point {
  public int X;
  public int Y;
  
  public Point(int x, int y) {  // constructor
    this.X = x;
    this.Y = y;
  }
  
  public void Move (int x, int y) {
    this.X = x;
    this.Y = y;
  }
  
  public void Move(Point newLocation) {  // overloading the 1st Move method
    Move(newLocation.X, newLocation.Y);
  }
}
```
* Overflowing
  * c# does not check for overflow
    * this means that value of a variable can be modified during runtime and when the value goes beyond the boundary of it's data type, overflow will occur
    * e.g.: byte num = 255; num++;  // num value will be the surplus value (in this case 0)
```c#
// If overflow is not desired, use checked keyword to enable overflow checking
// In the following example, increment will not occur and an exception will be thrown, which will cause an error
checked {
  byte number = 255;
  number++;
}
```
* Enum
  * Used to manage number type constants for better clarity and maintainability
  * Can be declared in namespace, in classes
```c#
// not reccommended method
const int RegularAirMail = 1;
const int RegisteredAirMail = 2;
const int Express = 3;

// Use enums for better management and for clarity
// default data type is an integer
public enum ShippingMethod : byte  // use : byte to change default data type
{
  // if value is not assigned, 1st value will start with 0
  // subsequent value will be incremented by 1 automatically if value is not assigned
  RegularAirMail = 1,
  RegisteredAirMail = 2,
  Express = 3
}

// get string value (ToString method not required if using System.Console.WriteLine)
ShippingMethod method = ShippingMethod.Express.ToString();  // Express
// get number value
ShippingMethod method = (int) ShippingMethod.Express;  // 3

// retrieve string value with number value
ShippingMethod methodType = (ShippingMethod) 3;  // Express
```
* Ref Modifier
  * Modifies value type
  * when pasing a value type to a method, a copy of the variable is sent to the method
    * changes applied to that variable in the method will not be visible upon return from the method
  * the value type can be modified using the ref modifier
    * when the ref modifier is used, a reference to the original variable will be sent to the target method
```c#
// typical value type cannot be modified case
public class Calculator {
  public int Add(int num){
    num += 2;
  }
}

class MainClass {
  public static void Main(string[] args) {
    Calculator cal = new Calculator3();
    int num = 1;
    cal.Add(num);
    System.Console.WriteLine(num);  // 1
  }
}


// using Ref Modifier
public class Calculator {
  public int Add(ref int num){  // add ref keyword
    num += 2;
  }
}

class MainClass {
  public static void Main(string[] args) {
    Calculator cal = new Calculator3();
    int num = 1;
    cal.Add(ref num);  // add ref keyword
    System.Console.WriteLine(num);  // 3
  }
}
```
* Out Modifier
  * use to return multiple values from a method
  * any parameter declared with the out modifier is expected to receive a value at the end of the method
```c#
// not using the "out" keyword will result in an error
public class Person {
  public void GetName(string name){
    name = "myName";
  }
}

class MainClass {
  public static void Main(string[] args) {
    Person person = new Person();
    string name;  // unassigned local variable error
    person.GetName(name);
    System.Console.WriteLine(name);
  }
}


// using the "out" keyword
public class Person {
  public void GetName(out string name){
    name = "myName";
  }
}

class MainClass {
  public static void Main(string[] args) {
    Person person = new Person();
    string name;
    person.GetName(out name);
    System.Console.WriteLine(name);  // "myName"
  }
}
```
* Readonly modifier
  * Prevents accidental overwriting of the value
```c#
// without readonly modifier
public System.Collections.Generic.List<int> orders = new System.Collections.Generic.List<int>();

public void MakeOrder() {
  orders = new System.Collections.Generic.List<int>();  // a new list will be reassigned
}


// using readonly modifier
public readonly System.Collections.Generic.List<int> orders = new System.Collections.Generic.List<int>();

public void MakeOrder() {
  orders = new System.Collections.Generic.List<int>();  // this will produce an error that the variable cannot be assigned
}
```
* Abstract modifier (polymorphism)
  * what?
    * indicates that a class or a member (method) is missing implementation
    * if a method is declared as abstract, the containing class needs to be declared as abstract too
    * the abstract methods must be implemented in the child class
    * abstract classes cannot be instantiated
  * why?
    * use abstract when you want to provide some common behavior, while forcing other developers to follow your design
```c#
public abstract class ParentClassName {  // if a method has an abstract keyword, the class must also have the abstract keyword
  public abstract void FunctionName();  // this will allow the child class to override this method
}
```
* Virtual modifier (polymorphism)
  * Used to modify a method, property, indexer, or event declaration and allow for it to be overridden in a derived (child) class
  * cannot be used with the static, abstract, private, or override modifiers
```c#
public class ParentClassName { 
  public virtual void FunctionName() {  // this will allow the child class to override this method
    do_something;
  }
}
```
* Override modifier (polymorphism)
  * required to extend or modify the abstract or virtual implementation of an inherited method, property, indexer, or event
```c#
public class ChildClassName : ParentClassName {
  public override void FunctionName() {  // this will override the inherited method
    do_something;
  }
}
```
* Sealed modifier (polymorphism)
  * prevents other classes from inheriting from it
  * it is the opposite of abstract classes
  * Use sealed modifier because selaed classes are slightly faster due to some run-time optimizations
```c#
// method 1: applying sealed modifier to the child class will prevent us from being able to create a class that derives from the child class
public sealed class ChildClassName : ParentClassName {  // new class will not be able to inherit from ChildClassName
  public override void FunctionName() {
    do_something;
  }
}


// method 2: applying sealed modifier to the overriding methods
public class ChildClassName : ParentClassName {
  public sealed override void FunctionName() {  // new class will be able to inherit from ChildClassName but will be unable to override the FunctionName that is sealed
    do_something;
  }
}
```
* Dynamic type
  * does not work on Apple products (Mac, IOS)
  * converting dynamic to static type does not require casting
```c#
// static type
string a = "test";  // cannot reassign to a different data type

// dynamic type
dynamic b = "test";  // allows variable to be reassigned to a different data type
b = 123;
```
* Generics
  * allows the crating of types that use other types
  * make classes reusable and with type-safety
```c#
public class Stack<T> {  // let data type be T
  public T testValue { get; set; }
  private System.Collections.Generic.List<T> stack = new System.Collections.Generic.List<T>();  // use data type

  public T Peek() {  // set return data type as T
    try {
      return stack[stack.Count - 1];
    } catch (System.ArgumentOutOfRangeException) {
      return default(T);  // return default value of data type T
    }
  }

  public void Push(T data) {  // set arg data type as T
    stack.Add(data);
  }

  public T Pop() {
    int lastIndex = stack.Count - 1;
    T val = stack[lastIndex];  // set data type as T
    stack.RemoveAt(lastIndex);
    return val;
  }
}

public class Printer {
  public void Print<T>(Stack<T> stack) {
    System.Console.WriteLine(stack.testValue);
  }
}

class MainClass {
  public static void Main() {
    Stack<string> s = new Stack<string>() {testValue="abc"};  // method 1
    // Stack<string> s = new Stack<string> {testValue="abc"};  // method 2
    // Stack<string> s = new Stack<string>();  // method 3
    Printer p = new Printer();
    p.Print(s);  // "abc", method 3 will cause this to result with ""
  }
}
```
* Generic contraints
  * Contraints are validations that we can put on generic type parameter
  * at the instantiation time of generic class, if client provides invalid type parameter then compiler will give an error
  * 6 types of contraints
1. where T : InterfaceName
```c#
// method 1: defining generics in methods with contraints
public class Maths {
  public int Max(int a, int b) {  // normal method
    return a > b ? a : b;
  }
  
  public T Max<T>(T a, T b) where T : System.IComparable {
    // return a > b ? a : b;  // this will produce an error
    return a.CompareTo(b) > 0 ? a : b;
  }
}

class MainClass {
  public static void Main() {
    Maths m = new Maths();
    int max1 = m.Max(2, 8);  // 8
    float max2 = m.Max(3.3f, 6.5f);  // 6.5
  }
}


// method 2: defining generics at class with contraints
public class Maths<T> where T : System.IComparable {
  public int Max(int a, int b) {  // normal method
    return a > b ? a : b;
  }
  
  public T Max(T a, T b) {
    return a.CompareTo(b) > 0 ? a : b;
  }
}

class MainClass {
  public static void Main() {
    Maths<int> m = new Maths<int>();
    int max1 = m.Max(2, 8);  // 8
    Maths<float> m = new Maths<float>();
    float max2 = m.Max(3.3f, 6.5f);  // 6.5
  }
}
```
2. where T : parentClass
```c#
public class Product {
  public string Title { get; set; }
  public float Price { get; set; }
}

public class Calculator<T> where T : Product {
  public float Cost(T product) {
    return product.Price;
  }
}

class MainClass {
  public static void Main() {
    Product p = new Product { Price = 2.3f };
    Calculator<Product> c = new Calculator<Product>();
    System.Console.WriteLine(c.Cost(p));  // 2.3
  }
}
```
3. where T : struct
```c#
public class Nullable<T> where T : struct {
    private object _value;

    public bool HasValue { 
        get { return _value != null; }
    }

    public Nullable() { }

    public Nullable(T value) {
        _value = value;
    }

    public T GetValueOrDefault() {
        if (HasValue)
            return (T)_value;
        return default(T);
    }
}

class MainClass {
    public static void Main() {
        Nullable<int> num = new Nullable<int>(5);
        System.Console.WriteLine(num.HasValue);  // true
        System.Console.WriteLine(num.GetValueOrDefault());  // 5
        
        Nullable<int> num2 = new Nullable<int>();
        System.Console.WriteLine(num2.HasValue);  // false
        System.Console.WriteLine(num2.GetValueOrDefault());  // 0
        
        Nullable<string> str = new Nullable<string>();  // error as string is not a value type
    }
}
```
4. where T : class
```c#
public class NodeList<T> where T : class
{}

class MainClass {
    public static void Main(string[] args) {
        NodeList<int> nodesOfInt = new NodeList<int>();  // error as int is a value type
        NodeList<string> nodesOfString = new NodeList<string>();  // string is a reference type
        NodeList<Employee> nodesOfEmployee = new NodeList<Employee>();  // Employee is a reference type
        NodeList<EventHandler> nodesOfAction = new NodeList<EventHandler>();  //EventHandler is a delegate and a reference type
    }
}
```
5. where T : new()
  * new() represents default constructor
  * no parameters allowed
```c#
public class NodeList<T> where T : new()
{}

public class ClassName1 {
    public ClassName1()
    {}
}

public class ClassName2 {
    public ClassName2(dataType argName)
    {}
}

class MainClass {
    public static void Main(string[] args){
        NodeList<ClassName1> c1 = new NodeList<ClassName1>();  // no error
        NodeList<ClassName2> c2 = new NodeList<ClassName2>();  // error as parameters are not allowed
    }
}
```
6. where T : U
  * 2 argument types (T and U)
  * U can be an interface, abstract class, or simple class
  * T must inherit or implements the U class
```c#
public class NodeList<T, U> where T : U {
    public void DoWork(T subClass, U baseClass)
    {}
}
 
public interface IEmployee
{}
 
public class Employee : IEmployee
{}
 
class MainClass{
    public static void Main() {
        NodeList<Employee, IEmployee> employeeNodes = new NodeList<Employee, IEmployee>();
    }
}
```
* Delegates
  * it is an object that knows how to call a method (or a group of methods)
  * it is a reference or a pointer to a function
  * it is for designing extensible and flexible apps (eg frameworks)
```c#
// without parameters
public delegate void DelegateName();  // use of "delegate" keyword is required

class MainClass {
  public static void Main() {
    // initialize delegate
    DelegateName delegateName = new DelegateName(DoSomethingMethod);  // method 1
    delegateName();  // run delegate
    
    DelegateName delegateName2 = DoSomethingMethod;  // method 2
    delegateName2();
    
    DelegateName delegateName3 = DoSomethingMethod;
    RunDelegate(delegateName3);  // method 3
    
    DelegateName delegateName4 = GetMyDelegate();  // method 4
    RunDelegate(delegateName4);
    
    DelegateName delegateName5 = delegate() { doSomething; }  // method 5: using anonymous methods
    delegateName5();
    
    DelegateName delegateName6 = delegate() { return doSomething; }  // method 6: return value with anonymous methods
    dataType variableName = delegateName6();
    
    DelegateName delegateName7 = () => { return doSomething; }  // method 7: return value with lambda expression
    dataType variableName = delegateName7();
  }
  
  public static void DoSomethingMethod() {
    doSomething;
  }
  
  public static void RunDelegate(DelegateName delegateName3) {
    delegateName3();
  }
  
  public static DelegateName GetMyDelegate() {
    return new DelegateName(DoSomethingMethod);
  }
}


// with parameters
public delegate void DelegateName(dataType argName);  // dataType must be the same as the pointed function

class MainClass {
  public static void Main() {
    // initialize delegate
    DelegateName delegateName = new DelegateName(DoSomethingMethod);  // method 1
    delegateName(argName_contents);  // must pass in argument
    
    DelegateName delegateName2 = DoSomethingMethod;  // method 2
    delegateName2(argName_contents);  // must pass in argument
    
    DelegateName delegateName3 = DoSomethingMethod;
    RunDelegate(delegateName3);  // method 3
    
    DelegateName delegateName4 = GetMyDelegate();  // method 4
    RunDelegate(delegateName4);
    
    DelegateName delegateName5 = delegate(dataType argName) { doSomethingWith_argName; }  // method 5: using anonymous methods
    delegateName5(argName_contents);
    
    DelegateName delegateName6 = delegate(dataType argName) { return doSomethingWith_argName; }  // method 6: return value with anonymous methods
    dataType variableName = delegateName6(argName_contents);
    
    DelegateName delegateName7 = (dataType argName) => { return doSomethingWith_argName; }  // method 7: return value with lambda expression
    dataType variableName = delegateName7(argName_contents);
  }
  
  public static void DoSomethingMethod(dataType argName) {  // dataType must be the same as the delegate
    doSomethingWith_argName;
  }
  
  public static void RunDelegate(DelegateName delegateName3) {
    delegateName3(argName_contents);  // must pass in argument
  }
  
  public static DelegateName GetMyDelegate() {
    return new DelegateName(DoSomethingMethod);
  }
}


// usage example
public delegate void Operation(int num);

class MainClass
{
    public static void Main(string[] args)
    {
        // method 1
        Operation op = Double;
        ExecuteOperation(2, op);  // result 4, display 4
        op = Triple;
        ExecuteOperation(2, op);  // result 6, display 46
        
        // method 2: use chaining
        Operation op2 = Double;
        op2 += Triple;
        ExecuteOperation(2, op2);  // 46
    }

    public static void Double(int num) {
        System.Console.Write(num * 2);
    }
    
    public static void Triple(int num) {
        System.Console.Write(num * 3);
    }

    public static void ExecuteOperation(int num, Operation operation) {
        operation(num);
    }
}
```
* Generic Delegates
  * Action: does not return a value
  * Func: returns a value
```c#
class MainClass
{
    public static void Main(string[] args)
    {
        // Declares delegate and operation in 1 line, does not return a value
        System.Action<int> op = num => { System.Console.WriteLine(num * 2); };  // similar to the Double example above
        op(3);  // 4
        
        // Declares delegate and operation in 1 line, returns a value
        // set input dataTypes first then output dataType
        System.Func<int, int> op2 = num => { return num * 3; };
        System.Console.WriteLine(op2(2));  // 6
    }
}
```
* Events
  * it is a way for 1 object to subscribe to events that are happening within another object and then do some sort of logic around that
```c#
// naive way of writing events
public class Person {
    private string _name;
    private ClockTower _tower;

    public Person(string name, ClockTower tower) {
        _name = name;
        _tower = tower;

        // chain events
        _tower.Chime += () => System.Console.WriteLine($"{_name} heard the chime.");
    }
}

public delegate void ChimeEventHandler();

public class ClockTower {
    public event ChimeEventHandler Chime;  // more events can be created to handle the different chime timings but it is hard coding

    public void ChimeFivePM() {
        Chime();
    }

    public void ChimeSixAM() {
        Chime();
    }
}

class MainClass {
    static void Main(string[] args) {
        // 1 tower
        ClockTower tower = new ClockTower();
        // 1 tower watched by multiple People
        Person person1 = new Person("John", tower);
        Person person2 = new Person("Sally", tower);
        tower.ChimeFivePM();  // can't tell the difference between the 2 events
        /*
        John heard the chime.
        Sally heard the chime.
        */
        tower.ChimeSixAM();  // can't tell the difference between the 2 events
        /*
        John heard the chime.
        Sally heard the chime.
        */
    }
}


// Using Event args
public class Person {  // subscriber
    private string _name;
    private ClockTower _tower;

    public Person(string name, ClockTower tower) {
        _name = name;
        _tower = tower;

        // chain events with +=
        // use event args in switch case to manage multiple cases
        _tower.Chime += (object sender, ClockTowerEventArgs args) =>
        {
            System.Console.WriteLine($"{_name} heard the chime from {((ClockTower)sender).name}.");
            switch(args.Time) {
                case 6: System.Console.WriteLine($"{_name} is waking up!");
                    break;
                case 17: System.Console.WriteLine($"{_name} is going home!");
                    break;
                default: break;
            }
        };
    }
}

public class ClockTowerEventArgs : System.EventArgs {  // create event class to distinsh between multiple cases
    public int Time { get; set; }
}

public delegate void ChimeEventHandler(object sender, ClockTowerEventArgs args);  // add event args to enable handling of multiple cases for 1 event type

public class ClockTower {  // publisher
    public string name = "tower A";
    public event ChimeEventHandler Chime;  // 1 event type to handle multiple cases

    public void ChimeFivePM() {
        Chime(this, new ClockTowerEventArgs { Time = 17 });  // use event class to create unique case
    }

    public void ChimeSixAM() {
        Chime(this, new ClockTowerEventArgs { Time = 6 });  // use event class to create unique case
    }
}

class MainClass {
    static void Main(string[] args) {
        // 1 tower
        ClockTower tower = new ClockTower();
        // 1 tower watched by multiple People
        Person person1 = new Person("John", tower);
        Person person2 = new Person("Sally", tower);
        tower.ChimeSixAM();
        /*
        John heard the chime from tower A.
        John is waking up!
        Sally heard the chime from tower A.
        Sally is waking up!
        */
        tower.ChimeFivePM();
        /*
        John heard the chime from tower A.
        John is going home!
        Sally heard the chime from tower A.
        Sally is going home!
        */
    }
}


// Using System.EventHandler (auto generate delegates)
public class Person {  // subscriber
    private string _name;
    private ClockTower _tower;

    public Person(string name, ClockTower tower) {
        _name = name;
        _tower = tower;

        // chain events with +=
        // use event args in switch case to manage multiple cases
        _tower.Chime += (object sender, ClockTowerEventArgs args) =>
        {
            System.Console.WriteLine($"{_name} heard the chime from {((ClockTower)sender).name}.");
            switch(args.Time) {
                case 6: System.Console.WriteLine($"{_name} is waking up!");
                    break;
                case 17: System.Console.WriteLine($"{_name} is going home!");
                    break;
                default: break;
            }
        };
    }
}

public class ClockTowerEventArgs : System.EventArgs {  // create event class to distinsh between multiple cases
    public int Time { get; set; }
}

// public delegate void ChimeEventHandler(object sender, ClockTowerEventArgs args);  // not required

public class ClockTower {
    public string name = "tower A";
    // public event ChimeEventHandler Chime;  // convert to the following
    public event System.EventHandler<ClockTowerEventArgs> Chime;  // by using Sysmtem.EventHandler it handles the delegate declaration for us

    public void ChimeFivePM() {
        Chime(this, new ClockTowerEventArgs { Time = 17 });
    }

    public void ChimeSixAM() {
        Chime(this, new ClockTowerEventArgs { Time = 6 });
    }
}

class MainClass {
    static void Main(string[] args) {
        ClockTower tower = new ClockTower();
        Person person1 = new Person("John", tower);
        Person person2 = new Person("Sally", tower);
        tower.ChimeSixAM();
        tower.ChimeFivePM();
    }
}
```
* Extension methods
  * allow us to add methods to an existing class without changing its source code or creating a new class that inherits from it
  * if have source code, modify source code instead of creating extension methods
```c#
public class Person {  // given to us by others, this source code we can't see or modify directly
    public string Name { get; set; }
    public int Age { get; set; }
}

public static class Extensions {  // creates an extension of the Person class by using the static in class declaration
    public static void SayHello(this Person person, Person person2) {  // this keyword must be added only for the 1st arg
        System.Console.WriteLine($"{person.Name} says hello to {person2.Name}");
    }
}

class MainClass {
    static void Main(string[] args) {
        Person p = new Person { Name = "John", Age = 21 };
        Person p2 = new Person { Name = "Sally", Age = 25 };
        p.SayHello(p2);  // "John says hello to Sally"
    }
}
```
* LINQ: Language Integrated Query
  * gives the capability to query objects
  * can qury
    * objects in memory, eg collections (LINQ to Objects)
    * Databases (LINQ to Entities)
    * XML (LINQ to XML)
    * ADO.NET Data Sets (LINQ to Data Sets)
  * keywords
    * where: set conditions
    * orderby
      * ascending order
        > orderby variableName
      * descending order
        > orderby variableName descending
    * select
      * cannot be used with group keyword
      * query result will become an array of values
      * must end with a ;
        > select variableName;
    * group
      * cannot be used with select keyword
      * query result will become an array of dictionaries
      * must end with a ;
        > group variableName by variableName;
```c#

// simple example
using System.Linq;  // this is required for query usage

class MainClass {
  public static void Main() {
    string sample = "The quick brown fox jumps over the lazy dog.";
    
    var resultArr = from c in sample.ToLower()
                    where c== 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u'
                    orderby c
                    select c;
                    // group c by c;
    foreach (var c in resultArr)
      System.Console.WriteLine(c);  // use for select to get value
      // System.Console.WriteLine(c.Key);  // use for group to get value
  }
}


// realistic example
using System.Linq;

public class Person {
  public string FirstName { get; set; }
  public string LastName { get; set; }
  public int Age { get; set; }
}

class MainClass {
  public static void Main() {
    System.Collections.Generic.List<Person> people = new System.Collections.Generic.List<Person> {
      new Person{FirstName="John", LastName="Doe", Age=25},
      new Person{FirstName="John2", LastName="Doe2", Age=26},
      new Person{FirstName="John3", LastName="Doe3", Age=20},
    };
    
    // method 1: LINQ Query Operators
    var resultArr = from p in people
                    where p.Age < 25
                    select p;
                    
    // method 2: LINQ Extension methods
    // var resultArr = person.Where(p => p.Age < 25).Select(p => p);
    
    foreach (var item in resultArr)
      System.Console.WriteLine(item.FirstName);  // prints out firstnames of those with age less than 25
  }
}
```
* Reflection
```c#
public class Sample { 
    public string Name { get; set; }
    public int Age;

    public void MyMethod() { }
}

class Program
{
    static void Main(string[] args)
    {
        var assembly = System.Reflection.Assembly.GetExecutingAssembly();
        System.Console.WriteLine(assembly.FullName);  // Override, Version=1.0.7333.32664, Culture=neutral, PublicKeyToken=null
        var types = assembly.GetTypes();
        foreach (var type in types) { 
            System.Console.WriteLine("class: " + type.Name + " BaseType: " + type.BaseType);  // class: Program BaseType: System.Object
            var props = type.GetProperties();
            foreach (var prop in props)
                System.Console.WriteLine("Property name: " + prop.Name + " Property type: " + prop.PropertyType);  // Property name: Name Property type: System.String
            var fields = type.GetFields();
            foreach (var field in fields)
                System.Console.WriteLine("Field: " + field.Name);  // Field: Age
            var methods = type.GetMethods();
            foreach (var method in methods)
                System.Console.WriteLine("Method: " + method.Name);
                /*
                // class: Program
                Method: Equals
                Method: GetHashCode
                Method: GetType
                Method: ToString

                // class: Sample
                Method: get_Name
                Method: set_Name
                Method: MyMethod
                Method: Equals
                Method: GetHashCode
                Method: GetType
                Method: ToString
                */
        }
    }
}
```
### c++
[back to top](#table-of-contents)
