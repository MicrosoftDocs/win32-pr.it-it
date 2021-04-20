---
title: Proprietà RepetitionPattern.Interval
description: Per lo scripting, ottiene o imposta la quantità di tempo tra ogni riavvio dell'attività.
ms.assetid: c48bd304-21f3-435e-99f5-3b2da0078bb8
keywords:
- Proprietà Interval Utilità di pianificazione
- Proprietà Interval Utilità di pianificazione, oggetto RepetitionPattern
- Oggetto RepetitionPattern Utilità di pianificazione proprietà Interval
topic_type:
- apiref
api_name:
- RepetitionPattern.Interval
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1e81920fffe5c9fd58dd36a028b924f54ebe6dd
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734176"
---
# <a name="repetitionpatterninterval-property"></a><span data-ttu-id="894f6-106">Proprietà RepetitionPattern.Interval</span><span class="sxs-lookup"><span data-stu-id="894f6-106">RepetitionPattern.Interval property</span></span>

<span data-ttu-id="894f6-107">Per lo scripting, ottiene o imposta la quantità di tempo tra ogni riavvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="894f6-107">For scripting, gets or sets the amount of time between each restart of the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="894f6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="894f6-108">Syntax</span></span>


```VB
RepetitionPattern.Interval As String
```



## <a name="property-value"></a><span data-ttu-id="894f6-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="894f6-109">Property value</span></span>

<span data-ttu-id="894f6-110">Intervallo di tempo tra ogni riavvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="894f6-110">The amount of time between each restart of the task.</span></span> <span data-ttu-id="894f6-111">Il formato di questa stringa è `P<days>DT<hours>H<minutes>M<seconds>S` (ad esempio, "PT5M" è di 5 minuti, "PT1H" è 1 ora e "PT20M" è 20 minuti).</span><span class="sxs-lookup"><span data-stu-id="894f6-111">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, "PT5M" is 5 minutes, "PT1H" is 1 hour, and "PT20M" is 20 minutes).</span></span> <span data-ttu-id="894f6-112">Il tempo massimo consentito è 31 giorni e il tempo minimo consentito è 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="894f6-112">The maximum time allowed is 31 days, and the minimum time allowed is 1 minute.</span></span>

## <a name="remarks"></a><span data-ttu-id="894f6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="894f6-113">Remarks</span></span>

<span data-ttu-id="894f6-114">Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="894f6-114">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="894f6-115">Durante la lettura o la scrittura di codice XML per un'attività, l'intervallo di ripetizione viene specificato [**nell'elemento Interval**](taskschedulerschema-interval-repetitiontype-element.md) dello schema Utilità di pianificazione attività.</span><span class="sxs-lookup"><span data-stu-id="894f6-115">When reading or writing XML for a task, the repetition interval is specified in the [**Interval**](taskschedulerschema-interval-repetitiontype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="894f6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="894f6-116">Requirements</span></span>



| <span data-ttu-id="894f6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="894f6-117">Requirement</span></span> | <span data-ttu-id="894f6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="894f6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="894f6-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="894f6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="894f6-120">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="894f6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="894f6-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="894f6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="894f6-122">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="894f6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="894f6-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="894f6-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="894f6-124"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="894f6-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="894f6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="894f6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="894f6-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="894f6-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="894f6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="894f6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894f6-128">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="894f6-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





