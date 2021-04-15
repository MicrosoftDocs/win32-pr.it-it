---
title: Proprietà TaskSettings. RunOnlyIfIdle
description: Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività.
ms.assetid: fca1d98e-0544-4301-a709-1e0dae762e07
keywords:
- Utilità di pianificazione proprietà RunOnlyIfIdle
- Utilità di pianificazione proprietà RunOnlyIfIdle, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà RunOnlyIfIdle
topic_type:
- apiref
api_name:
- TaskSettings.RunOnlyIfIdle
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8256b2a3d1dd96db9a8f29b49ce10f6c2fdb266d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400466"
---
# <a name="tasksettingsrunonlyifidle-property"></a><span data-ttu-id="bb357-106">Proprietà TaskSettings. RunOnlyIfIdle</span><span class="sxs-lookup"><span data-stu-id="bb357-106">TaskSettings.RunOnlyIfIdle property</span></span>

<span data-ttu-id="bb357-107">Per gli script, ottiene o imposta un valore booleano che indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="bb357-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span>

<span data-ttu-id="bb357-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="bb357-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb357-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb357-109">Syntax</span></span>


```VB
TaskSettings.RunOnlyIfIdle As Boolean
```



## <a name="property-value"></a><span data-ttu-id="bb357-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb357-110">Property value</span></span>

<span data-ttu-id="bb357-111">Se true, la proprietà indica che il Utilità di pianificazione eseguirà l'attività solo se il computer si trova in una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="bb357-111">If True, the property indicates that the Task Scheduler will run the task only if the computer is in an idle condition.</span></span> <span data-ttu-id="bb357-112">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="bb357-112">The default is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb357-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb357-113">Remarks</span></span>

<span data-ttu-id="bb357-114">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="bb357-114">When reading or writing XML for a task, this setting is specified in the [**RunOnlyIfIdle**](taskschedulerschema-runonlyifidle-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb357-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb357-115">Requirements</span></span>



| <span data-ttu-id="bb357-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb357-116">Requirement</span></span> | <span data-ttu-id="bb357-117">Valore</span><span class="sxs-lookup"><span data-stu-id="bb357-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb357-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb357-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb357-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb357-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bb357-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb357-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb357-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb357-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb357-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="bb357-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb357-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb357-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb357-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bb357-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb357-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb357-125"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb357-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb357-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb357-127">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bb357-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





