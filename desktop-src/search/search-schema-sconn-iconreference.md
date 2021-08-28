---
description: "&lt;L'elemento iconReference &gt; facoltativo specifica un'icona personalizzata per questo percorso. Questo elemento non ha attributi e nessun elemento figlio."
ms.assetid: c2fa5e99-a7fd-423e-9952-5233e8c83619
title: Elemento iconReference (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ff41d6dfd37e5e3fe780171701886b08b195ac
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882415"
---
# <a name="iconreference-element-search-connector-schema"></a>Elemento iconReference (schema del connettore di ricerca)

&lt;L'elemento iconReference &gt; facoltativo specifica un'icona personalizzata per questo percorso. Questo elemento non ha attributi e nessun elemento figlio.

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

Il formato del riferimento deve essere specificato in un formato adatto per la [funzione PathParseIconLocation,](/windows/desktop/api/shlwapi/nf-shlwapi-pathparseiconlocationa) ad esempio <dll file name> , <icon index> .

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <iconReference>example.dll,-1002</iconReference>
    ...
</searchConnectionDescription>
```



 

 
