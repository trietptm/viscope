## Installation ##
Copy vs.dll to windbg's winext directory

ex) C:\Program Files\Debugging Tools for Windows (x86)\winext

## Commands ##
**help: show help**

**dt: Show data structure in graph format**

**kb: show stack frames using heuristics, show exception records**

**u: disassemble and show in graph format**

**trace: trace by basic blocks and shows code path**

<pre>
!vs.trace -o <filename> -b 30 <address><br>
-o [filename]: Output filename<br>
-b <number>: Maximum number of basic block to trace<br>
-c: Automatic continue<br>
</pre>

**debuglevel: set debug level**

## Example ##
**Launch windbg
> "C:\Program Files\Debugging Tools for Windows (x86)\windbg"**

**Run sample program
> c:\windows\system32\notepad.exe**

**Start tracing on kernel32!CreateFileW**<pre>
!vs.trace -o CreateFile%d.dot kernel32!CreateFileW<br>
</pre>

**Output will be like following:**

![http://viscope.googlecode.com/svn/wiki/CreateFileW-0-Small.png](http://viscope.googlecode.com/svn/wiki/CreateFileW-0-Small.png)