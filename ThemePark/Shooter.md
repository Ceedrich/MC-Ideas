# Shooter

This is a simple shooter game where the player aims to hit as many targets as possible in the given time while sitting in a minecart.

1. the player enters the room and sits in the minecart
2. by pressing a button, the minecart starts moving and the player can shoot the targets
3. when the _time_ is up, the minecart stops and the targets close
4. the score is converted and shown on the seven segment display
5. the player can write down the score in a record book on a lectern
6. after a few moments, the shooter game resets itsself
7. when the player exits the room, the arrows get cleared.

## Implementation of the score system

| Name                    | Description                        | Signal input type | Signal output type     |
| ----------------------- | ---------------------------------- | ----------------- | ---------------------- |
| target block            |                                    | analog (bow)      | hex                    |
| hex to binary converter |                                    | hex               | binary                 |
| sequential adder        | keeps a running total of the score | binary            | binary                 |
| binary to bcd converter |                                    | binary            | bcd                    |
| bcd decoder             | converts a bcd number into 7-seg   | bcd               | 7-seg                  |
| display                 |                                    | 7-seg             | analog output (number) |

## Arrow clearing system

1. The pistons fixing the target retract and let the arrows fall down on a piston feed tape.
1. The feed tape moves the arrows into the collection area.
