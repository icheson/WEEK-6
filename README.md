Table
Copy
Model	Size	Top-1 Acc	Inference*
Float32 (baseline)	13.4 MB	0.93	42 ms
TensorFlow-Lite float	13.4 MB	0.93	28 ms
TensorFlow-Lite int8	0.27 MB	0.91	11 ms
*On Pixel-5 ARM CPU (single-thread).
Raspberry Pi 4 ≈ 25 ms for int8 model → > 30 FPS capability.
Edge AI Benefits for Real-Time Applications
Zero Latency Budget
No network round-trip; inference happens on the same silicon that acquires the sensor data → milliseconds instead of hundreds of milliseconds.
Privacy & Compliance
Images never leave the device—ideal for GDPR, HIPAA, or sensitive industrial environments.
Offline Reliability
Works in remote locations, underground, or on moving vehicles where connectivity is intermittent.
Bandwidth & Cost Savings
Only upload meta-data (e.g., “bin full”) instead of high-res video; reduces cellular data bills and cloud-storage fees.
Scalability Without Backend Load
Adding more cameras does not require more GPU servers; each node is self-sufficient.
Energy Efficiency
Quantised (int8) models consume ≈ 4× less energy than floating-point on modern ARM cores, extending battery life for portable or solar-powered devices.
Deterministic Timing
No jitter from shared cloud resources—crucial for robotics and safety-critical systems.
