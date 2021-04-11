---
description: Specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Elemento denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226013"
---
# <a name="denyalless-networkfilter-element"></a><span data-ttu-id="0aca7-103">Elemento denyAllESS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="0aca7-103">denyAllESS (networkFilter) Element</span></span>

<span data-ttu-id="0aca7-104">L'elemento denyAllESS (networkFilter) specifica se l'accesso a tutte le reti dell'infrastruttura è bloccato.</span><span class="sxs-lookup"><span data-stu-id="0aca7-104">The denyAllESS (networkFilter) element specifies if access to all infrastructure networks is blocked.</span></span> <span data-ttu-id="0aca7-105">Quando **denyAllESS** ha il valore true, i computer non possono connettersi a una rete dell'infrastruttura; in caso contrario, i computer possono connettersi alle reti dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0aca7-105">When **denyAllESS** has a value of TRUE, machines cannot connect to an infrastructure network; otherwise, machines may connect to infrastructure networks.</span></span>

<span data-ttu-id="0aca7-106">Il valore predefinito per questo elemento è FALSE.</span><span class="sxs-lookup"><span data-stu-id="0aca7-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="0aca7-107">Se **denyAllESS** non è specificato in un profilo, per impostazione predefinita i computer possono connettersi alle reti dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="0aca7-107">If **denyAllESS** is not specified in a profile, then by default machines may connect to infrastructure networks.</span></span>

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

<span data-ttu-id="0aca7-108">L'elemento **denyAllESS** è definito dall'elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0aca7-108">The **denyAllESS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aca7-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aca7-109">Requirements</span></span>



| <span data-ttu-id="0aca7-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aca7-110">Requirement</span></span> | <span data-ttu-id="0aca7-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0aca7-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0aca7-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aca7-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0aca7-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0aca7-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0aca7-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aca7-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0aca7-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0aca7-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0aca7-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0aca7-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="0aca7-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="0aca7-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0aca7-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="0aca7-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="0aca7-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="0aca7-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0aca7-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="0aca7-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




