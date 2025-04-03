# Generation Based Load Management System To Prevent Future Blackouts In Bangladesh
On November 2, 2014, Bangladesh experienced a complete nationwide blackout that lasted nearly 12 hours. The root cause was traced back to a power transmission overload at the Bheramara substation, part of the high-voltage link importing electricity from India. While the substation was rated to handle a maximum of 400 MW, it received 445 MW, triggering a technical failure. This led to a sudden drop in system frequency and initiated a cascading failure across the national grid, ultimately forcing all power plants offline and plunging the entire country into darkness.

Despite the presence of grid synchronization and Automatic Generation Control (AGC) systems in many countries, Bangladesh lacks a sufficient operating reserve to effectively use these traditional methods for blackout prevention. Hence, the incident highlighted a critical need for a more suitable, locally adaptable solution.

![Block Diagram of Our Proposed Model.png](https://github.com/mehedihassanarman/Generation-Based-Load-Management-System-to-Prevent-Future-Blackouts-in-Bangladesh/blob/main/Project%20Image/Block%20Diagram%20of%20Our%20Proposed%20Model.png)

This project introduces a simulation-based, generation-aware load management system specifically designed for energy infrastructures like Bangladesh’s. It aims to prevent future blackouts by maintaining balance between generation and demand, even in the event of power station failures. Our proposed system constantly monitors, analyzes, and controls the electric load and generation in real-time. The architecture is composed of four major functional components:

### 1. Power Generation Analyzer (PGA)
- Uses Phasor Measurement Units (PMUs) to gather real-time data from each power station.
- Identifies underperforming or failed stations through multi-step analysis.
- Isolates faulty stations from the power system to avoid instability.

2. **System Controller (SC)**
- Stores data on maximum generation capacity and current demand.
- Calculates how much of the load should remain connected based on the percentage of active generation.
- Sends load adjustment instructions to the operating software.

3. **Power System Frequency Analyzer (PSFA)**
- Calculates the current system frequency based on load vs. generation.
- Maintains frequency near the nominal 50 Hz value by adjusting demand when generation drops.
- Demonstrates how frequency stabilizes when the load is reduced in sync with generation.

4. **Load Area Controllers**
- Manage power distribution across 8 defined load areas.
- Enable section-wise load control, deciding which sectors receive power during low generation scenarios.
