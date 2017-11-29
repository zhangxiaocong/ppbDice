# ppbDice-Contract-Code

Environment set up
++++++++++++++++++

Install...
truffle
ethereum bridge (clone from Github, then run 'npm install in unzipped folder'

To deploy...
testrpc --mnemonic "case meadow shuffle purpose renew echo before correct rate artist seed net" -a 50

cd ~/IdeaProjects/ppbDice/ethereum-bridge-master
node bridge -a 49

cd ~/IdeaProjects/ppbDice/
rm -rf build/contracts

truffle compile --all
truffle migrate --reset

To test...
truffle test

To run....
truffle exec Dice.js