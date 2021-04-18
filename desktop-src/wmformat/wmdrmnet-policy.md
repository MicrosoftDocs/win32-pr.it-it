---
title: Struttura WMDRMNET_POLICY (wmdrmsdk. h)
description: La \_ struttura dei criteri WMDRMNET contiene i criteri da usare per le operazioni di Windows Media DRM per i dispositivi di rete.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Formato di Windows Media per la struttura WMDRMNET_POLICY
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324810"
---
# <a name="wmdrmnet_policy-structure"></a><span data-ttu-id="893bf-105">\_Struttura dei criteri WMDRMNET</span><span class="sxs-lookup"><span data-stu-id="893bf-105">WMDRMNET\_POLICY structure</span></span>

<span data-ttu-id="893bf-106">La struttura dei **\_ criteri WMDRMNET** contiene i criteri da usare per le operazioni di Windows Media DRM per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="893bf-106">The **WMDRMNET\_POLICY** structure contains the policy to be used for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="893bf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="893bf-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a><span data-ttu-id="893bf-108">Members</span><span class="sxs-lookup"><span data-stu-id="893bf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="893bf-109">**ePolicyType**</span><span class="sxs-lookup"><span data-stu-id="893bf-109">**ePolicyType**</span></span>
</dt> <dd>

<span data-ttu-id="893bf-110">Membro dell'enumerazione [**del \_ \_ tipo di criteri WMDRMNET**](wmdrmnet-policy-type.md) che specifica il tipo di criteri.</span><span class="sxs-lookup"><span data-stu-id="893bf-110">Member of the [**WMDRMNET\_POLICY\_TYPE**](wmdrmnet-policy-type.md) enumeration that specifies the type of policy.</span></span>

</dd> <dt>

<span data-ttu-id="893bf-111">**pbPolicy**</span><span class="sxs-lookup"><span data-stu-id="893bf-111">**pbPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="893bf-112">Buffer contenente i criteri.</span><span class="sxs-lookup"><span data-stu-id="893bf-112">Buffer containing the policy.</span></span> <span data-ttu-id="893bf-113">L'unico tipo di criteri attualmente supportato è **il \_ tipo di criteri WMDRMNET \_ \_ TRANSCRYPTPLAY**.</span><span class="sxs-lookup"><span data-stu-id="893bf-113">The only type of policy currently supported is **WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**.</span></span> <span data-ttu-id="893bf-114">Questo membro è un puntatore a una **struttura \_ \_ TRANSCRYPTPLAY dei criteri WMDRMNET** .</span><span class="sxs-lookup"><span data-stu-id="893bf-114">This member is a pointer to a **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="893bf-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="893bf-115">Remarks</span></span>

<span data-ttu-id="893bf-116">Questa struttura viene utilizzata come parametro per il metodo [**IWMDRMNetTransmitter:: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="893bf-116">This structure is used as a parameter for the [**IWMDRMNetTransmitter::GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="893bf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="893bf-117">Requirements</span></span>



| <span data-ttu-id="893bf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="893bf-118">Requirement</span></span> | <span data-ttu-id="893bf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="893bf-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="893bf-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="893bf-120">Header</span></span><br/> | <dl> <span data-ttu-id="893bf-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="893bf-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="893bf-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="893bf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="893bf-123">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="893bf-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="893bf-124">**\_ \_ requisiti globali del criterio WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="893bf-124">**WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS**</span></span>](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[<span data-ttu-id="893bf-125">**\_ \_ ambiente minimo per i criteri WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="893bf-125">**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**</span></span>](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[<span data-ttu-id="893bf-126">**\_criteri WMDRMNET \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="893bf-126">**WMDRMNET\_POLICY\_TRANSCRYPTPLAY**</span></span>](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[<span data-ttu-id="893bf-127">**\_tipo di criteri WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="893bf-127">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





