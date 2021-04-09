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
# <a name="scopeitem-element-search-connector-schema"></a><span data-ttu-id="c4357-103">Elemento scopeItem (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="c4357-103">scopeItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="c4357-104">L' <scopeItem> elemento rappresenta una singola voce nella tabella dell'ambito di esclusione/inclusione.</span><span class="sxs-lookup"><span data-stu-id="c4357-104">The <scopeItem> element represents a single entry in the exclusion/inclusion scope table.</span></span> <span data-ttu-id="c4357-105"><scopeItem> estende il tipo shellLinkType standard aggiungendo tre nuovi elementi che controllano l'inclusione e l'esclusione di cartelle, controllano la profondità dei risultati e specificano la posizione dell'ambito.</span><span class="sxs-lookup"><span data-stu-id="c4357-105"><scopeItem> extends the standard shellLinkType type by adding three new elements that control inclusion and exclusion of folders, control the depth of results, and specify the location of the scope.</span></span> <span data-ttu-id="c4357-106">Se l' <scope> elemento esiste, questo elemento è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4357-106">If the <scope> element exists, this element is required.</span></span> <span data-ttu-id="c4357-107">Ha tre elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="c4357-107">It has three child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4357-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4357-108">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c4357-109">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c4357-109">Element Information</span></span>



| <span data-ttu-id="c4357-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c4357-110">Parent Element</span></span>                                                           | <span data-ttu-id="c4357-111">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c4357-111">Child Elements</span></span>                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4357-112">Elemento Scope (Schema connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="c4357-112">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md) | <span data-ttu-id="c4357-113">[elemento Scope (Schema connettore di ricerca)](search-schema-sconn-scope-mode.md).</span><span class="sxs-lookup"><span data-stu-id="c4357-113">[scope Element (Search Connector Schema)](search-schema-sconn-scope-mode.md).</span></span>        |
|                                                                          | <span data-ttu-id="c4357-114">[elemento Scope (Schema connettore di ricerca)](search-schema-sconn-scope-depth.md).</span><span class="sxs-lookup"><span data-stu-id="c4357-114">[scope Element (Search Connector Schema)](search-schema-sconn-scope-depth.md).</span></span>       |
|                                                                          | <span data-ttu-id="c4357-115">[elemento URL scopeItem (Schema connettore di ricerca)](search-schema-sconn-scope-url.md).</span><span class="sxs-lookup"><span data-stu-id="c4357-115">[scopeItem url Element (Search Connector Schema)](search-schema-sconn-scope-url.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c4357-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4357-116">Remarks</span></span>

<span data-ttu-id="c4357-117">Usare gli <scope> <scopeItem> elementi e per identificare i percorsi in cui eseguire la ricerca e quali percorsi devono essere esclusi dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="c4357-117">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="c4357-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="c4357-118">Example</span></span>

<span data-ttu-id="c4357-119">Nell'esempio seguente viene illustrato un ambito di ricerca che include C: \\ ExampleFolder e tutte le relative cartelle figlio ad eccezione di c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="c4357-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



