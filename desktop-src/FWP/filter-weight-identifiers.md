---
title: Identificatori di peso del filtro (Fwpmu. h)
description: Filtrare gli identificatori di peso usati dal motore di filtro di base (BFE) per calcolare i pesi dei filtri generati automaticamente.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302354"
---
# <a name="filter-weight-identifiers"></a><span data-ttu-id="92140-103">Identificatori di peso del filtro</span><span class="sxs-lookup"><span data-stu-id="92140-103">Filter Weight Identifiers</span></span>

<span data-ttu-id="92140-104">Di seguito sono elencati gli identificatori di peso del filtro usati dal motore di filtro di base (BFE) per calcolare i pesi dei filtri generati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="92140-104">The filter weight identifiers used by the Base Filtering Engine (BFE) to compute auto-generated filter weights are listed below.</span></span>

<span data-ttu-id="92140-105">Per altre informazioni sulla generazione del peso del filtro, vedere [assegnazione del peso del filtro](filter-weight-assignment.md) .</span><span class="sxs-lookup"><span data-stu-id="92140-105">See [Filter Weight Assignment](filter-weight-assignment.md) for more information on filter weight generation.</span></span>

<dl> <dt>

<span data-ttu-id="92140-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**\_bit di \_ peso \_ automatico FWPM**</span><span class="sxs-lookup"><span data-stu-id="92140-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM\_AUTO\_WEIGHT\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92140-107">(60)</span><span class="sxs-lookup"><span data-stu-id="92140-107">(60)</span></span>
</dt> <dt>



<span data-ttu-id="92140-108">Numero di bit utilizzati per i pesi di filtro generati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="92140-108">Number of bits used for auto-generated filter weights.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92140-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**\_ \_ Max peso automatico \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="92140-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM\_AUTO\_WEIGHT\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92140-110">(**MAXUINT64** >> 4)</span><span class="sxs-lookup"><span data-stu-id="92140-110">(**MAXUINT64** >> 4)</span></span>
</dt> <dt>



<span data-ttu-id="92140-111">Peso massimo del filtro generato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="92140-111">Maximum auto-generated filter weight.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92140-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**</span><span class="sxs-lookup"><span data-stu-id="92140-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92140-113">0xC</span><span class="sxs-lookup"><span data-stu-id="92140-113">(0xC)</span></span>
</dt> <dt>



<span data-ttu-id="92140-114">BFE assegna un peso con questo valore di intervallo ai filtri IKE e AuthIP.</span><span class="sxs-lookup"><span data-stu-id="92140-114">BFE assigns a weight with this range value to IKE and AuthIP filters.</span></span>

<span data-ttu-id="92140-115">Per ulteriori informazioni sui filtri IKE/AuthIP, vedere [esenzioni IKE/AuthIP](ike-exemptions.md) .</span><span class="sxs-lookup"><span data-stu-id="92140-115">See [IKE/AuthIP Exemptions](ike-exemptions.md) for more information on IKE/AuthIP filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92140-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**\_IPSec FWPM intervallo di ponderazione \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92140-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM\_WEIGHT\_RANGE\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92140-117">(0x0)</span><span class="sxs-lookup"><span data-stu-id="92140-117">(0x0)</span></span>
</dt> <dt>



<span data-ttu-id="92140-118">BFE assegna un peso con questo valore di intervallo ai filtri dei criteri IPsec.</span><span class="sxs-lookup"><span data-stu-id="92140-118">BFE assigns a weight with this range value to IPsec policy filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92140-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_Max FWPM intervallo di ponderazione \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92140-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM\_WEIGHT\_RANGE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="92140-120">(**MAXUINT64** >> 60)</span><span class="sxs-lookup"><span data-stu-id="92140-120">(**MAXUINT64** >> 60)</span></span>
</dt> <dt>



<span data-ttu-id="92140-121">Valore massimo dell'intervallo di ponderazione del filtro consentito.</span><span class="sxs-lookup"><span data-stu-id="92140-121">Maximum allowed filter weight range value.</span></span>


</dt> </dl> </dd> </dl>

> [!Note]  
> <span data-ttu-id="92140-122">**MAXUINT64** rappresenta il valore massimo possibile di **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="92140-122">**MAXUINT64** represents the largest possible value of **UINT64**.</span></span> <span data-ttu-id="92140-123">Il valore di questa costante è 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="92140-123">The value of this constant is 0xFFFFFFFFFFFFFFFF.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92140-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92140-124">Requirements</span></span>



| <span data-ttu-id="92140-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="92140-125">Requirement</span></span> | <span data-ttu-id="92140-126">Valore</span><span class="sxs-lookup"><span data-stu-id="92140-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92140-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92140-127">Minimum supported client</span></span><br/> | <span data-ttu-id="92140-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92140-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92140-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92140-129">Minimum supported server</span></span><br/> | <span data-ttu-id="92140-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92140-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92140-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92140-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="92140-132"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="92140-132"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





