## Overview

HalfKP is a free, powerful UCI chess engine derived from Stockfish. It is not a complete chess program and requires a UCI-compatible GUI (e.g. Cute Chess, Fritz, Arena, Sigma Chess, Shredder, Chess Partner or Komodo) in order to be used comfortably.

## UCI parameters

Currently, HalfKP has the following UCI options:

  * #### Debug Log File
    Write all communication to and from the engine into a text file.

  * #### Contempt
    A positive value for contempt favors middle game positions and avoids draws.

  * #### Threads
    The number of CPU threads used for searching a position. For best performance, set
    this equal to the number of CPU cores available.

  * #### Hash
    The size of the hash table in MB.

  * #### Clear Hash
    Clear the hash table.

  * #### Ponder
    Let HalfKP ponder its next move while the opponent is thinking.

  * #### MultiPV
    Output the N best lines (principal variations, PVs) when searching.
    Leave at 1 for best performance.

  * #### Skill Level
    Lower the Skill Level in order to make HalfKP play weaker.

  * #### Move Overhead
    Assume a time delay of x ms due to network and GUI overheads. This is useful to
    avoid losses on time in those cases.

  * #### Minimum Thinking Time
    Search for at least x ms per move.

  * #### Slow Mover
    Lower values will make HalfKP take less time in games, higher values will
    make it think longer.

  * #### nodestime
    Tells the engine to use nodes searched instead of wall time to account for
    elapsed time. Useful for engine testing.

  * #### UCI_Chess960
    An option handled by your GUI. If true, HalfKP will play Chess960.

## Compiling HalfKP

The [MSYS2](https://www.msys2.org/) environment is recommended for compiling HalfKP on Windows.

To compile, type:

    make target ARCH=arch [COMP=comp]

Example: `make build ARCH=x86-64 COMP=mingw`

Lists of supported targets, archs and compilers can be viewed by typing `make help`.
