---
title: Trigger attività
description: Un trigger è un set di criteri che, se soddisfatti, avvia l'esecuzione di un'attività.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- creazione di trigger Utilità di pianificazione
- trigger Utilità di pianificazione
- trigger Utilità di pianificazione, descritti
- trigger Utilità di pianificazione, basato sul tempo
- trigger Utilità di pianificazione, basati su eventi
- trigger basati su eventi Utilità di pianificazione
- trigger basati sul tempo Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221074"
---
# <a name="task-triggers"></a><span data-ttu-id="23413-110">Trigger attività</span><span class="sxs-lookup"><span data-stu-id="23413-110">Task Triggers</span></span>

<span data-ttu-id="23413-111">Un trigger è un set di criteri che, se soddisfatti, avvia l'esecuzione di un'attività.</span><span class="sxs-lookup"><span data-stu-id="23413-111">A trigger is a set of criteria that, when met, starts the execution of a task.</span></span> <span data-ttu-id="23413-112">Utilità di pianificazione fornisce trigger basati sul tempo e basati su eventi che possono avviare un'attività in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="23413-112">Task Scheduler provides both time-based and event-based triggers that can start a task in several different ways.</span></span> <span data-ttu-id="23413-113">Una determinata attività può essere avviata da uno o più trigger.</span><span class="sxs-lookup"><span data-stu-id="23413-113">A given task can be started by one or more triggers.</span></span> <span data-ttu-id="23413-114">Un'attività può avere un massimo di 48 trigger.</span><span class="sxs-lookup"><span data-stu-id="23413-114">A task can have a maximum of 48 triggers.</span></span>

## <a name="time-based-triggers"></a><span data-ttu-id="23413-115">Trigger basati sul tempo</span><span class="sxs-lookup"><span data-stu-id="23413-115">Time-based Triggers</span></span>

<span data-ttu-id="23413-116">I trigger basati sul tempo avviano le attività a intervalli specificati.</span><span class="sxs-lookup"><span data-stu-id="23413-116">Time-based triggers start tasks at specified times.</span></span> <span data-ttu-id="23413-117">Questo include l'avvio dell'attività una volta a un'ora specifica o l'avvio più volte dell'attività in base a una pianificazione giornaliera, settimanale, mensile o mensile del giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="23413-117">This includes starting the task once at a specific time or starting the task multiple times on a daily, weekly, monthly, or monthly day-of-week schedule.</span></span>

## <a name="event-based-triggers"></a><span data-ttu-id="23413-118">Trigger basati su eventi</span><span class="sxs-lookup"><span data-stu-id="23413-118">Event-based Triggers</span></span>

<span data-ttu-id="23413-119">I trigger basati su eventi avviano un'attività in risposta a determinati eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="23413-119">Event-based triggers start a task in response to certain system events.</span></span> <span data-ttu-id="23413-120">È ad esempio possibile impostare trigger basati su eventi per avviare un'attività all'avvio del sistema, quando un utente accede al computer locale o quando il sistema diventa inattivo.</span><span class="sxs-lookup"><span data-stu-id="23413-120">For example, event-based triggers can be set to start a task when the system starts up, when a user logs on to the local computer, or when the system becomes idle.</span></span>

## <a name="multiple-triggers"></a><span data-ttu-id="23413-121">Più trigger</span><span class="sxs-lookup"><span data-stu-id="23413-121">Multiple Triggers</span></span>

<span data-ttu-id="23413-122">Ogni attività può essere avviata da uno o più trigger, consentendo l'avvio dell'attività in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="23413-122">Each task can be started by one or more triggers, allowing the task to be started in any number of ways.</span></span> <span data-ttu-id="23413-123">Tuttavia, più trigger sono implementati in modo diverso in Utilità di pianificazione 1,0 e Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="23413-123">However, multiple triggers are implemented differently in Task Scheduler 1.0 and Task Scheduler 2.0.</span></span>

<span data-ttu-id="23413-124">In Utilità di pianificazione 2,0 ogni trigger è definito da un'API trigger separata associata all'attività tramite la raccolta di trigger.</span><span class="sxs-lookup"><span data-stu-id="23413-124">In Task Scheduler 2.0, each trigger is defined by a separate trigger API that is associated with the task through the trigger collection.</span></span>

<span data-ttu-id="23413-125">In Utilità di pianificazione 1,0, più trigger possono essere considerati come una pianificazione, un set di volte in cui l'attività viene avviata.</span><span class="sxs-lookup"><span data-stu-id="23413-125">In Task Scheduler 1.0, multiple triggers can be thought of as a schedule, a set of times at which the task starts.</span></span> <span data-ttu-id="23413-126">In questo caso, la pianificazione è il set di volte (specificato dall'Unione di tutti i trigger associati all'elemento di lavoro) in cui verrà eseguito un elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="23413-126">In this case, the schedule is the set of times (specified by the union of all of the triggers associated with the work item) at which a work item will execute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23413-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23413-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23413-128">Ripetizione di un'attività</span><span class="sxs-lookup"><span data-stu-id="23413-128">Repeating A Task</span></span>](repeating-a-task.md)
</dt> <dt>

[<span data-ttu-id="23413-129">Tipi di trigger</span><span class="sxs-lookup"><span data-stu-id="23413-129">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="23413-130">Interfacce trigger</span><span class="sxs-lookup"><span data-stu-id="23413-130">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> <dt>

[<span data-ttu-id="23413-131">Informazioni sul Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="23413-131">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




