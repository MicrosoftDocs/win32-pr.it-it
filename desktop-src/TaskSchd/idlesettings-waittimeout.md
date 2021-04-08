---
title: Proprietà IdleSettings. WaitTimeout
description: Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.
ms.assetid: 1be1c62b-bab0-41f8-9f64-e778aba4891f
keywords:
- Utilità di pianificazione proprietà WaitTimeout
- Utilità di pianificazione proprietà WaitTimeout, oggetto IdleSettings
- Oggetto IdleSettings Utilità di pianificazione, proprietà WaitTimeout
topic_type:
- apiref
api_name:
- IdleSettings.WaitTimeout
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb8e2abbd200b2c10eaefeafe2082a00be636a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048466"
---
# <a name="idlesettingswaittimeout-property"></a><span data-ttu-id="83e0b-106">Proprietà IdleSettings. WaitTimeout</span><span class="sxs-lookup"><span data-stu-id="83e0b-106">IdleSettings.WaitTimeout property</span></span>

<span data-ttu-id="83e0b-107">Per gli script, ottiene o imposta un valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="83e0b-107">For scripting, gets or sets a value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="83e0b-108">Se per questa proprietà non viene specificato alcun valore, il servizio Utilità di pianificazione attenderà per un periodo di tempo indefinito che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="83e0b-108">If no value is specified for this property, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e0b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83e0b-109">Syntax</span></span>


```VB
IdleSettings.WaitTimeout As String
```



## <a name="property-value"></a><span data-ttu-id="83e0b-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="83e0b-110">Property value</span></span>

<span data-ttu-id="83e0b-111">Valore che indica l'intervallo di tempo durante il quale il Utilità di pianificazione attenderà che si verifichi una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="83e0b-111">A value that indicates the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="83e0b-112">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="83e0b-112">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="83e0b-113">Il tempo minimo consentito è pari a 1 minuto.</span><span class="sxs-lookup"><span data-stu-id="83e0b-113">The minimum time allowed is 1 minute.</span></span> <span data-ttu-id="83e0b-114">Se questo valore è **null**, il ritardo verrà impostato sul valore predefinito di 1 ora.</span><span class="sxs-lookup"><span data-stu-id="83e0b-114">If this value is **NULL**, then the delay will be set to the default of 1 hour.</span></span>

## <a name="remarks"></a><span data-ttu-id="83e0b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="83e0b-115">Remarks</span></span>

<span data-ttu-id="83e0b-116">Durante la lettura o la scrittura di codice XML per un'attività, questa impostazione viene specificata nell'elemento [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) dello schema utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="83e0b-116">When reading or writing XML for a task, this setting is specified in the [**WaitTimeout**](taskschedulerschema-waittimeout-idlesettingstype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="83e0b-117">Se un'attività viene attivata da un trigger inattivo, la proprietà **IdleSettings. WaitTimeout** viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="83e0b-117">If a task is triggered by an idle trigger, then the **IdleSettings.WaitTimeout** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="83e0b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83e0b-118">Requirements</span></span>



| <span data-ttu-id="83e0b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="83e0b-119">Requirement</span></span> | <span data-ttu-id="83e0b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="83e0b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="83e0b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83e0b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="83e0b-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83e0b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="83e0b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83e0b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="83e0b-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83e0b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="83e0b-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="83e0b-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="83e0b-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="83e0b-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="83e0b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="83e0b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83e0b-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83e0b-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83e0b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83e0b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e0b-130">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="83e0b-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="83e0b-131">**IdleSettings**</span><span class="sxs-lookup"><span data-stu-id="83e0b-131">**IdleSettings**</span></span>](idlesettings.md)
</dt> </dl>

 

 





