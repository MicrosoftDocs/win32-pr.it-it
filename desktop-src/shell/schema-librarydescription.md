---
description: L' <libraryDescription> elemento è il contenitore di livello superiore per la definizione della libreria. Questo elemento è obbligatorio.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: Elemento libraryDescription (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125cb01ce1bd38418c10f5b14ff7b28f64efba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977842"
---
# <a name="librarydescription-element-library-schema"></a><span data-ttu-id="19484-104">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="19484-104">libraryDescription Element (Library Schema)</span></span>

<span data-ttu-id="19484-105">L' <libraryDescription> elemento è il contenitore di livello superiore per la definizione della libreria.</span><span class="sxs-lookup"><span data-stu-id="19484-105">The <libraryDescription> element is the top-level container for the library definition.</span></span> <span data-ttu-id="19484-106">Questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19484-106">This element is required.</span></span>

## <a name="syntax"></a><span data-ttu-id="19484-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19484-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="19484-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="19484-108">Element Information</span></span>



| <span data-ttu-id="19484-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="19484-109">Parent element</span></span> | <span data-ttu-id="19484-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="19484-110">Child elements</span></span>                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | <span data-ttu-id="19484-111">[elemento Name (schema della libreria)](schema-library-name.md).</span><span class="sxs-lookup"><span data-stu-id="19484-111">[name Element (Library Schema)](schema-library-name.md).</span></span> <span data-ttu-id="19484-112">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19484-112">Required.</span></span>                                                     |
|                | <span data-ttu-id="19484-113">[elemento ownerSID (schema della libreria)](schema-library-ownersid.md).</span><span class="sxs-lookup"><span data-stu-id="19484-113">[ownerSID Element (Library Schema)](schema-library-ownersid.md).</span></span> <span data-ttu-id="19484-114">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19484-114">Optional.</span></span>                                             |
|                | <span data-ttu-id="19484-115">[elemento Version (schema della libreria)](schema-library-version.md).</span><span class="sxs-lookup"><span data-stu-id="19484-115">[version Element (Library Schema)](schema-library-version.md).</span></span> <span data-ttu-id="19484-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19484-116">Optional.</span></span>                                               |
|                | <span data-ttu-id="19484-117">[elemento isLibraryPinned (schema della libreria)](schema-library-islibrarypinned.md).</span><span class="sxs-lookup"><span data-stu-id="19484-117">[isLibraryPinned Element (Library Schema)](schema-library-islibrarypinned.md).</span></span> <span data-ttu-id="19484-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19484-118">Optional.</span></span>                               |
|                | <span data-ttu-id="19484-119">[elemento iconReference (schema della libreria)](schema-library-iconreference.md).</span><span class="sxs-lookup"><span data-stu-id="19484-119">[iconReference Element (Library Schema)](schema-library-iconreference.md).</span></span> <span data-ttu-id="19484-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19484-120">Optional.</span></span>                                   |
|                | <span data-ttu-id="19484-121">[elemento PropertyStore (schema della libreria)](schema-library-propertystore.md).</span><span class="sxs-lookup"><span data-stu-id="19484-121">[propertyStore Element (Library Schema)](schema-library-propertystore.md).</span></span> <span data-ttu-id="19484-122">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19484-122">Optional.</span></span>                                   |
|                | <span data-ttu-id="19484-123">[elemento TemplateInfo (schema della libreria)](schema-library-templateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="19484-123">[templateInfo Element (Library Schema)](schema-library-templateinfo.md).</span></span> <span data-ttu-id="19484-124">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="19484-124">Optional.</span></span>                                     |
|                | <span data-ttu-id="19484-125">[elemento searchConnectorDescriptionList (schema della libreria)](schema-library-searchconnectordescriptionlist.md).</span><span class="sxs-lookup"><span data-stu-id="19484-125">[searchConnectorDescriptionList Element (Library Schema)](schema-library-searchconnectordescriptionlist.md).</span></span> <span data-ttu-id="19484-126">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="19484-126">Required.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="19484-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="19484-127">Remarks</span></span>

<span data-ttu-id="19484-128">Ogni raccolta può contenere una o più posizioni che possono essere visualizzate o cercate da un utente tramite Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="19484-128">Each library can contain one or more locations that can be browsed or searched by a user using Windows Explorer.</span></span> <span data-ttu-id="19484-129">I percorsi vengono definiti dai connettori di ricerca usando [<searchConnectorDescription>](schema-library-searchconnectordescription.md) gli elementi in un [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) elemento contenitore.</span><span class="sxs-lookup"><span data-stu-id="19484-129">The locations are defined by search connectors using [<searchConnectorDescription>](schema-library-searchconnectordescription.md) elements in a [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) container element.</span></span>

<span data-ttu-id="19484-130">Una raccolta può avere un set univoco di proprietà e i percorsi nella libreria possono avere anche set di proprietà univoci.</span><span class="sxs-lookup"><span data-stu-id="19484-130">A library can have a unique set of properties, and locations in the library can also have unique sets of properties.</span></span> <span data-ttu-id="19484-131">Queste proprietà sono definite in [<property>](schema-library-property.md) elementi all'interno di un [<propertyStore>](schema-library-propertystore.md) elemento contenitore.</span><span class="sxs-lookup"><span data-stu-id="19484-131">These properties are defined in [<property>](schema-library-property.md) elements within a [<propertyStore>](schema-library-propertystore.md) container element.</span></span>

## <a name="example"></a><span data-ttu-id="19484-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="19484-132">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="19484-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19484-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19484-134">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="19484-134">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="19484-135">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="19484-135">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
