---
description: "&lt;L'elemento url specifica un URL che rappresenta &gt; l'ambito del connettore di ricerca. Questo elemento non ha elementi figlio e nessun attributo."
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: Elemento url scopeItem (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a1db669f7365f04bed49c769ab695ab674b20b
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886708"
---
# <a name="scopeitem-url-element-search-connector-schema"></a>Elemento url scopeItem (schema del connettore di ricerca)

&lt;L'elemento url specifica un URL che rappresenta &gt; l'ambito del connettore di ricerca. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre                                                                   | Elementi figlio |
|----------------------------------------------------------------------------------|----------------|
| [Elemento scopeItem (schema del connettore di ricerca)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Commenti

Il valore può essere un percorso file system locale o un URL.

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



 

 



