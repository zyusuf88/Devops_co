
zshrc file

1. open the file : `nano ~/.zshrc`
2. And then set the ZSH_THEME value to whatever value you want to use like this:
`ZSH_THEME="robbyrussell"`
### If having trouble with zsh files,  delete then redownlaod:

`rm -rf ~/.oh-my-zsh`
`rm ~/.zshrc`
`cp ~/.zshrc.pre-oh-my-zsh ~/.zshrc`
`source ~/.zshrc`
#### after that install again
`sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`


### sCRIPTING 

How to run a script from anywhere without specifing the path

1. Place the file in the PATH. run: `echo $PATH` . Any file in this directories can be run from anywhere
2. choose a file path for e.g: `/usr/local/bin` Type: `sudo mv name-of-file.sh /usr/local/bin/name-of-file`
3. chmod as this is a script : `sudo chmod +x /usr/local/bin/name-of-file`
4. *now you can run the `name-of-the-file` withought using bash or .sh. It will still run in ANY directory*