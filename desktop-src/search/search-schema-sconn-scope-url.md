---
description: L' <url> elemento specifica un URL che rappresenta l'ambito del connettore di ricerca. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: Elemento URL scopeItem (schema del connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c573308fe406fe4500f6bb8e88b3762fa0bbac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878786"
---
# <a name="scopeitem-url-element-search-connector-schema"></a><span data-ttu-id="c7283-104">Elemento URL scopeItem (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="c7283-104">scopeItem url Element (Search Connector Schema)</span></span>

<span data-ttu-id="c7283-105">L' <url> elemento specifica un URL che rappresenta l'ambito del connettore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c7283-105">The <url> element specifies a URL that represents the scope of the search connector.</span></span> <span data-ttu-id="c7283-106">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="c7283-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7283-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7283-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c7283-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="c7283-108">Element Information</span></span>



| <span data-ttu-id="c7283-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="c7283-109">Parent Element</span></span>                                                                   | <span data-ttu-id="c7283-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c7283-110">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c7283-111">Elemento scopeItem (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="c7283-111">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="c7283-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7283-112">Remarks</span></span>

<span data-ttu-id="c7283-113">Il valore può essere un percorso di file system locale o un URL.</span><span class="sxs-lookup"><span data-stu-id="c7283-113">The value can be a local file system path or a URL.</span></span>

## <a name="example"></a><span data-ttu-id="c7283-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="c7283-114">Example</span></span>

<span data-ttu-id="c7283-115">Nell'esempio seguente viene illustrato un ambito di ricerca che include C: \\ ExampleFolder e tutte le relative cartelle figlio ad eccezione di c: \\ ExampleFolder \\ ExcludeMe.</span><span class="sxs-lookup"><span data-stu-id="c7283-115">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



