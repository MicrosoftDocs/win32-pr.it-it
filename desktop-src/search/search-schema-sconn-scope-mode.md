---
description: L' <mode> elemento specifica se l'URL deve essere incluso o escluso dall'ambito del connettore di ricerca. I valori consentiti sono include ed exclude. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Elemento Mode (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750327"
---
# <a name="mode-element-search-connector-schema"></a><span data-ttu-id="96cea-105">Elemento Mode (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="96cea-105">mode Element (Search Connector Schema)</span></span>

<span data-ttu-id="96cea-106">L' <mode> elemento specifica se l'URL deve essere incluso o escluso dall'ambito del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="96cea-106">The <mode> element specifies whether the URL should be included or excluded from the scope of the search connector.</span></span> <span data-ttu-id="96cea-107">I valori consentiti sono `Include` e `Exclude`.</span><span class="sxs-lookup"><span data-stu-id="96cea-107">The allowed values are `Include` and `Exclude`.</span></span> <span data-ttu-id="96cea-108">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="96cea-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="96cea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96cea-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="96cea-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="96cea-110">Element Information</span></span>



| <span data-ttu-id="96cea-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="96cea-111">Parent Element</span></span>                                                                   | <span data-ttu-id="96cea-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="96cea-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="96cea-113">Elemento scopeItem (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="96cea-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="96cea-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="96cea-114">Remarks</span></span>

<span data-ttu-id="96cea-115">Non è possibile cercare o esplorare un ambito escluso.</span><span class="sxs-lookup"><span data-stu-id="96cea-115">An excluded scope cannot be searched or browsed.</span></span> <span data-ttu-id="96cea-116">È possibile annidare URL scopeItem.</span><span class="sxs-lookup"><span data-stu-id="96cea-116">You can nest scopeItem URLs.</span></span> <span data-ttu-id="96cea-117">Ad esempio, è possibile includere un ambito padre e tutti i relativi elementi figlio ad eccezione di uno aggiungendo l'URL padre come incluso, con il valore depth di Deep ed escludendo l'URL figlio.</span><span class="sxs-lookup"><span data-stu-id="96cea-117">For example, you can include a parent scope and all its children except one by adding the parent URL as included, with depth value of Deep, and excluding the child URL.</span></span>

## <a name="example"></a><span data-ttu-id="96cea-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="96cea-118">Example</span></span>

<span data-ttu-id="96cea-119">Nell'esempio seguente viene illustrato un ambito di ricerca che include C: \\ ExampleFolder e tutte le relative cartelle figlio ad eccezione di c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="96cea-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



