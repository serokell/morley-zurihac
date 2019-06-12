# Morley Hackathon (ZuriHac 2019)

Are you interested in smart contracts?
If you want to learn about this topic and get hands-on experience, developers from Serokell and Tocqueville are happy to offer some real-world tasks to you and help you to solve them.

[Morley](https://gitlab.com/morley-framework/morley) is a set of developer tools for the [Michelson language](https://tezos.gitlab.io/master/whitedoc/michelson.html) which is the smart contract language of the [Tezos blockchain](https://tezos.com/).
Tezos is a new platform for smart contracts and decentralized applications.
It's based on a Proof-of-Stake consensus algorithm and can evolve by upgrading itself.
Its smart contract language — Michelson – is a low-level stack-based language.
Unlike many other smart contract languages, Michelson is statically typed which can prevent many errors in contracts before they are deployed.

* Go through [this tutorial](https://gitlab.com/morley-framework/michelson-tutorial) to get familiar with Michelson.
* After that, clone [https://gitlab.com/morley-framework/morley](https://gitlab.com/morley-framework/morley) to start hacking.
* If you have Docker, you can try `morley` without building anything, just run the `scripts/morley.sh` script in the repo.
* In order to build the project, you need [Stack](https://docs.haskellstack.org/en/stable/README/).
Once you have it, you can use it directly or build the project using `Makefile` from the repo.
In the latter case type `make morley` to build Morley.

## Issues

For this hackathon we have selected a number of issues which we find the most suitable for it and copied them to GitLab.

* Go to [https://gitlab.com/morley-framework/morley/issues](https://gitlab.com/morley-framework/morley/issues) to see all of them.

We expect that different people will want to spend different amount of time on Morley, so we picked issues of different types:
1. Some issues are relatively big (but can be done within time frame of this hackathon) and imply adding new functionality.
2. Other issues are smaller and can be done faster.
They mostly imply improvements of existing functionality or adding something small.

### Overview

Here is an overview of all issues selected for Zurihac which should help you pick one to work on.
We start with the most interesting issues which require the biggest effort.
1. [TM-198](https://issues.serokell.io/issue/TM-198).
**Interactive debugger**.
You need to develop a simplified version of `gdb` for Michelson.
2. [TM-199](https://issues.serokell.io/issue/TM-199).
**REPL**.
Similar to the previous one, but here you need to develop a REPL to be able to execute standalone instructions.
3. [TM-201](https://issues.serokell.io/issue/TM-201).
**Optimizer**.
The goal here is to come up with a set of rules that can be used to optimize Michelson contract and implement them.

These issues are more substantial than others and will probably take more time.

5. [TM-57](https://issues.serokell.io/issue/TM-57).
There is a custom [`STACKTYPE` instruction](https://gitlab.com/morley-framework/morley/blob/master/docs/morleyInstructions.md#stacktype) which allows us to assert that the stack has a given type signature.
Currently one can write only concrete types (e. g. `int`) or type variables there, but not type constructors applied to type variables (e. g. `pair a b`).
The goal is to modify parser and typechecker to make it possible.
6. [TM-84](https://issues.serokell.io/issue/TM-84).
The goal is to update typechecker to print stack type after processing each instruction.
7. [TM-100](https://issues.serokell.io/issue/TM-100).
Pretty printer.
The goal is to update Michelson printer to print human-readable contract as opposed to printing everything on one line.

These issues are about improving existing functionality and should be easier to do.

If you have chosen an issue, please leave a comment stating that you are working on this issue, even if you are not sure that you'll complete it.
