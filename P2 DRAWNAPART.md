## DRAWNAPART: A Device Identification Technique based on Remote GPU Fingerprinting

A New Terchnique:
- Extend the tracking time of fingerprint-based tracking methods.
- Identifies a device from the unique properties of its GPU stack

Contributions:
- It is the first work that explores the manufacturing differences between identical GPUs and the first to exploit these differences in a privacy context.
- It demonstrates a robust technique for distinguishing between machines with identical hardware and software configurations, a technique that delivers practical accuracy gains in a realistic setting.

### GPU Fingerprinting

Aim to uniquely identify devices.

Physically Unclonable Function (PUF) & Execution Units (EUs)

When allocating a parallel set of vertex shader tasks, the WebGL stack tends to assign the tasks to different EUs in a non-randomized fashion. This allows us to issue multiple commands that target the same EUs.

We ensure that the execution time of the targeted EU dominates the execution time of the whole pipeline:
- Non-targeted EUs: A vertex shading program (Quick to complete)
- Targeted EUs: Execution time is highly sensitive to the differences among individual EUs.

![image](https://github.com/HongyuZhu999/HardwareSecurity/tree/main/images/P201.png)

GPU fingerprinting technique:
- Points are rendered in parallel using several EUs
- The EU drawing point i executes a stall function (dark), while other EUs return a hard-coded value (light)
- The execution time of each iteration is bounded by the slowest EU
