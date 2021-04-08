---
title: Proprietà trigger. StartBoundary
description: Per gli script, ottiene o imposta la data e l'ora di attivazione del trigger.
ms.assetid: 0687cdda-e72c-47cd-ac0c-0de2f8afc3e8
keywords:
- Utilità di pianificazione proprietà StartBoundary
- Utilità di pianificazione proprietà StartBoundary, oggetto trigger
- Utilità di pianificazione oggetto trigger, proprietà StartBoundary
topic_type:
- apiref
api_name:
- Trigger.StartBoundary
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 141e7e4d80d090e92ecb951917f60f972587d4b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740794"
---
# <a name="triggerstartboundary-property"></a><span data-ttu-id="7cef4-106">Proprietà trigger. StartBoundary</span><span class="sxs-lookup"><span data-stu-id="7cef4-106">Trigger.StartBoundary property</span></span>

<span data-ttu-id="7cef4-107">Per gli script, ottiene o imposta la data e l'ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="7cef4-107">For scripting, gets or sets the date and time when the trigger is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cef4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cef4-108">Syntax</span></span>


```VB
Trigger.StartBoundary As String
```



## <a name="property-value"></a><span data-ttu-id="7cef4-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7cef4-109">Property value</span></span>

<span data-ttu-id="7cef4-110">Data e ora di attivazione del trigger.</span><span class="sxs-lookup"><span data-stu-id="7cef4-110">The date and time when the trigger is activated.</span></span> <span data-ttu-id="7cef4-111">Il formato di data e ora deve essere il seguente: AAAA-MM-GGThh: MM: SS (+-) HH: MM.</span><span class="sxs-lookup"><span data-stu-id="7cef4-111">The date and time must be in the following format: YYYY-MM-DDTHH:MM:SS(+-)HH:MM.</span></span> <span data-ttu-id="7cef4-112">Ad esempio, la data dell'11 ottobre 2005 alle 1:21:17 nel fuso orario del Pacifico viene scritta come 2005-10-11T13:21:17-08:00.</span><span class="sxs-lookup"><span data-stu-id="7cef4-112">For example the date October 11th, 2005 at 1:21:17 in the Pacific Time zone would be written as 2005-10-11T13:21:17-08:00.</span></span> <span data-ttu-id="7cef4-113">La sezione (+-) HH: MM del formato descrive il fuso orario come un determinato numero di ore in anticipo o in base all'ora UTC (ora di Greenwich).</span><span class="sxs-lookup"><span data-stu-id="7cef4-113">The (+-)HH:MM section of the format describes the time zone as a certain number of hours ahead or behind Coordinated Universal Time (Greenwich Mean Time).</span></span>

## <a name="remarks"></a><span data-ttu-id="7cef4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cef4-114">Remarks</span></span>

<span data-ttu-id="7cef4-115">Durante la lettura o la scrittura di codice XML per un'attività, il limite di avvio del trigger viene specificato nell'elemento [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="7cef4-115">When reading or writing XML for a task, the trigger start boundary is specified in the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cef4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cef4-116">Requirements</span></span>



| <span data-ttu-id="7cef4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cef4-117">Requirement</span></span> | <span data-ttu-id="7cef4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7cef4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cef4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cef4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7cef4-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cef4-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7cef4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cef4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7cef4-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7cef4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7cef4-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="7cef4-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="7cef4-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7cef4-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7cef4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7cef4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cef4-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cef4-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cef4-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cef4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cef4-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7cef4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





