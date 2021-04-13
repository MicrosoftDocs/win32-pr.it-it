---
title: Interfacce trigger
description: Le API usate per gestire i trigger variano a seconda della versione del Utilità di pianificazione. In entrambi i casi, tuttavia, queste API consentono di creare nuovi trigger, recuperare e aggiornare i trigger esistenti ed eliminare i trigger che non sono più necessari.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- trigger Utilità di pianificazione, interfacce
- attiva Utilità di pianificazione, interfacce, descritte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339714"
---
# <a name="trigger-interfaces"></a><span data-ttu-id="162b7-106">Interfacce trigger</span><span class="sxs-lookup"><span data-stu-id="162b7-106">Trigger Interfaces</span></span>

<span data-ttu-id="162b7-107">Le API usate per gestire i trigger variano a seconda della versione del Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="162b7-107">The APIs that are used to manage triggers vary depending on the version of the Task Scheduler.</span></span> <span data-ttu-id="162b7-108">In entrambi i casi, tuttavia, queste API consentono di creare nuovi trigger, recuperare e aggiornare i trigger esistenti ed eliminare i trigger che non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="162b7-108">However, in both cases these APIs enable you to create new triggers, retrieve and update existing triggers, and delete triggers that are no longer required.</span></span>


<span data-ttu-id="162b7-109">Le applicazioni sviluppate con Utilità di pianificazione 2,0 possono usare oggetti e interfacce per creare, recuperare, modificare ed eliminare i trigger per un'attività.</span><span class="sxs-lookup"><span data-stu-id="162b7-109">Applications that are developed using Task Scheduler 2.0 can use objects and interfaces to create, retrieve, modify, and delete the triggers for a task.</span></span>

<span data-ttu-id="162b7-110">Nell'illustrazione seguente un'attività specifica una raccolta di trigger usando la relativa proprietà Triggers.</span><span class="sxs-lookup"><span data-stu-id="162b7-110">In the following illustration, a task specifies a collection of triggers using its Triggers property.</span></span> <span data-ttu-id="162b7-111">Questa raccolta contiene una o più API di trigger singole con ogni API che specifica un tipo di trigger specifico.</span><span class="sxs-lookup"><span data-stu-id="162b7-111">This collection contains one or more individual trigger APIs with each API specifying a specific trigger type.</span></span> <span data-ttu-id="162b7-112">Nell'illustrazione seguente, ad esempio, la raccolta di trigger contiene un trigger di avvio, un trigger LOGON e un trigger giornaliero.</span><span class="sxs-lookup"><span data-stu-id="162b7-112">For example, in the illustration below the trigger collection contains a boot trigger, logon trigger, and a daily trigger.</span></span>

