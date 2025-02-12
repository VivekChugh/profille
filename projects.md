# Vivek Chugh

**Sr Engineer** | vivekchugh.83@gmail.com | +1-226-220-0528 | 358 Chokecherry Cres, Waterloo, Ontario, Canada

Experienced system design and video professional with 18 years of diverse experience, including roles in Silicon Valley startups and Samsung. Proficient in problem-solving using data structures and algorithms, with expertise in Linux system programming and TCP-UDP/IP network stack internals. Demonstrated skills in developing fault-tolerant distributed systems within multithreading environments. Recognized for initiative, results-oriented approach, teamwork, and effective communication across various technical projects.

## Work Experience

**Sr Engineer L-8(Staff Engineer)** | Sep 2018 - Present | Ford Motors, Waterloo

Connectivity Manager  [C, C++, AOSP, AIDL, Embedded Linux, IP-Networking ] [Github-link](https://github.com/VivekChugh/profille/blob/main/project_Networking_CM.md)
- **Optimized network configuration performance** by reducing the time taken to set up IP rules, VLANs, and routing tables, improving initialization speed by [X]% (if measurable).  
- **Enhanced modularity and maintainability** by refactoring the codebase, introducing better abstraction layers for handling multiple network interfaces, making it easier to extend and debug. 
- **Improved security compliance** by integrating dynamic firewall rule management using iptables/nftables, strengthening protection against unauthorized network access.  
- **Streamlined development processes** by mentoring junior engineers, improving code review practices, and introducing best practices for C++ and Linux networking development.  
- **Strengthened fault tolerance and failover handling** by implementing automated network state monitoring and adaptive route reconfiguration in case of link failures.  
- **Refined technical documentation and knowledge sharing**, ensuring clearer architecture diagrams, configuration guides, and troubleshooting steps for seamless handover and maintenance.  

MQTT-Based ECU Communication System [C, C++, MQTT, AOSP, Embedded Linux] [Github-Link](https://github.com/VivekChugh/profille/blob/main/project_MQTT.md)
- **Optimized MQTT Broker Performance**: Enhanced the Mosquitto MQTT broker configuration on the Gateway ECU, resulting in improved message throughput and reduced latency in inter-ECU communications.
- **Developed Robust Client Libraries**: Created efficient and lightweight MQTT client libraries for various ECUs, facilitating seamless publish/subscribe interactions and ensuring reliable message delivery across the system.
- **Implemented Advanced Topic Management**: Designed a structured topic hierarchy and implemented access control mechanisms, ensuring secure and organized message routing between applications on different ECUs.
- **Enhanced System Scalability**: Refined the system architecture to support the addition of new ECUs and applications without significant reconfiguration, promoting scalability and ease of integration.
- **Improved Fault Tolerance**: Integrated mechanisms for detecting and handling communication failures, ensuring system resilience and maintaining reliable operation under adverse conditions

Autonomous Vehicle Mapping Application [ADAS, Localization, C++, QT] [Github-Link]()
- **Real-Time 3D Environment Reconstruction**: Developed and optimized algorithms to process sensor inputs from LiDAR, cameras, and GPS, enabling the application to construct accurate 3D models of the vehicle's surroundings in real-time.
- **Advanced Landmark Detection and Extraction**: Implemented sophisticated techniques to identify and extract significant landmarks such as buildings, road signs, and trees from sensor data, enhancing the application's environmental awareness.
- **Dynamic Map Updating**: Designed a system to compare detected landmarks with existing databases, allowing the application to dynamically update maps with new or altered landmarks, ensuring up-to-date navigation information.
- **Intuitive User Interface Design**: Created a user-friendly interface using Qt that visually represents the reconstructed environment and landmark data, providing users with clear and actionable insights into the vehicle's surroundings.
- **Optimized Sensor Data Integration**: Streamlined the integration of various sensor inputs to ensure synchronized and efficient data processing, improving the overall performance and responsiveness of the application.
- **Robust Testing and Validation**: Conducted extensive testing under diverse environmental conditions to validate the accuracy and reliability of the mapping and landmark detection features, leading to iterative enhancements and increased system robustness.

**Sr Engineer** | Nov 2016 - Jul 2018 | Faraday Future, Los Angeles 

Over-The-Air (OTA) Enabled Bootloader [C, Memory mapping, ISR] [Github-Link](https://github.com/VivekChugh/profille/blob/main/project_OTA_BL.md)
- **Enhanced Security Protocols**: Implemented advanced cryptographic checks, including SHA-256 hash verification and digital signature validation, to ensure the integrity and authenticity of firmware updates, significantly reducing the risk of unauthorized code execution.
- **Developed Fail-Safe Rollback Mechanism**: Designed and integrated a robust rollback feature that automatically reverts to the previous firmware version in case of update failures or corruption, preventing device bricking and ensuring continuous operation.
- **Optimized Partition Management**: Improved the bootloader's partition management system to efficiently handle multiple firmware slots, facilitating seamless transitions between current and updated firmware versions during OTA updates.
- **Reduced Bootloader Footprint**: Refactored low-level C code to minimize the bootloader's memory usage, achieving a more compact and efficient implementation suitable for resource-constrained embedded systems.
- **Streamlined OTA Update Process**: Enhanced the OTA update mechanism to support more reliable and faster firmware downloads over various wireless communication interfaces, improving the user experience and reducing downtime during updates.
- **Improved Documentation and Developer Support**: Created comprehensive documentation detailing the bootloader's architecture, update procedures, and troubleshooting guidelines, aiding future development and facilitating easier maintenance.

Vehicle Sensor Data Visualizer [C++, Qt Framework, Linux, Embedded Linux] [Githib-Link]()  
- **Real-Time Multi-Sensor Data Integration**: Developed a robust system to simultaneously process and display data from various vehicle sensors, including LiDAR, cameras, and ultrasonic sensors, ensuring synchronized and accurate real-time visualization.
- **Dynamic View Management**: Implemented a flexible interface allowing users to seamlessly switch between different sensor data views within a single window, enhancing user experience and situational awareness.
- **Optimized Rendering Performance**: Enhanced the rendering pipeline to efficiently handle high-frequency data streams, resulting in smooth visualization of video frames, point clouds, and distance readings without latency.
- **Advanced 3D Point Cloud Visualization**: Improved the rendering of LiDAR point clouds to provide detailed 3D representations of the vehicle's surroundings, aiding in better analysis and decision-making.
- **User-Friendly Interface Design**: Designed an intuitive user interface that presents complex sensor data in an accessible manner, allowing users to easily interpret and interact with the information.
- **Comprehensive Testing and Validation**: Conducted extensive testing with various sensor configurations and environmental conditions to ensure the application's reliability and robustness in real-world scenarios.

**Sr Tech Developer (Tech Lead)** | Jun 2015 - Oct 2016 | *Verizon, Dallas

Video QoS Benchmarking System [] [Github-Link]()
- **Real-Time Decoder Performance Monitoring**: Developed a system to continuously probe the video decoder every 10 seconds, capturing essential metrics such as the number of video frames processed and decode errors encountered, enabling immediate detection of performance issues. citeturn0search0
- **Quality of Experience (QoE) Assessment**: Implemented algorithms to calculate the user's perceived quality of the video stream based on decoder performance metrics, providing valuable insights into the end-user experience.
- **Efficient Data Collection and Analysis**: Designed the system to gather and analyze performance data with minimal overhead, ensuring that the monitoring process does not interfere with the normal operation of the Set-Top Box.
- **Integration with Embedded Linux Platform**: Implemented the software in C and C++ on an embedded Linux platform, leveraging the platform's capabilities to achieve efficient and reliable performance monitoring.
- **Proactive Error Detection and Reporting**: Established mechanisms to promptly identify and report decode errors, such as dropped or corrupted frames, facilitating timely interventions to maintain optimal video quality.
- **User-Centric Performance Metrics**: Focused on metrics that directly impact the user's viewing experience, ensuring that the system provides relevant and actionable information for maintaining high-quality video playback.

Video Streaming Server [] [Githib-Link]()  
- **Implementation of Adaptive Bitrate Streaming**: Developed support for MPEG-DASH and HLS protocols, enabling the server to provide video streams in multiple quality levels. This allows clients to dynamically switch between streams based on their current bandwidth, ensuring a smooth viewing experience. 
- **Efficient Content Segmentation**: Engineered the server to segment video content into smaller chunks, typically ranging from 2 to 10 seconds. This approach facilitates progressive fetching and buffering by clients, reducing latency and improving playback performance. 
- **Dynamic Bitrate Adaptation**: Implemented mechanisms that allow the server to adjust streaming quality in real-time, responding to fluctuations in network conditions to maintain optimal video playback without interruptions. 
- **Embedded Linux Platform Optimization**: Developed the server using C and C++ on an embedded Linux platform, ensuring efficient resource utilization and reliable performance across various devices and network environments. 
- **Enhanced Client Compatibility**: Ensured that the server's streaming capabilities are compatible with a wide range of client devices and media players by adhering to industry-standard streaming protocols and formats. 
- **Robust Error Handling and Recovery**: Implemented comprehensive error detection and recovery mechanisms to handle network disruptions and other issues gracefully, minimizing their impact on the user experience. 

**Sr Engineer, Grade 8** | May 2014 - May 2015 | Continental Automotives, Singapore


**Sr Software Engineer** | Aug 2005 - Apr 2014 | Samsung Labs, New Delhi


## Core Skills

Embedded Systems, Computer Vision, Video streaming., Automotive
Protocols : CAN, OBD2, UDS, LIN, CAN-FD, Network Protocols : RTP, RTSP,
RTMP, HLS, MPEG-DASH, SRT., Video Codecs and Containers : H.264, MP4,
MPEG-2 (TS and PS), HEVC.

## Education

Feb 2006 - Aug 2006

**Post Graduate Diploma** \|

GPA: 97.5

**Training School** Feb 2006 - Aug 2006

\| Advanced Computer

**Punjab Technical University** Aug 2001 - May 2005

**Bachelor of Technology** \| Electronics and Communication

GPA: 66
