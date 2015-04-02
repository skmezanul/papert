# Logo Commands #
```
Types:

WORDS:          FW BW ....
NUMBERS:        0, 0.1, 20
LISTS:          [1 2 3 5]
SYMBOLS:        "foo "bar
VARIABLES:      :foo :bar 


Supported Commands:

RESET           Clear the screen, move home.


Turtle Movement:

FORWARD n       Move the turtle forward n pixels
FW n    

BACKWARD n      Move the turtle backward n pixels

RIGHT n         Move the turtle left or right n degrees
RT n
LEFT n
LT n

SETX x          Set the co-ordinates of the turtle
SETY y
SETXY x y

HOME            Move the turtle to the home position


Drawing:

CLEARSCREEN     Clear the screen
CLEAR
CS

CIRCLE r        Draw a Circle of radius r around the turtle

ARC r d         Draw an arc of radius r for d degrees

PENUP           Lift the pen up and down
PU
PENDOWN
PD

COLOR [r g b]   Set the pen color

PENWIDTH w      Set the pen width


Arithmetic:

1 + 2                   1 * 2
SUM 1 2                 PRODUCT 1 2
(SUM 1 2 3 ...)         (PRODUCT 1 2 3 ...)

1 - 2                   1 / 2
DIFFERENCE 1 2          DIVIDE 1 2

1 % 2
MOD 1 2

Logical and Comparison:

1 = 1
EQUAL? 1 1
EQUALP 1 1

1 < 2                1 <= 2
LESS? 1 2               LESSEQUAL? 1 2
LESSP 1 2               LESSEQUALP 1 2

2 > 1                2 > 1
GREATER? 2 1            GREATEREQUAL? 2 1
GREATERP 2 1            GREATEREQUALP 2 1

AND TRUE FALSE          OR FALSE TRUE

Conditionals:

IF COND [IF_TRUE] 
IF 2 > 1 [FW 100]

IFELSE COND [IF_TRUE] [IF_FALSE]
IFELSE 2 > 1 [FW 100 RT 90] [BW 100 LT 90]


Setting and getting:

Set x to 1:             make "x 1
Adding :n to :x         :n + :x
Setting :x to :n + :x   make "x :x + :n

Looping:

REPEAT n [COMMANDS ...]

STOP    - Stop the current Repeat or function.

OUTPUT f  - Return f.
OP f


Defining and Calling:

TO FOO :ARG1 :ARG2 BODY END

TO SQUARE :length 
REPEAT 4 [FW :length RT 90]
END

SQUARE :10

TO POLYGON :length :sides
REPEAT :sides [FW :length RT 360/:sides]
END

POLYGON 5 10
```
Note: Simple Tail recursion is supported.