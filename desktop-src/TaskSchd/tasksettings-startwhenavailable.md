---
title: Proprietà TaskSettings. StartWhenAvailable
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il tempo pianificato.
ms.assetid: 911de67c-baf8-4346-9b4c-e39e5f96c0fe
keywords:
- Utilità di pianificazione proprietà StartWhenAvailable
- Utilità di pianificazione proprietà StartWhenAvailable, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà StartWhenAvailable
topic_type:
- apiref
api_name:
- TaskSettings.StartWhenAvailable
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63325fbf7aa9186e5748294c2ef57302efa0c79b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478364"
---
# <a name="tasksettingsstartwhenavailable-property"></a><span data-ttu-id="e2840-106">Proprietà TaskSettings. StartWhenAvailable</span><span class="sxs-lookup"><span data-stu-id="e2840-106">TaskSettings.StartWhenAvailable property</span></span>

<span data-ttu-id="e2840-107">Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il tempo pianificato.</span><span class="sxs-lookup"><span data-stu-id="e2840-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span>

<span data-ttu-id="e2840-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e2840-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2840-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e2840-109">Syntax</span></span>


```VB
TaskSettings.StartWhenAvailable As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e2840-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e2840-110">Property value</span></span>

<span data-ttu-id="e2840-111">Se true, la proprietà indica che il Utilità di pianificazione può avviare l'attività in qualsiasi momento dopo che è trascorso il tempo pianificato.</span><span class="sxs-lookup"><span data-stu-id="e2840-111">If True, the property indicates that the Task Scheduler can start the task at any time after its scheduled time has passed.</span></span> <span data-ttu-id="e2840-112">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="e2840-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2840-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2840-113">Remarks</span></span>

<span data-ttu-id="e2840-114">Questa proprietà si applica solo alle attività basate sul tempo con un limite finale o attività basate sul tempo impostate per la ripetizione infinita.</span><span class="sxs-lookup"><span data-stu-id="e2840-114">This property applies only to time-based tasks with an end boundary or time-based tasks that are set to repeat infinitely.</span></span>

<span data-ttu-id="e2840-115">Le attività avviate dopo il passaggio dell'ora pianificata, a causa della proprietà [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) impostata su true, vengono accodate nella coda delle attività del servizio Utilità di pianificazione e vengono avviate dopo un ritardo.</span><span class="sxs-lookup"><span data-stu-id="e2840-115">Tasks that are started after the scheduled time has passed (because of the [**StartWhenAvailable**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_startwhenavailable) property being set to True) are queued in the Task Scheduler service's queue of tasks and they are started after a delay.</span></span> <span data-ttu-id="e2840-116">Il ritardo predefinito è di 10 minuti.</span><span class="sxs-lookup"><span data-stu-id="e2840-116">The default delay is 10 minutes.</span></span>

<span data-ttu-id="e2840-117">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e2840-117">When reading or writing XML for a task, this setting is specified in the [**StartWhenAvailable**](taskschedulerschema-startwhenavailable-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2840-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2840-118">Requirements</span></span>



| <span data-ttu-id="e2840-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2840-119">Requirement</span></span> | <span data-ttu-id="e2840-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e2840-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2840-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2840-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2840-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2840-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e2840-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2840-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2840-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2840-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2840-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e2840-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2840-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2840-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2840-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e2840-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2840-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2840-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2840-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2840-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2840-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e2840-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