![interfacce del trigger dell'utilità di pianificazione 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a><span data-ttu-id="162b7-114">API oggetto per lo sviluppo di script</span><span class="sxs-lookup"><span data-stu-id="162b7-114">Object APIs for Scripting Development</span></span>

<span data-ttu-id="162b7-115">Per ulteriori informazioni sui metodi e sulle proprietà degli oggetti utilizzati per specificare i trigger, vedere:</span><span class="sxs-lookup"><span data-stu-id="162b7-115">For more information about the methods and properties of the objects that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="162b7-116">**TaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="162b7-116">**TaskDefinition**</span></span>](taskdefinition.md)
-   [<span data-ttu-id="162b7-117">**TriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="162b7-117">**TriggerCollection**</span></span>](triggercollection.md)
-   [<span data-ttu-id="162b7-118">**Trigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-118">**Trigger**</span></span>](trigger.md)
-   [<span data-ttu-id="162b7-119">**BootTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-119">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="162b7-120">**DailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-120">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="162b7-121">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-121">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="162b7-122">**IdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-122">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="162b7-123">**LogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-123">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="162b7-124">**MonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-124">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="162b7-125">**MonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="162b7-126">**RegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-126">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="162b7-127">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-127">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="162b7-128">**WeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-128">**WeeklyTrigger**</span></span>](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a><span data-ttu-id="162b7-129">Interfacce API per lo sviluppo in C++</span><span class="sxs-lookup"><span data-stu-id="162b7-129">Interfaces APIs for C++ Development</span></span>

<span data-ttu-id="162b7-130">Per ulteriori informazioni sui metodi e sulle proprietà delle interfacce utilizzate per specificare i trigger, vedere:</span><span class="sxs-lookup"><span data-stu-id="162b7-130">For more information about the methods and properties of the interfaces that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="162b7-131">**ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="162b7-131">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [<span data-ttu-id="162b7-132">**ITriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="162b7-132">**ITriggerCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [<span data-ttu-id="162b7-133">**ITrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-133">**ITrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [<span data-ttu-id="162b7-134">**IBootTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-134">**IBootTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [<span data-ttu-id="162b7-135">**IDailyTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-135">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="162b7-136">**IEventTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-136">**IEventTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [<span data-ttu-id="162b7-137">**IIdleTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-137">**IIdleTrigger**</span></span>](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [<span data-ttu-id="162b7-138">**ILogonTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-138">**ILogonTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [<span data-ttu-id="162b7-139">**IMonthlyDOWTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-139">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [<span data-ttu-id="162b7-140">**IMonthlyTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-140">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="162b7-141">**IRegistrationTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-141">**IRegistrationTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [<span data-ttu-id="162b7-142">**ITimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-142">**ITimeTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [<span data-ttu-id="162b7-143">**IWeeklyTrigger**</span><span class="sxs-lookup"><span data-stu-id="162b7-143">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a><span data-ttu-id="162b7-144">Interfacce del trigger Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="162b7-144">Task Scheduler 1.0 Trigger Interfaces</span></span>

<span data-ttu-id="162b7-145">Le applicazioni esistenti sviluppate con Utilità di pianificazione 1,0 possono usare i metodi disponibili dalle interfacce Utilità di pianificazione 1,0 per creare, recuperare, modificare ed eliminare i trigger per un [*elemento di lavoro*](w.md).</span><span class="sxs-lookup"><span data-stu-id="162b7-145">Existing applications that are developed using Task Scheduler 1.0 can use the methods that are available from the Task Scheduler 1.0 interfaces to create, retrieve, modify, and delete the triggers for a [*work item*](w.md).</span></span> <span data-ttu-id="162b7-146">Si noti, tuttavia, che tutte le interfacce, le enumerazioni e le strutture Utilità di pianificazione 1,0 sono obsolete e non devono essere utilizzate per lo sviluppo di nuove applicazioni.</span><span class="sxs-lookup"><span data-stu-id="162b7-146">However, note that all Task Scheduler 1.0 interfaces, enumerations, and structures are obsolete and should not be used for the development of new applications.</span></span>

<span data-ttu-id="162b7-147">Le due interfacce usate per eseguire questa operazione sono illustrate nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="162b7-147">The two interfaces that are used to do this are shown in the following illustration.</span></span> <span data-ttu-id="162b7-148">L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) viene utilizzata per gestire tutti i trigger associati a un elemento di lavoro. tale gestione include la creazione di un nuovo trigger per l'elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="162b7-148">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface is used to manage all the triggers that are associated with a work item (such management includes creating a new trigger for the work item).</span></span> <span data-ttu-id="162b7-149">L'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) viene utilizzata per gestire un trigger specifico.</span><span class="sxs-lookup"><span data-stu-id="162b7-149">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface is used to manage a specific trigger.</span></span>

![interfacce del trigger dell'utilità di pianificazione 1,0](images/tsktri2.png)

<span data-ttu-id="162b7-151">L'interfaccia [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fornisce metodi per la creazione di un nuovo trigger per un elemento di lavoro, il recupero del numero di trigger associati a un elemento di lavoro, il recupero delle [*strutture di trigger*](t.md) associate all'elemento di lavoro, il recupero delle stringhe del [*trigger*](t.md) associate all'elemento di lavoro e l'eliminazione dei trigger.</span><span class="sxs-lookup"><span data-stu-id="162b7-151">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for creating a new trigger for a work item, retrieving the number of triggers that are associated with a work item, retrieving the [*trigger structures*](t.md) that are associated with the work item, retrieving [*trigger strings*](t.md) that are associated with the work item, and for deleting triggers.</span></span>

<span data-ttu-id="162b7-152">Una volta che l'oggetto trigger è disponibile, è possibile usare l'interfaccia [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) per recuperare la struttura del trigger e la stringa del trigger e per impostare i criteri usati per attivare il trigger.</span><span class="sxs-lookup"><span data-stu-id="162b7-152">Once the trigger object is available, you can use the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger structure and the string of the trigger and to set the criteria that is used to fire the trigger.</span></span> <span data-ttu-id="162b7-153">Questa interfaccia viene utilizzata solo quando si utilizza un [*oggetto trigger di attività*](t.md).</span><span class="sxs-lookup"><span data-stu-id="162b7-153">This interface is used only when you are working with a [*task trigger object*](t.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="162b7-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="162b7-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="162b7-155">Trigger attività</span><span class="sxs-lookup"><span data-stu-id="162b7-155">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="162b7-156">Tipi di trigger</span><span class="sxs-lookup"><span data-stu-id="162b7-156">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="162b7-157">Strutture trigger</span><span class="sxs-lookup"><span data-stu-id="162b7-157">Trigger Structures</span></span>](trigger-structures.md)
</dt> </dl>

 

 