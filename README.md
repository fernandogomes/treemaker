# TreeMaker

[TreeMaker] is a computational origami tool developed by [Robert J. Lang]
for calculating crease patterns from stick figure–like tree diagrams. His talk
[*The math and magic of origami*][talk] includes a brief introduction to the
tool:

[![The math and magic of origami, Robert Lang, TED2008][talk_preview]][talk]

The software was last updated in 2006 and doesn't readily run on recent Ubuntu
releases. This repository provides a compatible legacy environment to allow it
to run on recent releases without modification.

## Dependencies

  - [Docker]

## Installation

 1. Clone the repository.

 1. Build TreeMaker and its environment:

    ```bash
    docker build --tag treemaker .
    ```

## Usage

 1. Run TreeMaker via a [wrapper] for `docker run` that configures access to the
    X server:

    ```console
    $ ./docker_run_x --rm treemaker --help
    Usage: TreeMaker [-v] [-h] [-d <str>] [document...]
      -v, --version         show program version
      -h, --help            show option list
      -d, --datadir=<str>   TreeMaker data directory path prefix
    ```


  [Docker]: https://www.docker.com/
  [Robert J. Lang]: http://www.langorigami.com/
  [talk]: https://youtu.be/NYKcOFQCeno?t=283
  [talk_preview]: https://img.youtube.com/vi/NYKcOFQCeno/mqdefault.jpg
  [TreeMaker]: http://www.langorigami.com/science/computational/treemaker/treemaker.php
  [wrapper]: docker_run_x
