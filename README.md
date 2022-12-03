# Presentation

This code runs the experimental validation for the paper:

Title: Minimisation of Spatial Models using Branching Bisimilarity
Authors: Vincenzo Ciancia, Jan Friso Groote, Diego Latella, Mieke Massink and Erik P. de Vink
FORMAL METHODS 2023 

See https://fm2023.isp.uni-luebeck.de

This repository is obtained by using "git archive" of the main branch with tag "zenodo-FM2023" of the repository:

https://github.com/VoxLogicA-Project/Validation-FM2023

# Usage

## Disclaimer

This archives only works on linux, and has been tested on ubuntu-20.04 and
ubuntu-21.10.

## Prerequisites

It is very likely that you already have all the dependencies installed, but just in
case: on ubuntu, one needs to install python3 and python3-pip

    sudo apt install python3 python3-pip 
    
after which the python prerequisites pandas and pillow can be installed using 

    pip3 install pandas pillow

## Running the tests

To run the tests, run the file runTests.py either directly

    ./runTests.py

(requires the execute bit set, but it should already be so after unpacking), or
via python3

    python3 ./runTests.py

## Results

See the comments in runTests.py or the paper to see what the tests are doing. 

The results are the files "rawdata.csv" (raw data from experiments) and
"results-table.csv" (table massaged to be included in latex; note that the
labels are not exactly the same as those in the paper but they should be clear
nevertheless.).

## Dockerfile

We also include a Dockerfile building against the ubuntu-22.04 image for
long-term reproducibility. 

Should you be unfamiliar with docker, but willing to use the images, you need to
have docker installed and working, then to build the image, then to run it, for
instance, using the two commands below.

    docker build --progress=plain .
    docker run --rm $(docker build -q .)

# COPYRIGHT

## mCRL2 License:

Boost Software License - Version 1.0 - August 17th, 2003

Permission is hereby granted, free of charge, to any person or organization
obtaining a copy of the software and accompanying documentation covered by
this license (the "Software") to use, reproduce, display, distribute,
execute, and transmit the Software, and to prepare derivative works of the
Software, and to permit third-parties to whom the Software is furnished to
do so, all subject to the following:

The copyright notices in the Software and this entire statement, including
the above license grant, this restriction and the following disclaimer,
must be included in all copies of the Software, in whole or in part, and
all derivative works of the Software, unless such copies or derivative
works are solely in the form of machine-executable object code generated by
a source language processor.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE, TITLE AND NON-INFRINGEMENT. IN NO EVENT
SHALL THE COPYRIGHT HOLDERS OR ANYONE DISTRIBUTING THE SOFTWARE BE LIABLE
FOR ANY DAMAGES OR OTHER LIABILITY, WHETHER IN CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
DEALINGS IN THE SOFTWARE.

## VoxLogicA/GraphLogicA license:

Copyright 2018 Vincenzo Ciancia.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.

A copy of the license is available in the file "Apache_License.txt".
You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

