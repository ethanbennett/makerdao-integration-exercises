<h1 align="center">
  Integration/Maker.js Examples
</h1>

### leverage

Lock ETH -> Draw DAI -> Exchange Dai for ETH -> repeat

__Example usage__
```shell
export KOVAN_PRIVATE_KEY=0xabc... # your key goes here
cd leverage
node . 1 400 0.1
```
* The first argument is the number of iterations
* The second argument is the ETH price floor
* The third argument is the initial amount of ETH

### react-example

Interact with Maker.js in the browser.

To set your private key:
* `cd react-example`
* `cp .env.example .env`
* Add your key (as a string) where prompted in `.env`


### topup

Prevent your CDP from getting liquidated (automated risk management) -- "top it up" with collateral to stay above a target collateralization ratio.

__Example usage__
```shell
export KOVAN_PRIVATE_KEY=0xabc... # your key goes here
cd topup
node . 1234 -t 2.5 -v
```
* The first argument is a CDP ID.
* The value for the `-t` argument is the target ratio.
* `-v` enables verbose mode (shows stack traces for errors).
