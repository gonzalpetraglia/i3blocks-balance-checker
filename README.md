# i3blocks balance checker

A simple script that checks the balance of some configured addresses

## Pre-Requisites

In addition to the obvious dependency on i3blocks you have to install some other packages for this to work properly:

`
sudo apt install curl jq
`

## Usage


To start using this block you should do the following steps:

1. Clone this repo


```
git clone https://github.com/gonzalpetraglia/i3blocks-balance-checker.git
```

2. Put the addresses you want to check inside the file addresses.txt, one address in each line. The file has some example addresses, you should remove them.



3. Put the following block on your i3blocks config, of course the interval can be changed and you should replace the placeholders. If the blockchain node's url is not defined it is defaulted to the public node of the RSK's testnet network. 


```
[balance_check]
command=cd <full-path-to-repo> && ./checkBalances <blockchain-node-url>
markup=pango
interval=60
```

## TODO
- Use i3blocks properties to pass the blockchain-node-url
- Enable fetching different addresses for different networks
- Make the threshold configuration more easy