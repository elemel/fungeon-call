# Chapter 2: Shortcut

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

You have entered another dungeon. You are again facing north, standing at the bottom of the staircase where you entered.

In this dungeon, there are additional wall types for turning diagonally (marked `{`, `(`, `)`, and `}` on the map). While facing a diagonal direction, the tile in front of you is the next tile in the diagonal direction. As before, you always walk forward if you can. You turn 135 degrees left in front of `{` walls, 45 degrees left in front of `(` walls, 45 degrees right in front of `)` walls, and 135 degrees right in front of `}` walls.

The cardinal turns (marked `[`, `#`, and `]`) have the same effect as before, but can now also cause you to turn between two diagonal directions.

After how many ticks do you return to the staircase? You should still include any initial time spent turning before leaving the staircase.


## Example

Consider a smaller dungeon:

```
{##[##
#.{.(#
{...]#
#].{<#
###.})
###))#
```

Below is a log of exploring the smaller dungeon. Your position at each tick is marked `@`.

```
Tick counter: 0
Direction: North

{##[##
#.{.(#
{...]#
#].{@#
###.})
###))#

---

Tick counter: 1
Direction: East

{##[##
#.{.(#
{...]#
#].{@#
###.})
###))#

---

Tick counter: 2
Direction: West

{##[##
#.{.(#
{...]#
#].{@#
###.})
###))#

---

Tick counter: 3
Direction: Southeast

{##[##
#.{.(#
{...]#
#].{@#
###.})
###))#

---

Tick counter: 4
Direction: South

{##[##
#.{.(#
{...]#
#].{@#
###.})
###))#

---

Tick counter: 5
Direction: Northwest

{##[##
#.{.(#
{...]#
#].{@#
###.})
###))#

---

Tick counter: 6
Direction: Northwest

{##[##
#.{.(#
{..@]#
#].{<#
###.})
###))#

---

Tick counter: 7
Direction: South

{##[##
#.{.(#
{..@]#
#].{<#
###.})
###))#

---

Tick counter: 8
Direction: Northeast

{##[##
#.{.(#
{..@]#
#].{<#
###.})
###))#

---

Tick counter: 9
Direction: North

{##[##
#.{.(#
{..@]#
#].{<#
###.})
###))#

---

Tick counter: 10
Direction: North

{##[##
#.{@(#
{...]#
#].{<#
###.})
###))#

---

Tick counter: 11
Direction: West

{##[##
#.{@(#
{...]#
#].{<#
###.})
###))#

---

Tick counter: 12
Direction: Southeast

{##[##
#.{@(#
{...]#
#].{<#
###.})
###))#

---

Tick counter: 13
Direction: Southwest

{##[##
#.{@(#
{...]#
#].{<#
###.})
###))#

---

Tick counter: 14
Direction: Southwest

{##[##
#.{.(#
{.@.]#
#].{<#
###.})
###))#

---

Tick counter: 15
Direction: Northwest

{##[##
#.{.(#
{.@.]#
#].{<#
###.})
###))#

---

Tick counter: 16
Direction: Northwest

{##[##
#@{.(#
{...]#
#].{<#
###.})
###))#

---

Tick counter: 17
Direction: South

{##[##
#@{.(#
{...]#
#].{<#
###.})
###))#

---

Tick counter: 18
Direction: South

{##[##
#.{.(#
{@..]#
#].{<#
###.})
###))#

---

Tick counter: 19
Direction: West

{##[##
#.{.(#
{@..]#
#].{<#
###.})
###))#

---

Tick counter: 20
Direction: Southeast

{##[##
#.{.(#
{@..]#
#].{<#
###.})
###))#

---

Tick counter: 21
Direction: Southeast

{##[##
#.{.(#
{...]#
#]@{<#
###.})
###))#

---

Tick counter: 22
Direction: Southeast

{##[##
#.{.(#
{...]#
#].{<#
###@})
###))#

---

Tick counter: 23
Direction: South

{##[##
#.{.(#
{...]#
#].{<#
###@})
###))#

---

Tick counter: 24
Direction: Southwest

{##[##
#.{.(#
{...]#
#].{<#
###@})
###))#

---

Tick counter: 25
Direction: Northeast

{##[##
#.{.(#
{...]#
#].{<#
###@})
###))#

---

Tick counter: 26
Direction: Northeast

{##[##
#.{.(#
{...]#
#].{@#
###.})
###))#

---

Symbol counters:
  #  2
  (  1
  )  3
  .  7
  <  1
  [  1
  ]  4
  {  6
  }  1
```
