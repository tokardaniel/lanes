1. Design a database to store the following information 
   1. Road Segments
      1. They have a unique ID
      2. They may have a name, but it's not mandatory
   2. Lanes 
      1. Every lane belongs to one and only one road segment
      2. The road centerline is identified as lane zero
      3. Right side lanes are numbered as -1, -2, -3, etc.
      4. Left side lanes are numbered as 1, 2, 3, etc.
      5. One-sided roads (e.g. positive lanes only) are possible
      6.  The width of the lanes is not constant along their length. The width of a lane
      is given at arbitrary points along its length, starting from the beginning of the 
      road segment (e.g. at 0 m the width is 3.0 m, at 100 m it is 3.5 m, at 150 m it 
      is 3.2 m.) The width of the zero lane is always 0.0 m.
   3. Lane connectivity 
      1. Previous lanes / next lanes
         1. More than one connecting lane is possible at both ends
         2. They are obviously on another road segment
2. Using the above database and your favorite Python tools to access it, provide Python 
functions for the following jobs. Please take care of handling bad input and cases when there 
is nothing to return 
   1. Given a Road Segment ID, return the number of lanes in both directions
   2. Given a Road Segment ID, a lane number and a distance from the start of the lane, 
   return the lane width at that position (you may need to interpolate)
   3. Given a Road Segment ID and a lane number, return the possible next lanes (Road 
   Segment ID and lane number), where the simulated vehicle can continue its route.