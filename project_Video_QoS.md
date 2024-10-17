### Project Overview: Video QoS benchmarking System

As a software engineer, I developed a system for an IPTV Set-Top Box that monitors the performance of the video decoder in real-time. The goal was to evaluate the **user's perceived quality** of the video stream based on decoder performance metrics. This software was implemented in **C and C++** on an **embedded Linux platform**.

---

### 1. **Purpose of the Software**:
   - The software continuously probes the video decoder on the **IPTV Set-Top Box** while it processes incoming video streams.
   - It gathers essential **performance metrics** such as:
     - **Number of video frames processed**.
     - **Number of decode errors encountered** (e.g., dropped or corrupted frames).
   - Based on these parameters, it calculates the **quality of experience (QoE)** for the user, providing insights into the perceived quality of the video stream.

---

### 2. **Key Features and Functionalities**:
   - **Regular Probing of Video Decoder**:
     - The software probes the video decoder every **10 seconds** to capture its current state.
     - It queries key decoder metrics like frame processing rate and error count.
   - **Tracking Video Processing Metrics**:
     - The system tracks the **total number of video frames** processed over time and any **decode errors** encountered, which could impact playback quality.
   - **Derivation of Video Quality**:
     - Based on decoder metrics, the software assesses **video quality degradation** (due to factors like frequent decode errors or dropped frames).
     - This can provide an indication of **buffering**, **network congestion**, or **hardware issues**.
   - **Reporting and Logging**:
     - The derived quality metrics are logged and can be reported back to a central server for further analysis.
     - Alerts can be generated if the user's **quality of experience (QoE)** drops below a certain threshold.

---

### 3. **How the Software Functions**:
   - **Initialization**:
     - Upon system startup, the software initializes and connects to the video decoder, setting up regular polling intervals (every 10 seconds).
   - **Probing the Decoder**:
     - At each interval, the software fetches the following metrics from the decoder:
       - **Frames processed**: Number of video frames successfully decoded since the last probe.
       - **Decode errors**: Number of errors encountered while decoding (e.g., due to packet loss or frame corruption).
   - **Deriving Quality Metrics**:
     - The gathered metrics are used to calculate the perceived **quality of the video stream**.
     - For example, a high number of decode errors over a short time frame would suggest poor video quality.
   - **Logging and Feedback**:
     - The data is stored in logs for future analysis, allowing network operators to monitor overall performance trends.
     - **Real-time feedback** can also be sent to user interfaces or central systems to report potential video quality issues.
   - **Adaptation Based on Data**:
     - If frequent errors are detected, the software could trigger adaptive actions, such as reducing stream bitrate to compensate for network limitations.

---

### 4. **Technologies Used**:
   - **C and C++**:
     - The software was written in **C and C++**, allowing direct interaction with the low-level video decoder API, ensuring minimal overhead and high performance.
   - **Embedded Linux**:
     - Running on an **embedded Linux platform**, the software leverages Linux’s process scheduling and resource management to ensure smooth, real-time operation.
   - **Decoder APIs**:
     - The system communicates with the **video decoder** through platform-specific APIs, fetching detailed video stream metrics like frame count and decode errors.
   - **Log Management**:
     - Implemented log management routines to record quality metrics and decode performance for long-term analysis.

---

### 5. **Steps Taken to Develop the Software**:
   1. **Requirement Gathering**:
      - Worked with the system architects and video streaming team to define the key metrics that affect video quality.
   2. **Design**:
      - Designed the software architecture to include periodic probing functionality, decoder API integration, and real-time quality metrics derivation.
      - Created flowcharts and state diagrams to map the interactions between the software and the video decoder.
   3. **Development**:
      - Implemented the core functionality in **C and C++**, ensuring efficient communication with the video decoder.
      - Utilized the decoder’s API to extract metrics and probe the state of the video stream.
   4. **Testing**:
      - Performed extensive testing on real-world video streams to validate that the software accurately measured video quality and could detect common issues like frame drops and errors.
      - Tested under various network conditions to ensure that the software could handle different levels of bandwidth or latency.
   5. **Optimization**:
      - Optimized the performance of the periodic probing mechanism to ensure minimal overhead on system resources, even when handling large video streams.
   6. **Logging and Error Handling**:
      - Added detailed **logging** functionality to capture probe data over time and implemented robust **error handling** to manage unexpected decoder states or network issues.
   7. **Final Integration and Deployment**:
      - Integrated the software into the IPTV Set-Top Box firmware and conducted end-to-end validation to ensure smooth operation alongside other system components.

---
