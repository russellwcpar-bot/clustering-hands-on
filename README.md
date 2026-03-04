# clustering-hands-on
Apply K-Means:
Interpretation:
By calculating the Adjusted Rand Index for different values of K, I observed that the score was highest at K=3. This shows that the data aligns best with the three actual species of Iris. As K increased beyond 3, the ARI decreased, indicating that the algorithm was creating artificial divisions that do not reflect the reality of the data 

Apply DBSCAN:
Interpretation:
DBSCAN works well for datasets with noise and outliers because it does not force every point into a cluster. It also does not require you to specify the number of clusters beforehand. DBSCAN was sensitive to the eps and min_samples parameters. My experiment showed that a small change in eps could result in either too many noise points or all points merging into one cluster. 
K-Means assumes clusters are relatively spherical, DBSCAN defines clusters based on density. For the Iris dataset, DBSCAN effectively identified the dense Setosa cluster but struggled with the overlapping Versicolor and Virginica regions.
DBSCAN was sensitive to the eps and min_samples parameters. My experiment showed that a small change in eps could result in either too many noise points or all points merging into a single large cluster.


Part D: Reflection
 	One use of clustering could be tools like COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) for predicting the likelihood of a defendant reoffending. These tools sort people into distinct groups based on how closely their profile matches offenders.  Certain demographic information as well as information on the initial crime would be taken. The system then assigns them to a risk cluster based on how closely their profile matches historical patterns of recidivism. The centroid for each group could be from low to high risk.


Ethical & Societal Considerations
Using clustering logic introduces a number of issues. For example if race is removed, the algorithm may use proxy variables like zip code or education level to recreate societal biases.  A ProPublica audit of the COMPASS  system found that Black defendants were incorrectly flagged as High Risk at nearly twice the rate of white defendants as a result of false positives. K means is also subject to an issue with centroid stability in this instance. If police focus their patrols in areas around the high risk centroid they may make more arrests there. These new arrests are fed back into the model reinforcing that centroid's position at those coordinates. This makes the center of the profile  a reflection of policing patterns, not just criminal behavior. Judges may rely too heavily on these objective scores, and ignore individual mitigating circumstances.


article https://www.propublica.org/article/machine-bias-risk-assessments-in-criminal-sentencing

