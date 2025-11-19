                              WEEK 1 
DAY 1 -- SYSTEM REVERSE ENGINEERING + NODE & TERMINAL MASTERING::::

LESSONS LEARNED :-
-Buffer : it is a storage container that holds all the data at once. good for 
small data.eg- downloading a whole vedio then watching it.
-Stream : loads the data in chunks. good for large data.eg- watching vedios
on youtube.
-fs.readFile()- tool for reading files asynchronously, buffer
-fs.readFileSync()- for synchronous read, buffer
-fs.createReadStream()- async, stream

WHAT BROKE :-
-I had problems with using stream.I was getting wrong output. But then i 
fixed it.

DAY 2 -- NODE CLI APP + CONCURRENCY + LARGE DATA PROCESSING::::

LESSONS LEARNED :-
-Asynchronous programming : when multiple tasks can happen at same time like
downloading a file while reading a file.it doesn't block other tasks as
 done in synchronous programming.
-CLI tool :command line interface tool is a program that we run on terminal
to interact with the system.eg-ls(for getting all files).
-here I learned to build a specific CLI, and the code file was named wordstat.js
-concurrency : JS achieves concurrency by non blocking operations. it means we
can switch tasks. we used promise.all() for concurrency
-performance measurement : process of finding out how long our code takes to
run. methods used in my code Date.now().
-worker thread : it lets you run tasks in parallel with your main code. they
help speed up the task that takes a long time , like heavy calculation or 
data processing without slowing down the rest of the work.eg - calculating 
fibonacci series

WHAT BROKE :-
-I had problems in writing the code, especially for concurrency part
-dividing data in chunks.

DAY 3 -- GIT MASTERY: RESET, REVERT, CHERRY-PICK,BISECT, STASH::::

LESSONS LEARNED :-
-git bisect : search tool for finding bugs
-git reset : you want to change something before commiting. if used then 
commit will be gone but changes will be removed from history but kept in your
 local folder.
-git reset hard : commit along with the changes will be gone
git revert : it created a new commit but keeps the previous one in history
-git stash : sometimes when we work on tasks we need to switch tasks so we 
dont want to commit yet so git stash temprarily stores your work(like a drawer)
so you work on something else and then come back(and take back from drawer)
-git pull : multiple people work on same project so when you work you use 
this command to get all the updated changes in your code as well so that you will
be working on the latest versions
-git stash apply - coming back to work that you stashed
-merging and resolving conflict

WHAT BROKE :-
-faced issues in bisecting but then fixed it

DAY 4 -- HTTP / API FORENSICS (USING CURL + POSTMAN + HEADERS) ::::

LESSONS LEARNED :-
-Traceroute : tool that helps see the path your data takes to travel to
server
- -v : verbose , it gives detailed output
-user agent : info sent by your browser to the server telling it who you are
-ETag : when we ask info from a server it gives a special code called ETag 
that we use when in future we want to get the same info about the same thing
we attach ETag with our request so if the info has changed it will give it but
if it hasnt changed data will not be sent from the server and it will give
304 not modified
-pagination : process of dividing large dataset into smaller chunks instead of 
loading them all at once. here we used limit and skip
-caching : a technique where frequently accessed data is stored temporarlily
in cache so future requests for the same data can be served faster
here we used etag
-headers : these are metadata sent with responses like what kind of data is
being sent , wheteher c aching is allowed, authentication etc

WHAT BROKE :-
-Nothing, there was not much code in this task, it was mostly theoritical

DAY 5 — AUTOMATION & MINI-CI PIPELINE::::

LESSONS LEARNED :-
-ESLint : tool that checks your code for error like syntax error.helps catch
errors quicky
-prettier : tool, makes sure code is properly formatted like intentation.
improves readability
-checksum : unique hash code for the file to make sure file hasn't been altered
helps verify that file hasn't been changed
-cron : forperforming a task or running a script at a particular time automatically
a scheduling tool
-husky : package downloaded. it runs automatially whenever you try to commit 
your code then runs ESLint and then prettier if problems arises then husky wont let 
you commit

WHAT BROKE :-
-face issues in setting up husky
