# Elastic SIEM Lab

The goal of my project was to independently set up and configure a robust security information and event management (SIEM) system using Elastic Stack on ARM architecture. My objective was to optimize log collection and transmission to the SIEM platform using Elastic Agents, while also refining my skills in security event analysis and threat detection. Additionally, I aimed to develop a custom dashboard within Elastic SIEM to visualize security events effectively and rigorously test alert rules for efficient threat response.

### Skills Learned

**Independent Setup and Configuration of Elastic Stack SIEM on ARM architecture:**
   - Developed proficiency in setting up and configuring complex software systems independently.
   - Demonstrated adaptability by navigating challenges specific to ARM architecture, showcasing problem-solving skills.
   - Exhibited self-motivated learning by mastering new concepts and technologies required for the setup.

**Implementation of Elastic Agents for Log Collection:**
   - Acquired skills in deploying and configuring Elastic Agents to collect and transmit logs efficiently.
   - Demonstrated understanding of data flow and optimization techniques to enhance security event monitoring.
   - Showcased ability to streamline processes for improved system performance and effectiveness.

**Generation and Analysis of Security Events:**
   - Gained hands-on experience in generating and analyzing security events, contributing to a deeper understanding of cybersecurity concepts.
   - Developed expertise in identifying patterns and anomalies within security data, essential for threat detection and response.
   - Enhanced knowledge of threat landscapes and mitigation strategies through practical application and analysis.

**Advanced Querying Techniques in Elastic SIEM:**
   - Leveraged advanced querying techniques within Elastic SIEM to proactively identify security incidents.
   - Developed proficiency in crafting complex queries to extract meaningful insights from large datasets.
   - Strengthened skills in network security monitoring and threat detection by effectively utilizing Elastic SIEM's querying capabilities.

**Development of Custom Dashboard and Testing Alert Rules:**
   - Demonstrated proficiency in data visualization and interpretation by developing a custom dashboard in Elastic SIEM.
   - Showcased skills in pattern recognition and data analysis through the design of visually intuitive security event representations.
   - Rigorously tested alert rules to ensure optimal threat response efficiency, showcasing attention to detail and commitment to system reliability.

### Tools Used

- Elastic Security Information and Event Management (SIEM) system for log ingestion and analysis.
- UTM Hypervisor for ARM64 processors.
- Kali Linux to host the Elastic Agent and produce network activity.

## Steps (This is an ARM based tutorial)

1. Setup

   -UTM Hypervisor Installation
      - First and foremost we will need a hypervisor to download the elastic agent to.
      - We are using the UTM Hypervisor for ARM Architecture CPUs go to the link provided and select "Download" on the left hand side https://mac.getutm.app/. <img width="1512" alt="Screenshot 2024-02-26 at 5 12 28 PM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/defc37b0-c742-4bcf-a2d5-e1f40d7f5374">
      - After it has finished downloading, open the file and run the installation agent and install the application
      - Now we need a linux distro to use as our host for elastic agent.
      - Open UTM and select Browse UTM Gallery and I selected Kali then select the "Download" button. If you would like to use your own ISO file, feel free to do so.
      - Once your ISO file is downloaded, double click it and it should extract a .utm virtual machine.
      - We are going to select "Create a New Virtual Machine" then select "Open" and select the .utm virtual machine.
      - This lab is not very intensive so you can keep the default Hardware settings.

-ElasticAgent Setup
      - Now we are going to start downloading ElasticAgent to the linux host machine.
  -ElasticAgent 
