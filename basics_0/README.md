
# **Bash Networking Script Project**

## **Project Overview**
This project involves creating Bash scripts to solve a variety of networking tasks. The focus is on using Bash to interact with network utilities, handle user inputs, and produce robust outputs. Each task has specific requirements, such as checking connectivity, listing network ports, and handling different conditions.

---

## **Project Tasks**

### **1. Display Listening Ports**
- **Objective:** Create a script to display all listening sockets on the system.
- **Requirements:**
  - Only show listening sockets.
  - Include the PID and program name associated with each socket.

#### **Example Usage:**
```bash
./1-display_listening_ports.sh
```

#### **Expected Output:**
```text
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 *:ssh                   *:*                     LISTEN      1240/sshd
udp        0      0 *:bootpc                *:*                                 562/dhclient

Active UNIX domain sockets (only servers)
Proto RefCnt Flags       Type       State         I-Node PID/Program name    Path
unix  2      [ ACC ]     STREAM     LISTENING     8559   835/dbus-daemon     /var/run/dbus/system_bus_socket
```

---

### **2. Ping a Host**
- **Objective:** Create a script that pings a given IP address to check if it is reachable.
- **Requirements:**
  - Accept the IP address as an argument.
  - If no argument is provided, display a usage message.
  - Ping the IP address 4 times.

#### **Example Usage:**
```bash
./2-ping_host.sh 8.8.8.8
```

#### **Expected Output:**
```text
PING 8.8.8.8 (8.8.8.8): 56 data bytes
64 bytes from 8.8.8.8: icmp_seq=0 ttl=118 time=15.4 ms
...
--- 8.8.8.8 ping statistics ---
4 packets transmitted, 4 packets received, 0% packet loss
round-trip min/avg/max/stddev = 15.4/15.6/15.8/0.2 ms
```

---

### **3. Validate IP Address Format**
- **Objective:** Write a script to validate whether a given string is a valid IPv4 address.
- **Requirements:**
  - Accept a string as an argument.
  - Display `Valid IP` or `Invalid IP` based on the input.

#### **Example Usage:**
```bash
./3-validate_ip.sh 192.168.1.1
Valid IP
./3-validate_ip.sh 300.300.300.300
Invalid IP
```

---

### **4. Display Active Connections**
- **Objective:** List all active connections on the system.
- **Requirements:**
  - Show all active connections for TCP and UDP protocols.
  - Include the local address, foreign address, and connection state.

#### **Example Usage:**
```bash
./4-active_connections.sh
```

#### **Expected Output:**
```text
Proto Recv-Q Send-Q Local Address           Foreign Address         State
tcp        0      0 192.168.1.10:ssh        192.168.1.1:49320       ESTABLISHED
udp        0      0 192.168.1.10:ntp        0.0.0.0:*               LISTEN
```

---

### **5. Ping an IP Address**
- **Objective:** Ping an IP address passed as an argument.
- **Requirements:**
  - Accept a string as an argument.
  - Display a usage message if no argument is provided.
  - Ping the IP address 5 times.

#### **Example Usage:**
```bash
./5-is_the_host_on_the_network 8.8.8.8
```

#### **Expected Output:**
```text
PING 8.8.8.8 (8.8.8.8): 56 data bytes
64 bytes from 8.8.8.8: icmp_seq=0 ttl=116 time=10.3 ms
...
--- 8.8.8.8 ping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss
```

---

## **Setup and Usage**

### **Make Scripts Executable**
To use the scripts, give them executable permissions:
```bash
chmod +x 1-display_listening_ports.sh 2-ping_host.sh 3-validate_ip.sh 4-active_connections.sh 5-is_the_host_on_the_network
```

### **Run the Scripts**
Run each script with the appropriate arguments (if required):
```bash
./script_name.sh [ARGUMENTS]
```

---

## **Learning Objectives**
- Learn how to create and execute Bash scripts.
- Use network utilities (`ping`, `netstat`, `ss`) in scripts.
- Handle user input validation and error messages.
- Display formatted outputs for better readability.

---

## **Project Files**

| File Name                     | Description                                           |
|-------------------------------|-------------------------------------------------------|
| `1-display_listening_ports.sh`| Displays all listening ports on the system.           |
| `2-ping_host.sh`              | Pings a given IP address to check connectivity.       |
| `3-validate_ip.sh`            | Validates whether a string is a valid IPv4 address.   |
| `4-active_connections.sh`     | Lists all active TCP and UDP connections.             |
| `5-is_the_host_on_the_network`| Pings an IP address 5 times with user input handling. |

---

## **Prerequisites**
- A Linux-based system with Bash installed.
- Basic knowledge of networking concepts and utilities.
- The `ping`, `netstat`, and `ss` commands available on your system.

---

## **Future Improvements**
- Add more robust validation for user inputs.
- Support IPv6 in addition to IPv4 for tasks.
- Include options for customizing script behavior (e.g., number of pings).

---

## **Author**
This project is designed to improve Bash scripting and networking skills. The tasks demonstrate practical uses of network commands in scripting environments.
