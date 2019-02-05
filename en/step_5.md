## Stick to the lines

You might notice that, if you draw a low bridge between the two platforms, or a line that slopes upwards, the cats end up walking through the platform rather than on top of it!

![Cats walking through the platform](images/cat-walk-through-platform.png)

--- task ---
In the code for the cat sprite, add another loop before the `next costume`{:class="blocklooks"} block. This time, the loop should tell the cat to move upwards by `2` until it is not touching blue.

![Cat sprite](images/cat-sprite.png)

--- hints ---
--- hint ---
The cat should `move up 2`{:class="blockmotion"} `repeatedly until`{:class="blockcontrol"} it is `not`{:class="blockoperators"} `touching blue`{:class="blocksensing"}.
--- /hint ---

--- hint ---
Here are the code blocks you need:

```blocks
<touching color [#0000ff]?>

change y by (2)

repeat until <>
end

not <>
```

--- /hint ---

--- hint ---
This is what your code should look like:

```blocks
when I start as a clone
show
repeat until <touching [edge v]?>
    move (10) steps
    repeat until <touching color [#0000ff]?>
        change y by (-2)
    end
+   repeat until <not <touching color [#0000ff]?>>
        change y by (2)
    end
    next costume
    wait (0.1) secs
end
delete this clone
```
--- /hint ---

--- /hints ---
--- /task ---

--- task ---
Click the green flag and try drawing a line that slopes upwards. Check that your cat follows this line.
--- /task ---
