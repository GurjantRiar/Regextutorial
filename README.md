# regextutorial
Regular expressions can be used to find certain patterns of characters within a string. You can also find and replace a character or sequence of characters within a string. They are also frequently used to validate input. This regex matches character information for valid e-mail addresses.

# Anchors
Anchors in Perl Regex do not match any character at all. Instead, they match a particular position as before, after, or between the characters. These are used to check not the string but its positional boundaries.
Following are the respective anchors in Perl Regex:

'^' '$', '\b', '\A', '\Z', '\z', '\G', '\p{....}', '\P{....}', '[:class:]'
 
^ or \A: It matches the pattern at the beginning of the string.

Syntax: (/^pattern/, /\Apattern/).

Example:


#!/usr/bin/perl
$str = "guardians of the galaxy";
  
# prints the pattern as it is
# starting with 'guardians'
print "$&\n" if($str =~ /^guardians/);
  
# prints the pattern 'gua'
print "$&\n" if($str =~ /\Agua/);
  
# prints nothing because 
# the 0th position doesn't start with 'a'
print "$&" if($str =~ /^ans/)

# Quantifiers

In this example, we used + to communicate there is another sequence to be matched as a greedy quantifier. We also used {2,6} as another greedy quantifer to specify the input should be a minimum of 2 characrtors to a maximum of 6 characters.

# Character Classes
In this regular expression, the charactor class /d is used which in Javasctipt classifies the use of any digit from 0 to 9.

# Grouping and Capturing
There are three groups being captured in this example. Group #1 is the username of the e-mail account [a-z0-9_\.-]. The second group captures the domain name or e-mail service being used [\da-z\.-]. Lastly, the third group captures the domain extention (i.e .com or .net) [a-z\.]{2,6}

# Bracket Expressions
Much like the groups in this example, there are also 3 bracket expressions. The information in the bracket expressions is opened and closed between brackets like this []. This indentifies which information is allowed to be matched.

Bracket Expression #1: [a-z0-9_\.-] - includes case sensitive characters from a-z, numbers from 0-9 an underscore, periods and hyphens.

Bracket Expression #2: [\da-z\.-] - includes all digits, case sensitive characters from a-z, periods and hyphens

Bracket Expression #3: [a-z\.] - includes case sensitive characters from a-z and periods.