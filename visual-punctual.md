# DECODED Lite --

A short, introductory workshop to livecoding in Estuary

## Visual Workshop

Open https://estuary.mcmaster.ca and enter "Solo Mode"

*Estuary is a free online tool for making music and visuals in a browser*

&nbsp;

Choose **Punctual** from the language selection box

*[Punctual](https://github.com/dktr0/Punctual) is an audio/visual livecoding language, we'll just be using the visuals today*

`circle` creates a circle

To make a circle appear on our screen, we need to tell it the **position**, the width or **diameter** we want it to have, and the **output** we want it to use (`rgb` in this case)

```
circle [0,0] 0.5 >> rgb;
```

To remove our circle, we can **comment** the line, or delete the pattern and evaluate the empty cell

```
-- circle [0,0] 0.5 >> rgb;
```

You can move it around by changing the **position** values - `-1.0` to `1.0` keeps it on screen

```
circle [-0.5,0.2] 0.5 >> rgb;
```

You can make it bigger or smaller by changing the **diameter** value

```
circle [0,0] 0.9 >> rgb;
```

Here are some more shapes to try - see the [Punctual Reference](https://github.com/dktr0/Punctual/blob/main/REFERENCE.md) for more information

| `hline` | `vline` | `point` | `rect` |
|---------|---------|---------|--------|

You can change the way it appears using different **outputs**

```
circle [0,0] 0.9 >> green
```

Here are some more outputs to try

| `red` | `blue` | `hsv` | `rgba` |
|---------|--------|-------|--------|


You can make more circles (shapes) by adding more values
```
circle [0,0,-0.5,0,0.5,0] 0.4 >> rgb;
```

You can get continuously changing values and use them in place of numbers. This is a `sin` graph changing the circle width

```
circle [0,0] (sin 0.5) >> rgb;
```

Here are some more graphs to try

| `tri` | `square` | `time` | `prox` |
|-------|----------|--------|--------|


Some graphs are controlled by the audio that is playing. Make a beat in a minitidal cell, then use `lo` as a Punctual graph to change the position of the `circle`

```
circle [0, lo] 0.5 >> rgb;
```

Here are some more audio reactive graphs to try

| `mid` | `hi` | `fft fx` | `fft fy` | `fft fxy` |
|-------|------|----------|----------|-----------|

Remember, continuous and audio reactive graphs can be used in place of **any** value

&nbsp;

You can create a tiled pattern of your shape using `tile`

```
tile 4 $ circle [0,0] 0.9 >> rgb;
```

Here are some other functions to transform your pattern

| `spin` | `zoom` | `move` |
|--------|--------|--------|


Colours can be changed by adding a list to the end of our pattern

```
circle [0,0] 0.9 * [0.2,0.1,0.8] >> rgb;
```

Each number in this list represents an amount of `red`, `green` and `blue`, because we are using the rgb output

If we use the `hsv` output, the numbers in the list represent `hue` (colour), `saturation` (intensity of colour) and `value` (brightness)

```
circle [0,0] 0.9 * [prox 0.5,1,0.5] >> hsv;
```

Finally, you can create trails for moving shapes with `fdbk`

```
circle [saw 0.5,0] 0.9 * [prox 0.5,1,0.5] >> hsv;
0.95 >> fdbk
```

---

**Congratulations!** You've completed the DECODED Lite visual/punctual course!

If you would like to continue learning more about livecoding with Minitidal, Punctual and Estuary, check out:

 - https://decoded.grbt.com.au for a detailed course
 - https://github.com/dktr0/Punctual for more Punctual information
 - https://github.com/cleary/livecode/ for heaps of my own examples
 - For any questions, I can be contacted via email
