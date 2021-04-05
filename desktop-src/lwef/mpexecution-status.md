---
title: Enumerazione MPEXECUTION_STATUS (MpClient. h)
description: Stato di esecuzione della minaccia possibile.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPEXECUTION_STATUS
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPEXECUTION_STATUS
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873597"
---
# <a name="mpexecution_status-enumeration"></a><span data-ttu-id="ef258-105">\_Enumerazione stato MPEXECUTION</span><span class="sxs-lookup"><span data-stu-id="ef258-105">MPEXECUTION\_STATUS enumeration</span></span>

<span data-ttu-id="ef258-106">Stato di esecuzione della minaccia possibile.</span><span class="sxs-lookup"><span data-stu-id="ef258-106">Possible threat execution status.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef258-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef258-107">Syntax</span></span>


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a><span data-ttu-id="ef258-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="ef258-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ef258-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**\_stato di esecuzione MP \_ \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="ef258-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP\_EXECUTION\_STATUS\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ef258-110">Lo stato di esecuzione non è noto.</span><span class="sxs-lookup"><span data-stu-id="ef258-110">Execution status is not known.</span></span>

</dd> <dt>

<span data-ttu-id="ef258-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**\_stato di esecuzione MP \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="ef258-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP\_EXECUTION\_STATUS\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="ef258-112">Bloccato dall'esecuzione con mini-filtro.</span><span class="sxs-lookup"><span data-stu-id="ef258-112">Blocked from execution by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="ef258-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**\_stato esecuzione \_ MP \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="ef258-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP\_EXECUTION\_STATUS\_ALLOWED**</span></span>
</dt> <dd>

<span data-ttu-id="ef258-114">Consentito per l'esecuzione con mini-filtro.</span><span class="sxs-lookup"><span data-stu-id="ef258-114">Allowed to execute by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="ef258-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**\_stato esecuzione MP in \_ \_ esecuzione**</span><span class="sxs-lookup"><span data-stu-id="ef258-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**MP\_EXECUTION\_STATUS\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="ef258-116">È in corso l'esecuzione della minaccia.</span><span class="sxs-lookup"><span data-stu-id="ef258-116">Threat is executing.</span></span>

</dd> <dt>

<span data-ttu-id="ef258-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**\_stato esecuzione \_ MP \_ non in \_ esecuzione**</span><span class="sxs-lookup"><span data-stu-id="ef258-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP\_EXECUTION\_STATUS\_NOT\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="ef258-118">La minaccia non è in esecuzione ed è disponibile solo dal motore durante la correzione.</span><span class="sxs-lookup"><span data-stu-id="ef258-118">Threat is not executing, and is only available from the engine during remediation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef258-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef258-119">Requirements</span></span>



| <span data-ttu-id="ef258-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef258-120">Requirement</span></span> | <span data-ttu-id="ef258-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ef258-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef258-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef258-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ef258-123">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ef258-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ef258-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef258-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ef258-125">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ef258-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ef258-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef258-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef258-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef258-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





