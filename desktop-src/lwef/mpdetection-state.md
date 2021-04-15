---
title: Enumerazione MPDETECTION_STATE (MpClient. h)
description: Stato della minaccia attualmente rilevata.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPDETECTION_STATE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPDETECTION_STATE
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476114"
---
# <a name="mpdetection_state-enumeration"></a><span data-ttu-id="243d8-105">\_Enumerazione dello stato MPDETECTION</span><span class="sxs-lookup"><span data-stu-id="243d8-105">MPDETECTION\_STATE enumeration</span></span>

<span data-ttu-id="243d8-106">Stato della minaccia attualmente rilevata.</span><span class="sxs-lookup"><span data-stu-id="243d8-106">The state of the currently detected threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="243d8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="243d8-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a><span data-ttu-id="243d8-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="243d8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="243d8-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**stato di MPDETECTION \_ \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="243d8-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION\_STATE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="243d8-110">In uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="243d8-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="243d8-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**\_stato MPDETECTION \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="243d8-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION\_STATE\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="243d8-112">Minaccia attiva.</span><span class="sxs-lookup"><span data-stu-id="243d8-112">Active threat.</span></span>

</dd> <dt>

<span data-ttu-id="243d8-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**\_stato MPDETECTION \_ terminato**</span><span class="sxs-lookup"><span data-stu-id="243d8-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="243d8-114">In sospeso 24 ore su uno spostamento da cancellare.</span><span class="sxs-lookup"><span data-stu-id="243d8-114">Pending 24 hours to a move to cleared.</span></span>

</dd> <dt>

<span data-ttu-id="243d8-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_azioni aggiuntive sullo stato MPDETECTION \_ \_**</span><span class="sxs-lookup"><span data-stu-id="243d8-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION\_STATE\_ADDITIONAL\_ACTIONS**</span></span>
</dt> <dd>

<span data-ttu-id="243d8-116">Sono necessarie azioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="243d8-116">Additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="243d8-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**\_stato MPDETECTION \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="243d8-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION\_STATE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="243d8-118">Errore di correzione non critico.</span><span class="sxs-lookup"><span data-stu-id="243d8-118">Non-critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="243d8-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**stato di MPDETECTION \_ \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="243d8-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION\_STATE\_CRITICALLY\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="243d8-120">Errore critico di correzione.</span><span class="sxs-lookup"><span data-stu-id="243d8-120">Critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="243d8-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**\_stato MPDETECTION \_ cancellato**</span><span class="sxs-lookup"><span data-stu-id="243d8-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION\_STATE\_CLEARED**</span></span>
</dt> <dd>

<span data-ttu-id="243d8-122">La minaccia non viene visualizzata nella query di stato, ma solo nella cronologia.</span><span class="sxs-lookup"><span data-stu-id="243d8-122">Threat does not show up in the state query, only in history.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="243d8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="243d8-123">Requirements</span></span>



| <span data-ttu-id="243d8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="243d8-124">Requirement</span></span> | <span data-ttu-id="243d8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="243d8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="243d8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="243d8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="243d8-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="243d8-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="243d8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="243d8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="243d8-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="243d8-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="243d8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="243d8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="243d8-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="243d8-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





