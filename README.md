# WolframLabs
Plot[x^(1/2) + 1/x, {x, -10, 10}]
Plot3D[x^2 + y^2, {x, -10, 10}, {y, -10, 10}]
ListPlot[{{1, 2}, {2, 0}, {3, 1}}]
ListLinePlot[{{1, 2}, {2, 0}, {3, 1}}]

Table[ x^(1/2) + 1/x, {x, 1, 5}] 
ParallelTable[x^(1/2) + 1/x, {x, 1, 5}]

FlipView[Table[ 
  Plot3D[ x^i +  y^i, {x, -10, 10}, {y, -10, 10}], {i, 1, 5}]]
SlideView[
 Table[Plot3D[ x^i +  y^i, {x, -10, 10}, {y, -10, 10}], {i, 1, 5}]]

Export["flipview.gif", 
 FlipView[Table[ 
   Plot3D[ x^i +  y^i, {x, -10, 10}, {y, -10, 10}], {i, 1, 5}]]]
Export["flipview.png", 
 FlipView[Table[ 
   Plot3D[ x^i +  y^i, {x, -10, 10}, {y, -10, 10}], {i, 1, 5}]]]
Export["slideview.gif", 
 SlideView[
  Table[ Plot3D[ x^i +  y^i, {x, -10, 10}, {y, -10, 10}], {i, 1, 5}]]]
Export["slideview.png", 
 SlideView[
  Table[ Plot3D[ x^i +  y^i, {x, -10, 10}, {y, -10, 10}], {i, 1, 5}]]]

Export["function.dat",  ParallelTable[x^(1/2) + 1/x, {x, 1, 5}]]
ListPlot[{Import["function.dat"]}]
