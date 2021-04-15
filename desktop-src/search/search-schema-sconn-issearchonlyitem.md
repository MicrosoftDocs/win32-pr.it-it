---
description: L'elemento booleano <isSearchOnlyItem> specifica se il provider di ricerca supporta la modalità browse oltre alla modalità di ricerca. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Elemento isSearchOnlyItem (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525453"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Elemento isSearchOnlyItem (schema del connettore di ricerca)

L'elemento booleano <isSearchOnlyItem> specifica se il provider di ricerca supporta la modalità browse oltre alla modalità di ricerca. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
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

Il valore `true` indica che la posizione del connettore di ricerca non può essere esplorata dagli utenti. Il valore `false` indica che gli utenti possono esplorare il percorso del connettore di ricerca.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



