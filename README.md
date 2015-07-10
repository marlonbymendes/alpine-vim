**The best way to use:**  
--------------------

Make an alias:  

```
alias edit="docker run -ti --rm -v $(pwd):/home/developer/workspace jare/vim-bundle"
```

Have fun!  

```
edit some.file
```

*[How to use docker without sudo](http://askubuntu.com/questions/477551/how-can-i-use-docker-without-sudo)*

**Plugins**  
------------
1. <https://github.com/bling/vim-airlined>   
2. <https://github.com/majutsushi/tagbar>   
3. <https://github.com/vim-scripts/EasyGrep>   
4. <https://github.com/jlanzarotta/bufexplorer>   
5. <https://github.com/kien/ctrlp.vim>   
6. <https://github.com/scrooloose/nerdtree>    
7. <https://github.com/jistr/vim-nerdtree-tabs>   
8. <https://github.com/scrooloose/syntastic>   
9. <https://github.com/tomtom/tlib_vim>   
10. <https://github.com/marcweber/vim-addon-mw-utils>   
11. <https://github.com/altercation/vim-colors-solarized>   
12. <https://github.com/vim-scripts/taglist.vim>   
13. <https://github.com/tpope/vim-commentary>   
14. <https://github.com/terryma/vim-expand-region>   
15. <https://github.com/tpope/vim-fugitive>   
16. <https://github.com/airblade/vim-gitgutter>   
17. <https://github.com/fatih/vim-go>   
18. <https://github.com/plasticboy/vim-markdown>   
19. <https://github.com/michaeljsmith/vim-indent-object>   
20. <https://github.com/terryma/vim-multiple-cursors>   
21. <https://github.com/tpope/vim-repeat>   
22. <https://github.com/tpope/vim-surround>   
23. <https://github.com/vim-scripts/mru.vim>   
24. <https://github.com/vim-scripts/YankRing.vim>   
25. <https://github.com/tpope/vim-haml>   
26. <https://github.com/garbas/vim-snipmate>   
27. <https://github.com/honza/vim-snippets>   
28. <https://github.com/derekwyatt/vim-scala>   
29. <https://github.com/Valloric/YouCompleteMe>  

**[.vimrc](https://github.com/JAremko/alpine-vim/blob/master/.vimrc)** 
------------------------------------------------------------------------
    

If you don't need YouCompleteMe, Python and "big" features use `jare/vim-bundle:no-ycm` instead. It's one-third the size of this image.

For newbies like me:
-----------------------

* To see fancy arrows you need [Powerline Fonts](http://askubuntu.com/questions/283908/how-can-i-install-and-use-powerline-plugin) on your machine. But if you don't need them remove `let g:airline_powerline_fonts = 1` from the
[.vimrc](https://github.com/JAremko/alpine-vim/blob/master/.vimrc)   

![With and without](http://i.imgur.com/yRWBFgn.jpg)   

* For Golang support you need to symlink goroot and gopath in to the root of the workspace. Or mount them with `-v <local_goroot>:<container_groot> -v <local_gopath>:<container_gopath>` and set environment variables `-e GOROOT=<container_groot> -e GOPATH=<container_gopath>`

* If you have problem with colors switch your terminal to the `solarized dark` theme and make sure that it uses default palette and  256 colors.

* If your terminal doesn't support 256 colors change `TERM` environment variable. For example `docker run .. -e TERM=xterm ...` and lines `set t_Co=256` and
`set term=xterm-256color` in the [.vimrc](https://github.com/JAremko/alpine-vim/blob/master/.vimrc)  accordingly.

**I managed to strip down the image from around 300MB to almost 100MB. Hopefully without breaking things. But mail me if something doesn't work:  <w3techplaygound@gmail.com>**
