---
title: Struttura WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (wmdrmsdk. h)
description: La \_ \_ struttura di ambiente minima dei criteri WMDRMNET \_ contiene i requisiti di sicurezza minimi per Windows Media DRM per i dispositivi di rete.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Formato di Windows Media per la struttura WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
- struttura Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330879"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a><span data-ttu-id="e32b2-105">\_Struttura di \_ ambiente minima dei criteri WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="e32b2-105">WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT structure</span></span>

<span data-ttu-id="e32b2-106">La struttura di **\_ \_ \_ ambiente minima dei criteri WMDRMNET** contiene i requisiti di sicurezza minimi per Windows Media DRM per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="e32b2-106">The **WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT** structure contains the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="e32b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e32b2-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a><span data-ttu-id="e32b2-108">Members</span><span class="sxs-lookup"><span data-stu-id="e32b2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e32b2-109">**wMinimumSecurityLevel**</span><span class="sxs-lookup"><span data-stu-id="e32b2-109">**wMinimumSecurityLevel**</span></span>
</dt> <dd>

<span data-ttu-id="e32b2-110">È necessario un livello di sicurezza minimo per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e32b2-110">Minimum application security level required.</span></span>

</dd> <dt>

<span data-ttu-id="e32b2-111">**dwMinimumAppRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="e32b2-111">**dwMinimumAppRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e32b2-112">È richiesta la versione minima dell'elenco di revoche di certificati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e32b2-112">Minimum application certificate revocation list version required.</span></span>

</dd> <dt>

<span data-ttu-id="e32b2-113">**dwMinimumDeviceRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="e32b2-113">**dwMinimumDeviceRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e32b2-114">È necessario un elenco di revoche di certificati minimo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e32b2-114">Minimum device certificate revocation list required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e32b2-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e32b2-115">Remarks</span></span>

<span data-ttu-id="e32b2-116">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="e32b2-116">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e32b2-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e32b2-117">Requirements</span></span>



| <span data-ttu-id="e32b2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e32b2-118">Requirement</span></span> | <span data-ttu-id="e32b2-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e32b2-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e32b2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e32b2-120">Header</span></span><br/> | <dl> <span data-ttu-id="e32b2-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e32b2-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e32b2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e32b2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e32b2-123">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="e32b2-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="e32b2-124">**criteri di WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="e32b2-124">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





