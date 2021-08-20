---
description: <iconReference>L'elemento facoltativo specifica un'icona personalizzata per questo percorso. Questo elemento non ha attributi e nessun elemento figlio.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Elemento iconReference (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76391eb7079414abe13c4e45696ee3eacb3b968eb93b342b1b9e67825fac85c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862586"
---
# <a name="iconreference-element-search-connector-schema"></a>Elemento iconReference (schema del connettore di ricerca)

<iconReference>L'elemento facoltativo specifica un'icona personalizzata per questo percorso. Questo elemento non ha attributi e nessun elemento figlio.

## <a name="syntax"></a>Sintassi


```
<!-- iconReference -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
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

Il formato del riferimento deve essere specificato in un formato adatto per la [funzione PathParseIconLocation:](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) (ad esempio, <dll file name> , <icon index> ).

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
