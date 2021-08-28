---
description: "&lt;L'elemento booleano isSearchOnlyItem specifica se il provider di ricerca supporta la &gt; modalità browse oltre alla modalità di ricerca. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo."
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Elemento isSearchOnlyItem (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524a69198a650e0cb995d2ff8b4fc942ebfdaddc
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883416"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a>Elemento isSearchOnlyItem (schema del connettore di ricerca)

&lt;L'elemento booleano isSearchOnlyItem specifica se il provider di ricerca supporta la &gt; modalità browse oltre alla modalità di ricerca. Questo elemento è facoltativo e non ha elementi figlio e nessun attributo.

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

Il valore indica che il percorso del connettore di ricerca `true` non può essere esplorato dagli utenti. Il valore `false` indica che gli utenti possono esplorare la posizione del connettore di ricerca.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



