# gpt-svg-experiment
Working to prompt chatgpt to create a SVG of a seven pointed star.

## Prompt
I couldn't get gpt 3.5 to do successfully do it, but I was able to get gpt-4 to work.  However I couldn't get it done in single prompt.  I ended up with a stupidly simple two prompt approach that worked.

```
Tell me how to draw a seven pointed star
```

Followed by the prompt:

```
Now follow that process and output that as SVG elements, creating a table of the connected points before outputting the SVG.
```

## Output

To draw a seven-pointed star, also known as a heptagram, follow these steps:

    Draw a circle: Begin by drawing a circle that will serve as a guide for placing the points of the star. This circle can be drawn using a compass or any other circular object as a template.

    Mark seven equidistant points: Divide the circumference of the circle into seven equal parts. To do this, you can use a protractor to measure an angle of approximately 51.43 degrees (360°/7) between each point. Alternatively, you can approximate the points' positions by eye. Mark each point on the circle.

    Connect the points: Start at any point and label it as point 1. From point 1, count three points clockwise (ignoring the starting point), and connect point 1 to this point (point 4) with a straight line. Repeat this process starting from point 4, counting three points clockwise and connecting it to the next point. Continue this process until all points are connected and you return to the starting point. The result will be a seven-pointed star.

Here is a step-by-step breakdown of the connections:

    Connect point 1 to point 4.
    Connect point 4 to point 7.
    Connect point 7 to point 3.
    Connect point 3 to point 6.
    Connect point 6 to point 2.
    Connect point 2 to point 5.
    Connect point 5 to point 1.

    Adjust and finalize the star: You may need to adjust the lines' length and angle to create a symmetrical and visually appealing star. Once you're satisfied with the star's appearance, you can darken the lines and erase the guiding circle if desired.

Following these steps, you'll be able to draw a seven-pointed star by hand.



Let's follow the process described above and create the table of connected points first:

| Point	    | Coordinates |
| -----     | ----------- |
|Point 1	|(200, 100)|
|Point 2	|(162.35, 178.18)|
|Point 3	|(77.75, 197.49)|
|Point 4	|(9.91, 143.40)|
|Point 5	|(9.91, 56.60)|
|Point 6	|(77.75, 2.51)|
|Point 7	|(162.35, 21.82)|

Connections (each point to the one that is three positions clockwise from it):

    Point 1 to Point 4
    Point 4 to Point 7
    Point 7 to Point 3
    Point 3 to Point 6
    Point 6 to Point 2
    Point 2 to Point 5
    Point 5 to Point 1

Now, let's create the SVG file using these connections:

xml

<svg xmlns="http://www.w3.org/2000/svg" width="300" height="300">
    <circle cx="100" cy="100" r="100" fill="none" stroke="black" />
    <line x1="200" y1="100" x2="9.91" y2="143.40" stroke="black" />
    <line x1="9.91" y1="143.40" x2="162.35" y2="21.82" stroke="black" />
    <line x1="162.35" y1="21.82" x2="77.75" y2="197.49" stroke="black" />
    <line x1="77.75" y1="197.49" x2="77.75" y2="2.51" stroke="black" />
    <line x1="77.75" y1="2.51" x2="162.35" y2="178.18" stroke="black" />
    <line x1="162.35" y1="178.18" x2="9.91" y2="56.60" stroke="black" />
    <line x1="9.91" y1="56.60" x2="200" y2="100" stroke="black" />
    <circle cx="200" cy="100" r="2" fill="red" />
    <circle cx="162.35" cy="178.18" r="2" fill="red" />
    <circle cx="77.75" cy="197.49" r="2" fill="red" />
    <circle cx="9.91" cy="143.40" r="2" fill="red" />
    <circle cx="9.91" cy="56.60" r="2" fill="red" />
    <circle cx="77.75" cy="2.51" r="2" fill="red" />
    <circle cx="162.35" cy="21.82" r="2" fill="red" />
</svg>

This SVG file contains a circle with a radius of 100, centered at (100, 100), and line elements connecting each point to the one that is three positions clockwise from it, forming a seven-pointed star. The individual red circles represent the seven points on the circle used to construct the star.