## NASA ROBOT Challenger

Technical Challenger

## Objectives

* The terrain should be 5x5 dimension.
* The robot starts in the position (0,0,N).
* The rebot returns the final position after execute command.
* The robot should respect the terrain limits.
* The robot should't save positions log.

## Request API examples

Command to REST:

`curl -s --request POST http://localhost:8080/rest/mars/MMRMMRMM`

Response:

```
{ "x": 2, "y": 0, "d": "S" }
```

OR

Command to TEXT:

`curl -s --request POST http://localhost:8080/text/mars/MMRMMRMM`

Response:

```
(2, 0, S)
```

* "x" to axis x
* "y" to axis y
* "d" to direction ("W"est, "N"orth, "E"ast and "S"outh)

## Docker runner

### Start

`./run_container.sh start`

### Stop

`./run_container.sh stop`

### Unit tests

`./run_container.sh tests`

## Standalone execution

### Install prerequisites

`pip3 install -r requirements.txt`

### Start API

`python3 robot/run.py`

### Unit tests

`puthon3 robot/tests.py`

### Terminal output example

```
esteves@morpheus:~/projects/nasa/robotpy$ python robot/run.py
 * Running on http://0.0.0.0:8080/
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /rest/mars/LLLL HTTP/1.1" 200 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /rest/mars/RRRR HTTP/1.1" 200 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /rest/mars/AAA HTTP/1.1" 400 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /rest/mars/MMLMMMMMMMMMMM HTTP/1.1" 400 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /rest/mars/MML HTTP/1.1" 200 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /text/mars/MML HTTP/1.1" 200 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /rest/mars/MMMMMRMMMMMRMMMMMRMMMMMR HTTP/1.1" 200 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /rest/mars/MMRMMRMM HTTP/1.1" 200 -
 127.0.0.1 - - [12/Jul/2017 08:09:29] "POST /text/mars/MMRMMRMM HTTP/1.1" 200 -
```
