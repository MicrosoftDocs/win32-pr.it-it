---
description: L' <scopeItem> elemento rappresenta una singola voce nella tabella dell'ambito di esclusione/inclusione.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Elemento scopeItem (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128491"
---
# <a name="scopeitem-element-search-connector-schema"></a>Elemento scopeItem (schema del connettore di ricerca)

L' <scopeItem> elemento rappresenta una singola voce nella tabella dell'ambito di esclusione/inclusione. <scopeItem> estende il tipo shellLinkType standard aggiungendo tre nuovi elementi che controllano l'inclusione e l'esclusione di cartelle, controllano la profondità dei risultati e specificano la posizione dell'ambito. Se l' <scope> elemento esiste, questo elemento è obbligatorio. Ha tre elementi figlio e nessun attributo.

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
| [Elemento Scope (Schema connettore di ricerca)](search-schema-sconn-scope.md) | [elemento Scope (Schema connettore di ricerca)](search-schema-sconn-scope-mode.md).        |
|                                                                          | [elemento Scope (Schema connettore di ricerca)](search-schema-sconn-scope-depth.md).       |
|                                                                          | [elemento URL scopeItem (Schema connettore di ricerca)](search-schema-sconn-scope-url.md). |



 

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



 

 



