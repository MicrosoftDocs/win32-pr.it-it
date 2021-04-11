---
title: Enumerazione WINBIO_ANTI_SPOOF_POLICY_ACTION ( \_ tipi WINBIO. h)
description: Specifica i tipi di azioni da eseguire per i criteri di antispoofing di un utente.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumerazione Windows Biometric Framework API
- Puntatore di enumerazione PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964443"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a><span data-ttu-id="0c142-105">\_ \_ \_ Enumerazione azione criterio anti spoofing WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="0c142-105">WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION enumeration</span></span>

<span data-ttu-id="0c142-106">Specifica i tipi di azioni da eseguire per i criteri di antispoofing di un utente.</span><span class="sxs-lookup"><span data-stu-id="0c142-106">Specifies the types of actions you take for the antispoofing policy of a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c142-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c142-107">Syntax</span></span>


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a><span data-ttu-id="0c142-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="0c142-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0c142-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO \_ anti \_ spoofing \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="0c142-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO\_ANTI\_SPOOF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c142-110">Disattiva il rilevamento dello spoofing per un fattore biometrico.</span><span class="sxs-lookup"><span data-stu-id="0c142-110">Turns off the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="0c142-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO \_ anti \_ spoofing \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="0c142-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO\_ANTI\_SPOOF\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0c142-112">Attiva il rilevamento dello spoofing per un fattore biometrico.</span><span class="sxs-lookup"><span data-stu-id="0c142-112">Turns on the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="0c142-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**rimozione di WINBIO \_ anti \_ spoofing \_**</span><span class="sxs-lookup"><span data-stu-id="0c142-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO\_ANTI\_SPOOF\_REMOVE**</span></span>
</dt> <dd>

<span data-ttu-id="0c142-114">Rimuove l'intero criterio di antispoofing per il fattore biometrico dall'account.</span><span class="sxs-lookup"><span data-stu-id="0c142-114">Removes the entire antispoofing policy for the biometric factor from the account.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c142-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c142-115">Requirements</span></span>



| <span data-ttu-id="0c142-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c142-116">Requirement</span></span> | <span data-ttu-id="0c142-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0c142-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c142-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c142-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0c142-119">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0c142-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="0c142-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c142-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0c142-121">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="0c142-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="0c142-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c142-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c142-123"><dt>WinBio \_ types. h (includere WinBio. h per le applicazioni client o WinBio \_ Adapters. h per gli adapter)</dt></span><span class="sxs-lookup"><span data-stu-id="0c142-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c142-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c142-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c142-125">**\_ \_ \_ Azione criterio anti-spoofing WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="0c142-125">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="0c142-126">**\_origine criteri \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="0c142-126">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> </dl>

 

 





