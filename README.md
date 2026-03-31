# BYOP-Artificial-Intelligence

Optimizing Urban Traffic Flow (System Design & Logic)

What the project does:

The system simulates a four-way intersection. Unlike traditional lights that change every 30 seconds regardless of traffic, SmartStream performs three key functions:

1.Density Assessment: It "scans" the number of vehicles in each lane (represented by data arrays) to determine which direction needs the longest green light.

2.Emergency Preemption: It detects "Emergency" flags in the data stream and immediately triggers a "Green Wave" for that lane, overriding all other timers.

3.State Swapping: It manages the transition between North-South and East-West flows using efficient variable swapping to ensure no two directions are green simultaneously, preventing "gridlock" errors in the logic.

How the project is set up:

Since this is a Python-based logic simulation, the setup is straightforward.

Environment: Ensure you have Python 3.x installed. No external libraries are strictly required, though time (built-in) is useful for simulating delays.

1.File Structure: Create a main file named traffic_manager.py.

2.Data Structure: Represent the lanes using lists. For example:

  north_lane = ["car", "car", "ambulance", "car"]

  east_lane = ["car", "car"]

How to use the system:
Once the code is written, you interact with it by feeding it different "Traffic Scenarios."

Step 1: Input Data. You can manually update the lane lists or create a function that randomly populates them to simulate a busy rush hour.

Step 2: Run the Optimization. Call your optimization function. The system will output the calculated timing. For example: "North-South Green duration: 45s (High Density)."

Step 3: Trigger an Emergency. Insert an "Ambulance" or "Fire Truck" string into a low-priority lane. The system should immediately output: "Emergency Detected: East-West Override Initiated."

Step 4: Observe the State Swap. Watch the variables swap values as the North-South flow stops and the East-West flow begins, ensuring the "Safety Buffer" (Yellow light logic) is maintained.




