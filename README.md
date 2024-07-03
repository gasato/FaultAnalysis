# FaultAnalysis
Several QGIS Tools and Algorithms for Fault Analysis

## FaultSegmentAz.model3
Explode fault linestring segments and calculate their azimuth as data preparation for and orientation analysis and using in a line direction histogram.

## FractureAnalysisDensity.model3
Calculation of fracture density is defined as the number of fractures per unit of area enumerated in terms of unique points, as fracture centers, using hexagons as a sample window (based partially on Mauldon, 1998; Mauldon and Dershowitz, 2000 )

## FractureAnalysisDensityCircularWindow.model3
Calculation of fracture density as defined by Mauldon (1998)  defined as the sum of fractures longitud per unit of area using circular windows (based on Mauldon, 1998; Mauldon and Dershowitz, 2000 )

## FractureAnalysisIntensity.model3
Calculation of fracture intensity as defined by Mauldon (1998)  defined as the sum of fractures longitud per unit of area using hexagons as a sample window (based partially on Mauldon, 1998; Mauldon and Dershowitz, 2000 )

## FractureAnalysisIntensityCircularWindow.model3
Calculation of fracture intensity as defined by Mauldon (1998)  defined as the sum of fractures longitud per unit of area using circular windows (based on Mauldon, 1998; Mauldon and Dershowitz, 2000 )

## FractureConnectivityNodes.model3
Generate a point layer detecting X Y I fault nodes.

ToDo: Detect E (external or boundary) not valid nodes.

## lineamentDensityGrid.py
A simple method for calculation of a lineament density grid based on total lengths of lineaments inside of each cell. 

## lineamentDensityHeatMap.model3
Lineament density map based on extracting points along each lineament and using them for producing a density map by Heat Map algorithm (Asato, 2022)

## lineamentIntersections.model3
Lineament intersections detection. Produce a point layer. This is a clone of native:lineintersections QGIS algorithm. 

## lineamentParamCalc.py
Calculation of lineamet length, azimuth and orientation by quadrants
