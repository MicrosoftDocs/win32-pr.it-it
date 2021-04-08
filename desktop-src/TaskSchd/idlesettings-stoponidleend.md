---
title: Proprietà IdleSettings. StopOnIdleEnd
description: Per la creazione di script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.
ms.assetid: 5908bf6b-227a-4234-a741-82cf38163171
keywords:
- Utilità di pianificazione proprietà StopOnIdleEnd
- Utilità di pianificazione proprietà StopOnIdleEnd, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, proprietà StopOnIdleEnd
topic_type:
- apiref
api_name:
- IdleSettings.StopOnIdleEnd
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f475c0a05d43cf0fbdd7097c1ee083f9040b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873493"
---
# <a name="idlesettingsstoponidleend-property"></a><span data-ttu-id="34cd7-106">Proprietà IdleSettings. StopOnIdleEnd</span><span class="sxs-lookup"><span data-stu-id="34cd7-106">IdleSettings.StopOnIdleEnd property</span></span>

<span data-ttu-id="34cd7-107">Per la creazione di script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="34cd7-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="34cd7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34cd7-108">Syntax</span></span>


```VB
IdleSettings.StopOnIdleEnd As Boolean
```



## <a name="property-value"></a><span data-ttu-id="34cd7-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="34cd7-109">Property value</span></span>

<span data-ttu-id="34cd7-110">Valore booleano che indica che il Utilità di pianificazione terminerà l'attività se la condizione di inattività termina prima del completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="34cd7-110">A Boolean value that indicates that the Task Scheduler will terminate the task if the idle condition ends before the task is completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="34cd7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="34cd7-111">Remarks</span></span>

<span data-ttu-id="34cd7-112">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="34cd7-112">When reading or writing XML for a task, this setting is specified in the [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="34cd7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34cd7-113">Requirements</span></span>



| <span data-ttu-id="34cd7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="34cd7-114">Requirement</span></span> | <span data-ttu-id="34cd7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="34cd7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34cd7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34cd7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="34cd7-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34cd7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="34cd7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34cd7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="34cd7-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34cd7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="34cd7-120">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="34cd7-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="34cd7-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="34cd7-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="34cd7-122">DLL</span><span class="sxs-lookup"><span data-stu-id="34cd7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34cd7-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34cd7-123"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34cd7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34cd7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34cd7-125">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="34cd7-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="34cd7-126">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="34cd7-126">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





