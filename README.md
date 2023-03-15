# Iamza Digital id Online Documents Repository

The following will be used as a convenient scratch pad so share some information with the larger Digital Identity Project for South Africa.

As a start in the sub folders are the  Schema ID and Credential Definition ID's for the Cornerstone Identity followed by the Address, Vaccine credential, Savings account credential and the Mobile phone/Sim card RICA credentials.

The entire IAMZA (Digital Identity South Africa) Sandbox environment is build using the HyperLedger Aries, HyperLedger Indy and HyperLedger Ursa framework, which is a implimentation forllowing the concepts of the Self Sovrin Digital Identity (SSI).

The IAMZA stack uses AIP 1.0 (indy credentials) and URL message types instead of URI message types (https://github.com/hyperledger/aries-cloudagent-python/issues/1788#issuecomment-1142650753).

The Schema's and Credential definitions can be view using:
	https://indyscan.io/txs/SOVRIN_BUILDERNET/domain

    HyperLedger Aries: 
        https://github.com/hyperledger/aries
        https://github.com/hyperledger/aries-rfcs
        https://www.hyperledger.org/use/aries
    
    HyperLedger Indy: 
        https://hyperledger-indy.readthedocs.io/en/latest/
        https://www.hyperledger.org/category/hyperledger-indy
        https://github.com/hyperledger/indy-sdk
    
    HyperLedger Ursa: 
        https://github.com/hyperledger/ursa
        https://github.com/hyperledger/ursa-python
        https://wiki.hyperledger.org/display/ursa
        
        
## April 2023 Demo

Demo
 
Each participant to stand up:

	Issuers:
	Cornerstone ID credential issuer using common cornerstone id schema.
	Proof of Account Issuer using common proof of account schema.
  	Contactable -> + Proof of mobile device/account issuer using common Rica schema.

  	Verifier:
  	Each participant verifier enabled to verify creds based schema id's for:
               
        Required:
	  		cornerstone id credential,
    	  	proof of account credential,
    		proof of mobile device/account
               
    	Optional:
    		proof of address
    	
    	
Interaction 1.

                BankservAfrica issues a Cornerstone ID credential to holder A into whatever wallet Holder A uses.
 
Interaction 2.

                Holder A presents credential to fin institute A, which does a verification or identity,
                Fin institute A then issues an proof of account (bank account) credential to Holder A.
 
Interaction 3.  

                Holder A presents cornerstone id credential and proof of account (bank account) to Contactable (Telco Domain).           
                Contactable issues proof of mobile device/account credential.
               
Interaction 4.

                At this stage any of the other issuers (fin institutes, banks, Gary) can opt to verify the proof of mobile device, as a input for their records.
               
            
The above cycle can now be repeated with anyone else taking up any of the interaction points, with a new Holder and a new mobile credential agent (wallet) in play.

  
For this stage I left proof of address out.
Anyone has the option to be able to issue address credential (after cornerstone id cred verification) and/or verify address credential also.
 
At this stage if anyone wants to populate the photo attribute they can.
If at this stage anyone wants to display a picture contained in the photo attribute they can, but the lack of eiter is not critical for the demo.
 
At this stage all schema definitions and cred def's will be maintained on Sovrin TestNet.
Everyone will be provided with the Sovrin TestNet Genesis file address list.
 
Each issuer to be configured to point to IAMZA gov body endorser (BankservAfrica Endorser instance).
All Cred def definitions to be done by issuers. The defined cred def, based on the common schema def to then be passed to BSA to be endorsed after which BSA
hand it to Sovrin Test net to be written onto the ledger, after which BSA will pass the cred def id back to the requester, enabling the issuer to use the cred def id to issue credentials.


Additional technical detail will be added.