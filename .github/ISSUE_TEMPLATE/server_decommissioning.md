---
name: Server Decomissioning
about: Action workflow for decommissioning linux servers at IDC.
title: '<!-- A short title to the point -->'
labels: 'task'

---

# Decommissioning a Linux Server  

**Describe which server(s) is/are to be decommissioned and why**
<p>ID-Service Now: <input type="text" size="20" maxlength="40" name="ID-Number" value="ID-Number" /></p>  <!-- put the ID Number here -->
<!-- A clear and concise description of what the problem is. -->  

<!--The steps from confluence https://unibe-ch.atlassian.net/wiki/x/moU8Aw  are followed.  -->

>**Servername :** <!-- Servername to decommission -->  
>**FQDN:** <!-- FQDN -->  
>**IP:** <!-- IP -->  
>**Contact person:** <!-- Contact person -->  
>**Projectname:** <!-- Name of the project -->

**Screenshots**
<!-- If applicable, add screenshots to help explain your problem. -->

**Additional context**
<!-- Add any other context about the problem here. -->


# Action Items

- [ ] Pause system in [PRTG](https://idprtg.unibe.ch) indefinitely with a comment "marked for decommissioning"
- [ ] Revoke SSL certificate. Assignment group "ID - PKI" ID <!-- put the ID Number here -->
      <p>ID-Service Now: <input type="text" size="20" maxlength="40" name="ID-Number" value="ID-Number" /></p>  
- [ ] Delete DNS Entries (if possible), otherwise create a Ticket in Service Now to the assignment group "ID - Hostmaster" (Technikcal Service: DDI (DNS/DHCP/IP)) with the request to delete the Host entry:
         <p>ID-Service Now: <input type="text" size="20" maxlength="40" name="ID-Number" value="ID-Number" /></p>  
    **DNS list**
  > - [ ] <!-- <FQDN> and <IP> -->
  
  > - [ ] <!-- <FQDN> and <IP> -->  

  > - [ ] <!-- <FQDN> and <IP> -->

- [ ] Delete AD entry if server im AD (sssd auth)
- [ ] Delete PRTG entries
- [ ] Remove host from configuration management (Ansible) 
- [ ] Remove Database from configuration management (Ansible)
- [ ] Delete any email accounts
- [ ] Cancel Backup (Tape). Email to Büren, Peter (ID) <peter.vonbueren@unibe.ch> 
- [ ] In the Secret Server (if possible) delete (AKA deactivate) passwords and information that are no longer used. (https://idsecret.unibe.ch/SecretServer)
- [ ] Firewall-Rules: create a Ticket in Service Now to assignment group "ID - Security" (Technical Service: Firewalldienste) with Hostname/IP with the request to delete all firewall rules 
       <p>ID-Service Now: <input type="text" size="20" maxlength="40" name="ID-Number" value="ID-Number" /></p>   <!-- put the ID Number here -->
- [ ] Elasticsearch: create a Ticket in Service Now to assignment "ID - Security" (Technical Service: Elasticsearch) with the request to delete the host from elasticsearch. 
        <p>ID-Service Now: <input type="text" size="20" maxlength="40" name="ID-Number" value="ID-Number" /></p> <!-- put the ID Number here -->
- [ ] Check documentation to see if there are any references to other dependencies that need to be deleted
- [ ] Delete any documentation for the System
- [ ] Inform those responsible for the system and ask them to delete relevant documentation in their space in confluence.
- [ ] Database in PostgreSQL will also be deleted if it exists. 
- [ ] NAS configs will be deleted. Send a Email with the Servername and IP to Roland, Trummer <roland.trummer@unibe.ch> and wait the confirmation
- [ ] Shut down the system
- [ ] Delete the server:
  - [ ] a.) delete VM in vCenter, if VM cannot be deleted → create a Ticket to ESXI Team with the request to delete the server
  - [ ] b.) If hardware system → remove the disks, wipe them and pass them on correctly place (Dispose of in the container in the basement, where the electronic waste is), Check the inventory number and check the next steps with Lead SYS (disposal / Storage)

- [ ] Close decommissioning Ticket im Service now with status resolved


