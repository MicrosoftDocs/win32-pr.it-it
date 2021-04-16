---
title: Elemento Repetition (triggerBaseType)
description: Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Elemento di ripetizione Utilità di pianificazione
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477777"
---
# <a name="repetition-triggerbasetype-element"></a><span data-ttu-id="578b0-104">Elemento Repetition (triggerBaseType)</span><span class="sxs-lookup"><span data-stu-id="578b0-104">Repetition (triggerBaseType) Element</span></span>

<span data-ttu-id="578b0-105">Specifica la frequenza con cui viene eseguita l'attività e il tempo per cui il modello di ripetizione viene ripetuto dopo l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="578b0-105">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

<span data-ttu-id="578b0-106">L'elemento di **ripetizione** è definito dal tipo complesso [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="578b0-106">The **Repetition** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="578b0-107">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="578b0-107">Parent element</span></span>



| <span data-ttu-id="578b0-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="578b0-108">Element</span></span>                                                                                     | <span data-ttu-id="578b0-109">Derivato da</span><span class="sxs-lookup"><span data-stu-id="578b0-109">Derived from</span></span>                                                                               | <span data-ttu-id="578b0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="578b0-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="578b0-111">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="578b0-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="578b0-112">**bootTriggerType**</span><span class="sxs-lookup"><span data-stu-id="578b0-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="578b0-113">Specifica un trigger che avvia un'attività quando viene avviato il sistema.</span><span class="sxs-lookup"><span data-stu-id="578b0-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="578b0-114">**CalendarTrigger**</span><span class="sxs-lookup"><span data-stu-id="578b0-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="578b0-115">**calendarTriggerType**</span><span class="sxs-lookup"><span data-stu-id="578b0-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="578b0-116">Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="578b0-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="578b0-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="578b0-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="578b0-118">**eventTriggerType**</span><span class="sxs-lookup"><span data-stu-id="578b0-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="578b0-119">Specifica un trigger che avvia un'attività quando si verifica un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="578b0-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="578b0-120">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="578b0-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="578b0-121">**idleTriggerType**</span><span class="sxs-lookup"><span data-stu-id="578b0-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="578b0-122">Specifica un trigger che avvia un'attività quando il computer entra in uno stato di inattività.</span><span class="sxs-lookup"><span data-stu-id="578b0-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="578b0-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="578b0-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="578b0-124">**logonTriggerType**</span><span class="sxs-lookup"><span data-stu-id="578b0-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="578b0-125">Specifica un trigger che avvia un'attività quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="578b0-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="578b0-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="578b0-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="578b0-127">**registrationTriggerType**</span><span class="sxs-lookup"><span data-stu-id="578b0-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="578b0-128">Specifica un trigger che avvia un'attività quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="578b0-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="578b0-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="578b0-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="578b0-130">**timeTriggerType**</span><span class="sxs-lookup"><span data-stu-id="578b0-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="578b0-131">Specifica un trigger che avvia un'attività quando viene attivato il trigger.</span><span class="sxs-lookup"><span data-stu-id="578b0-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="child-elements"></a><span data-ttu-id="578b0-132">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="578b0-132">Child elements</span></span>



