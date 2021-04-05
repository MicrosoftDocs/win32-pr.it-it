---
title: Struttura BG_JOB_TIMES (Deliveryoptimization. h)
description: La struttura BG_JOB_TIMES fornisce timestamp relativi ai processi.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Struttura BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740322"
---
# <a name="bg_job_times-structure"></a><span data-ttu-id="f161b-104">Struttura BG_JOB_TIMES</span><span class="sxs-lookup"><span data-stu-id="f161b-104">BG_JOB_TIMES structure</span></span>

<span data-ttu-id="f161b-105">La struttura **BG_JOB_TIMES** fornisce timestamp relativi ai processi.</span><span class="sxs-lookup"><span data-stu-id="f161b-105">The **BG_JOB_TIMES** structure provides job-related time stamps.</span></span>

## <a name="syntax"></a><span data-ttu-id="f161b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f161b-106">Syntax</span></span>


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a><span data-ttu-id="f161b-107">Members</span><span class="sxs-lookup"><span data-stu-id="f161b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f161b-108">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="f161b-108">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="f161b-109">Ora di creazione del processo.</span><span class="sxs-lookup"><span data-stu-id="f161b-109">Time the job was created.</span></span> <span data-ttu-id="f161b-110">L'ora viene specificata come [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="f161b-110">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="f161b-111">**ModificationTime**</span><span class="sxs-lookup"><span data-stu-id="f161b-111">**ModificationTime**</span></span>
</dt> <dd>

<span data-ttu-id="f161b-112">Ora dell'Ultima modifica apportata al processo oppure byte trasferiti.</span><span class="sxs-lookup"><span data-stu-id="f161b-112">Time the job was last modified or bytes were transferred.</span></span> <span data-ttu-id="f161b-113">L'aggiunta di file o la chiamata di uno dei metodi set nelle interfacce [ \* *Metodo ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) modifica questo valore.</span><span class="sxs-lookup"><span data-stu-id="f161b-113">Adding files or calling any of the set methods in the [\**IBackgroundCopyJob\** _](/previous-versions//mt811348(v=vs.85)) interfaces changes this value.</span></span> <span data-ttu-id="f161b-114">Inoltre, le modifiche allo stato del processo e alla chiamata dei metodi [_ *Suspend* \*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)e [**complete**](ibackgroundcopyjob-complete.md) cambiano questo valore.</span><span class="sxs-lookup"><span data-stu-id="f161b-114">In addition, changes to the state of the job and calling the [_ *Suspend*\*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md), and [**Complete**](ibackgroundcopyjob-complete.md) methods change this value.</span></span> <span data-ttu-id="f161b-115">L'ora viene specificata come [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="f161b-115">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="f161b-116">**TransferCompletionTime**</span><span class="sxs-lookup"><span data-stu-id="f161b-116">**TransferCompletionTime**</span></span>
</dt> <dd>

<span data-ttu-id="f161b-117">Ora in cui il processo è entrato nello stato BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="f161b-117">Time the job entered the BG_JOB_STATE_TRANSFERRED state.</span></span> <span data-ttu-id="f161b-118">L'ora viene specificata come [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="f161b-118">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f161b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f161b-119">Requirements</span></span>



| <span data-ttu-id="f161b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f161b-120">Requirement</span></span> | <span data-ttu-id="f161b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f161b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f161b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f161b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f161b-123">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="f161b-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f161b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f161b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f161b-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f161b-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f161b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f161b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f161b-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f161b-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f161b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f161b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f161b-129">**Metodo ibackgroundcopyjob:: gettimes**</span><span class="sxs-lookup"><span data-stu-id="f161b-129">**IBackgroundCopyJob::GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

