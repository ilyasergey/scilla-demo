# Scilla Examples and Exercises

To run the demo, build the latest version of Scilla from the
[development repository](https://github.com/Zilliqa/scilla).

## Preliminaries

Make sure to build the latest
[Scilla sources](https://github.com/Zilliqa/scilla).

## Fun with Scilla expressions

Check out the examples from the `expressions` folder.

### How to run the examples

For type checking:

```
$SCILLA_HOME/bin/type-checker file.scilla
```

For evaluation:

```
$SCILLA_HOME/bin/eval-runner  file.scilla
```

## Playing with Contracts

From the folder `contracts`, run

```
easyrun.sh contractName testNum
```

to execute contract `contractName` with a specific test input number `testNum`.

For instance, running

```
easyrun.sh helloWorld 1
```

will execure the first transaction on the contract `helloWorld`.

To _type-check_ the contract, run

```
$SCILLA_HOME/bin/scilla-checker contract.scilla
```

## Scilla Hackthon Challanges

Check the [list of available tasks](https://github.com/ilyasergey/scilla-demo/blob/master/hackathon/Tasks.md).
