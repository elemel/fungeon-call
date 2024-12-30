# Chapter 1: Wallflower

You have entered a dungeon. You struggle to find your bearings using a conveniently provided map:

```
##########[###########]##############][#######]#[####################]########
###.]......]####]##[...############][....[#]#]....[################[...##]####
##]...###[..###].......[##########]....[.##..[##...]################....]....]
#[...]#......[]##]....[#############..[#..]......].#################].#....[.#
##.].###[.#..#.]....[]##]###########.]##]...[#[....######]#########]..[][..#.#
####.[[...[..]....]..]]..##########]....[..##[..##]######..]##[###]..[#[##[..#
##[...][.]]..#.#[]#]..#.....]#####]#].#]#..][..]#[......[...]#...[..[...[...]#
###.[##]..##]#.#####].#].]#...<.]..#..]##[.[..]....]#]..#.[....]...]#.[....]##
]...#####.]....#####..[]..#..[[....].#[#####.]##]..[##.[].#..].#[##[..#.[[]###
#..[####[...##[####[...[].#]###[#.#]...###]#...[..[#[..#..][.[[###[..[#]####[#
#]..]######[#######[#]....[###[...###].....#[#...]#[..[[.###[######.]#####[#.]
##[.##############[.#]]....[###.#[####[.#].###]#####.]#..]######]#].####]#...[
###..########[####..[....]..#]..#####...[..[########..]..[####[#.]....[#...[.#
###..#######.....[....[[###.##.[#####]....]#########].[.[#####...[#]#....][..#
###..[#######.[#...[#]#...[.]...]###]..[############....[#####.#..]##]#####.]#
###]..]#####]..[[#]#[...]...[.[]#]#[..[##############..[######.#].][######].##
####[.#######]..]..#..[.#[##[.##[....[###############]######[.......[####]...[
##]....[######].#....]####]....]#.#.]######################[...[#..]#######].#
#[..#[]#######..[].###]####[.....#[..####################]...]..][##[.#].....#
[..[###]#####[...[.....##.###[..]##..########]##########[..#]#]..###..[..###]#
#.]####...]##....].[##.##.####[......]#####]#.]###.####[..[##]...[#[....[#####
#...]#].#..]#..[##[###.##.#][##[####.[####..]..##].......]##[..[##[##..]######
#[#.#]..[[..].]######].#]....[####[#]#[##].....#[..##]...#[...[]...##]...[#]##
###.#..[##[.#.#######..]#.[...]....[...]....[[.[..[###..[##[.....#.###[#.[...#
[.....[####...[#####].....##]....]...]...#[]#]...]####..]#######[[..........[#
#[#]#######[#############[#####[]###]###[#######]#####]#################[#]###
```

You are standing at the bottom of the staircase where you entered (marked `<` on the map), facing north (up on the map). Before leaving the dungeon, you are compelled to explore it.

You can walk on the floor tiles (marked `.`). You always walk forward if you can, without turning. Walking to the next tile takes one tick of dungeon time.

Whenever you are about to walk into a wall (marked `[`, `#`, or `]`), you instead stay where you are and turn. You turn 90 degrees left in front of `[` walls, 180 degrees around in front of `#` walls, and 90 degrees right in front of `]` walls. Staying and turning also takes one tick. Never mind if you still face a wall after turning. You can deal with that during the next tick.

You start counting ticks immediately, including any time spent turning before leaving the staircase. You leave the dungeon by returning to the staircase. After how many ticks do you leave the dungeon?


## Example

Consider a smaller dungeon:

```
#[###]##
#....<.[
#.]....#
]....#]#
###[####
```

Below is a log of exploring the smaller dungeon. Your position at each tick is marked `@`.

```
Tick counter: 0
Direction: North
Level: 0

#[###]##
#....@.[
#.]....#
]....#]#
###[####

---

Tick counter: 1
Direction: East
Level: 0

#[###]##
#....@.[
#.]....#
]....#]#
###[####

---

Tick counter: 2
Direction: East
Level: 0

#[###]##
#....<@[
#.]....#
]....#]#
###[####

---

Tick counter: 3
Direction: North
Level: 0

#[###]##
#....<@[
#.]....#
]....#]#
###[####

---

Tick counter: 4
Direction: South
Level: 0

#[###]##
#....<@[
#.]....#
]....#]#
###[####

---

Tick counter: 5
Direction: South
Level: 0

#[###]##
#....<.[
#.]...@#
]....#]#
###[####

---

Tick counter: 6
Direction: West
Level: 0

#[###]##
#....<.[
#.]...@#
]....#]#
###[####

---

Tick counter: 7
Direction: West
Level: 0

#[###]##
#....<.[
#.]..@.#
]....#]#
###[####

---

Tick counter: 8
Direction: West
Level: 0

#[###]##
#....<.[
#.].@..#
]....#]#
###[####

---

Tick counter: 9
Direction: West
Level: 0

#[###]##
#....<.[
#.]@...#
]....#]#
###[####

---

Tick counter: 10
Direction: North
Level: 0

#[###]##
#....<.[
#.]@...#
]....#]#
###[####

---

Tick counter: 11
Direction: North
Level: 0

#[###]##
#..@.<.[
#.]....#
]....#]#
###[####

---

Tick counter: 12
Direction: South
Level: 0

#[###]##
#..@.<.[
#.]....#
]....#]#
###[####

---

Tick counter: 13
Direction: South
Level: 0

#[###]##
#....<.[
#.]@...#
]....#]#
###[####

---

Tick counter: 14
Direction: South
Level: 0

#[###]##
#....<.[
#.]....#
]..@.#]#
###[####

---

Tick counter: 15
Direction: East
Level: 0

#[###]##
#....<.[
#.]....#
]..@.#]#
###[####

---

Tick counter: 16
Direction: East
Level: 0

#[###]##
#....<.[
#.]....#
]...@#]#
###[####

---

Tick counter: 17
Direction: West
Level: 0

#[###]##
#....<.[
#.]....#
]...@#]#
###[####

---

Tick counter: 18
Direction: West
Level: 0

#[###]##
#....<.[
#.]....#
]..@.#]#
###[####

---

Tick counter: 19
Direction: West
Level: 0

#[###]##
#....<.[
#.]....#
].@..#]#
###[####

---

Tick counter: 20
Direction: West
Level: 0

#[###]##
#....<.[
#.]....#
]@...#]#
###[####

---

Tick counter: 21
Direction: North
Level: 0

#[###]##
#....<.[
#.]....#
]@...#]#
###[####

---

Tick counter: 22
Direction: North
Level: 0

#[###]##
#....<.[
#@]....#
]....#]#
###[####

---

Tick counter: 23
Direction: North
Level: 0

#[###]##
#@...<.[
#.]....#
]....#]#
###[####

---

Tick counter: 24
Direction: West
Level: 0

#[###]##
#@...<.[
#.]....#
]....#]#
###[####

---

Tick counter: 25
Direction: East
Level: 0

#[###]##
#@...<.[
#.]....#
]....#]#
###[####

---

Tick counter: 26
Direction: East
Level: 0

#[###]##
#.@..<.[
#.]....#
]....#]#
###[####

---

Tick counter: 27
Direction: East
Level: 0

#[###]##
#..@.<.[
#.]....#
]....#]#
###[####

---

Tick counter: 28
Direction: East
Level: 0

#[###]##
#...@<.[
#.]....#
]....#]#
###[####

---

Tick counter: 29
Direction: East
Level: -1

---

Symbol counters:
  #  4
  .  17
  <  1
  [  3
  ]  4
```

You leave the smaller dungeon after 29 ticks.
