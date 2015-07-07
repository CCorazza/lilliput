![Scale icon](http://b.dryicons.com/images/icon_sets/minimalistica_icons/png/128x128/cut.png) Cut down on your code and gain back those precious octets. 

*Maybe you were looking for [uglify](https://github.com/mishoo/UglifyJS2) ?*
*Uglify is a powerful, and really complete library for npm with dependencies, 59 contributors and something like 6 millions download a month.*

This is not it. Lilliput is a really lightweight functionnal script that take your files and * "minify" * them.

You may clone or unzip this project into your own, or use `npm install lilliput`.
===
###### Use
===

`lilliput`: same as

`lilliput -A, --all` : take and compress every file in your directory and subdirectories into one, named `all.min.css`

`-S, --separate` : every file in your directory and subdirectories is minified, but retain its name as `file_name.min.css`

`-d, --delete` : remove the file(s) used to create the mini version from your directory.

`-D, --delete-all` : remove all files used to create the mini version from your directory. (Be careful !)

`-O, --output [name]` : specify the name of your output file as `new_name.min.css`. Implies `--all` if you do not supply file names as optional arguments. Is irrelevant with `--separate`. However, you can use as many `--output` or ``--delete`` as you provide filenames. 

For example :


``` shell

$> lilliput -A
	> [x] created all.min.css
$> lilliput file1.css  file2.css -d file3.css file4.css -O adhoc
	> [x] created adhoc.min.css
	> [x] removed file2.css
	> [x] file5.css, file6.css, tintin.css were ignored.

```