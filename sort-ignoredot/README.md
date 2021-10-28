# sort-ignoredot
This patch adds the option to ignore the initial dot character in a filename when sorting files so 'dotfiles' are sorted by their actual letters, like in `ls -a`.

**before**
`
.bbb
aaa
ccc
`

**after**
`
aaa
.bbb
ccc
`
