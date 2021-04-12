---
title: Elemento ExecutionTimeLimit (triggerBaseType)
description: Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.
ms.assetid: f78e7c7b-d069-4920-9435-020f6e081eff
keywords:
- Utilità di pianificazione elemento ExecutionTimeLimit
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fbe56fb0431ab109b1a19030ae6ba20af55492ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478184"
---
# <a name="executiontimelimit-triggerbasetype-element"></a><span data-ttu-id="35bb9-104">Elemento ExecutionTimeLimit (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="35bb9-104">ExecutionTimeLimit (triggerBaseType) Element</span></span>

<span data-ttu-id="35bb9-105">Specifica l'intervallo di tempo massimo in cui l'attività può essere avviata dal trigger.</span><span class="sxs-lookup"><span data-stu-id="35bb9-105">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span> <span data-ttu-id="35bb9-106">Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti).</span><span class="sxs-lookup"><span data-stu-id="35bb9-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="35bb9-107">Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="35bb9-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
 />
```

<span data-ttu-id="35bb9-108">L'elemento **ExecutionTimeLimit** è definito dal tipo complesso [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="35bb9-108">The **ExecutionTimeLimit** element is defined by the [**triggerBaseType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="35bb9-109">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="35bb9-109">Parent element</span></span>



| <span data-ttu-id="35bb9-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="35bb9-110">Element</span></span>                                                                                     | <span data-ttu-id="35bb9-111">Derivato da</span><span class="sxs-lookup"><span data-stu-id="35bb9-111">Derived from</span></span>                                                                               | <span data-ttu-id="35bb9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35bb9-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35bb9-113">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb9-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="35bb9-114">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb9-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="35bb9-115">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="35bb9-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="35bb9-116">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb9-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="35bb9-117">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb9-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="35bb9-118">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="35bb9-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="35bb9-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb9-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="35bb9-120">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb9-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="35bb9-121">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="35bb9-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="35bb9-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb9-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="35bb9-123">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb9-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="35bb9-124">Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="35bb9-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="35bb9-125">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb9-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="35bb9-126">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb9-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="35bb9-127">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="35bb9-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="35bb9-128">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb9-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="35bb9-129">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb9-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="35bb9-130">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="35bb9-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="35bb9-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="35bb9-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="35bb9-132">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="35bb9-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="35bb9-133">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="35bb9-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="35bb9-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="35bb9-134">Remarks</span></span>

<span data-ttu-id="35bb9-135">Per lo sviluppo di script, il limite di tempo di esecuzione viene specificato utilizzando la [**Trigger.Exeproprietà cutionTimeLimit**](trigger-executiontimelimit.md) ereditata dagli oggetti trigger all.</span><span class="sxs-lookup"><span data-stu-id="35bb9-135">For scripting development, the execution time limit is specified using the [**Trigger.ExecutionTimeLimit**](trigger-executiontimelimit.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="35bb9-136">Per lo sviluppo in C++, il limite di tempo di esecuzione viene specificato tramite la proprietà [**ITrigger:: ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) ereditata dalle interfacce del trigger all.</span><span class="sxs-lookup"><span data-stu-id="35bb9-136">For C++ development, the execution time limit is specified using the [**ITrigger::ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit) property that is inherited by the all trigger interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="35bb9-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35bb9-137">Requirements</span></span>



| <span data-ttu-id="35bb9-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="35bb9-138">Requirement</span></span> | <span data-ttu-id="35bb9-139">Valore</span><span class="sxs-lookup"><span data-stu-id="35bb9-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="35bb9-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35bb9-140">Minimum supported client</span></span><br/> | <span data-ttu-id="35bb9-141">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35bb9-141">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="35bb9-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35bb9-142">Minimum supported server</span></span><br/> | <span data-ttu-id="35bb9-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35bb9-143">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="35bb9-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35bb9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35bb9-145">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="35bb9-145">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="35bb9-146">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="35bb9-146">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





