## VISUAL EXAMPLES OF THE MODEL

Below are two randomly generated planar graphs with 30 (the default) edges and its coloring according to the rules of the theorems.

The following two images show the before and after of the model running. In the case for these two, only four colors were needed to color the graph; hence, proving The Four Color Theorem.

![ABM-FourColorExample1.png](https://github.com/Kaan-Ince/The-Five-Color-Theorem-Model/blob/main/ABM-FourColorExample1.png)

![ABM-FourColorExample2.png](https://github.com/Kaan-Ince/The-Five-Color-Theorem-Model/blob/main/ABM-FourColorExample2.png)

The following two images show another graph where five colors were needed to color the graph, giving a visual proof for The Five Color Theorem.

![ABM-FiveColorExample1.png](https://github.com/Kaan-Ince/The-Five-Color-Theorem-Model/blob/main/ABM-FiveColorExample1.png)

![ABM-FiveColorExample2.png](https://github.com/Kaan-Ince/The-Five-Color-Theorem-Model/blob/main/ABM-FiveColorExample2.png)


Below is the information included in the Info tab of the NetLogo file:
## WHAT IS IT?

This model is a visualization of a result from Graph Theory called The Five Color Theorem. The theorem states that every planar graph is 5-colorable. The definition of a planar graph is as follows: A graph G is called a planar graph if G can be drawn in the plane so that no two of its edges cross each other. The model produces a planar graph (although it might not look like such in the interface window, if one were able to move the nodes, it would be seen that the resulting graphs are planar, see the "Extending The Model" section on the Info tab for more on this topic) then applies the theorem to color the vertices, giving a neat visualization to the theorem.

## HOW IT WORKS

During setup, user-defined number of vertices are created first in white color and scattered across the window. In order to achieve a more visually pleasing graph, there is a layout-springs calculation that repeats 50 times so that the vertices pushes each other away to achieve a spread out final graph. In order to end up with a simpler graph, there is a proximity-based edge rule so for vertex-a and vertex-b were to be connected, there must not be another vertex between them. This ensures that the graph after setup remains planar (note that the model almost always produces a planar graph, but with the restrictions of the window in NetLogo interface, it might not seem obvious on paper). On go, the model colors the vertices within the rules of the theorem, namely so that no two adjacent vertices receive the same color. Agents first check neighbors and obtain the list of the color indices from 0 to 4 that they are using. This vertex (agent) then looks on the palette of colors available, starting at index 0 and assigns itself the lowest color index possible. The vertex updates its variable named vertex-color and we get the visualization of the coloring on the interface window. Finally, a last check is done at the end to make sure that the process halts if the setup were to produce a graph that is non-planar. In this case, the user is notified with a message box and the stop command is put in place. The user is encouraged to press setup again to generate another graph, since this possibility is extremely rare but possible due to the geometric approximation nature of the setup method.

## HOW TO USE IT

First thing the user should do is decide on the number of vertices the resulting graph should have. There is a slider to define this number. After, the user can press the setup button to generate the graph with its vertices (first in white) and edges (in gray). Finally, when the user presses the go button, the vertices are colored with the five available colors (namely blue, green, yellow, red, magenta), showcasing that the theorem holds. The monitors on the right shows how many vertices are colored in different colors so the user can further check that all the vertices are colored and inspect the window with the colored graph to see the rules of the theorem are followed.

## THINGS TO NOTICE

One might notice that in some cases (especially when creating a graph with low number of vertices) only four colors were needed to color the graph according to the rules of the theorem. This is normal since The Five Color Theorem is an extension of another theorem, namely The Four Color Theorem. The Four Color Theorem states that the chromatic number of every planar graph is at most 4. Chromatic number is the smallest number of colors in any coloring of a graph G. This model demonstrates the Five Color Theorem as opposed to the Four Color Theorem since the proof of The Four Color Theorem is complex and needs more advanced computer-assisted tools, but it automatically proves the Five Color Theorem. And in some cases, this visualization also applies to the Four Color Theorem.

## THINGS TO TRY

The user can try gradually upping the number of vertices in the graph to see how the theorem still works when the graph is planar. The monitors on the right of the model window show how many nodes are colored in their respective color. One can see that (especially when the number of vertices in the graph is low) the coloring is done with only four colors. This ties in with The Four Color Theorem that states: The vertices of every planar graph can be colored with at most four colors so that no two adjacent vertices receive the same color.

## EXTENDING THE MODEL

Although the model almost always produces a planar graph so the application of the Five Color Theorem works, on the interface of NetLogo it might not seem obvious that the graph is planar (since you cannot move around the "nodes" so some edges seem like they are crossing). One might further go into detail with the code to ensure that the graph produced after setup is planar without having to move around the nodes to show that there are actually no edge crossings (this might prove difficult if the number of vertices for the setup is high, since the window is really limited in size). Further, some edges are extending outside the scope of the window in the interface tab, so one might but a tighter restriction on the max number of vertices the model should generate to get a 100% readable visualization. Finally, one can modify the code in ways so that instead of coloring every vertex in a single tick, the process of coloring is done on seperate ticks. I opted out of this to provide a simple and fast visualization of the theorem.

## NETLOGO FEATURES

No special or unusual NetLogo features.

## RELATED MODELS

No other related models from the NetLogo library nor the Internet (within my search range).

## CREDITS AND REFERENCES

The definition of planar graph and chromatic number, and the statements of the four and five color theorems from: Chartrand, G., & Zhang, P. (2012). A First Course in Graph Theory. http://catdir.loc.gov/catdir/enhancements/fy1201/2011038125-d.html
