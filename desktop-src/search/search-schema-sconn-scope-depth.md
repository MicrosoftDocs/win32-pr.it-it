---
description: L' <depth> elemento specifica se l'ambito del connettore di ricerca deve includere URL figlio. I valori consentiti sono Deep e Shallow. Questo elemento non ha elementi figlio e nessun attributo.
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Elemento Depth (Schema connettore di ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966532"
---
# <a name="depth-element-search-connector-schema"></a><span data-ttu-id="5c80d-105">Elemento Depth (Schema connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="5c80d-105">depth Element (Search Connector Schema)</span></span>

<span data-ttu-id="5c80d-106">L' <depth> elemento specifica se l'ambito del connettore di ricerca deve includere URL figlio.</span><span class="sxs-lookup"><span data-stu-id="5c80d-106">The <depth> element specifies whether the search connector's scope should include child URLs.</span></span> <span data-ttu-id="5c80d-107">I valori consentiti sono `Deep` e `Shallow`.</span><span class="sxs-lookup"><span data-stu-id="5c80d-107">The allowed values are `Deep` and `Shallow`.</span></span> <span data-ttu-id="5c80d-108">Questo elemento non ha elementi figlio e nessun attributo.</span><span class="sxs-lookup"><span data-stu-id="5c80d-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c80d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c80d-109">Syntax</span></span>


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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



## <a name="element-information"></a><span data-ttu-id="5c80d-110">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="5c80d-110">Element Information</span></span>



| <span data-ttu-id="5c80d-111">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="5c80d-111">Parent Element</span></span>                                                                   | <span data-ttu-id="5c80d-112">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="5c80d-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="5c80d-113">Elemento scopeItem (schema del connettore di ricerca)</span><span class="sxs-lookup"><span data-stu-id="5c80d-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="5c80d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c80d-114">Remarks</span></span>

<span data-ttu-id="5c80d-115">Se la profondità è profonda, gli utenti possono sfogliare o cercare gli elementi nel livello URL di scopeItem o in qualsiasi URL figlio.</span><span class="sxs-lookup"><span data-stu-id="5c80d-115">If the depth is deep, users can browse or search items in the scopeItem's URL level or within any child URLs.</span></span>

## <a name="example"></a><span data-ttu-id="5c80d-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c80d-116">Example</span></span>

<span data-ttu-id="5c80d-117">Nell'esempio seguente viene illustrato un ambito di ricerca che include C: \\ FolderA e tutte le relative cartelle figlio e c: \\ FolderB ma nessuna delle relative cartelle figlio.</span><span class="sxs-lookup"><span data-stu-id="5c80d-117">The following example shows a search scope that includes C:\\FolderA and all its child folders and C:\\FolderB but none of its child folders.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



