
### 1. **Overview of the System**:
   - **Purpose**: The project involves the development of a communication system between various **Electronic Control Units (ECUs)** in a car. Applications running on different ECUs need to communicate with each other. This system uses the **MQTT protocol** for lightweight, efficient message exchange between applications residing on the same or different ECUs.
   - **MQTT Architecture**: 
     - One of the ECUs, called the **Gateway ECU**, hosts the **Mosquitto MQTT Broker**.
     - Applications running on other ECUs (or on the Gateway ECU) use a client library that provides APIs to publish and subscribe to specific topics.
   
### 2. **Key Features**:
   - **Publish/Subscribe Model**: Communication is based on the MQTT protocol, where applications can **publish** messages to specific topics and **subscribe** to topics to receive messages. This allows for decoupled communication between different ECU applications.
   - **Centralized MQTT Broker**: The **Gateway ECU** runs a centralized MQTT broker (using Mosquitto) that handles all message routing between ECUs. It ensures messages are distributed to the correct subscribers.
   - **Lightweight Communication**: The system is designed to be efficient, with minimal resource usage, making it suitable for automotive applications with limited bandwidth and computational power.
   - **Cross-ECU Communication**: The system supports communication between applications running on different ECUs, enabling data sharing and coordination between various systems in the vehicle (e.g., engine control, body control, infotainment).
   - **API Library for Applications**: Applications on each ECU link to a custom MQTT library, which provides simple **publish/subscribe APIs** for communication.
   - **Real-time Data Exchange**: Allows real-time data exchange between various ECUs (e.g., sharing sensor data between the engine control unit and a safety control unit).

### 3. **How the System Functions**:
   - **MQTT Broker on Gateway ECU**:
     - The **Gateway ECU** hosts the **Mosquitto MQTT broker**, which acts as the central point for all message traffic.
     - The broker listens for connection requests from different ECUs and manages message routing.
     - When an application publishes a message to a topic, the broker routes the message to all subscribed clients (ECUs) that have expressed interest in that topic.
   - **ECU Applications Using MQTT Client Library**:
     - Each application running on the ECUs links to an MQTT client library.
     - This library abstracts the low-level MQTT protocol and provides an easy-to-use API with functions like `publish(topic, message)` and `subscribe(topic, callback)`.
   - **Publish/Subscribe Model**:
     - Applications publish messages to topics based on their function (e.g., an engine control unit might publish sensor data to a topic like `engine/sensor/rpm`).
     - Other applications, like a safety control unit, subscribe to relevant topics (e.g., subscribing to `engine/sensor/rpm` to get real-time RPM data).
   - **Real-Time Communication**:
     - As new messages are published, the MQTT broker distributes them in real-time to all subscribing clients.
     - This enables quick data exchange between ECUs, supporting functions like sensor fusion, safety alerts, or infotainment updates.
   - **Error Handling and Fault Tolerance**:
     - The system supports MQTT’s **Quality of Service (QoS)** levels to guarantee message delivery based on the importance of the data.
     - Error handling mechanisms are in place to retry message deliveries in case of communication interruptions or ECU failures.

### 4. **Technologies Used**:
   - **C++**: The core communication logic and MQTT client library were developed in C++. C++ was chosen for its performance and compatibility with low-level ECU systems.
   - **Mosquitto MQTT Broker**: The **Mosquitto** MQTT broker, a lightweight and open-source implementation, was used on the Gateway ECU to handle message routing and management.
   - **MQTT Client Library**:
     - Developed a custom MQTT client library in C++ for the applications running on the ECUs.
     - The library wrapped the **Paho MQTT** C++ client or similar lightweight MQTT libraries for embedding into automotive systems.
   - **In-Car Network (CAN, Ethernet)**:
     - The ECUs communicated over an in-car network like **CAN (Controller Area Network)** or **Automotive Ethernet**, allowing the MQTT messages to be transported efficiently across different ECUs.
   - **Quality of Service (QoS)**:
     - Implemented different QoS levels for message delivery, ranging from **at most once** (QoS 0) to **exactly once** (QoS 2), depending on the criticality of the data.
   - **TLS/SSL Encryption**:
     - Secured MQTT communication using **TLS/SSL** to ensure encrypted and authenticated data exchange between ECUs, especially for safety-critical or sensitive data.

### 5. **Development Process**:
   - **Requirement Gathering**:
     - Defined the types of messages and data that needed to be shared between ECUs (e.g., sensor data, control signals, system alerts).
     - Identified the network communication requirements for in-vehicle systems (e.g., CAN or Ethernet) to ensure that MQTT could work efficiently within these constraints.
   - **MQTT Broker Setup on Gateway ECU**:
     - Configured and deployed the **Mosquitto MQTT broker** on the Gateway ECU. This involved setting up the broker to handle multiple clients (ECUs) and ensuring that message traffic was managed efficiently.
     - Configured broker security, including user authentication, TLS/SSL for encrypted communication, and topic-based access control to restrict sensitive messages to authorized ECUs only.
   - **Developing the MQTT Client Library**:
     - Developed a **lightweight C++ MQTT client library** that provided a high-level API for ECU applications.
     - The library allowed applications to easily publish messages to the broker and subscribe to topics of interest.
     - Integrated callback mechanisms to notify applications when new messages were received on subscribed topics.
   - **Integration with ECU Applications**:
     - Worked with different ECU subsystems (e.g., powertrain, body control, infotainment) to integrate the MQTT library into their software stacks.
     - Provided guidelines for developers to define appropriate MQTT topics for their data (e.g., `engine/sensor/rpm`, `infotainment/media/playback`).
   - **Testing & Debugging**:
     - Simulated communication between different ECUs in the vehicle to test the system's robustness and scalability.
     - Implemented test cases to verify that the publish/subscribe model worked correctly and that messages were reliably delivered across ECUs in real-time.
     - Ensured the broker handled edge cases like ECU disconnections, retries, and QoS guarantees.
   - **Performance Optimization**:
     - Tuned the system for low latency and minimal CPU and memory usage, ensuring real-time communication for safety-critical ECUs.
     - Optimized message handling and ensured that the broker could handle high message loads efficiently.
   
### 6. **Challenges Addressed**:
   - **Network Latency**: Ensured the MQTT communication system met the real-time requirements of in-car applications, optimizing for low-latency communication between ECUs.
   - **Scalability**: Designed the system to support multiple ECUs and high message throughput without overloading the broker or network.
   - **Security**: Integrated security measures like **TLS encryption** and **authentication** to ensure that only authorized ECUs could publish or subscribe to specific topics.
   - **Reliability**: Implemented MQTT’s **QoS levels** to guarantee reliable message delivery, especially for critical applications like safety and engine control.
