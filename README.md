# PKGenerator_Checker
Generate Bitcoin Private Keys and check them against blockexplorer.com

Stupid Python Script that Generates random private keys and checks them in realtime...call this poor mans Mining for BTC - same chances as solo but you could find an address w/ money in it 🤑  This is for entertainment only and is designed to demonstrate how IMPOSSIBLE it is to realistically get a collision and take control of someone else's coin...Credits to @Shlomi for the inspiration...

# Instructions

<strong>BIG OL DISCLAIMER</strong>:  I cannot emphasize this enough - this is for **DEMONSTRATION** and **ENTERTAINMENT** purposes ... you will have much better success finding employment, buying bitcoin and holding it than to have this little goofy script find a populated private key with a balance....though if you happen to find a populated address you may as well call the pressess and let em know you beat the odds with that extreme luck.

1. Clone this script - download it or in the terminal use `git clone https://github.com/Frankenmint/PKGenerator_Checker/`
2. Let's install some dependencies!  `pip install ecdsa hashlib base58 requests`
3. Navigate to the directory: `cd PKGenerator_Checker`
5. Run it! `python PkMaker.py`

# Notes


* What's Going on?:  A random 32 byte Numer is generated and encoded into Hex - Basially a number between 1 and 2^256 OR if counting in decimal form:[115792089237316195423570985008687907853269984665640564039457584007913129639936](http://www.calculatorsoup.com/calculators/algebra/exponent.php).  Then, that key is hashed a few times into a public address [according to these standard rules](https://en.bitcoin.it/w/images/en/9/9b/PubKeyToAddr.png) and is fired off to blockexplorer.com using their API. The script then prints the balance to the console window.
* I threw this together while following along [this video series](https://www.youtube.com/playlist?list=PLH4m2oS2ratfeNpZAoVwPlQqEr3HgNu7S) and reccomend YOU instead watch through the tutorials for your own benefit and to better grasp what happens at the protocol level for [Bitcoin](https://bitcoin.org)


Here's a demonstration of it in action

![demo working](http://g.recordit.co/z6QqeZyEM1.gif "We're Generating Private Keys and Checking Them on the Fly!")

