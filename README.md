## NASA ROBOT Challenger

Technical Challenger

## Objectives

* The terrain should be 5x5 dimension.
* The robot starts in the position (0,0,N).
* The rebot returns the final position after execute command.
* The robot should respect the terrain limits.
* The robot should't save positions log.

## Request API example

Command:

`curl -s --request POST http://localhost:8080/rest/mars/MMRMMRMM`

Response:

```
{ "x": 2, "y": 0, "d": "S" }
```

x to axis x
y to axis y
d to direction (West, North, East and South)

## Docker runner

### Start

`./run_container.sh start`

### Stop

`./run_container.sh start`

### Unit tests

`./run_container.sh start`

## Standalone execution

### Start

`puthon3 run.py`

### Unit tests

`puthon3 tests.py`
