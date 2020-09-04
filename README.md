DeskQ (Golang version)
================

The purpose of DeskQ is to provide a way to access or start stuff  
from one place on your desktop. Its like a **"command-line menu."**

DeskQ is a windowless entry field that you position on your desktop.  

You can do things like this:  
* Save URLs and recall them later
* Save text from the clipboard and access later
* Quickly launch an Internet search from your desktop
* Run searches for specific services (like: Google Maps)
* Execute commands to launch programs, documents, or URLs, scripts, ...

DeskQ is a compiled Go binary using the Gtk3 GUI

All of the deskq files must be located in  
one folder.  

Always start deskq from the folder with  
all of the files:  
```text
    serv.txt        user commands, links, services 
    hist.txt        history of search requests  
    clip.txt        saved text clipings  
    urls.txt        saved URLs  
    seaq.txt        search engine query string (comes with Google's)  
    edit.txt        user's text editor name; example: gedit  
    winmet.txt       window metrics file  
    deskq           the binary for DeskQ  


    To activate a command hit Enter or click button (black square)
    Note: You can drag & drop text into the Entry box as well.
        
        Enter or type:  Action:
        
            list        opens dialog with list of saved URLs
            hist        open dialog with list of search texts
            edit        opens all aux text files for editing 
                        or viewing in your text editor
            todo        opens todo.txt in your text editor
            help        opens help.txt in your text editor
            sc          saves contents of clipboard to either
                        clip.txt or urls.txt
            >http...    open the URL in your browser
       
        Enter text for a search
        runs the search in your browser and
        saves the text of your query into hist.txt
```

The __serv.txt__ file: 

You can set up custom links, commands, and services  
by editing the serv.txt file.  
commands must start with one of these characters . ; $  
(see serv.txt for examples)  

Use 0-3 args when setting up a local command.  
The command must be in the system search path.  

Targeted web searches (services) must begin with one letter and a  
colon (:) (see serv.txt for examples)  

Here is the serv.txt file that comes with the distribution:  
```text
    ----COMMANDS----
;git,https://github.com
;greatcourses,https://www.thegreatcourses.com/
;term,xfce4-terminal --geometry 85x32+50+300
;htop,x-terminal-emulator -e htop
;news,https://microsoftnews.msn.com
;reboot,reboot
;dev,bash dev.sh
;serv,xed serv.txt
----SERVICES----
a,Amazon,https://smile.amazon.com/s/ref=nb_sb_noss_1?field-keywords=
m,Google Maps,https://www.google.com/maps/search/
y,YouTube,https://www.youtube.com/results?search_query=
i,Google Images,http://images.google.com/images?q=
w,Wikipedia,https://en.wikipedia.org/w/index.php?title=Special:Searc. . . .
p,Php,http://php.net/manual-lookup.php?pattern=
```

    E N D
