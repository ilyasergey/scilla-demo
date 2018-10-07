## Possible Tasks for the Scilla Hackathon

### Tooling Support

* A REPL for Scilla expressions
* Runner for statements (as we currently have for expressions)
* Property-based testing/fuzzing (a la QuickCheck)
* Write an input generator from message signatures
* A DSL for scripting interaction scenarios with Scilla contracts
* An Emacs completion for Scilla library functions and identifiers
* Code review tool for Scilla

### Implementing Contracts in Scilla

* Implement an Oracle contract with callbacks (see oraclize.it)
* Contract for supporting state channel
* Atomic Swap
* Rock-Paper-Scissors (https://eprint.iacr.org/2015/460.pdf)

### Language Infrastructure and Checkers

* Compiling a subset to Wasm (and support Hello world contract)
* Contract validation (user-defined validation to be run offline before deployment), implemented as static checkers in the pipeline
  * Uniformity of messages being sent (all have same fields)
  * Checking for “prodigal” contracts [give money for free](http://ilyasergey.net/papers/maian-draft.pdf)
  * Detect if a contract can be locking money forever ([“greedy”](http://ilyasergey.net/papers/maian-draft.pdf))
* Simple program checks
  * No integer overflows.
  * No transition accepts payment more than once (proposed solution in [scilla#265](https://github.com/Zilliqa/scilla/pull/265))
  * At least one transition accepts payment.
  * No transition invocation sends more than one message per Recipient.
  * All to the contract imported libraries are used
  * All library functions defined in the contract file are used.
