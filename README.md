# DECODED Lite --

An introductory workshop to livecoding in Estuary

## Audio Workshop

Open https://estuary.mcmaster.ca and enter "Solo Mode"

*Estuary is a free online tool for making music and visuals in a browser*

&nbsp;

Choose Minitidal from the language selection box

*Minitidal is based on the popular [Tidalcycles](https://tidalcycles.org/) livecoding language*

&nbsp;

`bd` is a bass drum sample (sound)

You can play the sound once per cycle using:

```
sound "bd"
```

&nbsp;

Here are some other sounds to try
 - `sd` a snare drum
 - `hh` a high hat
 - `cp` a clap
 - `~` is a rest (no sound)

You can add more `bd` events to play the sound more times per cycle

```
sound "bd bd bd bd"
```

&nbsp;

On the fourth step, the bass drum sound will be played twice

```
sound "bd bd bd [bd bd]"
```
&nbsp;

This can also be written using the multiplication symbol `*`

```
sound "bd bd bd bd*2"
```
&nbsp;

Try replacing the `*` with some different punctuation symbols

 - `!` exclamation
 - `/` divide by
 - `@` *at* symbol

&nbsp;

*Note: you can see all the sounds by typing `!localview audiomap` into the terminal/chat box*

&nbsp;

You can make a pattern play faster using `fast`

```
fast 2 $ sound "bd ~ [cp bd] bd"
```

What do you think `slow` might do instead of `fast`?





| `!` | `/` | `@` |
|-----|-----|-----|
