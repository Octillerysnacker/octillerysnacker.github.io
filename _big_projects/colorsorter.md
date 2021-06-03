---
name: Color Sorter
image: image10.png
summary: A claw-machine-like apparatus which sorts colored bricks.
---

I made a machine similar to an arcade claw machine which sorts randomly scattered colored bricks. The machine consists of a rectangular grabber, which can be set to either pass through or collide with bricks, as well as a brick scanner. The grabber moves along all 3 translational axes, as well as rotating along the vertical axis. All the movement in the simulation is physics based; the challenge was that I can only control the forces being applied on the grabber and the grabber's function. The scanner is mainly for aesthetic purposes, although I'm hoping to use actual image processing in the future.

I designed the machine so that I can write various "programs" which run the machine in different ways. The programs are regular C#, but they utilize enumerators so that I can write the programs like any other, without worrying about whether the machine has finished a given statement. The main sorting program roughly follows these steps:

1. "Scan" for bricks

2. Internally sort the bricks by hue

3. Gather all the bricks into a single area, ordered by the distance away as well as its height off the ground

4. Starting from the top of the created pile, move each brick to another area

5. If the brick is not face down, knock it over

6. Move and rotate the brick to its designated spot

There's a lot of complications, especially since bricks can be underneath one another and bricks can fly out of the working area. While the sorting process is not 100% perfect, it does a pretty good job and I had fun solving these problems.

The project is made using Unity, C#, and Visual Studio.

## Videos

Here's a timelapse of the machine sorting some bricks.

<iframe src="https://drive.google.com/file/d/1FrhpDZD6i8neu70l1HA3vpGFR93ByDEi/preview" class="video"></iframe>

## Additional Links

Source Code (zip): [https://drive.google.com/file/d/1ssnuGMkJKeIWiyYq5gih8wwGT70eV7gQ/view?usp=sharing](https://drive.google.com/file/d/1ssnuGMkJKeIWiyYq5gih8wwGT70eV7gQ/view?usp=sharing)