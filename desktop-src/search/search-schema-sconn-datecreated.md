---
description: L' <dateCreated> elemento facoltativo identifica la data e l'ora in cui è stato creato il connettore di ricerca usando lo standard ISO 8601. Non ha elementi figlio e nessun attributo.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Elemento dateCreated (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750343"
---
# <a name="datecreated-element-search-connector-schema"></a>Elemento dateCreated (schema del connettore di ricerca)

L' <dateCreated> elemento facoltativo identifica la data e l'ora in cui è stato creato il connettore di ricerca usando lo standard ISO 8601. Non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Commenti

Il formato del valore di questo elemento segue lo standard ISO 8601. Un uso comune è uno dei seguenti:

-   \[Aaaa \] - \[ mm \] - \[ gg \] T \[ HH \] : \[ mm \] : \[ SS \] ± \[ HH \] : \[ mm \] ("1981-04-05T14:30:30-05:00")
-   \[AAAA \] \[ mm \] \[ gg \] T \[ HH \] \[ mm \] \[ SS \] Z ("19810405T193030Z")

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



