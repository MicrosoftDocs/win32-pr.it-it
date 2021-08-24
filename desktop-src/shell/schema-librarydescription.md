---
description: <libraryDescription>L'elemento è il contenitore di primo livello per la definizione della libreria. Questo elemento è obbligatorio.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: Elemento libraryDescription (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a454321649746dc9408110e2fb96a616934977022ac80a4c0325494d354bfb46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942061"
---
# <a name="librarydescription-element-library-schema"></a>Elemento libraryDescription (schema della libreria)

<libraryDescription>L'elemento è il contenitore di primo livello per la definizione della libreria. Questo elemento è obbligatorio.

## <a name="syntax"></a>Sintassi


```
<!-- libraryDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
    <xs:include schemaLocation="commonTypes-ms.xsd"/>
    <xs:element name="libraryDescription">
        <xs:complexType>
            <xs:all>
                <xs:element name="name" type="xs:string"/>
                <xs:element name="ownerSID" minOccurs="0"/>
                <xs:element name="version" type="xs:int" minOccurs="0"/>
                <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
                <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
                <xs:element name="propertyStore" minOccurs="0">
                    <xs:complexType>
                        <xs:complexContent>
                            <xs:extension base="propertyStoreType"/>
                        </xs:complexContent>
                    </xs:complexType>
                </xs:element>
                <xs:element name="templateInfo" minOccurs="0">
                    <xs:complexType>
                        <xs:all>
                            <xs:element name="folderType" minOccurs="0"/>
                        </xs:all>
                    </xs:complexType>
                </xs:element>
                <xs:element name="searchConnectorDescriptionList" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence minOccurs="0">
                            <xs:element name="searchConnectorDescription" 
                             type="searchConnectorDescriptionType" minOccurs="0" 
                             maxOccurs="unbounded"/>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```



## <a name="element-information"></a>Informazioni sull'elemento



| Elemento padre | Elementi figlio                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | [Elemento name (schema di libreria)](schema-library-name.md). Obbligatorio.                                                     |
|                | [Elemento ownerSID (schema di libreria)](schema-library-ownersid.md). facoltativo.                                             |
|                | [Elemento version (schema della libreria)](schema-library-version.md). facoltativo.                                               |
|                | [Elemento isLibraryPinned (schema di libreria)](schema-library-islibrarypinned.md). facoltativo.                               |
|                | [Elemento iconReference (schema di libreria)](schema-library-iconreference.md). facoltativo.                                   |
|                | [Elemento propertyStore (schema di libreria)](schema-library-propertystore.md). facoltativo.                                   |
|                | [Elemento templateInfo (schema della libreria)](schema-library-templateinfo.md). facoltativo.                                     |
|                | [Elemento searchConnectorDescriptionList (schema di libreria)](schema-library-searchconnectordescriptionlist.md). Obbligatorio. |



 

## <a name="remarks"></a>Commenti

Ogni libreria può contenere uno o più percorsi che possono essere esplorati o cercati da un utente usando Windows Explorer. I percorsi vengono definiti dai connettori di ricerca usando [<searchConnectorDescription>](schema-library-searchconnectordescription.md) gli elementi in un elemento [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) contenitore.

Una libreria può avere un set univoco di proprietà e i percorsi nella libreria possono anche avere set univoci di proprietà. Queste proprietà sono definite negli elementi all'interno [<property>](schema-library-property.md) di un elemento [<propertyStore>](schema-library-propertystore.md) contenitore.

## <a name="example"></a>Esempio


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> <dt>

[Schema di descrizione del connettore di ricerca](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
