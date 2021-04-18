---
description: L' <scope> elemento facoltativo specifica una raccolta di <scopeItem> elementi che definiscono le inclusioni e le esclusioni dell'ambito per questo particolare connettore di ricerca.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento Scope (Schema connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f49041170db80de48d312596249d5c4dca835e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306077"
---
# <a name="scope-element-search-connector-schema"></a>Elemento Scope (Schema connettore di ricerca)

L' <scope> elemento facoltativo specifica una raccolta di <scopeItem> elementi che definiscono le inclusioni e le esclusioni dell'ambito per questo particolare connettore di ricerca. Se <scope> è presente, deve contenere almeno un <scopeItem> elemento. Questo elemento non ha attributi.

## <a name="syntax"></a>Sintassi


```
<!-- scope -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                       ...
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                                                   | Elementi figlio                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [elemento scopeItem (schema del connettore di ricerca)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Commenti

Usare gli <scope> <scopeItem> elementi e per identificare i percorsi in cui eseguire la ricerca e quali percorsi devono essere esclusi dalla ricerca.

## <a name="example"></a>Esempio

Nell'esempio seguente viene illustrato un ambito di ricerca che include C: \\ ExampleFolder e tutte le relative cartelle figlio ad eccezione di c: \\ ExampleFolder \\ ExcludeMe.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



