---
description: Specifica un tipo di rete.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317114"
---
# <a name="networktype-networkitemtype-element"></a><span data-ttu-id="335d3-103">Elemento networkType (networkItemType)</span><span class="sxs-lookup"><span data-stu-id="335d3-103">networkType (networkItemType) Element</span></span>

<span data-ttu-id="335d3-104">L'elemento networkType (networkItemType) specifica un tipo di rete.</span><span class="sxs-lookup"><span data-stu-id="335d3-104">The networkType (networkItemType) element specifies a network type.</span></span> <span data-ttu-id="335d3-105">Esistono due tipi di reti: reti di infrastruttura (SSE) e reti ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="335d3-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

<span data-ttu-id="335d3-106">L'elemento **networkType** è definito dal tipo complesso [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="335d3-106">The **networkType** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="335d3-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="335d3-107">Requirements</span></span>



| <span data-ttu-id="335d3-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="335d3-108">Requirement</span></span> | <span data-ttu-id="335d3-109">Valore</span><span class="sxs-lookup"><span data-stu-id="335d3-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="335d3-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="335d3-110">Minimum supported client</span></span><br/> | <span data-ttu-id="335d3-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="335d3-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="335d3-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="335d3-112">Minimum supported server</span></span><br/> | <span data-ttu-id="335d3-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="335d3-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="335d3-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="335d3-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="335d3-115">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="335d3-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="335d3-116">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="335d3-116">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="335d3-117">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="335d3-117">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="335d3-118">**rete (Consenti)**</span><span class="sxs-lookup"><span data-stu-id="335d3-118">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="335d3-119">**rete (blocco)**</span><span class="sxs-lookup"><span data-stu-id="335d3-119">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




