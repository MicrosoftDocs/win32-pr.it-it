---
description: Specifica se il servizio di configurazione automatica per reti cablate richiede l'utilizzo di 802.1 X per l'autenticazione della porta.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314753"
---
# <a name="onexenforced-security-element"></a><span data-ttu-id="25a97-103">Elemento OneXEnforced (Security)</span><span class="sxs-lookup"><span data-stu-id="25a97-103">OneXEnforced (security) Element</span></span>

<span data-ttu-id="25a97-104">L'elemento **OneXEnforced** (Security) specifica se il servizio di configurazione automatica per reti cablate richiede l'utilizzo di 802.1 x per l'autenticazione della porta.</span><span class="sxs-lookup"><span data-stu-id="25a97-104">The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <span data-ttu-id="25a97-105">Quando **OneXEnforced** è true, il servizio di configurazione automatica deve usare 802.1 x per l'autenticazione della porta.</span><span class="sxs-lookup"><span data-stu-id="25a97-105">When **OneXEnforced** is TRUE, the automatic configuration service must use 802.1X for port authentication.</span></span> <span data-ttu-id="25a97-106">Quando **OneXEnforced** è false, il servizio di configurazione automatica tenterà di utilizzare 802.1 x per l'autenticazione della porta, ma il servizio eseguirà il fallback a nessuna autenticazione se per qualsiasi motivo l'autenticazione 802.1 x non riesce.</span><span class="sxs-lookup"><span data-stu-id="25a97-106">When **OneXEnforced** is FALSE, then the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.</span></span>

<span data-ttu-id="25a97-107">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="25a97-107">This element is optional.</span></span> <span data-ttu-id="25a97-108">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="25a97-108">The default value is FALSE.</span></span>

<span data-ttu-id="25a97-109">Questo elemento ha un valore significativo solo se [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) è true.</span><span class="sxs-lookup"><span data-stu-id="25a97-109">This element only has a meaningful value if [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) is TRUE.</span></span> <span data-ttu-id="25a97-110">Se **OneXEnabled** è false, il valore di questo elemento viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="25a97-110">If **OneXEnabled** is FALSE, then the value of this element is ignored.</span></span>

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

<span data-ttu-id="25a97-111">L'elemento **OneXEnforced** è definito dall'elemento [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="25a97-111">The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="25a97-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25a97-112">Requirements</span></span>



| <span data-ttu-id="25a97-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="25a97-113">Requirement</span></span> | <span data-ttu-id="25a97-114">Valore</span><span class="sxs-lookup"><span data-stu-id="25a97-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25a97-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25a97-115">Minimum supported client</span></span><br/> | <span data-ttu-id="25a97-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25a97-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25a97-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25a97-117">Minimum supported server</span></span><br/> | <span data-ttu-id="25a97-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25a97-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25a97-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25a97-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="25a97-120">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="25a97-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="25a97-121">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="25a97-121">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="25a97-122">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="25a97-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="25a97-123">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="25a97-123">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




