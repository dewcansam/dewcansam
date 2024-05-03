# Help4 doxygen file template

This is the template that should be used for all files. Note that this is using 
C-style comment heading. Other languages should use their respected comment 
blocks. That will be on the todo list. I made all the templates years ago.
However, they should be updated and placed here.

<pre>
/***************************************************************************//*!
    @copyright      $date_created
    @attention      This work is licensed under CC BY-SA 4.0
    @file           $filename.ext
    @version        1.1
    @date           $date_updated
    @author         $name
    @details        expanded info for file
    @bug            command bug is to list things to be done - future
    @todo           command todo is for things that HAVE been done - past
    @warning        command warning is for alerts - present
***************************************************************************** */
</pre>

**@copyright** is the date the file was created. This HAS to be here to fix date mangling by the OS. **Required**

**@attention** is the copyright tag. This has to be here because the copyright tag is being used for the init date. **Required**

**@file** is the filename. This can be filename with or without the extension, version or date if filename includes that info.

**@version** is the version number. Duh. Really should be in float notation N.N **Required**

**@date** is the date of the last edit or last modification. Does not really need to be here. **Optionial**

**@author** is the name of the author. Include a single author line for every author. **Required**

**@details** is the main idea of the file or function. i.e. What am I writing this file or function for. **Required**

**@bug** command bug is a list of things to be done - future

**@warning** command warning is a list for alerts - present

**@todo** command todo is a list of things that HAVE been done - past **Required**

I have a very different idea of what a todo is. 
What I view as a todo is that it should be kinda of a log of things done for that file or function.
If you stop and think a @bug, @todo, and @warning are levels for the exact same thing.

Things that need to get done. A @bug is something that you have found wrong and need todo it.
A @warning is something that you are trying to warn people of and probably should todo it.
So why a @todo when a @bug can be used for the same thing.
So I differentiate them by saying a @bug is something to be done. A @todo is something already done. 

The doxygen commands @bug @warning @todo should be in that order. 
Especially since the @todo should be a log that gets ammended anytime something major is done.

## History

So back in 1999 when I first started working for a small web programming outfit.
We were a group of 5-6 guys that generally had differnet areas so stomping on other workers toes was not much of an issue.
I started as a HTML, javascript and rough graphic designer. It was quickly noted that I needed to be working on the backend.
I taught myself PHP, ASP, CFM and SQL (along with flash, but we won't talk about that)
Upon learning those, then it was mostly Vic as lead and Jim and I were sub.
And quickly started having issues with 1 person changing a file without anyone else knowing. 
We were using a editor named Visual SlickEdit. VSE allowed to create templates that had variables you could change.
I developed something like this and set some defs. Everyone else loved it and it was adopted company wide. 
The @todo section was also very popular as it left a record of file changes. With a copy on everyone's computer
the @todo and diff made things so much easier to compare and track in the days before git.

The first couple of file headers were just VSE templates that we shared. Not sure when we (I) found doxygen, because the
VSE htemplate that I had come up with was not that far from doxygen tags. At some point the were modified to comply with doxygen.
I have been using them ever since.


