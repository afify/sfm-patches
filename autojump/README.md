# autojump

This patch integrates a directory jumper into sfm, just like the
[autojump](https://github.com/jarun/nnn/blob/master/plugins/autojump)
plugin does with nnn, which was the source of inspiration.

The autojump patch introduces a new command format string
`jump_cmd_format` with the `%s` directive and a new keybinding `z`
into `config.def.h` .  Upon pressing `z`, sfm ask for user input.
Sfm substitutes the input string into the command format
to produce a jump command script. Sfm runs this script and fetches its output.
Sfm assumes that the output is an **absolute path**
to a directory and tries to cd it if possible.

The default `jump_cmd_format` assumes the presence of
[zoxide](https://github.com/ajeetdsouza/zoxide) and
[fzf](https://github.com/junegunn/fzf) in the system.
Though the autojump patch can work with any script that outputs an
absolute path.
The patch can be applied with `git apply sfm-autojump-....diff` .
