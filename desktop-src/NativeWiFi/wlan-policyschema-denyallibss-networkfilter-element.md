---
description: Specifica se l'accesso a tutte le reti ad hoc è bloccato.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Elemento denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306499"
---
# <a name="denyallibss-networkfilter-element"></a><span data-ttu-id="36343-103">Elemento denyAllIBSS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="36343-103">denyAllIBSS (networkFilter) Element</span></span>

<span data-ttu-id="36343-104">L'elemento denyAllIBSS (networkFilter) specifica se l'accesso a tutte le reti ad hoc è bloccato.</span><span class="sxs-lookup"><span data-stu-id="36343-104">The denyAllIBSS (networkFilter) element specifies if access to all ad-hoc networks is blocked.</span></span> <span data-ttu-id="36343-105">Quando **denyAllIBSS** ha il valore true, i computer non possono connettersi a una rete ad hoc; in caso contrario, è possibile che i computer si connettano alle reti ad hoc.</span><span class="sxs-lookup"><span data-stu-id="36343-105">When **denyAllIBSS** has a value of TRUE, machines cannot connect to an ad-hoc network; otherwise, machines may connect to ad-hoc networks.</span></span>

<span data-ttu-id="36343-106">Il valore predefinito per questo elemento è FALSE.</span><span class="sxs-lookup"><span data-stu-id="36343-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="36343-107">Se **denyAllIBSS** non è specificato in un profilo, per impostazione predefinita i computer possono connettersi alle reti ad hoc.</span><span class="sxs-lookup"><span data-stu-id="36343-107">If **denyAllIBSS** is not specified in a profile, then by default machines may connect to ad-hoc networks.</span></span>

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

<span data-ttu-id="36343-108">L'elemento **denyAllIBSS** è definito dall'elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="36343-108">The **denyAllIBSS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="36343-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36343-109">Requirements</span></span>



| <span data-ttu-id="36343-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="36343-110">Requirement</span></span> | <span data-ttu-id="36343-111">Valore</span><span class="sxs-lookup"><span data-stu-id="36343-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="36343-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36343-112">Minimum supported client</span></span><br/> | <span data-ttu-id="36343-113">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36343-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36343-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36343-114">Minimum supported server</span></span><br/> | <span data-ttu-id="36343-115">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36343-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36343-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36343-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="36343-117">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="36343-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="36343-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="36343-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="36343-119">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="36343-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="36343-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="36343-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




