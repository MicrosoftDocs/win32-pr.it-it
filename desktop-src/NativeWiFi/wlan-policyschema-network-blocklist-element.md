---
description: Definisce una rete bloccata.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Elemento Network (Blocker)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318256"
---
# <a name="network-blocklist-element"></a><span data-ttu-id="5634f-103">Elemento Network (Blocker)</span><span class="sxs-lookup"><span data-stu-id="5634f-103">network (blockList) Element</span></span>

<span data-ttu-id="5634f-104">L'elemento Network (Blocker) definisce una rete bloccata.</span><span class="sxs-lookup"><span data-stu-id="5634f-104">The network (blockList) element defines a blocked network.</span></span> <span data-ttu-id="5634f-105">Un computer non è in grado di connettersi a una rete bloccata.</span><span class="sxs-lookup"><span data-stu-id="5634f-105">A machine cannot connect to a blocked network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="5634f-106">L'elemento **Network** è definito dall'elemento [**Blocker**](wlan-policyschema-blocklist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5634f-106">The **network** element is defined by the [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5634f-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5634f-107">Requirements</span></span>



| <span data-ttu-id="5634f-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="5634f-108">Requirement</span></span> | <span data-ttu-id="5634f-109">Valore</span><span class="sxs-lookup"><span data-stu-id="5634f-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5634f-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5634f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="5634f-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5634f-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5634f-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5634f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="5634f-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5634f-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5634f-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5634f-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="5634f-115">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="5634f-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5634f-116">**blockList**</span><span class="sxs-lookup"><span data-stu-id="5634f-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="5634f-117">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="5634f-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5634f-118">**blocco (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="5634f-118">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




