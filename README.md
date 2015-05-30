# Guide for Test Based Certification Tools

Authors: Filippo Gaudenzi

Dipartimento di Informatica Università degli Studi di Milano Crema, Italy, 26013


This repositories hosts CMs to be used on the the prototype availabe as explained in D3.3 Annex.

TestManager and TestAgent are available as VMs on the UMIL ftp repository.
Follow the guide on the annex to make them run.

Once the whole system is up and running is possible to use the CMs here available, to see how advance certification process are managed and executed.

The three type of advanced certifications hosted here are:
	- Hybrid Certification
	- Composition of Certificates
	- Incremental Certification

Please, in order to interact with the TestManager SOAP interface, use Firefox and install SOA Client (https://addons.mozilla.org/it/firefox/addon/soa-client/). To connect to Test Manager Interface set the WSDL address as http://<testmanagerIP>:8080/CumulustestManager-0.0.1-SNAPSHOT/services/TestManagerAPI?wsdl. If evertything is fine you should see a dashboard as in Figure 1:

![alt text](https://raw.githubusercontent.com/fgaudenzi/TBprototypeInstallation/master/Others/SOA.png "Figure 1")Figure 1


The Test Manager comes alredy with 2 certificate stored in its Database. Both Certificate refers to the same proprety "Storage-confidentiality" and address two OpenStack deployment hosted at Unimi. The related CM are at:
	[Openstack 1](https://raw.githubusercontent.com/fgaudenzi/TBprototypeInstallation/master/OpenStack1.xml)
	[Openstack 2](https://raw.githubusercontent.com/fgaudenzi/TBprototypeInstallation/master/OpenStack1.xml)
Openstack 1 satisfys the property, indeed the Certificate is in ISSUED state. 
	It is possible to check it running the operation 6 : getCertificate_Testing from the SOA Client using as ID=1432910969401
Openstack 2 doesn't satisfy the property, and its certificate is in REVOKED state.
	It is possible to check it running the operation 6 : getCertificate_Testing from the SOA Client using as ID=1432911193779


## Hybrid Certification