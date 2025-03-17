# NIST-CSF-Security-Incident-Response

## Introduction
This mock security incident report was created as part of the **Cybersecurity Documentation Portfolio** for the **Google Coursera Cybersecurity Certificate**. The aim of this project is to deepen the understanding of network vulnerabilities and demonstrate how the **NIST Cybersecurity Framework (CSF)** can be applied in real-world scenarios to secure and respond to network-level incidents.

## Scenario
You are a cybersecurity analyst working for a multimedia company that provides web design, graphic design, and social media marketing services to small businesses. Recently, the company experienced a **DDoS (Distributed Denial-of-Service)** attack that disrupted the internal network for two hours. The attack flooded the network with a large volume of **ICMP (Internet Control Message Protocol)** packets, which caused the network services to go offline.

The incident management team responded by **blocking incoming ICMP packets**, disabling non-critical network services, and restoring essential services to regain network access.

After the attack, a deeper investigation by the cybersecurity team revealed that an **unconfigured firewall** allowed the attack to flood the network. The malicious actor used this vulnerability to perform the DDoS attack.

The team then implemented a series of measures to prevent future incidents:
- A new firewall rule to **limit incoming ICMP packets**.
- **Source IP address verification** on the firewall to block spoofed IP addresses.
- **Network monitoring tools** to detect abnormal traffic.
- An **IDS/IPS system** to filter suspicious ICMP traffic.

## Objective
This report aims to use the **NIST Cybersecurity Framework (CSF)** to analyze and improve the company’s network security postures. The CSF’s five core functions—**Identify**, **Protect**, **Detect**, **Respond**, and **Recover**—will be applied to assess the incident and develop a comprehensive security strategy.

The following steps will focus on aligning the company’s incident response and overall security posture with the NIST CSF.

## Incident Report Analysis

### Summary
Recently, the company experienced a **DDoS attack**, causing the company’s network services to be unavailable for two hours. After the company’s cybersecurity team investigated the security event, they found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a DDoS attack.

### NIST CSF Phases

| Phase       | Description                                                                                                                                                        |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Identify** | The attack involved the flood of ICMP packets to the network, which ended up overwhelming it and causing disruption. The entire internal network was affected. |
| **Protect**  | The cybersecurity team implemented a new firewall rule to limit the rate of ICMP packets, and an IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics to harden the network against DDoS attacks. |
| **Detect**   | The cybersecurity team configured source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets and implemented network monitoring software to detect abnormal traffic patterns. |
| **Respond**  | The team acted quickly to contain the DDoS attack by blocking incoming ICMP packets and taking non-critical network services offline, which allowed them to restore business operations. A thorough root cause analysis was conducted to determine how the attacker exploited the unconfigured firewall to bypass security measures. To improve the response process, the team developed and tested incident response protocols for similar attacks, ensuring they could react more swiftly in the future. They also automated traffic filtering and mitigation techniques for DDoS attacks, such as rate-limiting and IP blocking, to quickly deploy emergency security measures during a future attack. |
| **Recover**  | To recover from an ICMP flood DDoS attack, the first step is to restore normal access to critical network services. For future incidents, external ICMP flooding attacks will be blocked at the firewall level, and non-essential services will be temporarily suspended to manage network load. Once the flooding traffic subsides, the recovery process will involve gradually bringing all services back online, starting with the critical systems, and finally restoring the non-essential ones. |

## Notes
This was a challenging yet insightful exercise. One of the main takeaways was the importance of **effective firewall configuration** and **real-time network monitoring** to detect and prevent such attacks. I learned the value of each phase of the **NIST Cybersecurity Framework** and how it can be leveraged to improve security operations and response times.

Another area of improvement would be to schedule regular **penetration testing exercises** to evaluate the security posture of the organization, ensuring that all defenses are effective and that the network is resilient to potential attacks.

### Key References:
- [Understanding and Responding to Distributed Denial-of-Service Attacks](https://www.cisa.gov/sites/default/files/publications/Understanding_and_Responding_to_Distributed_Denial_of_Service_Attacks.pdf)
- [NIST Cybersecurity Framework Overview](https://www.nist.gov/cyberframework)

## Reflections
I found this exercise both challenging and rewarding. Documenting each phase of the NIST Cybersecurity Framework helped me gain a better understanding of how to manage and respond to incidents. Although I initially struggled to create clear and concise documentation, I now feel confident that my approach is close to the example provided. In the future, I plan to improve my writing for clarity and make sure I explain each phase more smoothly.

I also want to explore ways to use automated systems to respond faster during incidents and find better ways to connect incident response plans with existing business continuity strategies.

