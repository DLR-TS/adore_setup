
<!--
********************************************************************************
* Copyright (C) 2017-2020 German Aerospace Center (DLR). 
* Eclipse ADORe, Automated Driving Open Research https://eclipse.org/adore
*
* This program and the accompanying materials are made available under the 
* terms of the Eclipse Public License 2.0 which is available at
* http://www.eclipse.org/legal/epl-2.0.
*
* SPDX-License-Identifier: EPL-2.0 
*
* Contributors: 
*   Andrew Koerner
*   Daniel Heß 
********************************************************************************
-->

# ADORe Setup and Getting started
ADORe is an open source toolkit for automated vehicle control and decision making, with the main repository [eclipse/adore](https://github.com/eclipse/adore).
Some modules of ADORe are available at [github/dlt-ts](https://github.com/dlr-ts).
This respository describes setup and getting started for all ADORe repositories.

## System Setup and Requirements
The ADORe team tries to keep system requirements as general as is possible, but some dependencies cannot be avoided.
To use the ADORe build system you must have docker, docker compose, and make installed and configured for your user.
Here is a script to set up system requirements: [install_docker.sh](install_docker.sh)

## Checking out a Repository
Our git repositories use submodules. Configure your ssh keys for [github.com].
You may check-out the main repository in the following way:
```bash
git clone --recurse-submodules git@github.com:eclipse/adore.git
```
If you need a single submodule in a stand-alone context, this is possible as well:
```bash
git clone --recurse-submodules git@github.com:dlr-ts/adore_if_ros_msg.git
```

### Building a Module
Each module provides a Makefile and docker context for build. 
You can build a module by navigating to the module and running 
make build such as the following example:
```bash
cd adore_if_ros_msg
make build
```
After building you can run unit tests by running the provided target:
```bash
make test
```
