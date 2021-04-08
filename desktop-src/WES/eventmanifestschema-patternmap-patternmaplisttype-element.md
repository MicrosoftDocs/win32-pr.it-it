---
title: Elemento patternMap (PatternMapListType)
description: Definisce un mapping tra due espressioni regolari. Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.
ms.assetid: 5cf28d38-4cc3-4a7b-a64b-3ad1cb42ebef
keywords:
- EventLog elemento patternMap
topic_type:
- apiref
api_name:
- patternMap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ae29d60e39515a7c4b4db334f947abc44df5ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047792"
---
# <a name="patternmap-patternmaplisttype-element"></a><span data-ttu-id="99207-105">Elemento patternMap (PatternMapListType)</span><span class="sxs-lookup"><span data-stu-id="99207-105">patternMap (PatternMapListType) Element</span></span>

<span data-ttu-id="99207-106">Definisce un mapping tra due espressioni regolari.</span><span class="sxs-lookup"><span data-stu-id="99207-106">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="99207-107">Viene utilizzata un'espressione per trovare una stringa corrispondente nella stringa del messaggio e l'altra per modificare la stringa prima che il servizio lo riporti nella stringa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="99207-107">One expression is used to find a matching string in the message string, and the other is used to alter the string before the service places it back in the message string.</span></span>

``` syntax
<xs:element name="patternMap"
    type="PatternMapType"
 />
```

<span data-ttu-id="99207-108">L'elemento **patternMap** è definito dal tipo complesso [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="99207-108">The **patternMap** element is defined by the [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="99207-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99207-109">Requirements</span></span>



| <span data-ttu-id="99207-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="99207-110">Requirement</span></span> | <span data-ttu-id="99207-111">Valore</span><span class="sxs-lookup"><span data-stu-id="99207-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99207-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99207-112">Minimum supported client</span></span><br/> | <span data-ttu-id="99207-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99207-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99207-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99207-114">Minimum supported server</span></span><br/> | <span data-ttu-id="99207-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99207-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99207-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99207-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="99207-117">**Elemento padre**</span><span class="sxs-lookup"><span data-stu-id="99207-117">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="99207-118">**patternMaps (NamedQueryType)**</span><span class="sxs-lookup"><span data-stu-id="99207-118">**patternMaps (NamedQueryType)**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md)
</dt> </dl>

 

 





