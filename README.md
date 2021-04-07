This repository contains the Catala source files; build rules to produce JS from
them; and a UI on top of them.

Installation
============

- Obtain the [OPAM package manager](https://opam.ocaml.org/), e.g. `brew install opam`
- Setup OPAM, if not already done, e.g. `opam init`
- Install Catala: `opam install catala`

Building & testing
==================

- Build: `make -C backend` -- this will refresh `frontend/main.js`
- Test the Catala source: `make -C backend test`

Running the code
================

Opening up `frontend/index.html` should work locally without even starting an
HTTP server.
