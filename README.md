# IMPORTANT

I'm not the author of this software.

It has beed developed by [Gene Kogan](https://twitter.com/genekogan) as part of the ['Machine Learning for Artists'](http://ml4a.github.io/) repository.

The code has been forked here because we plan to use it in our insertions workshop at the Eastern Bloc.

For further info about ML4A, please, check its [official website](http://ml4a.github.io/) and the original [KeyboardOSC repo](https://github.com/ml4a/ml4a-ofx/tree/master/osc-modules/KeyboardOSC).

PS: If you want to test incoming OSC messages, you can use the Max patch 'osc-sender.maxpat' available inside the 'bin' folder.

---

# Keyboard Osc

This interface enables you to simulate keystrokes in any application over OSC.

![](http://projects.stoj.io/keyboard-controller/app.png)


## Examples
With this app you can through OSC control any kind of keyboard-based interaction in across your operating system.


Combined with the AudioClassifier you can play Wolfenstein 3D using sounds:
[![Watch video on Vimeo](http://projects.stoj.io/keyboard-controller/wolfenstein.jpg)](https://vimeo.com/154583964)


Or play Tetris with FaceTracker2OSC

![](http://projects.stoj.io/keyboard-controller/face-tetris.gif)


## Usage
In `bin/data/settings.xml` you can set what keys to trigger and on what OSC address.


#### Keys
Under `<keys>` you can add another input by adding the follwing:

```
<input>
    <key>DOWN</key>
	<osc-id>1</osc-id>
</input>
```
`<key>` is name of the key (See possible keystrokes further down) and `<osc-id>` is the OSC message (number) the key will be triggered upon.

#### OSC settings
In the `settings.xml` you can change the port (`<port>`), the keystroke address (`<address>`) as well as addresses for enabling / disabling keystroke simulation (`<enable> <disable>`).

You can also set for how long each key will be pressed down for (in milliseconds):
`<key-duration>100</key-duration>`


#### Warning :dizzy_face:
When enabling keystrokes, the keys will be triggered in whatever app that's in focus, so be careful, especially with not having your source-code open at the same time.



#### Status
Currently only tested macOs 10.12.4 (Sierra)



## Possible keystrokes
You can control all keys except for key modifiers (`shift`, `ctrl`, `alt` & `cmd`)

`a-z`, `0-9`, `Function keys F[1-15]`

Arrowkeys:

```
UP
DOWN
LEFT
RIGHT
```

Special keys:

```
`
.
*
+
/
-
=
]
[
RETURN
ENTER
TAB
SPACE
DELETE
ESCAPE
CLEAR
HELP
HOME
PGUP
PGDN
END
```
