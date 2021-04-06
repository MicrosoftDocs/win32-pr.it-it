---
title: Proprietà TaskSettings. AllowHardTerminate
description: Per la creazione di script, ottiene o imposta un valore booleano che indica che l'attività può essere terminata dal servizio Utilità di pianificazione usando TerminateProcess.
ms.assetid: 1dfd692e-efbe-41a2-8dbd-b14cf26bbcb7
keywords:
- Utilità di pianificazione proprietà AllowHardTerminate
- Utilità di pianificazione proprietà AllowHardTerminate, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà AllowHardTerminate
topic_type:
- apiref
api_name:
- TaskSettings.AllowHardTerminate
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c38e117ebc3d2175b952f01698987ccb65f7af5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742415"
---
# <a name="tasksettingsallowhardterminate-property"></a><span data-ttu-id="d2388-106">Proprietà TaskSettings. AllowHardTerminate</span><span class="sxs-lookup"><span data-stu-id="d2388-106">TaskSettings.AllowHardTerminate property</span></span>

<span data-ttu-id="d2388-107">Per la creazione di script, ottiene o imposta un valore booleano che indica che l'attività può essere terminata dal servizio Utilità di pianificazione usando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="d2388-107">For scripting, gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="d2388-108">Il servizio tenterà di chiudere l'attività in esecuzione inviando la notifica di [**\_ chiusura WM**](../winmsg/wm-close.md) . se l'attività non risponde, l'attività verrà terminata solo se questa proprietà è impostata su true.</span><span class="sxs-lookup"><span data-stu-id="d2388-108">The service will try to close the running task by sending the [**WM\_CLOSE**](../winmsg/wm-close.md) notification, and if the task does not respond, the task will be terminated only if this property is set to true.</span></span>

<span data-ttu-id="d2388-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d2388-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2388-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2388-110">Syntax</span></span>


```VB
TaskSettings.AllowHardTerminate As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d2388-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d2388-111">Property value</span></span>

<span data-ttu-id="d2388-112">Se true, l'attività può essere terminata usando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span><span class="sxs-lookup"><span data-stu-id="d2388-112">If True, the task can be terminated by using [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess).</span></span> <span data-ttu-id="d2388-113">Se false, l'attività non può essere terminata utilizzando **TerminateProcess**.</span><span class="sxs-lookup"><span data-stu-id="d2388-113">If False, the task cannot be terminated by using **TerminateProcess**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2388-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2388-114">Remarks</span></span>

<span data-ttu-id="d2388-115">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d2388-115">When reading or writing XML for a task, this setting is specified in the [AllowHardTerminate](taskschedulerschema-allowhardterminate-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2388-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2388-116">Requirements</span></span>



| <span data-ttu-id="d2388-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2388-117">Requirement</span></span> | <span data-ttu-id="d2388-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d2388-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2388-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2388-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2388-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2388-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d2388-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2388-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2388-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2388-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d2388-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d2388-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d2388-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d2388-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d2388-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d2388-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2388-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2388-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2388-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2388-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2388-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="d2388-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

