# minicommenter

Minialist Commenter, is a Vim commenting plugin.
Unlike other full feature plugins, minicommenter offers the bare minimum for easy commenting.

The unique command `:ToggleComment` is exposed. It is used to comment a single, or a range, of lines.

A global option `g:minicomment_always_use_block` can use to prefer the use of block commenting when available. Note that this still comments line per line. Example for a C/C++ filetype:

With `g:minicomment_always_use_block = 0` (default):

```c
// int main(int argc, char* argv[]) { return 0; }
```

With `g:minicomment_always_use_block = 1`:

```c
/* int main(int argc, char* argv[]) { return 0; } */
```

## Install

**Requires Vim >= 8.0**

The easiest way is to use Vim built-in package manager.

```
mkdir -p ~/.vimrc/pack/plugins/start
cd ~/.vimrc/pack/plugins/start
git clone https://github.com/qdebroise/minicommenter.git
```

Then, you can add the following mapping in your `.vimrc`

```vim
noremap <leader>cc :ToggleComment<CR>
```
