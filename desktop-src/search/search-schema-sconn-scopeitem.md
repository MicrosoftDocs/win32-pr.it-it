---
description: "&lt;L'elemento scopeItem &gt; rappresenta una singola voce nella tabella dell'ambito di esclusione/inclusione."
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Elemento scopeItem (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a585acd065efcbc58091d4c8bebce733ed2c73
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880450"
---
# <a name="scopeitem-element-search-connector-schema"></a>Elemento scopeItem (schema del connettore di ricerca)

&lt;L'elemento scopeItem &gt; rappresenta una singola voce nella tabella dell'ambito di esclusione/inclusione. &lt;scopeItem estende il tipo shellLinkType standard aggiungendo tre nuovi elementi che controllano l'inclusione e l'esclusione di cartelle, controllano la profondità dei risultati e specificano la posizione &gt; dell'ambito. Se &lt; &gt; l'elemento scope esiste, questo elemento è obbligatorio. Ha tre elementi figlio e nessun attributo.

## <a name="syntax"></a>Sintassi


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
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



| Elemento padre                                                           | Elementi figlio                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Elemento scope (schema del connettore di ricerca)](search-schema-sconn-scope.md) | [Elemento scope (schema del connettore di ricerca)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [Elemento scope (schema del connettore di ricerca)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [Elemento url scopeItem (schema del connettore di ricerca)](search-schema-sconn-scope-url.md). |



 

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



 

 



