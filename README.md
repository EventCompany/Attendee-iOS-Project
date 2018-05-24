# Attendee-iOS-Project
Event Attendee
The SAP Event Attendee app is a community project licensed under Apache License Version 2.0. The app provides organizers of SAP community events a platform for the participant registration. It's running already in production using the SAP Mentors SAP Cloud Platform Account sponsored by SAP IT.

# Public Participant List
Participant Registration (SCN Account required)
Organizer Backend (Additional authorization required)
Receptionist

If you're organizing a SAP community event please reach out to Gregor Wolf to get access to the Organizer Backend. A more detailed description can be found in How to create a SIT registration form with the SAP Event Registration App?. If you want to contribute please check the open issues, fork the project and start coding.

This repository contains the backend for the SITreg app. It is developed on SAP HANA XS Classic (XSC) using mainly XSODATA to expose an OData API. For more details check out the information in the Wiki. You can find the frontend projects here:

SITRegParticipantList
SITregParticipant
SITregReceptionist
SITregOrganizer
Setup Guide
In addition to the following expert guide you can check out the setup guide in the Wiki.

# Backend
You must have developer authorization in your HANA System. To try this project just spin up your own HANA Multitennant Database Container (MDC) on the HANA Cloud Platform Trial (HCP). Open the SAP HANA Web-based Development Workbench and create the package:

com/sap/sapmentors/sitreg
After you've created the package right click on the sitreg package and choose Syncronize with GitHub. Provide your GitHub credentials to allow the HANA system to read your GitHub repositories. As you can't specify a GitHub repository URL you have to fork the project so you have it in your repository list. Then choose the cloned repository and GitHub branch master. Click Fetch to retreive the content. After that step you have to activate the artifacts. Try a right click activate all.

# To test the different services with the correct authorizations setup the users:

PARTICIPANT
ORGANIZER
COORGANIZER
RECEPTIONIST
SITREGADMIN
Assign the roles:

com.sap.sapmentors.sitreg.roles::participant (to PARTICIPANT)
com.sap.sapmentors.sitreg.roles::organizer (to ORGANIZER and COORGANIZER)
com.sap.sapmentors.sitreg.roles::receptionist (to RECEPTIONIST)
com.sap.sapmentors.sitreg.roles::admin (to SITREGADMIN)
to be able to test the different services also according the correct implementation of the authorizations.

