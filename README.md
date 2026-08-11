# keywords
# Technical Fundamentals & Software Engineering Guide

## TL;DR

A single-source cheat sheet covering everything from physical silicon to AI models. Jump to any topic below to get straight to the core concepts without fluff.
A single-source sheet covering everything from physical silicon to AI models. Jump to any topic below to get straight to the core concepts.

---

## 1. Hardware Fundamentals

Hardware comprises the physical, tangible components of a computing system.

* **CPU (Central Processing Unit):** The "brain" of the computer that executes program instructions via the Fetch-Decode-Execute cycle.
* **RAM (Random Access Memory):** Volatile primary memory used for fast, temporary data storage while programs are running. Data is lost when powered off.
* **Storage (SSD / HDD):** Non-volatile secondary memory used for long-term data retention. Solid State Drives (SSDs) use flash memory for much faster read/write speeds compared to magnetic Hard Disk Drives (HDDs).
* **Motherboard:** The primary printed circuit board (PCB) that connects and routes communication between the CPU, RAM, storage, and peripheral devices via buses.

---

## 2. Computer Architecture

Computer architecture defines how hardware components are structured and integrated to execute software.

```
+-------------------------------------------------------------+
|                         CPU                                 |
|  +--------------------+  +-------------------------------+  |
|  | Control Unit (CU)  |  | Arithmetic Logic Unit (ALU)   |  |
|  +--------------------+  +-------------------------------+  |
|  +-------------------------------------------------------+  |
|  | Registers (PC, MAR, MDR, ACC)                         |  |
|  +-------------------------------------------------------+  |
+------------------------------+------------------------------+
                               |
                   System Bus  | (Data, Address, Control)
                               |
+------------------------------+------------------------------+
|                   Main Memory (RAM)                         |
+-------------------------------------------------------------+

```

* **Von Neumann Architecture:** The standard model where program instructions and data share the same physical memory space and bus system.
* **Registers:** Microscopic, high-speed storage locations directly inside the CPU (e.g., Program Counter, Accumulator) used for immediate data operations.
* **Cache Memory (L1, L2, L3):** Extremely fast, small memory layers located on or near the CPU die to store frequently accessed data, reducing RAM access latency.
* **Instruction Set Architecture (ISA):** The interface between hardware and software (e.g., x86, ARM) that defines the commands a CPU can execute.

---

## 3. Operating Systems (OS)

The OS is system software that manages computer hardware, software resources, and provides common services for programs.

* **Kernel:** The core of the OS that operates with full privileges to manage system resources (memory, CPU scheduling, device drivers).
* **Process vs. Thread:**
* **Process:** An executing instance of a program with its own isolated memory space.
* **Thread:** The smallest unit of execution *within* a process; threads in the same process share memory.


* **Memory Management & Virtual Memory:** The OS maps virtual memory addresses used by applications to physical RAM or disk storage (paging), preventing applications from interfering with each other's memory.
* **File System:** The method and data structure the OS uses to control how data is stored and retrieved on disk (e.g., NTFS, ext4, APFS).

---

## 4. Networking Fundamentals

Computer networking enables two or more systems to exchange data using standardized protocols.

* **OSI 7-Layer Model:** A conceptual framework for understanding network traffic:
1. *Physical:* Cables, bits, radio waves
2. *Data Link:* MAC addresses, switches
3. 3. *Network:* IP addresses, routers
4. *Transport:* TCP/UDP ports, segments
5. *Session:* Connection management
6. *Presentation:* Data encryption, formatting
7. *Application:* HTTP, FTP, SMTP


* **TCP vs. UDP:**
* **TCP (Transmission Control Protocol):** Connection-oriented, guarantees packet order and delivery (used for web, email).
* **UDP (User Datagram Protocol):** Connectionless, faster, does not guarantee delivery or ordering (used for streaming, gaming).


* **IP Addressing (IPv4 / IPv6):** Logical numerical labels assigned to devices on a network for identification and routing.

---

## 5. Localhost & Ports

How computers route internal traffic and distinguish between different services.

* **Localhost (127.0.0.1):** A loopback network interface that allows a computer to send network calls back to itself without broadcasting over an external network.
* * **Ports:** Virtual endpoints (numbered 0 to 65535) used by an IP address to direct network traffic to specific applications or services.
* **Common Standard Ports:**
* `80`: HTTP (Unencrypted web traffic)
* `443`: HTTPS (Encrypted web traffic)
* `22`: SSH (Secure Shell)
* `3306`: MySQL Database
* `5432`: PostgreSQL Database



---

## 6. Device Communication

Methods devices use to transmit signals to one another over short or long distances.

* **Serial vs. Parallel:** Serial transmits data bit-by-bit over a single channel (modern standard like USB), while parallel transmits multiple bits simultaneously over multiple wires.
* **Wireless Protocols:**
* **Wi-Fi (IEEE 802.11):** High-bandwidth wireless networking over local areas.
* **Bluetooth:** Low-power, short-range wireless communication for paired devices.
* * **Hardware Interfaces:** Standardized physical buses for connecting components (e.g., PCIe for GPUs/SSDs, I2C/SPI for microcontrollers).

---

## 7. Internet Basics

The global network of interconnected computer networks using the TCP/IP protocol suite.

* **DNS (Domain Name System):** The "phonebook of the internet" that translates human-readable domain names (e.g., `google.com`) into machine-readable IP addresses.
* **HTTP / HTTPS:** The protocol for transferring web documents. HTTPS uses TLS/SSL encryption to secure data in transit.
* **Routers & Switches:**
* **Switch:** Connects devices within the same local network (LAN).
* **Router:** Connects multiple different networks together (e.g., LAN to the WAN/Internet).



---

## 8. Programming

The process of writing instructions that a computer can interpret and execute.

* **Compiled vs. Interpreted:**
* **Compiled (e.g., C++, Rust):** Code is converted directly into machine code before execution, resulting in higher speed.
* **Interpreted (e.g., Python, JavaScript):** Code is read and executed line-by-line by an interpreter at runtime.


* **Paradigm Concepts:**
* **Procedural:** Code structured around functions and sequential steps.
* **Object-Oriented (OOP):** Code organized into "Objects" containing state (properties) and behavior (methods).
* **Functional:** Code built around pure functions, avoiding shared state and mutable data.
