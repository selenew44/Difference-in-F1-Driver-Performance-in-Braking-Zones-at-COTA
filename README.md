# Comparative Analysis of Aston Martin Drivers' Performance at Turn 12 Braking Zone of COTA
#### Project Status: Active

## Project Description
This project is an extension of the 2025 Aramco Stem Challenge, in which it was proposed that Aston Martin cars easily lose pace in braking zones and the team should focus on improving braking efficiency. This project is designed to test this assumption, by investigating the difference in braking zone performance between Aston Martin drivers(Alonso and Stroll) and other drivers, specifically in the 2025 United Sates Grand Prix at turn 12. By assigning all valid telemetry data points in the braking zone to bins with width of 1.0, an average speed profile across all valid laps for each selected driver is calculated and plotted for analysis. 

### Methods Used
* Inferential Statistics
* Accuracy Filtering
* Data Visualization
* Signal Processing
* Time-Series Analysis

### Technologies
* Python
* Pandas
* NumPy
* Matplotlib
* FastF1 API
* Jupyter Notebooks

## Methodology
### 1. Data Filtering
Laps are filtered to remove:
- FastF1 generated data
- pit laps
- deleted laps
- laps under non-green track conditions

This ensures average speed profiles across drivers are comparable.

### 2. Distance Binning
To reduce sensor noise and allow averaging across laps, telemetry points are discretized into 1.0-meter distance bins to:
- ensure each bin represents the same physical location, and average speed profiles across drivers are comparable
- enable consistent aggregation across laps, and thus ensure the behaviors captured are statistically representative, not lap-specific noise

### 3. Visualisation
Average profiles are plotted using Matplotlib:
- consistent driver color mapping via get_driver_color
- dashed line styles to visually distinguish Stroll from Alonso
- apex location marked with a vertical reference line

Drivers selected for comparative analysis include:
- Oscar Piastri (McLaren)
- George Russell (Mercedes)
- Charles Leclerc (Ferrari)

## Conclusion
- The decelerations of Aston Martin drivers are smaller than that of other drivers, seen from the relatively flatter lines reprensenting Alonso and Stroll.
- There is a measurable lag in the transition from deceleration to acceleration for AM drivers past turn 12 apex. While other drivers stabilize their minimum speed near the Apex, AM drivers, particularly Stroll, continue to decelerate after exiting turn 12.
