# Godot transition shader
Simple fade in / out godot shader

# My first Godot shader!

Hi guys. This is my first godot shader which i created with help of [AWESOME GD QUEST!](https://www.youtube.com/channel/UCxboW7x0jZqFdvMdCFKTMsQhttps://www.youtube.com/channel/UCxboW7x0jZqFdvMdCFKTMsQ) 


## How it looks?

Well... I made a video to show it in action!

[![Godot Transition Shader!](http://www.drujduv.net/sharex/img/brave_oCfYB7uVjr.png)](https://www.youtube.com/watch?v=ahtvIqhhYeY&feature=youtu.be "Click to see")

### How to use it?

Just add color rectangle in godot, put it over screen and add shader material.

### How to add new transition? 

It is easy... Basically any black and white image will work fine. You can download pack of transitions which i used :)

#### Tips and tricks

How to change shader parameters in GDscript?

First you need to get your material. For example:

```
var material = get_node("UI/fade_in_out").get_material()
```
After that, just change variables of shader
In this case we have:

cutoff (you can set it to 0 (invisible) to 1 (black screen)
smooth size (how blurry you want your shader)
wave_speed_x and wave_speed_y (how much will transition jiggle)

So, let's say we want to change transition to half done. In ready function you will write this:
```
material.set_shader_param("cutoff",0.5)
```
0.5 is half of 1 so we are good.

You can also animate your shader parameters with animation node! Just create new animation node. Then new animation and open shader. You will see little icon key on side of every parameter. Set frame to 0, set parameter to 0 and click on key next to cutoff. Then set frame to 1,2,3 or how long you will want your animation. Set cutoff parameter to one and click again on little key icon. And you are done!

I hope this helped you to create neat transitions for your game! 

P.S. Sorry for my horrible english!
