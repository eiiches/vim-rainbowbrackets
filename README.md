rainbowbrackets.vim
===================

This plugin displays brackets in different colors according to their nesting levels.
Idea is from the [Rainbow Parenthesis](http://www.vim.org/scripts/script.php?script_id=1230) plugin.

![Screen shot](https://github.com/eiiches/vim-rainbowbrackets/raw/master/screenshot.png)

Configuration
-------------

Here's my configuration. But in most cases, the default settings will suffice.

	let g:rainbowbrackets_colors =
				\ [
				\   'ctermfg=9',
				\   'ctermfg=10',
				\   'ctermfg=33',
				\   'ctermfg=190'
				\ ]
	let g:rainbowbrackets_enable_round_brackets = 1
	let g:rainbowbrackets_enable_curly_brackets = 0
	let g:rainbowbrackets_enable_square_brackets = 0
	let g:rainbowbrackets_enable_angle_brackets = 0
	
	augroup vimrc-rainbowbrackets
		autocmd!
		autocmd FileType javascript let b:rainbowbrackets_enable_curly_brackets = 1
	augroup END

Functions
---------

`rainbowbrackets#update()`: Update hightlights using current `b:rainbowbrackets_enable_*_brackets` settings.

`rainbowbrackets#clear()`: Clear highlights.

