I DO NOT MAINTAIN THIS PACKAGE; I do not know perl.
If someone can and wants to maintain this then please
clone it (and let me know, thanks).

This is the latest version (and only copy!) that I could
find on the net. Archived here before that got lost too..


Output of 'cvs2html -help' follows:

---

A Perl program to transform the 'cvs log' output to HTML.
Usage of cvs2html

cvs2html [-a [-b][-k]] [-n NUMDIF] [-l/-L FTPHOME]
         [-e] [-f] [-d "MMM DD [YYYY]"] [-D DD] [-i IMAGE] [-h]
         [-v] [-w FRAMEWIDTH] [-s PERCENTAGE] [-N MAXCHRONO]
         [-rREV1:REV2] [-c/-C CFILENAME] -O/o HTMLNAME
         [-P CVSPATH] [-V VERBOSITY] [-x SKIPFILENAME]
         [-R CVSWEB ROOT]

Try: cvs2html -help

 cvs2html -O foo
 outputs html files foo.html and alike for each subdirectory
 Note that if foo is a directory the files are stored there
 using the name of the repository as the base filename.

 cvs2html -O foo -v
 which outputs a html file to the file foo.html including
 information about the CVSROOT setting.

 Using -o instead of -O, frames will be made for easy control.

 If -e is specified the log messages are printed
 in courier (non-proportional) font.

 If -c CFILENAME is specified a chronological sorted list of all log
 entries will be saved in CFILENAME (CFILENAME is a full html filename)
 Use -C CFILENAME instead of -c to do reverse sort of the log file.
 Add -p to include cvs log information into the CFILENAME.

 If -a is specified additional fields and files are generated
 containing differences betweeen versions
 in a xdiff-like side by side manner.
 The -n NUMDIF will only output the lastest NUMDIF diff files.
 The -N MAXCHRONO will only show the last MAXCHRONO file changes
 in the chronological list of changes.

 if -b is specified in addition to diff-mode
 spcaces are used as breakpoint to wrap the text
 so the two columns don't exceed the total width
 If -k is specified in addition to diff-mode
 changes in lines caused by CVS-keyword substition
 are ignored.
 If an option -l ftphome is given links to the files relative
 to the URL ftphome is made. Use -L ftphtmlhome to do the same as
 -l, but substitutes file extension with .html

 If an option -d "month day year" is given (year optional) any
 log message prior to that date is omitted. The three first 
 letters of the name of the month is used, e.g., Jun 5.
 A -D DD option will drop any log DD days ago or earlier

 If an option -rREVISIONTAG1:REVISIONTAG2 is given, then
 the log messages are only shown between those revision
 REVISIONTAG1 and REVISIONTAG2. If a file was not tagged
 then the whole revision story of the file will be shown.

 If -o and -w FRAMEWIDTH is used the left frame will have
 FRAMEWIDTH pixels. Add -f when using the -o option to 
 generate individual log files for each file.
 Use -s PERCENTAGE to set width of the fraction of the left
 bar in percentage.

 Use -i IMAGE to replace the background with file specified as IMAGE

 Use -P CVSPATH to specify an explicit location cvs.  The
 default value is simply 'cvs', which means that cvs is in your
 path.

 Use -V VERBOSITY to make cvs2html report what it is doing. A
 value of 0 means be quiet and bigger numbers means more output.
 This is especially useful, when something went wrong.

 Use -R CVSWEBROOT to make reports intergrated with cvsweb.
 The argument should be the symbolic_name in cvsweb.conf.

 Use -x SKIPFILENAME to to exclude all information about files
 with that name.

 The html file also contains anchors, if a file foo.html
 containing a file e.g., foofoo.m is generated then it is
 possible to search http://CORRECT_URL/foo.html#foofoo.m

 Example :
 cvs2html  -l http://cvs.sslug.dk/linuxbog -f -p \\ 
   -o cvs2html/index.html -v -a -b -n 6 -C crono.html
 makes cvs2html/ with individual log data for each file 
 with links relative to "http://cvs.sslug.dk/linuxbog"
 and creates a chronological log file "crono.html".

 cvs2html with no arguments displays this help
 Peter Toft et al, Technical University of Denmark, 1997

