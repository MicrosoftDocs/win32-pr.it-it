---
description: L' <iconReference> elemento facoltativo specifica un'icona personalizzata per questa posizione. Questo elemento non ha attributi e nessun elemento figlio.
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Elemento iconReference (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c181efe3bb8ac04f08d4fa16016d3468af6f10c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525464"
---
# <a name="iconreference-element-search-connector-schema"></a>Elemento iconReference (schema del connettore di ricerca)

L' <iconReference> elemento facoltativo specifica un'icona personalizzata per questa posizione. Questo elemento non ha attributi e nessun elemento figlio.

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

Il formato del riferimento deve essere specificato in un formato appropriato per la funzione [PathParseIconLocation](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) : (ad esempio, <dll file name> , <icon index> ).

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
