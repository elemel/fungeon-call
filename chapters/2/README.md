# Chapter 2: Shortcut

You have entered another dungeon. You are standing at the bottom of the staircase where you entered, facing north. You study the provided map:

```
########}{{#############({[#(######]}##]#############]#]##)#}}{})]#]##########
########].(#####[})####{].)...#}{#)..[..]#########)#...()].{).[..[.)}#########
#####{.).{..((..)..[](##.{.]({.{}..({.[).]}{#######.((}..[...[..].].]#########
#####)..{{[{.).).))..]}).(]#..(({].}[#[}.].########{...][.({]#[}{#[.}#########
####[#)#.])..(.).)}...#.}.#}.[###.}<###.).#.{(######{[.##[)]{##{#[.}]](#######
###]).##.{.)).).(].(.).#.#](.]###..((]){)#[#.#######..({##{.(..}[...].}#)#####
##)#.[[#.})](.[])}#(})#(})..({###[#.#[.#.#{...]#####...)####.[.[][{{..).}#####
#{..}.}[)..})########}((].)#######.(#.).).}[[.}####[.)}{###}.)).#.](#[.{#{##)]
#.]](.)###].]#######](..(.)######{[..)]{.#((.{]#####.){#####)..[.).}[.#).))..(
[.([.}{{##..][]]]###].##.({###)###})()..{}..###((##}#.{######))].}}..)(.(..).)
#.#)...((##..(..{###].){))#)).#)[###(.#))#[.((]..){)..]#######.[{.((}{}.(({].#
#(.[#{}.##){].(...{#){.](]...]..(###}(..#[#.)}.{(..).({#######...)([.#.{.}..)#
[.])]].}####([]#)(.}]]...}{.}).[]#)]]]]..#{).].](.{.[.#]###[((...}).))...)].}#
[.}##..(#{######[.](..)}..[}.[.)).)..(#.#}#}.].#[}[(...(#)).#{(].).]...{..}).}
#[..[}..{.##[#{#).{.[{[..#..[#[..].#).#{.][#).}(.##{#)]#(..)..[.}]..)[)[}[#.[)
#(.]##]#..(##..).][.().#.#.(####(#{)[...].(###(]....))...[}).(].)#..{###.)[.)[
#[{.]##(}{..#[.).)..].)}(]#})#}#.###{)).}.)#{##{.}({...[#[#((.{}.)..]##.[....#
#{(.{)..}(}[..).)[.}(..[####..}.((###{.[{..}#.[(...(}[######..}](.](##.#..[.((
#(..].](.{#.(][#.){..(..)[#[.].}.[###(]..(}#.).]#[].[{]{###].#.[.{}..(.[.){(]#
#].(.}#(..]####]{]##.)[#.]#).]}..]######({#.##.#]#.(}..(}][((.))(#.[).{)}{####
#{..]{#.).(#{#].{#].{.#({(]..}(.(}###({)[{.{}](.#})..(#.)(.((.[#({..(]{#######
##]([#((.{{#)..).].(#.([.{.)[#.}#(#[([.(.{].#..[.{#((#.]{.]....){.]]...)######
#######{.....[#[.(.#}{..#..}#[.[#[.}....}...){.{(]({(.)..#[]{[(.].)#[)#{######
########.(]#####..)##}}](].##].{..[.(}}#]#))#.()..}.{{{..(..(]..#).###########
#######.#######{(.[#######(##)).(#)}########.(..{].]....{.}]..#(....##########
######[{)#######]#}###########)############{#]{##{}]#([])#)#]##]####}#########
```

In this dungeon, there are additional wall types for turning diagonally (marked `{`, `(`, `)`, or `}` on the map). You turn 135 degrees left in front of `{` walls, 45 degrees left in front of `(` walls, 45 degrees right in front of `)` walls, and 135 degrees right in front of `}` walls. As before, you always walk forward if you can. Walking forward can now also mean walking in a diagonal direction (southwest, northwest, northeast, or southeast).

The cardinal walls (marked `[`, `#`, or `]`) have the same effect as before. They can now also make you turn from one diagonal direction to another.

You leave the dungeon by returning to the staircase. After how many ticks do you leave the dungeon?


