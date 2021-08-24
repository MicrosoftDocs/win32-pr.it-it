---
description: L'elemento booleano facoltativo specifica se la posizione descritta dal connettore di ricerca è indicizzata (in locale o in remoto usando Windows Search 4 o versione <isIndexed> successiva).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento isIndexed (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afcd1a95ec14b3bbea80374d8925a88231feb0110a421c2c850a297672d0c1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711051"
---
# <a name="isindexed-element-search-connector-schema"></a>Elemento isIndexed (schema del connettore di ricerca)

L'elemento booleano facoltativo specifica se la posizione descritta dal connettore di ricerca è indicizzata (in locale o in remoto usando Windows Search 4 o versione <isIndexed> successiva). Il valore predefinito è true per le cartelle locali. Questo elemento non ha elementi figlio e nessun attributo.

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



 

 



