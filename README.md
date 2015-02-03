Byteplay lets you convert Python code objects into equivalent objects which are 
easy to play with, and lets you convert those objects back into living Python 
code objects. It's useful for applying crazy transformations on Python functions, 
and is also useful in learning Python byte code intricacies. Check the 
documentation to see it in action!

Byteplay was written by Noam Yorav-Raphael. Support for Python 2.6 and 2.7 was 
added by Greg X. Iain Lowe is maintaining and packaging byteplay for 2.x.
Support for Python 3.x was added by Andrew Barnert.

Byteplay is pretty reliable - Python's complete test suite continues to pass 
after you use byteplay to disassemble all the code in the standard library and 
assemble it again!

Well, that's with 2.5. With 2.6+, various things don't work right inside 
certain combinations of try and with statements. For 2.x, only continue seems
to be affected, and there's a hacky fix for that. For 3.x, there are additional
problems with continue, again hackily fixed, and also for yield from, and
possibly other things. At present, you can't even reassemble the entire stdlib
(although it's pretty close).
