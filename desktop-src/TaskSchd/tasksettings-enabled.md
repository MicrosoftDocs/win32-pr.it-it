---
title: Proprietà TaskSettings. Enabled
description: Per gli script, ottiene o imposta un valore booleano che indica che l'attività è abilitata. L'attività può essere eseguita solo quando questa impostazione è true.
ms.assetid: af8aa237-3402-4a82-b6ef-b713e1757d3a
keywords:
- Utilità di pianificazione proprietà abilitata
- Utilità di pianificazione proprietà Enabled, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà Enabled
topic_type:
- apiref
api_name:
- TaskSettings.Enabled
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6805d7b754ac2c3553d5fde91826ffa192b91d97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400748"
---
# <a name="tasksettingsenabled-property"></a><span data-ttu-id="98421-107">Proprietà TaskSettings. Enabled</span><span class="sxs-lookup"><span data-stu-id="98421-107">TaskSettings.Enabled property</span></span>

<span data-ttu-id="98421-108">Per gli script, ottiene o imposta un valore booleano che indica che l'attività è abilitata.</span><span class="sxs-lookup"><span data-stu-id="98421-108">For scripting, gets or sets a Boolean value that indicates that the task is enabled.</span></span> <span data-ttu-id="98421-109">L'attività può essere eseguita solo quando questa impostazione è true.</span><span class="sxs-lookup"><span data-stu-id="98421-109">The task can be performed only when this setting is True.</span></span>

<span data-ttu-id="98421-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="98421-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98421-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="98421-111">Syntax</span></span>


```VB
TaskSettings.Enabled As Boolean
```



## <a name="property-value"></a><span data-ttu-id="98421-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="98421-112">Property value</span></span>

<span data-ttu-id="98421-113">Se true, l'attività è abilitata.</span><span class="sxs-lookup"><span data-stu-id="98421-113">If True, the task is enabled.</span></span> <span data-ttu-id="98421-114">Se false, l'attività non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="98421-114">If False, the task is not enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="98421-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="98421-115">Remarks</span></span>

<span data-ttu-id="98421-116">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="98421-116">When reading or writing XML for a task, this setting is specified in the [**Enabled (settingsType)**](taskschedulerschema-enabled-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="98421-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98421-117">Requirements</span></span>



| <span data-ttu-id="98421-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="98421-118">Requirement</span></span> | <span data-ttu-id="98421-119">Valore</span><span class="sxs-lookup"><span data-stu-id="98421-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98421-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98421-120">Minimum supported client</span></span><br/> | <span data-ttu-id="98421-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98421-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="98421-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="98421-122">Minimum supported server</span></span><br/> | <span data-ttu-id="98421-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98421-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="98421-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="98421-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="98421-125"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="98421-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="98421-126">DLL</span><span class="sxs-lookup"><span data-stu-id="98421-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98421-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98421-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98421-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="98421-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98421-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="98421-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





