REMOTE COMPUTER LABORATORY ACCESS FOR STUDENTS AND TEACHERS.

Project Overview.
    My end of course project was titled: design and implementation of a remote computer laboratory access for students and teachers. The objective being for students and teachers to access the computing laboratory in the faculty of engineering and technology in the university of Buea.

    This project aimed at overcoming the challengees faced by users in accessing physical computer laboratory, such as idle computer resources during non working hours, limited capacity of the laboratories, inability to acquire performant hardware or software required by students or lecturers.

Project Architecture
List of Cloud Services used:
- Cloud Compute Engine for creating virtual machines
-VPC Networking
        CLOUD Network Address Translation (NAT)
        Identity Aware Proxy
        Firewall Rules
-Authentication and Authorization
        Google groups for creating
-Boot Disk and LINUX Operating System.
-Network File Storage


SETUP
    COMPUTE ENGINE
    Create 4 virtual machine instances, with Ubuntu as their operating system.
    Turn off public IP address for all machines,but allow 

    NETWORKING
    Create 3 subnets: Student, Teeachers, Admin subnet.These subnets will contain the virtual machines created above.
    Configure firewall rule 

    Operating systems
    At the level of the operating system, configure the following services:
        XFCE4 for remote desktop protocol,
        NFS which is network file storage
        LDAP for centralized authentication
        Also download required software, in this case : VirtualBox, Vs code, setup Java development environment.
        setup one virtual machine in the admin subnet as both LDAP server and NFS server.


CREDENTIALS and ACCESS.

    gcloud compute start-iap-tunnel [virtual machine's id] 3389 --local-host-port=localhost:8080 --zone=[virtual machine's zone]
