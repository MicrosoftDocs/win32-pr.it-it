---
title: Proprietà TaskSettings. DeleteExpiredTaskAfter
description: Per gli script, ottiene o imposta il periodo di tempo durante il quale il Utilità di pianificazione resterà in attesa prima di eliminare l'attività dopo la scadenza.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- Utilità di pianificazione proprietà DeleteExpiredTaskAfter
- Utilità di pianificazione proprietà DeleteExpiredTaskAfter, oggetto TaskSettings
- Oggetto TaskSettings Utilità di pianificazione, proprietà DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475958"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a><span data-ttu-id="04a0b-106">Proprietà TaskSettings. DeleteExpiredTaskAfter</span><span class="sxs-lookup"><span data-stu-id="04a0b-106">TaskSettings.DeleteExpiredTaskAfter property</span></span>

<span data-ttu-id="04a0b-107">Per gli script, ottiene o imposta il periodo di tempo durante il quale il Utilità di pianificazione resterà in attesa prima di eliminare l'attività dopo la scadenza.</span><span class="sxs-lookup"><span data-stu-id="04a0b-107">For scripting, gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="04a0b-108">Se per questa proprietà non viene specificato alcun valore, il servizio Utilità di pianificazione non eliminerà l'attività.</span><span class="sxs-lookup"><span data-stu-id="04a0b-108">If no value is specified for this property, then the Task Scheduler service will not delete the task.</span></span>

<span data-ttu-id="04a0b-109">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="04a0b-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a0b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04a0b-110">Syntax</span></span>


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a><span data-ttu-id="04a0b-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="04a0b-111">Property value</span></span>

<span data-ttu-id="04a0b-112">Stringa che ottiene o imposta il periodo di tempo durante il quale il Utilità di pianificazione resterà in attesa prima di eliminare l'attività dopo la scadenza.</span><span class="sxs-lookup"><span data-stu-id="04a0b-112">A string that gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="04a0b-113">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="04a0b-113">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="04a0b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="04a0b-114">Remarks</span></span>

<span data-ttu-id="04a0b-115">Un'attività scade dopo il superamento del limite finale per tutti i trigger associati all'attività.</span><span class="sxs-lookup"><span data-stu-id="04a0b-115">A task expires after the end boundary has been exceeded for all triggers associated with the task.</span></span> <span data-ttu-id="04a0b-116">Il limite finale per un trigger viene specificato dalla proprietà [EndBoundary](trigger-endboundary.md) ereditata da tutti gli oggetti trigger.</span><span class="sxs-lookup"><span data-stu-id="04a0b-116">The end boundary for a trigger is specified by the [EndBoundary](trigger-endboundary.md) property inherited by all trigger objects.</span></span>

<span data-ttu-id="04a0b-117">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="04a0b-117">When reading or writing XML for a task, this setting is specified in the [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="04a0b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04a0b-118">Requirements</span></span>



| <span data-ttu-id="04a0b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="04a0b-119">Requirement</span></span> | <span data-ttu-id="04a0b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="04a0b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04a0b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04a0b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="04a0b-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04a0b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="04a0b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04a0b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="04a0b-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04a0b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04a0b-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="04a0b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="04a0b-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04a0b-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04a0b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="04a0b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04a0b-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04a0b-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04a0b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04a0b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a0b-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="04a0b-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





