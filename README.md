# Networking_concepts


# 🌐 Network Infrastructure & Protocol Fundamentals

A comprehensive guide to understanding how data moves across the web, from low-level routing to high-level application protocols.

---

## 🏗️ 1. The Foundation: TCP/IP Stack
To understand networking, you must understand the **TCP/IP Model**, which dictates how data is packetized, addressed, transmitted, routed, and received.

### Key Layers:
* **Link Layer:** Physical hardware (Ethernet, Wi-Fi).
* **Internet Layer (IP):** Handles host addressing and packet routing (**IPv4/IPv6**).
* **Transport Layer (TCP/UDP):** Manages host-to-host communication.
    * **TCP (Transmission Control Protocol):** Connection-oriented, ensures data arrives intact and in order (Three-way handshake).
    * **UDP (User Datagram Protocol):** Connectionless, faster but "fire and forget" (Streaming, Gaming).
* **Application Layer:** Where **HTTP, DNS, and FTP** reside.



---

## 🚦 2. Network Routing
Routing is the process of selecting a path for traffic in a network or between or across multiple networks.

* **IP Addressing:** Every device needs a unique identifier.
* **Subnetting:** Segmenting a large network into smaller, manageable pieces for security and performance.
* **Routers:** Devices that forward data packets between computer networks. They use **Routing Tables** to decide the best path.
* **Gateways:** The "exit point" for a network to talk to the outside world (the Internet).

---

## ⚖️ 3. Load Balancing
Load balancing ensures that no single server bears too much demand. By spreading the work, you improve responsiveness and availability.

### Types of Load Balancers:
1.  **L4 Load Balancer (Transport Layer):** Routes traffic based on IP and Port. It doesn't "look" at the data inside the packet. Fast and efficient.
2.  **L7 Load Balancer (Application Layer):** Routes traffic based on the content of the request (URL paths, HTTP headers, Cookies). Ideal for microservices.



### Algorithms:
* **Round Robin:** Sequential distribution.
* **Least Connections:** Sends traffic to the server with the fewest active sessions.
* **IP Hash:** Uses the client's IP to ensure they always hit the same server (Sticky Sessions).

---

## 🔍 4. DNS (Domain Name System)
DNS is the "Phonebook of the Internet." It translates human-readable names (www.google.com) into machine-readable IP addresses (142.250.190.46).

**The Lookup Process:**
1.  **Recursive Resolver:** Your ISP's server that starts the search.
2.  **Root Nameserver:** Directs the query to the correct TLD (.com, .org).
3.  **TLD Nameserver:** Points to the Authoritative Nameserver.
4.  **Authoritative Nameserver:** Holds the final IP mapping.



---

## 📄 5. HTTP (Hypertext Transfer Protocol)
The protocol of the World Wide Web. It is an application-layer protocol sent over TCP.

* **Statelessness:** Each request is independent. (This is why we use Cookies/Tokens for sessions).
* **Verbs:** `GET` (Retrieve), `POST` (Create), `PUT` (Update), `DELETE` (Remove).
* **Status Codes:**
    * `2xx`: Success
    * `3xx`: Redirection
    * `4xx`: Client Error (e.g., 404 Not Found)
    * `5xx`: Server Error (e.g., 500 Internal Server Error)
* **HTTPS:** HTTP + **TLS/SSL** encryption. It ensures that the data sent between the browser and server is encrypted and secure.

---

## 🛠️ Summary Checklist for DevOps/SRE
- [ ] Understand the **3-way Handshake** (SYN, SYN-ACK, ACK).
- [ ] Know the difference between **Public vs. Private IPs**.
- [ ] Understand **TTL (Time to Live)** in DNS records.
- [ ] Differentiate between **Health Checks** and **Load Balancing**.
