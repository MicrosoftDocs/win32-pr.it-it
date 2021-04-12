---
title: Enumerazione MPTHREAT_ACTION (MpClient. h)
description: Possibili azioni di minaccia.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_ACTION
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_ACTION
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119667"
---
# <a name="mpthreat_action-enumeration"></a><span data-ttu-id="bcf99-105">\_Enumerazione azione MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="bcf99-105">MPTHREAT\_ACTION enumeration</span></span>

<span data-ttu-id="bcf99-106">Possibili azioni di minaccia.</span><span class="sxs-lookup"><span data-stu-id="bcf99-106">Possible threat actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf99-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcf99-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a><span data-ttu-id="bcf99-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="bcf99-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bcf99-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**\_azione di minaccia MP \_ \_ sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="bcf99-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP\_THREAT\_ACTION\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**\_azione di minaccia MP \_ \_ pulita**</span><span class="sxs-lookup"><span data-stu-id="bcf99-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP\_THREAT\_ACTION\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_ \_ quarantena azione minaccia MP \_**</span><span class="sxs-lookup"><span data-stu-id="bcf99-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP\_THREAT\_ACTION\_QUARANTINE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**\_azione di minaccia MP \_ \_ Rimuovi**</span><span class="sxs-lookup"><span data-stu-id="bcf99-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP\_THREAT\_ACTION\_REMOVE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**\_azione di minaccia MP \_ \_ Consenti**</span><span class="sxs-lookup"><span data-stu-id="bcf99-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP\_THREAT\_ACTION\_ALLOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**\_azione di minaccia MP \_ \_ USERDEFINED**</span><span class="sxs-lookup"><span data-stu-id="bcf99-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP\_THREAT\_ACTION\_USERDEFINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**NoAction MP \_ Threat \_ Action \_**</span><span class="sxs-lookup"><span data-stu-id="bcf99-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP\_THREAT\_ACTION\_NOACTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**\_ \_ blocco azione minaccia \_ MP**</span><span class="sxs-lookup"><span data-stu-id="bcf99-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP\_THREAT\_ACTION\_BLOCK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="bcf99-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_ \_ \_ valore massimo azione minaccia \_ MP**</span><span class="sxs-lookup"><span data-stu-id="bcf99-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP\_THREAT\_ACTION\_MAX\_VALUE**</span></span>
<span data-ttu-id="bcf99-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bcf99-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bcf99-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcf99-119">Requirements</span></span>



| <span data-ttu-id="bcf99-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf99-120">Requirement</span></span> | <span data-ttu-id="bcf99-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bcf99-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf99-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcf99-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf99-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bcf99-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bcf99-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcf99-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf99-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bcf99-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcf99-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcf99-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcf99-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcf99-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





