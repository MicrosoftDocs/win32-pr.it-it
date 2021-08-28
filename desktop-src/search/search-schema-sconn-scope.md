---
description: L'elemento scope facoltativo specifica una raccolta di elementi scopeItem che definiscono le inclusioni e le esclusioni dell'ambito &lt; &gt; per questo particolare &lt; &gt; connettore di ricerca.
ms.assetid: 9e92e3db-3d5e-4f86-8d67-90eb5469b04b
title: Elemento scope (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c011eee8def80a7f1d395a7a52a72d30fb4935
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886693"
---
# <a name="scope-element-search-connector-schema"></a>Elemento scope (schema del connettore di ricerca)

L'elemento scope facoltativo specifica una raccolta di elementi scopeItem che definiscono le inclusioni e le esclusioni dell'ambito &lt; &gt; per questo particolare &lt; &gt; connettore di ricerca. Se &lt; scope &gt; è presente, DEVE contenere almeno un &lt; elemento &gt; scopeItem. Questo elemento non ha attributi.

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

Usare gli elementi scope e scopeItem per identificare i percorsi in cui eseguire la ricerca &lt; e i percorsi da escludere dalla &gt; &lt; &gt; ricerca.

## <a name="example"></a>Esempio

L'esempio seguente illustra un ambito di ricerca che include C: ExampleFolder e tutte le cartelle figlio ad \\ eccezione di C: \\ ExampleFolder \\ ExcludeMe.


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



 

 



