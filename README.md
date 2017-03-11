## Synopsis

This package contains a skeleton FFBO Application, to enable quick creation of new apps.

## Installation

This component can be run using docker, with local bindings.

First you must update the url parameter in config.py to reflect the IP address of the local FFBO processor instead of local host:

Then you can build and run the component using the scrips in the docker folder:
    sh docker_build.sh
    sh docker_run.sh

