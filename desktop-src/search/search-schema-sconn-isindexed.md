---
description: L'elemento booleano facoltativo <isIndexed> specifica se il percorso descritto dal connettore di ricerca è indicizzato (in locale o in remoto usando Windows Search 4 o versione successiva).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento SetIndex (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128495"
---
# <a name="isindexed-element-search-connector-schema"></a>Elemento SetIndex (schema del connettore di ricerca)

L'elemento booleano facoltativo <isIndexed> specifica se il percorso descritto dal connettore di ricerca è indicizzato (in locale o in remoto usando Windows Search 4 o versione successiva). Il valore predefinito è true per le cartelle locali. Questo elemento non ha elementi figlio e nessun attributo.

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



 

 



