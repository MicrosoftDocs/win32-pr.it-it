---
description: L' <propertyStore> elemento specifica un set di una o più proprietà utilizzate da questa libreria. Questo elemento è facoltativo e non ha attributi.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (schema della libreria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980319"
---
# <a name="propertystore-element-library-schema"></a><span data-ttu-id="f71d9-104">Elemento propertyStore (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="f71d9-104">propertyStore Element (Library Schema)</span></span>

<span data-ttu-id="f71d9-105">L' <propertyStore> elemento specifica un set di una o più proprietà utilizzate da questa libreria.</span><span class="sxs-lookup"><span data-stu-id="f71d9-105">The <propertyStore> element specifies a set of one or more properties used by this library.</span></span> <span data-ttu-id="f71d9-106">Questo elemento è facoltativo e non ha attributi.</span><span class="sxs-lookup"><span data-stu-id="f71d9-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f71d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f71d9-107">Syntax</span></span>

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="f71d9-108">Informazioni sull'elemento</span><span class="sxs-lookup"><span data-stu-id="f71d9-108">Element Information</span></span>



| <span data-ttu-id="f71d9-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="f71d9-109">Parent Element</span></span>                                                               | <span data-ttu-id="f71d9-110">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f71d9-110">Child Elements</span></span>                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f71d9-111">Elemento libraryDescription (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="f71d9-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="f71d9-112">Elemento Property (schema della libreria)</span><span class="sxs-lookup"><span data-stu-id="f71d9-112">property Element (Library Schema)</span></span>](schema-library-property.md) |



 

## <a name="remarks"></a><span data-ttu-id="f71d9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f71d9-113">Remarks</span></span>

<span data-ttu-id="f71d9-114">L' <propertyStore> elemento può contenere uno o più <property> elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="f71d9-114">The <propertyStore> element can have one or more <property> child elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f71d9-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f71d9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f71d9-116">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="f71d9-116">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="f71d9-117">Cerca nello schema di descrizione del connettore</span><span class="sxs-lookup"><span data-stu-id="f71d9-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
