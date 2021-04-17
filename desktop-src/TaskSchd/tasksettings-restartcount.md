---
title: Proprietà TaskSettings. RestartCount
description: Per gli script, ottiene o imposta il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- Utilità di pianificazione proprietà RestartCount
- Utilità di pianificazione proprietà RestartCount, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà RestartCount
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400467"
---
# <a name="tasksettingsrestartcount-property"></a><span data-ttu-id="dbfd7-106">Proprietà TaskSettings. RestartCount</span><span class="sxs-lookup"><span data-stu-id="dbfd7-106">TaskSettings.RestartCount property</span></span>

<span data-ttu-id="dbfd7-107">Per gli script, ottiene o imposta il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="dbfd7-107">For scripting, gets or sets the number of times that the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="dbfd7-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="dbfd7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfd7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dbfd7-109">Syntax</span></span>


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a><span data-ttu-id="dbfd7-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="dbfd7-110">Property value</span></span>

<span data-ttu-id="dbfd7-111">Il numero di volte in cui il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="dbfd7-111">The number of times that the Task Scheduler will attempt to restart the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbfd7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="dbfd7-112">Remarks</span></span>

<span data-ttu-id="dbfd7-113">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**count**](taskschedulerschema-count-restarttype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="dbfd7-113">When reading or writing XML for a task, this setting is specified in the [**Count**](taskschedulerschema-count-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfd7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dbfd7-114">Requirements</span></span>



| <span data-ttu-id="dbfd7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfd7-115">Requirement</span></span> | <span data-ttu-id="dbfd7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dbfd7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfd7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbfd7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfd7-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbfd7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dbfd7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dbfd7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfd7-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbfd7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dbfd7-121">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="dbfd7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="dbfd7-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dbfd7-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dbfd7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dbfd7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbfd7-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbfd7-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbfd7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dbfd7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfd7-126">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="dbfd7-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





