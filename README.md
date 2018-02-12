# Dotfiles
In this `README.md` I will show you what kind of Aliases I am using and how I configured them.

### Aliases
I use aliases to enhance my workflow. Long or complicated command lines that I use frequently, are shortened in to speed up my workflow.  

The followings lines have been inserted in `.bashrc`  
Use `nano .bashrc` to insert the following lines.  

##### Alias for testing:
`alias test='"het is gelukt!"'`  
I use this alias to test if my dotfile is working.

##### Alias for connecting my Raspberry Pi:
`alias pi='ssh pi@192.168.1.134'`  
I use this alias to quick-jump to my Raspberry Pi, using a SSH connection.

##### Alias for git checkout:  
`alias gco='git checkout'`  
I find this a convenient and quick way to switch between branches.

### Prompt
I wanted to have a simple and logical prompt for my terminal. I have used the following code:  
`parse_git_branch() {
     git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\ Tom \[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "`  

### Welcome Message

in the `.bash_profile` file I've inserted an `echo`. This will print my welcome message to my terminal, every time when I start it.  

I have inserted the following code:  
`echo "Is that a police?, I'm calling the weed!"`  
I have decided to use 'memes' in my welcome message to cheer myself up, whatever my mood might be.  
[Click here](https://www.youtube.com/watch?v=GAxD39rGUeE) to discover the meme I have used.



### Resources:
* [Prompt mod](https://www.digitalocean.com/community/tutorials/an-introduction-to-useful-bash-aliases-and-functions)
* [Welcome Message](https://unix.stackexchange.com/questions/171938/how-to-display-welcome-message-in-unix)
