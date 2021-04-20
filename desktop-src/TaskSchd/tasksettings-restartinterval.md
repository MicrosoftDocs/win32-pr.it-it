---
title: TaskSettings.RestartInterval - proprietà
description: Per lo scripting, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.
ms.assetid: ad6f254d-55a8-478e-984e-a459f22043b5
keywords:
- Proprietà RestartInterval Utilità di pianificazione
- Proprietà RestartInterval Utilità di pianificazione, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione proprietà , RestartInterval
topic_type:
- apiref
api_name:
- TaskSettings.RestartInterval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f127c5d434b5cb1e6dec6d8a3c68ee343fa00ffc
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734146"
---
# <a name="tasksettingsrestartinterval-property"></a><span data-ttu-id="9ec47-106">TaskSettings.RestartInterval - proprietà</span><span class="sxs-lookup"><span data-stu-id="9ec47-106">TaskSettings.RestartInterval property</span></span>

<span data-ttu-id="9ec47-107">Per lo scripting, ottiene o imposta un valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="9ec47-107">For scripting, gets or sets a value that specifies how long the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="9ec47-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="9ec47-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec47-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ec47-109">Syntax</span></span>


```VB
TaskSettings.RestartInterval As String
```



## <a name="property-value"></a><span data-ttu-id="9ec47-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9ec47-110">Property value</span></span>

<span data-ttu-id="9ec47-111">Valore che specifica per quanto tempo il Utilità di pianificazione tenterà di riavviare l'attività.</span><span class="sxs-lookup"><span data-stu-id="9ec47-111">A value that specifies how long the Task Scheduler will attempt to restart the task.</span></span> <span data-ttu-id="9ec47-112">Se questa proprietà è impostata, deve essere impostata anche la proprietà [**RestartCount.**](tasksettings-restartcount.md)</span><span class="sxs-lookup"><span data-stu-id="9ec47-112">If this property is set, the [**RestartCount**](tasksettings-restartcount.md) property must also be set.</span></span> <span data-ttu-id="9ec47-113">Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti).</span><span class="sxs-lookup"><span data-stu-id="9ec47-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="9ec47-114">Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="9ec47-114">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ec47-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ec47-115">Remarks</span></span>

<span data-ttu-id="9ec47-116">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata [**nell'elemento Interval**](taskschedulerschema-interval-restarttype-element.md) dello schema Utilità di pianificazione dati.</span><span class="sxs-lookup"><span data-stu-id="9ec47-116">When reading or writing XML for a task, this setting is specified in the [**Interval**](taskschedulerschema-interval-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec47-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ec47-117">Requirements</span></span>



| <span data-ttu-id="9ec47-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ec47-118">Requirement</span></span> | <span data-ttu-id="9ec47-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9ec47-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec47-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ec47-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec47-121">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9ec47-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9ec47-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ec47-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec47-123">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9ec47-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9ec47-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="9ec47-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ec47-125"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ec47-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9ec47-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9ec47-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ec47-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ec47-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec47-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ec47-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec47-129">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="9ec47-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





