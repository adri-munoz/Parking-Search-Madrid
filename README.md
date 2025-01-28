# Parking-Search-Madrid

# Overview

Parking Search Madrid is an iOS application that helps users find street and garage parking spots in Madrid, focusing primarily on the ZBEDEP (Zero/Low Emissions Zone) area.

As you cannot park on the street within the ZBEDEP area unless you have a special permit, the app enables the user to find the closest garages or closest streets (outside the ZBEDEP) to a searched location.

The app also enables to save records of the parking tickets obtained during parking in a garage for future reference and appeal a penalty in case the parking record is not properly processed by the government.

# Resources

- **Zona ZBEDEP** https://servpub.madrid.es/IDEAM_WBGEOPORTAL/dataset.iam?id=ab7bf756-1234-488f-9395-f2b37baeaebc
- **Calles Aparcamiento** https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=4973b0dd4a872510VgnVCM1000000b205a0aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default
- **Parkings Públicos** https://datos.madrid.es/egob/catalogo/202625-0-aparcamientos-publicos.json

# Current Implementation Details

- Uses MapKit for the map display with a visualization overlay of the ZBEDEP area
- ZBEDEP area is parsed from a binary created from the data available [here](https://servpub.madrid.es/IDEAM_WBGEOPORTAL/dataset.iam?id=ab7bf756-1234-488f-9395-f2b37baeaebc)
- Street locations are queried from a .db file created from the data available [here](https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=4973b0dd4a872510VgnVCM1000000b205a0aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default)
- Parkings are fetched via MapKit
- Uses SwiftData to store ParkingRecords