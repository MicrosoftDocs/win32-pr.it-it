---
title: Metodo RegisteredTask. getruntimes
description: Per gli script, ottiene le ore pianificate per l'esecuzione dell'attività registrata in un determinato periodo di tempo.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Metodo getruntimes Utilità di pianificazione
- Metodo getruntimes Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo getruntimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c15aba82c5515578a3c58a485e47718d09176483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518502"
---
# <a name="registeredtaskgetruntimes-method"></a><span data-ttu-id="f31d4-106">Metodo RegisteredTask. getruntimes</span><span class="sxs-lookup"><span data-stu-id="f31d4-106">RegisteredTask.GetRunTimes method</span></span>

<span data-ttu-id="f31d4-107">Per gli script, ottiene le ore pianificate per l'esecuzione dell'attività registrata in un determinato periodo di tempo.</span><span class="sxs-lookup"><span data-stu-id="f31d4-107">For scripting, gets the times that the registered task is scheduled to run during a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="f31d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f31d4-108">Syntax</span></span>


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a><span data-ttu-id="f31d4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f31d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f31d4-110">*inizia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f31d4-110">*begin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31d4-111">Ora di inizio per la query.</span><span class="sxs-lookup"><span data-stu-id="f31d4-111">The starting time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="f31d4-112">*fine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f31d4-112">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f31d4-113">Ora di fine della query.</span><span class="sxs-lookup"><span data-stu-id="f31d4-113">The ending time for the query.</span></span>

</dd> <dt>

<span data-ttu-id="f31d4-114">*numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f31d4-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f31d4-115">Numero di volte pianificate in cui l'attività viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="f31d4-115">The number of scheduled times the task will run.</span></span>

</dd> <dt>

<span data-ttu-id="f31d4-116">*rgstTaskTimes* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f31d4-116">*rgstTaskTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f31d4-117">Orari pianificati in cui l'attività viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="f31d4-117">The scheduled times that the task will run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f31d4-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f31d4-118">Return value</span></span>

<span data-ttu-id="f31d4-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f31d4-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f31d4-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="f31d4-120">Remarks</span></span>

<span data-ttu-id="f31d4-121">Se l'attività registrata contiene trigger disabilitati singolarmente, questi trigger avranno comunque effetto sul successivo runtime pianificato che viene restituito anche se sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="f31d4-121">If the registered task contains triggers that are individually disabled, these triggers will still affect the next scheduled run time that is returned even though they are disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="f31d4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f31d4-122">Requirements</span></span>



| <span data-ttu-id="f31d4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f31d4-123">Requirement</span></span> | <span data-ttu-id="f31d4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f31d4-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f31d4-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f31d4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f31d4-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f31d4-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f31d4-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f31d4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f31d4-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f31d4-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f31d4-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f31d4-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="f31d4-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f31d4-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f31d4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f31d4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f31d4-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f31d4-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31d4-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f31d4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31d4-134">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="f31d4-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f31d4-135">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="f31d4-135">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





