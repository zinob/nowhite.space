# White space is harmfull

All to often perfectly usefull comits to open source projects are rejected because they are to "airy" or "to dense". Whoch os fWhite space harmful

All to often perfectly useful commits to open source projects are rejected because they are to "airy" or "to dense". There is this notion that adding a character that often does not have any meaning but some [times](https://uvesway.wordpress.com/2013/03/11/some-whitespace-pitfalls-in-bash-programming/) [might](https://stackoverflow.com/questions/12293205/c-is-a-white-space-independent-language-exception-to-the-rule) would make code more legible. This is of cause [just as inane](http://www.linusakesson.net/programming/syntaxhighlighting/) as the idea that adding random dabs of colour to code would make it more understandable. 

Linus Torvalds notes that “If you need more than three levels of indentation your code is broken and should be rewritten” which is reflected in the [Linux Coding Style](https://www.kernel.org/doc/Documentation/process/coding-style.rst).

But of cause, only 3 levels of indentation is trivial to keep in your mind. So rather than wasting valuable horizontal space with useless white-space characters which might at best serve as a malplaced comment and at worst as a down right misleading comment
```
   int target = 8;
   int largest_divisor = 0, divisor = 0;
   for ( divisor = 2; divisor < target - 1; divisor ++ )
      if (target % divisor == 0)
         printf( "found divisor %i\n", divisor );
         largest_divisor = divisor;

   printf( "The largest divisor is %i\n", largest_divisor );
```
Wait what? The largest divisor of 8 is 7? Of cause it is not! There are just semantically irrelevant characters placed there to fool your eyes into believing that there are blocks where there are not!
Compare this to the much more honest whitespaceless example:
```
int largest_devisor=0,devisor=0;
int target=8;
for(devisor=2;devisor<target-1;devisor++)
if(target % devisor == 0)
printf("found devisor %i\n",devisor);
largest_devisor=devisor;
printf("The largest devisor is %i\n",largest_devisor);
```
Here there are no characters to fool the eye, if this is not obvious to you, then you are just not a very experienced programmer.
