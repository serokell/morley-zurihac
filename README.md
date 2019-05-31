# Morley Hackathon (ZuriHac 2019)

[Morley](https://gitlab.com/morley-framework/morley) is a set of developers tools for the [Michelson language](https://tezos.gitlab.io/master/whitedoc/michelson.html) which is the smart contract language of the Tezos blockchain.
During [the hackathon](https://zfoh.ch/zurihac2019/) participants will contribute to Morley.

Michelson is a low-level stack-based language.
The best way to quickly learn Michelson is to go through [this tutorial](https://gitlab.com/morley-framework/michelson-tutorial).
Also make sure to read [`README`](https://gitlab.com/morley-framework/morley/blob/master/README.md) in the `morley` repo.

## Issue tracker

Please note that Morley uses [YouTrack](https://issues.serokell.io/issues/TM) as issue tracker.
You can login there using GitHub account.
For this hackathon we have selected a number of issues which we find the most suitable for it.
All of them have `tm:zurihac` tag.
Full list of all issues with this tag is available [here](https://issues.serokell.io/issues?q=project:%20%7BTezos%20Michelson%7D%20tag:tm:zurihac).
We expect that different people will want to spend different amount of time on Morley.
So we picked issues of different types:
1. Some issues are relatively big (but can be done within time frame of this hackathon) and imply adding new functionality.
2. Other issues are smaller and can be done faster.
They mostly imply improvements of existing functionality or adding something small.

## Overview of the issues

Here is an overview of all issues with `tm:zurihac` tag which should help you pick one to work on.
We start with the most interesting issues which require the biggest effort.
1. [TM-198](https://issues.serokell.io/issue/TM-198).
Interactive debugger.
You need to develop a simplified version of `gdb` for Michelson.
2. [TM-199](https://issues.serokell.io/issue/TM-199).
REPL.
Similar to the previous one, but here you need to develop a REPL to be able to execute standalone instructions.
3. [TM-201](https://issues.serokell.io/issue/TM-201).
Optimizer.
The goal here is to come up with a set of rules that can be used to optimize Michelson contract and implement them.
4. [TM-200](https://issues.serokell.io/issue/TM-200).
Gas consumption profiler.
You need to gather statistics about gas consumption and display it in some nice way.
5. [TM-57](https://issues.serokell.io/issue/TM-57).
There is a custom [`STACKTYPE` instruction](https://gitlab.com/morley-framework/morley/blob/master/docs/morleyInstructions.md#stacktype) which allows us to assert that the stack has a given type signature.
Currently one can write only concrete types (e. g. `int`) or type variables there, but not type constructors applied to type variables (e. g. `pair a b`).
The goal is to modify parser and typechecker to make it possible.
6. [TM-84](https://issues.serokell.io/issue/TM-84).
The goal is to update typechecker to print stack type after processing each instruction.
7. [TM-100](https://issues.serokell.io/issue/TM-100).
Pretty printer.
The goal is to update Michelson printer to print human-readable contract as opposed to printing everything on one line.

First four issues are more substantial and will probably take more time.
Fifth issue looks simpler, but may also take substantial amount of time.
Last two issues are about improving existing functionality and should be easier to do.

## How to proceed

If you have chosen an issue, here are your further steps:
1. Please leave a comment stating that you are working on this issue, even if you are not sure that you'll complete it.
2. Take a look at [contribution guidelines](https://gitlab.com/morley-framework/morley/blob/master/CONTRIBUTING.md).
3. Start hacking ;-)
