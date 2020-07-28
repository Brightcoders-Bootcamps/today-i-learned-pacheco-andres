# Today I Learned by *[Andres Pacheco]*

Ruby and Rails official documentation reading personal journal

## Week 1

### Thursday 23, July 2020 *[ARGF]*
ARGF is a sequence designed for use in scripts that process files given as command line arguments or passed through STDIN.

The arguments passed to your script are stored in the ARGV array, one argument per element. ARGF assumes that any argument other than the file name has been removed from ARGV.

Example
$ ruby ​​argf.rb --verbose archivo1 archivo2

ARGV # => ["--verbose", "archivo1", "archivo2"]
opción = ARGV.shift # => "--verbose"
ARGV # => ["archivo1", "archivo2"]

––––––––––––––––––––––––––––––
ARGV . reemplazar [ "archivo1" ]
 ARGF . readlines  # Devuelve el contenido del archivo1 como una matriz 
ARGV            # => [] 
ARGV . reemplace [ "archivo2" , "archivo3" ]
 ARGF . read       # Devuelve el contenido de file2 y file3


 ### Friday 24, July 2020 *[ArgumentoError]*

 Raised when the arguments are wrong and there isn't a more specific Exception class.

Ex: passing the wrong number of arguments

[1, 2, 3].first(4, 5)
raises the exception:

ArgumentError: wrong number of arguments (given 2, expected 1)
Ex: passing an argument that is not acceptable:

[1, 2, 3].first(-4)
raises the exception:

ArgumentError: negative array size

### Monday 27, July 2020 *[Array]*

Array
Arrays are ordered, integer-indexed collections of any object.

Array indexing starts at 0, as in C or Java. A negative index is assumed to be relative to the end of the array—that is, an index of -1 indicates the last element of the array, -2 is the next to last element in the array, and so on.

Creating Arrays¶ ↑
A new array can be created by using the literal constructor []. Arrays can contain different types of objects. For example, the array below contains an Integer, a String and a Float:

ary = [1, "two", 3.0] #=> [1, "two", 3.0]

### Tuesday 28, July 2020 *[BasicObject]*

BasicObject is the parent class of all classes in Ruby. It's an explicit blank class.

BasicObject can be used for creating object hierarchies independent of Ruby's object hierarchy, proxy objects like the Delegator class, or other uses where namespace pollution from Ruby's methods and classes must be avoided.

To avoid polluting BasicObject for other users an appropriately named subclass of BasicObject should be created instead of directly modifying BasicObject:
 ==========
class MyObjectSystem < BasicObject
end