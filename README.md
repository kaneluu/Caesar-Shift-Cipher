# Caesar-Shift-Cipher
Read in a STREAM of text, (not just a line, but a stream of arbitrary
length, until you encounter EOF  [cin.eof() == true]) a char at a time,
and as you do so, shift each >>>letter<<< forward in the alphabet a
certain number of places.  The number of places is read from the command
line in argv[1], and turned into an int with: int shift = atoi(argv[1]) ;

You should build on the waterpump.cpp program which was provided to you.

READ THE COMMAND LINE FOR AN INTEGER IN ARGV[1]
int shift = atoi( argc[1]) ;

Example:

(using shift 13)
Hello, Jack
Uryyb, Wnpx


Run it through atoi() to convert the command line string to an integer:

int shift = atoi(argv[1]) ;


Remember that if you shift a letter off the end of the alphabet, we must 
"wrap around" so we come back in down by 'a'.

Here's the pseudocode:

read in a character c

if (c is a letter )
{
	make c lowercase

	make c a number between 0 and 25

	add the shift value to c

	mod c so it's between 0 and 25 again

	add a 'a' to c so it's a real ASCII letter again.
}
print c on the output  // this happens for ALL input, not just letters!
