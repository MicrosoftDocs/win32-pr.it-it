---
description: "&lt;L'elemento mode specifica se &gt; l'URL deve essere incluso o escluso dall'ambito del connettore di ricerca. I valori consentiti sono Include ed Exclude. Questo elemento non ha elementi figlio e nessun attributo."
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Elemento mode (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e096bb21d634da6107359c014b82f1b367aba1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886750"
---
# <a name="mode-element-search-connector-schema"></a>Elemento mode (schema del connettore di ricerca)

&lt;L'elemento mode specifica se &gt; l'URL deve essere incluso o escluso dall'ambito del connettore di ricerca. I valori consentiti sono `Include` e `Exclude`. Questo elemento non ha elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
                            </xs:all>
                        </xs:complexType>
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



| Elemento padre                                                                   | Elementi figlio |
|----------------------------------------------------------------------------------|----------------|
| [Elemento scopeItem (schema del connettore di ricerca)](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a>Commenti

Non è possibile cercare o esplorare un ambito escluso. È possibile annidare gli URL scopeItem. Ad esempio, è possibile includere un ambito padre e tutti i relativi elementi figlio tranne uno aggiungendo l'URL padre come incluso, con il valore di profondità Deep ed escludendo l'URL figlio.

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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



