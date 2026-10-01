Don't Look At It

a lil horror game i made with just html canvas + js, no libraries or anything. runs straight in the browser.

basically ur stuck in a maze, theres a monster in there with u, find the key and get to the door before ur sanity or ur life runs out lol.

how to run it

just open index.html in any browser. thats it, no build step no npm no nothing. everything (css + js) is in the one file.

controls
WASD - move around
ARROW KEYS - aim ur flashlight
SHIFT - run (but its loud, monster can hear u)
F - flashlight on/off
ENTER - start
R - restart after u die/win
the actual mechanic (important)

dont just point the flashlight at the monster and keep it there. if u stare at it too long it gets angry and lunges at u. so glance dont stare, basic premise of the whole game really.

stuff thats tracked
battery - drains while flashlight is on, recharges when off
sanity - drains over time, drains faster in the dark and when the monster is close. hits 0 = u lose
key indicator - top middle, tells u if uve found the key yet
how the maze/monster work (for anyone reading the code)
maze is generated fresh every game using randomized DFS (recursive backtracker), found the algorithm online honestly, pretty standard stuff
monster has 2 states - wander and chase. it switches to chase if it sees u (line of sight check) or hears u running
it also "remembers" where u were for a bit even after losing sight of u, so it doesnt feel dumb
when ur sanity gets low (<40) there's a chance of a fake monster spawning near u just to mess with u, its not real, cant hurt u
known issues / stuff i didnt bother fixing
no mobile touch controls, keyboard only for now
audio uses the Web Audio API directly, so first sound only plays after you interact w page (browser autoplay rule, cant avoid it)
maze size is fixed (13x13), didnt make it adjustable
no save/pause, if u close the tab ur progress is gone, its a short game anyway so eh
todo (maybe, if i come back to this)
 touch/mobile support
 difficulty settings (maze size, monster speed etc)
 sound toggle / volume slider
 maybe add more than 1 monster??
notes

made this mostly for fun / to mess around with canvas + procedural generation, not meant to be some polished product so forgive the messy bits in the code lol. everything's in index.html, didnt bother splitting into files since its small enough.
