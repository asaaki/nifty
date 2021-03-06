Nifty
=====

Helper script for setting up the boilerplate required when writing a NIF. I'm using it by installing as an archive, but I guess you *could* install it as a dep.

## Install

```elixir
git clone git@github.com:rossjones/nifty.git
cd nifty
mix do archive.build, archive.install
```

## Commands

```elixir
# Creates a skeleton Makefile, c source and Elxiir module.
mix nifty.gen --library hello --module MyApp.Nif
```

The compile and clean tasks should happen when your normal ```mix compile``` and ```mix clean``` calls happen.


## Extra info

How to set up compilation for make was found at <http://spin.atomicobject.com/2015/03/16/elixir-native-interoperability-ports-vs-nifs/#comment-531191>  which was very helpful in getting started. The mix tasks are derived from <https://github.com/asbaker/elixir-interop-examples/tree/master/serial_nif>