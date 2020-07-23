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