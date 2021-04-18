---
title: Enumerazione MPTHREAT_STATUS (MpClient. h)
description: Possibile stato di minaccia.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_STATUS
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_STATUS
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301405"
---
# <a name="mpthreat_status-enumeration"></a><span data-ttu-id="8a7fd-105">\_Enumerazione stato MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="8a7fd-105">MPTHREAT\_STATUS enumeration</span></span>

<span data-ttu-id="8a7fd-106">Possibile stato di minaccia.</span><span class="sxs-lookup"><span data-stu-id="8a7fd-106">Possible threat status.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a7fd-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a><span data-ttu-id="8a7fd-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="8a7fd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8a7fd-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**\_stato minaccia \_ MP \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP\_THREAT\_STATUS\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**\_stato della minaccia MP \_ \_ rilevato**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP\_THREAT\_STATUS\_DETECTED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**\_stato della minaccia MP \_ \_ pulito**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**MP\_THREAT\_STATUS\_CLEANED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**stato della minaccia MP in \_ \_ \_ quarantena**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP\_THREAT\_STATUS\_QUARANTINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**\_stato minacce \_ MP \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP\_THREAT\_STATUS\_REMOVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**\_stato minacce \_ MP \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP\_THREAT\_STATUS\_ALLOWED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**\_stato delle minacce MP \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP\_THREAT\_STATUS\_BLOCKED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**\_ \_ pulizia stato minacce \_ MP \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**MP\_THREAT\_STATUS\_CLEAN\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**\_ \_ \_ quarantena stato minacce MP \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**MP\_THREAT\_STATUS\_QUARANTINE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**\_ \_ rimozione stato minacce \_ MP \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP\_THREAT\_STATUS\_REMOVE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**\_errore di \_ stato della minaccia \_ MP \_**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP\_THREAT\_STATUS\_ALLOW\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**\_stato della minaccia MP \_ \_ abbandonato**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP\_THREAT\_STATUS\_ABANDONED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="8a7fd-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**\_ \_ blocco stato minacce \_ MP \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="8a7fd-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**MP\_THREAT\_STATUS\_BLOCK\_FAILED**</span></span>
<span data-ttu-id="8a7fd-122"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8a7fd-122"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="8a7fd-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a7fd-123">Requirements</span></span>



| <span data-ttu-id="8a7fd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a7fd-124">Requirement</span></span> | <span data-ttu-id="8a7fd-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8a7fd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7fd-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a7fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8a7fd-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8a7fd-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8a7fd-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a7fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8a7fd-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8a7fd-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8a7fd-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a7fd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a7fd-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a7fd-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





