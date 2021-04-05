---
description: Specifica l'identificatore del set di servizi (SSID) di una rete wireless.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Elemento NetworkName (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884553"
---
# <a name="networkname-networkitemtype-element"></a><span data-ttu-id="99eae-103">Elemento NetworkName (networkItemType)</span><span class="sxs-lookup"><span data-stu-id="99eae-103">networkName (networkItemType) Element</span></span>

<span data-ttu-id="99eae-104">L'elemento NetworkName (networkItemType) specifica l'identificatore del set di servizi (SSID) di una rete wireless.</span><span class="sxs-lookup"><span data-stu-id="99eae-104">The networkName (networkItemType) element specifies the service set identifier (SSID) of a wireless network.</span></span>

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

<span data-ttu-id="99eae-105">L'elemento **NetworkName** è definito dal tipo complesso [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="99eae-105">The **networkName** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="99eae-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99eae-106">Requirements</span></span>



| <span data-ttu-id="99eae-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="99eae-107">Requirement</span></span> | <span data-ttu-id="99eae-108">Valore</span><span class="sxs-lookup"><span data-stu-id="99eae-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99eae-109">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99eae-109">Minimum supported client</span></span><br/> | <span data-ttu-id="99eae-110">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99eae-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99eae-111">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99eae-111">Minimum supported server</span></span><br/> | <span data-ttu-id="99eae-112">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="99eae-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99eae-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99eae-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="99eae-114">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="99eae-114">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="99eae-115">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="99eae-115">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="99eae-116">**Possibili elementi padre immediati nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="99eae-116">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="99eae-117">**rete (Consenti)**</span><span class="sxs-lookup"><span data-stu-id="99eae-117">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="99eae-118">**rete (blocco)**</span><span class="sxs-lookup"><span data-stu-id="99eae-118">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




