# ProcessX
Repository for QGIS ProcessX Plug-In

This Plug-In adds a new processing provider to QGIS. It contains a variety of processing algorithms.

The algorithms are:

### Vector - Conditional:
- (New in v1.0) **Join Attributes By Nearest With Condition**: Joins the attributes of the x nearest features if an expression condition returns true.
- (New in v1.0) **Count Features In Features With Condition**: Counts features in another layers features (can be lines and polygons as well as points and different geometric predicates like intersects, within, disjoint, equals...) if an expression condition returns true.
- (New in v1.0) **Select Duplicates By Similarity**: Selects possible duplicates in a layer by distance and attribute like exact attribute match, soundex, hamming distance, levenshtein distance or longest common substring.
- (New in v1.0) **Conditional Intersection**: Creates an intersection geometry between the features of two layers only if an expression condition returns true. This algorithm can also be used as polygon-self-intersection.
- (New in v1.1) **Count Points in Polygons With Condition**: Counts points in polygons (intersects or within) if an expression condition returns true (This algorithm is a lot faster than "Count Features In Features With Condition" when counting 2D-Single-Points in Polygons).

### Vector - Creation
- (New in v1.0) **Create Timepolygons With Pointcount**: Creates x duplicates of given polygons in a given timerange with from- and to-timestamp and the pointcount falling inbetween this timerange and geometry.
- (New in v1.0) **Geometry Layer From Geojson String Field**: Creates a duplicated layer of the input with modified geometry, taken from a field with a valid GeoJSON-String.
- (New in v1.1) **Create Nested Grid**: Creates a parent grid and x child grids. You can choose how many childcells a parent shall have in x and y direction.

### OpenTripPlanner
- (New in v1.0) **OtpRoutes**: Requests routes from an OpenTripPlanner instance and creates a linelayer from the returned geometry and attributes.
- (New in v1.0) **OtpTraveltime**: Adds some attributes to a given layer based on OpenTripPlanner routing results.