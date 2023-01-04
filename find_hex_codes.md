USE CASES


Looking for Hex Color Values at the End of a Style Block Missing a Semicolon

:#\b\w{1,6}\b"
 
/*
\b is the word boundary
w{1,6} looks for a string with a length of 6
*/


Looking for Hex Color Values with Lowercase Alpha Characters

#[a-f0-9]{6};
 
/* 
[a-f] looks for lowercase alpha chars
[a-f0-9] looks for numeric chars to not exclude hex values that have numbers as well
{6} looks for a six character string
*/




REFERENCE



LOOKAHEAD

x(?=y)
 
/* EXAMPLE [string to search](?=[string to look for]) */
 
&copy;(?=&nbsp;)

/* Looking for instances of "&copy" followed by "&nbsp;" */



NEGATIVE LOOKAHEAD

x(?!y)
 
/* EXAMPLE [string to search](?![string to look for]) */
 
&copy;(?!&nbsp;)

/* Looking for instances of "&copy" NOT followed by "&nbsp;" */



LOOKBEHIND

(?<=y)x
 
/* EXAMPLE [string to search](?![string to look for]) */
 
(?<=&nbsp;)&copy;
/* Looking for instances of "&copy" preceded by "&nbsp;" */



NEGATIVE LOOKBEHIND

(?<!y)x
 
/* EXAMPLE [string to search](?![string to look for]) */
 
(?<!&nbsp;)&copy;
/* Looking for instances of "&copy" NOT preceded by "&nbsp;" */



OR

(x|y)
 
/* EXAMPLE ([look for this thing]|[or look for this other thing!]) */
 
(&nbsp;|&copy;)
/* Looking for instances of "&copy" or "&nbsp;" */

