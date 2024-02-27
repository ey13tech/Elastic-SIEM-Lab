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

   - UTM Hypervisor Installation
      - First and foremost we will need a hypervisor to download the elastic agent to.
      - We are using the UTM Hypervisor for ARM Architecture CPUs go to the link provided and select "Download" on the left hand side https://mac.getutm.app/. <img width="1512" alt="Screenshot 2024-02-26 at 5 12 28 PM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/defc37b0-c742-4bcf-a2d5-e1f40d7f5374">
      - After it has finished downloading, open the file and run the installation agent and install the application
      - Now we need a linux distro to use as our host for elastic agent.
      - Open UTM and select Browse UTM Gallery and I selected Kali then select the "Download" button. If you would like to use your own ISO file, feel free to do so.
      - Once your ISO file is downloaded, double click it and it should extract a .utm virtual machine.
      - We are going to select "Create a New Virtual Machine" then select "Open" and select the .utm virtual machine.
      - This lab is not very intensive so you can keep the default Hardware settings.

   - ElasticAgent Setup
      - Now we are going to start downloading ElasticAgent to the linux host machine.
      - Go ahead and follow the link provided to the Elastic website and create an account https://cloud.elastic.co/login?redirectTo=%2Fdeployments%2Fcreate
      - You should see a "Create your first deployment" screen <img width="1512" alt="Screenshot 2024-02-27 at 8 11 42 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/36a3050b-c01f-41ee-899c-2c34b57d6553">
      - We will leave the settings for this deployment as default.
      - After it is prepared we will select "Continue" then select explore on your own at the bottom of the page
      - We are going to click on the three stacked lines in the top left then select "Add Integrations" on the bottom <img width="1512" alt="Screenshot 2024-02-27 at 8 21 48 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/961830d4-e402-4a0b-b4f7-ea53fa62eb4c">
      - We are going to add "Elastic Defend" so select that option. If it is not present use the search bar at the top to find it. Now we will select "Add Elastic Defend." <img width="1512" alt="Screenshot 2024-02-27 at 8 23 36 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/90ca454f-8993-44aa-8afc-498bc8939799">
      - Now select "Install Elastic Agent at the bottom of the screen.<img width="1512" alt="Screenshot 2024-02-27 at 8 24 48 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/932c99c3-0173-4e10-958a-82e92ea1c851">
      - You should now see a Linux Tar code. We need to alter it so it is able to be used by ARM architecture.
      - This is what yours will look like after altering. I swapped every instance of "x86_" with "arm".
     

        <img width="301" alt="Screenshot 2024-02-27 at 8 37 52 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/02758196-e79d-44d2-a2a9-ccd24fa63e59">
       - Now we will paste the altered code into our virtual machines terminal. Wait for the download to finish and it should prompt you with a message in the screenshot below
         <img width="1277" alt="Screenshot 2024-02-27 at 8 41 33 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/616bacf0-57ec-4876-ab55-9f463093dc31">
       -  Also the elastic agent webpage should have updated and confirm the agents enrollment.
         <img width="1512" alt="Screenshot 2024-02-27 at 8 43 11 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/b950a711-ec7e-4846-ade1-957b8d99a8a2">
       - Now we will select "Add the integration," then "Confirm incoming data." After doing so, it will send information to the host to confirm the reception of data.
         <img width="1512" alt="Screenshot 2024-02-27 at 8 48 28 AM" src="https://github.com/ey13tech/Elastic-SIEM-Lab/assets/117955695/8bad51fa-df2e-4346-b458-7d074a7f59e2">
       - Now we are ready to start analyzing data, creating data visualization, and creating alerts.


       

         
         
