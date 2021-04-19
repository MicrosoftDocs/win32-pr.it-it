---
title: Trigger inattivi per Utilità di pianificazione 1,0
description: Un trigger inattivo è un trigger basato su eventi che viene attivato un numero specifico di volte dopo che il computer diventa inattivo. Sono presenti più condizioni che definiscono quando un computer diventa inattivo, ad esempio quando non si verifica alcun input della tastiera o del mouse.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298033"
---
# <a name="idle-triggers-for-task-scheduler-10"></a><span data-ttu-id="3bfa1-104">Trigger inattivi per Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="3bfa1-104">Idle Triggers for Task Scheduler 1.0</span></span>

<span data-ttu-id="3bfa1-105">Un trigger inattivo è un trigger basato su eventi che viene attivato un numero specifico di volte dopo che il computer diventa inattivo.</span><span class="sxs-lookup"><span data-stu-id="3bfa1-105">An idle trigger is an event-based trigger that is fired a specific number of times after the computer becomes idle.</span></span> <span data-ttu-id="3bfa1-106">Sono presenti più condizioni che definiscono quando un computer diventa inattivo, ad esempio quando non si verifica alcun input della tastiera o del mouse.</span><span class="sxs-lookup"><span data-stu-id="3bfa1-106">There are multiple conditions that define when a computer becomes idle, such as when no keyboard or mouse input occurs.</span></span>

<span data-ttu-id="3bfa1-107">I trigger inattivi vengono creati specificando trigger di evento attività in \_ \_ \_ \_ inattività nel membro del [**\_ \_ tipo di trigger attività**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) della struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="3bfa1-107">Idle triggers are created by specifying TASK\_EVENT\_TRIGGER\_ON\_IDLE in the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="3bfa1-108">Il trigger inattivo viene attivato quando il sistema diventa inattivo per la quantità di tempo specificata dal tempo di attesa inattivo dell'elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="3bfa1-108">The idle trigger is fired when the system becomes idle for the amount of time that is specified by the idle wait time of the work item.</span></span>

> [!Note]  
> <span data-ttu-id="3bfa1-109">Quando \_ \_ viene specificato il trigger dell'evento dell'attività \_ su \_ Idle, i membri **wStartHour**, **wStartMinute** e **Type** della struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="3bfa1-109">When TASK\_EVENT\_TRIGGER\_ON\_IDLE is specified, the **wStartHour**, **wStartMinute**, and **Type** members of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure are ignored.</span></span>

 

<span data-ttu-id="3bfa1-110">È possibile impostare il tempo di attesa inattivo di un elemento di lavoro chiamando il metodo [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) .</span><span class="sxs-lookup"><span data-stu-id="3bfa1-110">You can set the idle wait time of a work item by calling the [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) method.</span></span> <span data-ttu-id="3bfa1-111">Questo metodo imposta la quantità di tempo (in minuti) che il sistema deve rimanere inattivo prima che il trigger venga attivato e l'elemento di lavoro venga eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bfa1-111">This method sets the amount of time (in minutes) that the system must remain idle before the trigger is fired and the work item is executed.</span></span>

<span data-ttu-id="3bfa1-112">Per recuperare il tempo di inattività di un'attività, chiamare il metodo [**IScheduledWorkItem:: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .</span><span class="sxs-lookup"><span data-stu-id="3bfa1-112">To retrieve the idle time of a task, call the [**IScheduledWorkItem::GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bfa1-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3bfa1-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bfa1-114">Trigger attività</span><span class="sxs-lookup"><span data-stu-id="3bfa1-114">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




