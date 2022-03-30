# DECODED Lite --

A short, introductory workshop to livecoding in Estuary

## Audio Workshop

Open https://estuary.mcmaster.ca and enter "Solo Mode"

*Estuary is a free online tool for making music and visuals in a browser*

Choose **Minitidal** from the language selection box

*Minitidal is based on the popular [Tidalcycles](https://tidalcycles.org/) livecoding language*

`bd` is a bass drum sample (sound)

You can play the sound once per cycle using:

```
sound "bd"
```

**Stop** the sound by putting `--` in front of it, or delete all the code and evaluate an empty cell

```
-- sound "bd"
```

You can add more `bd` events to play the sound more times per cycle

```
sound "bd bd bd bd"
```

On the fourth step, the bass drum sound will be played twice

```
sound "bd bd bd [bd bd]"
```

This can also be written using the multiplication symbol `*`

```
sound "bd bd bd bd*2"
```

Try replacing the `*` with some different punctuation symbols

 - `!` exclamation
 - `/` divide by
 - `@` *at* symbol

Here are some other sounds to try

| `~` | `hh` | `cp` | `sd` | `sprvibe` | `flbass` |
|-----|------|------|------|-----------|----------|

You can make a pattern play faster using `fast`

```
fast 2 $ sound "bd ~ [cp bd] bd"
```

What do you think `slow` might do instead of `fast`?

`# speed` is an effect to change the pitch of a note, making the pitch higher or lower

```
sound "bd bd" # speed 2
```

`every` will apply a function or effect after a number of cycles

```
every 4 (fast 2) $ sound "bd ~ [cp bd] bd"
```

to apply an effect to every, you need to add a `#`

```
every 4 (# speed 2) $ sound "bd ~ [cp bd] bd"
```

`numbers` is a folder of samples of someone counting

```
sound "numbers"
```

You can use a colon `:` after the sample name to access different samples in the sample folder

```
sound "numbers:0 numbers:1 numbers:2 numbers:3"
```

If a sound plays for a long time and overlaps with the next sound, you can use `# cut 1` to stop it when the next sample plays:

```
sound "moog" # cut 1
```

*Note: you can see all the sounds by typing `!localview audiomap` into the terminal/chat box of a new estuary tab*

More functions to try:

| `rev` | `palindrome` | `hurry` | `chop` | `sometimes` | `someCyclesBy` |
|-------|--------------|---------|--------|-------------|--------------|

More effects to try:

| `# gain` | `# end` | `# vowel` | `# pan` | `# hcutoff` | `# cutoff` |
|----------|---------|-----------|---------|-------------|------------|


---

**Congratulations!** You've completed the DECODED Lite audio/minitidal course!

If you would like to continue learning more about livecoding with Minitidal, Punctual and Estuary, check out:

 - https://decoded.grbt.com.au for a detailed course
 - https://tidalcycles.org/docs/ for more Tidalcycles/Minitidal information
 - https://github.com/cleary/livecode/ for heaps of my own examples
 - For any questions, I can be contacted via email
