---
description: Specifica se il servizio di configurazione automatica per reti cablate tenterà l'autenticazione della porta tramite 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232427"
---
# <a name="onexenabled-security-element"></a><span data-ttu-id="deee9-103">Elemento OneXEnabled (Security)</span><span class="sxs-lookup"><span data-stu-id="deee9-103">OneXEnabled (security) Element</span></span>

<span data-ttu-id="deee9-104">L'elemento **OneXEnabled** (Security) specifica se il servizio di configurazione automatica per reti cablate tenterà l'autenticazione della porta tramite 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="deee9-104">The **OneXEnabled** (security) element specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <span data-ttu-id="deee9-105">Quando **OneXEnabled** è false, il servizio di configurazione automatica non utilizza mai 802.1 x per l'autenticazione della porta.</span><span class="sxs-lookup"><span data-stu-id="deee9-105">When **OneXEnabled** is FALSE, the automatic configuration service never uses 802.1X for port authentication.</span></span> <span data-ttu-id="deee9-106">Quando **OneXEnabled** è true, il servizio di configurazione automatica tenta l'autenticazione della porta tramite 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="deee9-106">When **OneXEnabled** is TRUE, then the automatic configuration service attempts port authentication using 802.1X.</span></span>

<span data-ttu-id="deee9-107">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="deee9-107">This element is optional.</span></span> <span data-ttu-id="deee9-108">Il valore predefinito è TRUE.</span><span class="sxs-lookup"><span data-stu-id="deee9-108">The default value is TRUE.</span></span> <span data-ttu-id="deee9-109">Quando **OneXEnabled** non viene specificato in un profilo, è possibile usare 802.1 x per l'autenticazione della porta.</span><span class="sxs-lookup"><span data-stu-id="deee9-109">When **OneXEnabled** is not specified in a profile, then 802.1X may be used for port authentication.</span></span>

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

<span data-ttu-id="deee9-110">L'elemento **OneXEnabled** è definito dall'elemento [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="deee9-110">The **OneXEnabled** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="deee9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="deee9-111">Requirements</span></span>



| <span data-ttu-id="deee9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="deee9-112">Requirement</span></span> | <span data-ttu-id="deee9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="deee9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="deee9-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="deee9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="deee9-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="deee9-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="deee9-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="deee9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="deee9-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="deee9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="deee9-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="deee9-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="deee9-119">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="deee9-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="deee9-120">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="deee9-120">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="deee9-121">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="deee9-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="deee9-122">**sicurezza (MSM)**</span><span class="sxs-lookup"><span data-stu-id="deee9-122">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




