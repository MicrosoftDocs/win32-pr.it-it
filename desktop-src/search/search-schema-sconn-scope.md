---
description: L'elemento facoltativo specifica una raccolta di elementi che definiscono le inclusioni e le esclusioni di <scope> ambito per questo particolare <scopeItem> connettore di ricerca.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento scope (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d5fcdb3908f495d07199c61a2005a4f97ba5a01c641fb4e854961489e7abe0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944301"
---
# <a name="scope-element-search-connector-schema"></a>Elemento scope (schema del connettore di ricerca)

L'elemento facoltativo specifica una raccolta di elementi che definiscono le inclusioni e le esclusioni di <scope> ambito per questo particolare <scopeItem> connettore di ricerca. Se <scope> è presente, DEVE contenere almeno un <scopeItem> elemento. Questo elemento non ha attributi.

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
| [Elemento searchConnectorDescriptionType (schema del connettore di ricerca)](search-schema-searchconnectordescription.md) | [Elemento scopeItem (schema del connettore di ricerca)](search-schema-sconn-scopeitem.md). |



 

## <a name="remarks"></a>Commenti

Usare gli elementi e per identificare i percorsi da cercare <scope> e i percorsi da escludere dalla <scopeItem> ricerca.

## <a name="example"></a>Esempio

L'esempio seguente illustra un ambito di ricerca che include C: ExampleFolder e tutte le relative cartelle \\ figlio ad eccezione di C: \\ ExampleFolder \\ ExcludeMe.


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



 

 



