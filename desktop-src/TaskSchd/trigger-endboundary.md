---
title: Proprietà trigger. EndBoundary
description: Per gli script, ottiene o imposta la data e l'ora di disattivazione del trigger. Il trigger non può avviare l'attività dopo che è stata disattivata.
ms.assetid: f34e6ba8-f6ef-43a0-8e3a-76c6a5f1ac04
keywords:
- Utilità di pianificazione proprietà EndBoundary
- Utilità di pianificazione proprietà EndBoundary, oggetto trigger
- Utilità di pianificazione oggetto trigger, proprietà EndBoundary
topic_type:
- apiref
api_name:
- Trigger.EndBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b385dddf186484bc17cff9f92d979cd64381335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048146"
---
# <a name="triggerendboundary-property"></a><span data-ttu-id="5d064-107">Proprietà trigger. EndBoundary</span><span class="sxs-lookup"><span data-stu-id="5d064-107">Trigger.EndBoundary property</span></span>

<span data-ttu-id="5d064-108">Per gli script, ottiene o imposta la data e l'ora di disattivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="5d064-108">For scripting, gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="5d064-109">Il trigger non può avviare l'attività dopo che è stata disattivata.</span><span class="sxs-lookup"><span data-stu-id="5d064-109">The trigger cannot start the task after it is deactivated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d064-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d064-110">Syntax</span></span>


```VB
Trigger.EndBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="5d064-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5d064-111">Property value</span></span>

<span data-ttu-id="5d064-112">Data e ora in cui il trigger viene disattivato.</span><span class="sxs-lookup"><span data-stu-id="5d064-112">The date and time when the trigger is deactivated.</span></span> <span data-ttu-id="5d064-113">Il formato di data e ora deve essere il seguente: AAAA-MM-GGThh: MM: SS (+-) HH: MM.</span><span class="sxs-lookup"><span data-stu-id="5d064-113">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="5d064-114">Ad esempio, la data dell'11 ottobre 2005 alle 1:21:17 nel fuso orario del Pacifico viene scritta come 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="5d064-114">For example the date October 11th, 2005 at 1:21:17 in the Pacific time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="5d064-115">La sezione (+-) HH: MM del formato descrive il fuso orario come un determinato numero di ore in anticipo o in base all'ora UTC (ora di Greenwich).</span><span class="sxs-lookup"><span data-stu-id="5d064-115">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="5d064-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d064-116">Remarks</span></span>

<span data-ttu-id="5d064-117">Durante la lettura o la scrittura di codice XML per un'attività, la proprietà Enabled viene specificata utilizzando l'elemento [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="5d064-117">When reading or writing XML for a task, the enabled property is specified using the [**EndBoundary**](taskschedulerschema-endboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d064-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d064-118">Requirements</span></span>



| <span data-ttu-id="5d064-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d064-119">Requirement</span></span> | <span data-ttu-id="5d064-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5d064-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d064-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d064-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d064-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d064-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5d064-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5d064-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d064-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d064-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d064-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="5d064-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="5d064-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5d064-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5d064-127">DLL</span><span class="sxs-lookup"><span data-stu-id="5d064-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d064-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d064-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d064-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d064-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d064-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="5d064-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





