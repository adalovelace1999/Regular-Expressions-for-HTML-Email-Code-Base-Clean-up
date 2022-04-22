# Using Regular Expressions in Atom



Searching with regular expressions in Atom is really easy! Just make sure the regex button is selected when searching and turn the case sensitivity button off.



## General Expressions



### Searching for a String Followed by Something

x(?=y)

#### Explanation

Also known as a lookahead, a type of Regex Assertion

EXAMPLE [string to search](?=[string to look for]) 

&copy;(?=&nbsp;)

Looking for instances of "&copy" followed by "&nbsp;" 



### Searching for a String NOT Followed by Something

x(?!y)

#### Explanation

Also known as a negative lookahead, a type of Regex Assertion

EXAMPLE [string to search](?![string to look for]) 

&copy;(?!&nbsp;)

Looking for instances of "&copy" NOT followed by "&nbsp;" 



### Searching for a String Preceded by Something

(?<=y)x

#### Explanation

Also known as a lookbehind, a type of Regex Assertion

EXAMPLE [string to search](?![string to look for]) 

(?<=&nbsp;)&copy;

Looking for instances of "&copy" preceded by "&nbsp;" 



### Searching for a String NOT Preceded by Something

(?<!y)x

#### Explanation

Also known as a negative lookbehind, a type of Regex Assertion

EXAMPLE [string to search](?![string to look for]) 

(?<!&nbsp;)&copy;

Looking for instances of "&copy" NOT preceded by "&nbsp;" 



### Looking for Multiple Things at Once (OR condition)

(x|y)

#### Explanation

See MDN documentation on Groups and Ranges for more info

EXAMPLE ([look for this thing]|[or look for this other thing!])

(&nbsp;|&copy;)

Looking for instances of "&copy" or "&nbsp;"



## Email-Specific Use Cases



### Looking for Hex Color Values at the End of a Style Block Missing a Semicolon

:#\b\w{1,6}\b"

#### Explanation

\b is the word boundary

w{1,6} looks for a string with a length of 6



### Looking for Hex Color Values with Lowercase Alpha Characters

#[a-f0-9]{6};

#### Explanation

[a-f] looks for lowercase alpha chars

[a-f0-9] looks for numeric chars to not exclude hex values that have numbers as well

{6} looks for a six character string



 