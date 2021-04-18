---
title: Tipo complesso QueryListType
description: Definisce un elenco di query che possono contenere un set di selettori ed eliminati utilizzati per includere eventi in o escludere eventi dal set di risultati.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Log eventi di tipo complesso QueryListType
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301548"
---
# <a name="querylisttype-complex-type"></a><span data-ttu-id="61785-104">Tipo complesso QueryListType</span><span class="sxs-lookup"><span data-stu-id="61785-104">QueryListType Complex Type</span></span>

<span data-ttu-id="61785-105">Definisce un elenco di query che possono contenere un set di selettori ed eliminati utilizzati per includere eventi in o escludere eventi dal set di risultati.</span><span class="sxs-lookup"><span data-stu-id="61785-105">Defines a list of queries that can contain a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="61785-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="61785-106">Child elements</span></span>



| <span data-ttu-id="61785-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="61785-107">Element</span></span>                                                  | <span data-ttu-id="61785-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="61785-108">Type</span></span>                                                   | <span data-ttu-id="61785-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61785-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61785-110">**Query**</span><span class="sxs-lookup"><span data-stu-id="61785-110">**Query**</span></span>](queryschema-query-querylisttype-element.md) | [<span data-ttu-id="61785-111">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="61785-111">**QueryType**</span></span>](queryschema-querytype-complextype.md) | <span data-ttu-id="61785-112">Definisce un set di selettori ed eliminati utilizzati per includere eventi in o escludere eventi dal set di risultati.</span><span class="sxs-lookup"><span data-stu-id="61785-112">Defines a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="61785-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61785-113">Requirements</span></span>



| <span data-ttu-id="61785-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="61785-114">Requirement</span></span> | <span data-ttu-id="61785-115">Valore</span><span class="sxs-lookup"><span data-stu-id="61785-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61785-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61785-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61785-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61785-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61785-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61785-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61785-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61785-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





