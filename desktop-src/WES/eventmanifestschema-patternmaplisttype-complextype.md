---
title: Tipo complesso PatternMapListType
description: Non usato. Definisce un elenco di coppie di espressioni regolari utilizzate per modificare la stringa del messaggio.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Log eventi di tipo complesso PatternMapListType
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340303"
---
# <a name="patternmaplisttype-complex-type"></a><span data-ttu-id="c61d3-105">Tipo complesso PatternMapListType</span><span class="sxs-lookup"><span data-stu-id="c61d3-105">PatternMapListType Complex Type</span></span>

<span data-ttu-id="c61d3-106">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c61d3-106">Not used.</span></span> <span data-ttu-id="c61d3-107">Definisce un elenco di coppie di espressioni regolari utilizzate per modificare la stringa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="c61d3-107">Defines a list of regular expression pairs that are used to alter the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c61d3-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c61d3-108">Child elements</span></span>



| <span data-ttu-id="c61d3-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c61d3-109">Element</span></span>                                                                         | <span data-ttu-id="c61d3-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c61d3-110">Type</span></span>                                                                     | <span data-ttu-id="c61d3-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c61d3-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c61d3-112">**patternMap**</span><span class="sxs-lookup"><span data-stu-id="c61d3-112">**patternMap**</span></span>](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [<span data-ttu-id="c61d3-113">**PatternMapType**</span><span class="sxs-lookup"><span data-stu-id="c61d3-113">**PatternMapType**</span></span>](eventmanifestschema-patternmaptype-complextype.md) | <span data-ttu-id="c61d3-114">Definisce un mapping tra due espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="c61d3-114">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="c61d3-115">Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="c61d3-115">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span> <span data-ttu-id="c61d3-116">Viene utilizzato il primo mapping dei criteri che corrisponde a e altri modelli non vengono tentati.</span><span class="sxs-lookup"><span data-stu-id="c61d3-116">The first pattern mapping that matches is used and other patterns are not tried.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c61d3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c61d3-117">Requirements</span></span>



| <span data-ttu-id="c61d3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c61d3-118">Requirement</span></span> | <span data-ttu-id="c61d3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c61d3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c61d3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c61d3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c61d3-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c61d3-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c61d3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c61d3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c61d3-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c61d3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