## Example

Consider a smaller dungeon:

```
{{#}{){#
#.(<..(]
[#.{[#.[
#)#...[(
###[)([#
```

Below is a log of exploring the smaller dungeon. Your position at each tick is marked `@`.

```
Tick counter: 0
Direction: North
Level: 0

{{#}{){#
#.(@..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 1
Direction: Southeast
Level: 0

{{#}{){#
#.(@..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 2
Direction: Northeast
Level: 0

{{#}{){#
#.(@..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 3
Direction: West
Level: 0

{{#}{){#
#.(@..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 4
Direction: Southwest
Level: 0

{{#}{){#
#.(@..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 5
Direction: Southwest
Level: 0

{{#}{){#
#.(<..(]
[#@{[#.[
#)#...[(
###[)([#

---

Tick counter: 6
Direction: West
Level: 0

{{#}{){#
#.(<..(]
[#@{[#.[
#)#...[(
###[)([#

---

Tick counter: 7
Direction: East
Level: 0

{{#}{){#
#.(<..(]
[#@{[#.[
#)#...[(
###[)([#

---

Tick counter: 8
Direction: Northwest
Level: 0

{{#}{){#
#.(<..(]
[#@{[#.[
#)#...[(
###[)([#

---

Tick counter: 9
Direction: Northwest
Level: 0

{{#}{){#
#@(<..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 10
Direction: South
Level: 0

{{#}{){#
#@(<..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 11
Direction: North
Level: 0

{{#}{){#
#@(<..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 12
Direction: Southwest
Level: 0

{{#}{){#
#@(<..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 13
Direction: Southeast
Level: 0

{{#}{){#
#@(<..(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 14
Direction: Southeast
Level: 0

{{#}{){#
#.(<..(]
[#@{[#.[
#)#...[(
###[)([#

---

Tick counter: 15
Direction: Southeast
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#@..[(
###[)([#

---

Tick counter: 16
Direction: South
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#@..[(
###[)([#

---

Tick counter: 17
Direction: East
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#@..[(
###[)([#

---

Tick counter: 18
Direction: East
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#.@.[(
###[)([#

---

Tick counter: 19
Direction: East
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#..@[(
###[)([#

---

Tick counter: 20
Direction: North
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#..@[(
###[)([#

---

Tick counter: 21
Direction: South
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#..@[(
###[)([#

---

Tick counter: 22
Direction: Southeast
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#..@[(
###[)([#

---

Tick counter: 23
Direction: Northeast
Level: 0

{{#}{){#
#.(<..(]
[#.{[#.[
#)#..@[(
###[)([#

---

Tick counter: 24
Direction: Northeast
Level: 0

{{#}{){#
#.(<..(]
[#.{[#@[
#)#...[(
###[)([#

---

Tick counter: 25
Direction: Southeast
Level: 0

{{#}{){#
#.(<..(]
[#.{[#@[
#)#...[(
###[)([#

---

Tick counter: 26
Direction: East
Level: 0

{{#}{){#
#.(<..(]
[#.{[#@[
#)#...[(
###[)([#

---

Tick counter: 27
Direction: North
Level: 0

{{#}{){#
#.(<..(]
[#.{[#@[
#)#...[(
###[)([#

---

Tick counter: 28
Direction: Northwest
Level: 0

{{#}{){#
#.(<..(]
[#.{[#@[
#)#...[(
###[)([#

---

Tick counter: 29
Direction: Northwest
Level: 0

{{#}{){#
#.(<.@(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 30
Direction: South
Level: 0

{{#}{){#
#.(<.@(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 31
Direction: North
Level: 0

{{#}{){#
#.(<.@(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 32
Direction: Northeast
Level: 0

{{#}{){#
#.(<.@(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 33
Direction: West
Level: 0

{{#}{){#
#.(<.@(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 34
Direction: West
Level: 0

{{#}{){#
#.(<@.(]
[#.{[#.[
#)#...[(
###[)([#

---

Tick counter: 35
Direction: West
Level: -1

---

Symbol counters:
  #  4
  (  4
  )  3
  .  9
  <  1
  [  6
  ]  1
  {  6
  }  1
```

You leave the smaller dungeon after 35 ticks.