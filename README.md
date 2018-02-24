# ppbDice-Contract-Code

#   Environment set up:

Install...
truffle
ethereum bridge (clone from Github(https://github.com/oraclize/ethereum-bridge), then run 'npm install' in unzipped folder

(Optional Install)
Solidity intellij plugIn
Solhint intellij plugIn (depends on installing 'solhint JS' file  in '/usr/local/lib/node_modules/solhint/solhint.js')

To deploy...
testrpc --mnemonic "case meadow shuffle purpose renew echo before correct rate artist seed net" -a 50

cd ~/IdeaProjects/ppbDice/ethereum-bridge-master
node bridge -a 49
  or if using 'truffle develop'
node bridge -H localhost:9545 -a 9 --dev

cd ~/IdeaProjects/ppbDice/
rm -rf build/contracts

truffle migrate --reset --compile-all
  or if using 'truffle develop'
migrate --reset

To run unit tests...
truffle test

If using 'truffle develop' to call contracts directly
truffle develop --log (in a separate window)
truffle develop  (in a separate window, and then run the following)
    compile
    migrate --reset
    Dice.deployed().then(function(instance){return instance.bet({value: 1});});
    Dice.deployed().then(function(instance){return instance.logPosition.call();}).then(function(value){return value.toNumber()});
    Dice.deployed().then(function(instance){return instance.investorsProfit.call();}).then(function(value){return value.toNumber()});
    Dice.deployed().then(function(instance){return instance.investorsLoses.call();}).then(function(value){return value.toNumber()});
    Dice.deployed().then(function(instance){return instance.winAmount.call();}).then(function(value){return value.toNumber()});

To run....
truffle exec TestDice.js

To debug.....
truffle debug 0x48689dd9172ac7a0ccc2496ecd2245d5a5071a7bb64fd28cdf880444a4ac76d5
