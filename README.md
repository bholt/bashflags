BashFlags
=========

Stand-alone command-line argument parsing for bash, in the style of Google's `gflags` library.

To use this library, include this script in your project and:

~~~bash
# source this script
source flags.bash

# declare your flags, e.g.:
declare_flag 'num' 0 'Number of elements.'

# pass command-line args to be parsed
parse_flags $@

# use declared flag
echo "Num: $FLAGS_num"

# get extra args (those after --)
echo "Extra: $FLAGS_extra"
~~~

## Git subtree
You can include this library as a subdirectory in your git project as follows:

~~~bash
git subtree add --squash --prefix=third-party/bashflags git@github.com:bholt/bashflags.git master
~~~

To update to a newer version of the utility:

~~~bash
# if you haven't already, add the remote:
git remote add bashflags git@github.com:bholt/bashflags.git
# pull down the changes
git pull -s subtree --squash bashflags master
# commit the changes as a single commit (enter a helpful commit message)
git commit -m"update bashflags"
~~~
