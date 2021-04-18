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
# <a name="scope-element-search-connector-schema"></a><span data-ttu-id="20a2c-103">Elemento Scope (Schema connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="20a2c-103">scope Element (Search Connector Schema)</span></span>

<span data-ttu-id="20a2c-104">L' <scope> elemento facoltativo specifica una raccolta di <scopeItem> elementi che definiscono le inclusioni e le esclusioni dell'ambito per questo particolare connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="20a2c-104">The optional <scope> element specifies a collection of <scopeItem> elements that define the scope inclusions and exclusions for this particular search connector.</span></span> <span data-ttu-id="20a2c-105">Se <scope> è presente, deve contenere almeno un <scopeItem> elemento.</span><span class="sxs-lookup"><span data-stu-id="20a2c-105">If <scope> is present, it MUST contain at least one <scopeItem> element.</span></span> <span data-ttu-id="20a2c-106">Questo elemento non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="20a2c-106">This element has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a2c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20a2c-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="20a2c-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="20a2c-108">Element Information</span></span>



| <span data-ttu-id="20a2c-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="20a2c-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="20a2c-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="20a2c-110">Child Elements</span></span>                                                                    |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="20a2c-111">Elemento searchConnectorDescriptionType (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="20a2c-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | <span data-ttu-id="20a2c-112">[elemento scopeItem (schema del connettore di ricerca)](search-schema-sconn-scopeitem.md).</span><span class="sxs-lookup"><span data-stu-id="20a2c-112">[scopeItem Element (Search Connector Schema)](search-schema-sconn-scopeitem.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="20a2c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="20a2c-113">Remarks</span></span>

<span data-ttu-id="20a2c-114">Usare gli <scope> <scopeItem> elementi e per identificare i percorsi in cui eseguire la ricerca e quali percorsi devono essere esclusi dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="20a2c-114">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="20a2c-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="20a2c-115">Example</span></span>

<span data-ttu-id="20a2c-116">Nell'esempio seguente viene illustrato un ambito di ricerca che include C: \\ ExampleFolder e tutte le relative cartelle figlio ad eccezione di c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="20a2c-116">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



