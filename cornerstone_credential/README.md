# Iamza Digital id Online Documents Repository

The following will be used as a convenient scratch pad so share some information with the larger Digital Identity Project for South Africa.

As a start below is the Schema ID and Credential Definition ID's for the Cornerstone Identity.

The Sandbox Issuer Agent / environment can be access via the web at 

   The Issuer requires a valid South African ID number (ID Check is performed), in future this will be verified by a call to South Africal Department of Home Affairs (DHA), but for now we are using a "fake" DHA API, as such the ID number is required to be pre entered into our database. Please send ID Number, Name & Surname to George Leonard at georgel@bankservafrica.com to be entered.

   Live Issuer:    https://issuer.iamza-sandbox.com/
   Live verifier: https://verifier.iamza-sandbox.com/


   ## Cornerstone Credential

        -- Schema ID
           BER7WwiAMK9igkiRjPYpEp:2:Cornerstone_Credential:2.1

        -- Credential Definition ID
           BER7WwiAMK9igkiRjPYpEp:3:CL:52285:IAMZA Cornerstone Credential

        -- As Per Sovrin
           https://indyscan.io/tx/SOVRIN_BUILDERNET/domain/52285


   ## Cornerstone ID Credential, Address Credential & Vaccine Credential Veriffier Code Location
      
      https://github.com/bsaiamza/cornerstone-verifier
