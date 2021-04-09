---
title: Enumerazione MPTHREAT_DETECTION (MpClient. h)
description: Possibili tipi noti di rilevamento delle minacce non valide.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_DETECTION
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_DETECTION
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741007"
---
# <a name="mpthreat_detection-enumeration"></a><span data-ttu-id="ea1b8-105">\_Enumerazione rilevamento MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="ea1b8-105">MPTHREAT\_DETECTION enumeration</span></span>

<span data-ttu-id="ea1b8-106">Possibili tipi noti di rilevamento delle minacce non valide.</span><span class="sxs-lookup"><span data-stu-id="ea1b8-106">Possible known bad threat detection types.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea1b8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea1b8-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a><span data-ttu-id="ea1b8-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="ea1b8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ea1b8-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_concreta \_ rilevamento minacce MP \_**</span><span class="sxs-lookup"><span data-stu-id="ea1b8-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP\_THREAT\_DETECTION\_CONCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="ea1b8-110">È stata rilevata una minaccia tramite firme concrete.</span><span class="sxs-lookup"><span data-stu-id="ea1b8-110">Threat was detected via concrete signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ea1b8-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_ \_ euristica rilevamento minacce MP \_**</span><span class="sxs-lookup"><span data-stu-id="ea1b8-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP\_THREAT\_DETECTION\_HEURISTIC**</span></span>
</dt> <dd>

<span data-ttu-id="ea1b8-112">Minaccia rilevata tramite euristica.</span><span class="sxs-lookup"><span data-stu-id="ea1b8-112">Threat was detected via heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="ea1b8-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_rilevamento minacce \_ MP \_ generico**</span><span class="sxs-lookup"><span data-stu-id="ea1b8-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP\_THREAT\_DETECTION\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="ea1b8-114">È stata rilevata una minaccia tramite firme generiche.</span><span class="sxs-lookup"><span data-stu-id="ea1b8-114">Threat was detected via generic signatures.</span></span>

</dd> <dt>

<span data-ttu-id="ea1b8-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**\_rilevamento minacce \_ MP \_ sospetto**</span><span class="sxs-lookup"><span data-stu-id="ea1b8-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP\_THREAT\_DETECTION\_SUSPICIOUS**</span></span>
</dt> <dd>

<span data-ttu-id="ea1b8-116">Minaccia rilevata tramite il monitoraggio del comportamento.</span><span class="sxs-lookup"><span data-stu-id="ea1b8-116">Threat was detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="ea1b8-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**\_ \_ FastPath rilevamento minacce \_ MP**</span><span class="sxs-lookup"><span data-stu-id="ea1b8-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP\_THREAT\_DETECTION\_FASTPATH**</span></span>
</dt> <dd>

<span data-ttu-id="ea1b8-118">È stata rilevata una minaccia tramite FastPath.</span><span class="sxs-lookup"><span data-stu-id="ea1b8-118">Threat was detected via fastpath.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea1b8-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea1b8-119">Requirements</span></span>



| <span data-ttu-id="ea1b8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea1b8-120">Requirement</span></span> | <span data-ttu-id="ea1b8-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ea1b8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1b8-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea1b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1b8-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ea1b8-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ea1b8-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea1b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1b8-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ea1b8-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea1b8-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea1b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1b8-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea1b8-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





