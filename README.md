Debugging overlapping points in a variable font

3-axis variable font. It's a double inline, with each axis controlling the weight of the outside shape, the middle shape, and the inside shape. Each layer should disappear, so that it can be used as an outline, completely filled, inline, or double inline.
![3-axis](/images/axis-description.png)
![needs to disappear](/images/need-to-disappear)


### The problem
When an axis is at the min, or two axes are set to the same value, weird things happen, especially in Illustrator. When all the axes are at different values, it renders as expected. I'm assuming the renderers don't like multiple points sharing the same coordinates.  

I get different results in different environments, leading me to believe it's an issue on the rendering side, rather than generation. Chrome Canary renders as expected. Fontview is close, but there are some slivers visible. 

![Illustrator](/images/illustrator.png)
![Illustrator](/images/fontview.png)