| <span data-ttu-id="578b0-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="578b0-133">Element</span></span>                                                                                   | <span data-ttu-id="578b0-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="578b0-134">Type</span></span>     | <span data-ttu-id="578b0-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="578b0-135">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="578b0-136">**Durata**</span><span class="sxs-lookup"><span data-stu-id="578b0-136">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   | <span data-ttu-id="578b0-137">duration</span><span class="sxs-lookup"><span data-stu-id="578b0-137">duration</span></span> | <span data-ttu-id="578b0-138">Specifica il tempo di ripetizione del pattern.</span><span class="sxs-lookup"><span data-stu-id="578b0-138">Specifies how long the pattern is repeated.</span></span><br/>                                                              |
| [<span data-ttu-id="578b0-139">**Interval**</span><span class="sxs-lookup"><span data-stu-id="578b0-139">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   | <span data-ttu-id="578b0-140">duration</span><span class="sxs-lookup"><span data-stu-id="578b0-140">duration</span></span> | <span data-ttu-id="578b0-141">Specifica la quantità di tempo tra ogni riavvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="578b0-141">Specifies the amount of time between each restart of the task.</span></span><br/>                                           |
| [<span data-ttu-id="578b0-142">**StopAtDurationEnd**</span><span class="sxs-lookup"><span data-stu-id="578b0-142">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="578b0-143">boolean</span><span class="sxs-lookup"><span data-stu-id="578b0-143">boolean</span></span>  | <span data-ttu-id="578b0-144">Specifica che un'istanza in esecuzione dell'attività viene arrestata alla fine della durata del modello di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="578b0-144">Specifies that a running instances of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="578b0-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="578b0-145">Remarks</span></span>

<span data-ttu-id="578b0-146">Se si specifica una durata di ripetizione per un'attività, è necessario specificare anche l'intervallo di ripetizione.</span><span class="sxs-lookup"><span data-stu-id="578b0-146">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="578b0-147">Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata cinque volte.</span><span class="sxs-lookup"><span data-stu-id="578b0-147">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="578b0-148">Le cinque ripetizioni possono essere definite dal modello seguente.</span><span class="sxs-lookup"><span data-stu-id="578b0-148">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="578b0-149">Un'attività viene avviata all'inizio del primo minuto.</span><span class="sxs-lookup"><span data-stu-id="578b0-149">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="578b0-150">L'attività successiva inizia alla fine del primo minuto.</span><span class="sxs-lookup"><span data-stu-id="578b0-150">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="578b0-151">L'attività successiva inizia alla fine del secondo minuto.</span><span class="sxs-lookup"><span data-stu-id="578b0-151">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="578b0-152">L'attività successiva inizia alla fine del terzo minuto.</span><span class="sxs-lookup"><span data-stu-id="578b0-152">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="578b0-153">L'attività successiva inizia alla fine del quarto minuto.</span><span class="sxs-lookup"><span data-stu-id="578b0-153">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="578b0-154">**Windows Server 2003, Windows XP e windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata quattro volte.</span><span class="sxs-lookup"><span data-stu-id="578b0-154">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="578b0-155">**Windows Vista, Windows 7, Windows server 2008, Windows 8 e Windows server 2012:** In genere, l'impostazione della durata della ripetizione su un multiplo esatto dell'intervallo produce i numeri descritti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="578b0-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 and Windows Server 2012:** Usually, setting the repetition duration to an exact multiple of the interval yields the numbers described above.</span></span> <span data-ttu-id="578b0-156">Tuttavia, in determinate condizioni di carico elevato, è possibile che la durata di timeout venga avviata prima che TaskScheduler possa avviare l'intervallo di attività finale.</span><span class="sxs-lookup"><span data-stu-id="578b0-156">However, under certain heavy load conditions, it is possible for the duration to timeout before TaskScheduler can launch the final task interval.</span></span>

<span data-ttu-id="578b0-157">Per lo sviluppo di script, il modello di ripetizione viene specificato utilizzando la proprietà [**trigger. ripetition**](trigger-repetition.md) ereditata da tutti gli oggetti trigger.</span><span class="sxs-lookup"><span data-stu-id="578b0-157">For scripting development, the repetition pattern is specified using the [**Trigger.Repetition**](trigger-repetition.md) property that is inherited by all the trigger objects.</span></span>

<span data-ttu-id="578b0-158">Per lo sviluppo in C++, il modello di ripetizione viene specificato utilizzando la proprietà [**ITRigger:: ripetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) ereditata da tutte le interfacce del trigger.</span><span class="sxs-lookup"><span data-stu-id="578b0-158">For C++ development, the repetition pattern is specified using the [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) property that is inherited by all the trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="578b0-159">Esempio</span><span class="sxs-lookup"><span data-stu-id="578b0-159">Examples</span></span>

<span data-ttu-id="578b0-160">Nel codice XML seguente viene definito un elemento trigger di avvio che specifica un modello di ripetizione per un trigger.</span><span class="sxs-lookup"><span data-stu-id="578b0-160">The following XML defines a boot trigger element that specifies a repetition pattern for a trigger.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="578b0-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="578b0-161">Requirements</span></span>



| <span data-ttu-id="578b0-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="578b0-162">Requirement</span></span> | <span data-ttu-id="578b0-163">Valore</span><span class="sxs-lookup"><span data-stu-id="578b0-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="578b0-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="578b0-164">Minimum supported client</span></span><br/> | <span data-ttu-id="578b0-165">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="578b0-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="578b0-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="578b0-166">Minimum supported server</span></span><br/> | <span data-ttu-id="578b0-167">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="578b0-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="578b0-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="578b0-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="578b0-169">Elementi dello schema Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="578b0-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="578b0-170">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="578b0-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





