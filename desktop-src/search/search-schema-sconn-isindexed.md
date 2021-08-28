---
description: L'elemento booleano facoltativo isIndexed specifica se la posizione descritta dal connettore di ricerca è indicizzata (in locale o in remoto usando Windows Search 4 o versione &lt; &gt; successiva).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento isIndexed (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3588d451631ab8d0bb8313092b5b1ee7bb5c9dc4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881843"
---
# <a name="isindexed-element-search-connector-schema"></a>Elemento isIndexed (schema del connettore di ricerca)

L'elemento booleano facoltativo isIndexed specifica se la posizione descritta dal connettore di ricerca è indicizzata (in locale o in remoto usando Windows Search 4 o versione &lt; &gt; successiva). Il valore predefinito è true per le cartelle locali. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
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



 

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



