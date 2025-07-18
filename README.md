# security-Groups-And-Nacls

During this project, well explore the core concepts of Amazon Web Services (AWS), specifically focusing on Security Groups and Network Access Control Lists (NACLs). Our objective is to understand these fundamental components of AWS infrastructure, including how Security Groups control inbound and outbound traffic to EC2 instances, and how NACLs act as subnet-level firewalls, regulating traffic entering and exiting subnets. Through practical demonstrations and interactive exercises, we'll navigate the AWS management console to deploy and managE these critical components effectively. 


# Project Goals: 

* Understand the concepts of Security Groups and Network Access Control Lists (NACLs) in AWS. 

* Explore how Security Groups and NACLs function as virtual firewalls to control inbound and outbound traffic. 

* Gain hands-on experience with configuring Security Groups and NACLs to allow or deny specific types of traffic. 

# Learning Outcome:

 * Gain proficiency in configuring Security Groups and NACLs to control network traffic within AWS environments. 

* Understand the differences between Security Groups and NACLs, including their scope, statefulness, and rule configurations. 

* Learn how to troubleshoot network connectivity issues by analyzing Security Group and NACL configurations. 

* Develop a deeper understanding of AWS networking concepts and best practices for securing cloud environments. 


# What is Security Group? 

Imagine you're hosting a big party at your house. You want to make sure only the people you invite can come in, and you also want to control what they can do once they're inside. 

AWS security groups are like bouncers at the door of your party. They decide who gets to come in (inbound traffic) and who gets kicked out (outbound traffic). Each security group is like a set of rules that tells the bouncers what's allowed and what's not. 

For example, you can create a security group for your web server that only allows traffic on port 80 (the standard port for web traffic) from the internet. This means only web traffic can get through, keeping your server safe from other kinds of attacks. 

Similarly, you can have another security group for your database server that only allows traffic from your web server. This way, your database is protected, and only your web server can access it, like a VIP area at your party. 

In simple terms, security groups act as barriers that control who can access your AWS resources and what they can do once they're in. They're like digital bouncers that keep your party (or your cloud) safe and secure. 

# What is NACL? 


NACL stands for Network Access Control List. Think of it like a security checkpoint for your entire neighborhood in the AWS cloud. Imagine your AWS resources are houses in a neighborhood, and you want to control who can come in and out. That's where NACLs come in handy. 

NACLs are like neighborhood security guards. They sit at the entrance and check every person (or packet of data) that wants to enter or leave the neighborhood. 

But here's the thing: NACLs work at the subnet level, not the individual resource level like security groups. So instead of controlling access for each house (or AWS resource), they control access for the entire neighborhood (or subnet). 

You can set rules in your NACL to allow or deny traffic based on things like IP addresses, protocols, and ports. For example, you can allow web traffic (HTTP) but block traffic on other ports like FTP or SSH. 

Unlike security groups, which are stateful (meaning they remember previous interactions), NACLs are stateless. This means you have to explicitly allow inbound and outbound traffic separately, unlike security groups where allowing inbound traffic automatically allows outbound traffic related to that session. 

In simple terms, NACLs act as gatekeepers for your AWS subnets, controlling who can come in and out based on a set of rules you define. They're like the security guards that keep your neighborhood (or your AWS network) safe and secure. 

# Difference between Security Groups and NACL 


Security Groups in AWS act like virtual firewalls that control traffic at the instance level. They define rules for inbound and outbound traffic based on protocols, ports, and IP addresses. Essentially, they protect individual instances by filtering traffic, allowing only authorized communication. 

On the other hand, Network Access Control Lists (NACLs) function at the subnet level, overseeing traffic entering and leaving subnets. They operate as a barrier for entire subnets, filtering traffic based on IP addresses and protocol numbers. Unlike security groups, NACLs are stateless, meaning they don't remember the state of the connection, and each rule applies to both inbound and outbound traffic independently. 

Note- In security groups, there's no explicit "deny" option as seen in NACLs; any rule configured within a security group implies permission, meaning that if a rule is established, it's automatically allowed. 


: LETS COME TO THE PRACTICAL PART,

THIS PRATICAL WILL BE TWO PART 

1 - SECURITY GROUP
2 - NACL

# Security group 

* Initially We'll examine the configuration of inbound and outbound rules for security groups. 

* Create a security group allowing HTTP for all traffic and attach it to the instance. 

# explore various scenarios:  

* Implement inbound traffic rules for HTTP and SSH protocols and allow outbound traffic for all. 

* Configure inbound rules for HTTP with no outbound rules. Remove both inbound and outbound rules. Have no inbound rules but configure outbound rules for all traffic. 

# NACL 

* Examine the default settings for both inbound and outbound rules in NACL configuration. 

* Modify the inbound rules to permit traffic from any IPv4 CIDR on all ports.

* Adjust the outbound rules to allow traffic to all CIDRs. 


