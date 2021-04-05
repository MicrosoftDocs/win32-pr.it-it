---
title: Enumerazione BG_JOB_PRIORITY (Deliveryoptimization. h)
description: L'enumerazione BG_JOB_PRIORITY definisce i valori costanti che specificano il livello di priorità di un processo.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Enumerazione BG_JOB_PRIORITY
- Enumerazione BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048229"
---
# <a name="bg_job_priority-enumeration"></a><span data-ttu-id="51fdf-105">Enumerazione BG_JOB_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="51fdf-105">BG_JOB_PRIORITY enumeration</span></span>

<span data-ttu-id="51fdf-106">L'enumerazione **BG_JOB_PRIORITY** definisce i valori costanti che specificano il livello di priorità di un processo.</span><span class="sxs-lookup"><span data-stu-id="51fdf-106">The **BG_JOB_PRIORITY** enumeration defines the constant values that specify the priority level of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fdf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51fdf-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a><span data-ttu-id="51fdf-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="51fdf-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="51fdf-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span><span class="sxs-lookup"><span data-stu-id="51fdf-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span></span>
</dt> <dd>

<span data-ttu-id="51fdf-110">Trasferisce il processo in primo piano.</span><span class="sxs-lookup"><span data-stu-id="51fdf-110">Transfers the job in the foreground.</span></span> <span data-ttu-id="51fdf-111">I trasferimenti in primo piano competono per la larghezza di banda di rete con altre applicazioni, che possono ostacolare l'esperienza di rete dell'utente.</span><span class="sxs-lookup"><span data-stu-id="51fdf-111">Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience.</span></span> <span data-ttu-id="51fdf-112">Questo è il livello di priorità più alto.</span><span class="sxs-lookup"><span data-stu-id="51fdf-112">This is the highest priority level.</span></span>

</dd> <dt>

<span data-ttu-id="51fdf-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span><span class="sxs-lookup"><span data-stu-id="51fdf-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="51fdf-114">Trasferisce il processo in background.</span><span class="sxs-lookup"><span data-stu-id="51fdf-114">Transfers the job in the background.</span></span> <span data-ttu-id="51fdf-115">I trasferimenti in background utilizzano una piccola percentuale di larghezza di banda di rete.</span><span class="sxs-lookup"><span data-stu-id="51fdf-115">Background transfers use a small percentage of network bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="51fdf-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span><span class="sxs-lookup"><span data-stu-id="51fdf-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="51fdf-117">Il comportamento è lo stesso per tutti i processi non in primo piano.</span><span class="sxs-lookup"><span data-stu-id="51fdf-117">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="51fdf-118">Per informazioni dettagliate, vedere i commenti in BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="51fdf-118">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> <dt>

<span data-ttu-id="51fdf-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span><span class="sxs-lookup"><span data-stu-id="51fdf-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="51fdf-120">Il comportamento è lo stesso per tutti i processi non in primo piano.</span><span class="sxs-lookup"><span data-stu-id="51fdf-120">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="51fdf-121">Per informazioni dettagliate, vedere i commenti in BG_JOB_PRIORITY_HIGH.</span><span class="sxs-lookup"><span data-stu-id="51fdf-121">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51fdf-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="51fdf-122">Remarks</span></span>

<span data-ttu-id="51fdf-123">È possibile eseguire contemporaneamente più trasferimenti in primo piano e in background.</span><span class="sxs-lookup"><span data-stu-id="51fdf-123">Multiple foreground and background transfers can take place simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fdf-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51fdf-124">Requirements</span></span>



| <span data-ttu-id="51fdf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="51fdf-125">Requirement</span></span> | <span data-ttu-id="51fdf-126">Valore</span><span class="sxs-lookup"><span data-stu-id="51fdf-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fdf-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51fdf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="51fdf-128">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="51fdf-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="51fdf-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51fdf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="51fdf-130">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51fdf-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="51fdf-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51fdf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="51fdf-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="51fdf-132"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51fdf-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51fdf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fdf-134">**Metodo ibackgroundcopyjob:: GetPriority**</span><span class="sxs-lookup"><span data-stu-id="51fdf-134">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[<span data-ttu-id="51fdf-135">**Metodo ibackgroundcopyjob:: sepriority**</span><span class="sxs-lookup"><span data-stu-id="51fdf-135">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





