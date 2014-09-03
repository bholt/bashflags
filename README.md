BashFlags
=========

Stand-alone command-line argument parsing for bash, in the style of Google's `gflags` library.

To use this library, include this script in your project and:

~~~ bash
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
