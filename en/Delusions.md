---
title: ConEmu | Console-related delusions

description: "There are several delusions frequently said by users.
   This article explains few of them."

breadcrumbs:
 - url: TableOfContents.html#conemu
   title: ConEmu

readalso:
 - url: TableOfContents.html#terms
   title: ConEmu terms
 - url: ConEmuFAQ.html
   title: Frequently Asked Questions
 - url: TerminalVsShell.html
   title: Terminal vs Shell

otherlang:
   en: /en/Delusions.html
   ru: /ru/Delusions.html
---

# Console-related delusions

* [Not a console application](#delusion-1)
* [Not a console window](#delusion-2)


<h2 id="delusion-1">
To treat PuTTY, mintty and others as ‘console applications’.
</h2>

Simplifying, a ‘console application’ is an executable which
interacts with user via data input/output (mainly text). A ‘Console
application’ is not able to ‘draw’ anything, it has not graphical
interface at all. It works with input/output streams only
(redirection, pipes, magic symbols `<`, `>`, `|`).

    cmd /? > cmd.log & type cmd.log | find "HKEY"

When a ‘console application’ starts in Windows the special console
window is created and that very window does all text drawing, which
‘console application’ has printed, and that window redirects user
keypresses into ‘console application’ input buffer. This console
window is often called (local) terminal.

PuTTY, KiTTY, mintty and other terminals ARE NOT ‘console
applications’. They are graphical applications (have their own
graphical interfaces) able to connect to remote servers to run
‘console applications’ remotely, or they are working as local
terminals allowing input/output ability to ‘console applications’ on
your local PC.

You can't redirect terminal "output" into any local file because
terminal is working with display and keyabord but not any
input/output streams. The only exception is logging specially
configured in that exact terminal.

<h2 id="delusion-2">
To name standard Windows console - ‘cmd.exe’.
</h2>

Windows has its own terminal (or ‘console window’) which is often
erroneously called ‘cmd.exe’. Just press Win+R and run, for example,
"powershell.exe". You will not see "cmd.exe" in the started process
tree. In older versions of Windows versions different executables create a
console window. For Windows 7 or higher it is "conhost.exe".

Not ‘cmd.exe’, just a ‘console’!
