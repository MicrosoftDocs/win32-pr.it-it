---
title: Enumerazione WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: Il \_ \_ tipo di enumerazione tipo di criteri WMDRMNET elenca i tipi di criteri disponibili per le operazioni di Windows Media DRM per i dispositivi di rete.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Formato Windows Media enumerazione WMDRMNET_POLICY_TYPE
- Enumerazione formato Windows Media
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330878"
---
# <a name="wmdrmnet_policy_type-enumeration"></a><span data-ttu-id="eca48-105">Enumerazione del tipo di \_ criteri WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="eca48-105">WMDRMNET\_POLICY\_TYPE enumeration</span></span>

<span data-ttu-id="eca48-106">Il tipo di enumerazione **\_ \_ tipo di criteri WMDRMNET** elenca i tipi di criteri disponibili per le operazioni di Windows Media DRM per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="eca48-106">The **WMDRMNET\_POLICY\_TYPE** enumeration type lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca48-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eca48-107">Syntax</span></span>


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a><span data-ttu-id="eca48-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="eca48-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="eca48-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**tipo di criteri WMDRMNET non \_ \_ \_ definito**</span><span class="sxs-lookup"><span data-stu-id="eca48-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET\_POLICY\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="eca48-110">I tipi di criteri non definiti non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="eca48-110">Undefined policy types are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="eca48-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_tipo di criteri WMDRMNET \_ \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="eca48-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**</span></span>
</dt> <dd>

<span data-ttu-id="eca48-112">Il criterio regola la capacità di convertire il contenuto protetto da DRM di Windows Media in DRM Windows Media protetto per i dati dei dispositivi di rete e riprodurlo in un dispositivo di rete.</span><span class="sxs-lookup"><span data-stu-id="eca48-112">The policy governs the ability to convert content protected by Windows Media DRM into protected Windows Media DRM for Network Devices data and play it back on a networked device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eca48-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="eca48-113">Remarks</span></span>

<span data-ttu-id="eca48-114">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="eca48-114">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="eca48-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eca48-115">Requirements</span></span>



| <span data-ttu-id="eca48-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eca48-116">Requirement</span></span> | <span data-ttu-id="eca48-117">Valore</span><span class="sxs-lookup"><span data-stu-id="eca48-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eca48-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eca48-118">Header</span></span><br/> | <dl> <span data-ttu-id="eca48-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="eca48-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eca48-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eca48-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca48-121">**Tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="eca48-121">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="eca48-122">**criteri di WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="eca48-122">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





