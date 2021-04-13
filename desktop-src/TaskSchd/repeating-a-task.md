---
title: Ripetizione di un'attività
description: Utilità di pianificazione possibile eseguire un'attività un numero qualsiasi di volte in cui viene attivato un trigger.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- modello di ripetizione Utilità di pianificazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331228"
---
# <a name="repeating-a-task"></a><span data-ttu-id="dcb73-104">Ripetizione di un'attività</span><span class="sxs-lookup"><span data-stu-id="dcb73-104">Repeating A Task</span></span>

<span data-ttu-id="dcb73-105">Utilità di pianificazione possibile eseguire un'attività un numero qualsiasi di volte in cui viene attivato un trigger.</span><span class="sxs-lookup"><span data-stu-id="dcb73-105">Task Scheduler can run a task any number of times times after a trigger is fired.</span></span> <span data-ttu-id="dcb73-106">A tale scopo, il trigger definisce uno schema di ripetizione che indica Utilità di pianificazione per quanto tempo deve continuare a ripetere l'attività e l'intervallo di tempo tra ogni ripetizione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="dcb73-106">To do this, the trigger defines a repetition pattern that tells Task Scheduler how long it should continue to repeat the task and the time interval between each task repetition.</span></span>

## <a name="repetition-pattern"></a><span data-ttu-id="dcb73-107">Modello di ripetizione</span><span class="sxs-lookup"><span data-stu-id="dcb73-107">Repetition Pattern</span></span>

<span data-ttu-id="dcb73-108">Nella figura seguente viene illustrato un modello di ripetizione con una durata di 60 minuti e un intervallo di 25 minuti.</span><span class="sxs-lookup"><span data-stu-id="dcb73-108">The following illustration shows a repetition pattern with a duration of 60 minutes and an interval of 25 minutes.</span></span> <span data-ttu-id="dcb73-109">Tenere presente che, in questo caso, Utilità di pianificazione esegue l'attività quando viene attivato il trigger, esegue nuovamente l'attività dopo 25 minuti, quindi esegue nuovamente l'attività dopo 50 minuti a seconda dell'impostazione della [**Proprietà StopAtDurationEnd di IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) per lo scripting).</span><span class="sxs-lookup"><span data-stu-id="dcb73-109">Be aware that in this case, Task Scheduler runs the task when the trigger is fired, it runs the task again after 25 minutes, then runs the task again after 50 minutes depending on the setting of the [**StopAtDurationEnd property of IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) for scripting).</span></span> <span data-ttu-id="dcb73-110">Se la proprietà **StopAtDurationEnd** è impostata su True, utilità di pianificazione arresta l'ultima istanza dell'attività se è ancora in esecuzione dopo 60 minuti.</span><span class="sxs-lookup"><span data-stu-id="dcb73-110">If the **StopAtDurationEnd** property is set to True, Task Scheduler stops the last instance of the task if it is still running after 60 minutes.</span></span> <span data-ttu-id="dcb73-111">Se la proprietà **StopAtDurationEnd** è impostata su false, l'ultima istanza dell'attività viene eseguita indipendentemente dalla durata.</span><span class="sxs-lookup"><span data-stu-id="dcb73-111">If the **StopAtDurationEnd** property is set to False, the last instance of the task is run regardless of the duration.</span></span>

![modello di ripetizione trigger](images/repetition-pattern.png)

<span data-ttu-id="dcb73-113">Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata cinque volte.</span><span class="sxs-lookup"><span data-stu-id="dcb73-113">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started five times.</span></span> <span data-ttu-id="dcb73-114">Le cinque ripetizioni possono essere definite dal modello seguente:</span><span class="sxs-lookup"><span data-stu-id="dcb73-114">The five repetitions can be defined by the following pattern:</span></span>

1.  <span data-ttu-id="dcb73-115">Un'attività viene avviata all'inizio del primo minuto.</span><span class="sxs-lookup"><span data-stu-id="dcb73-115">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="dcb73-116">L'attività successiva inizia alla fine del primo minuto.</span><span class="sxs-lookup"><span data-stu-id="dcb73-116">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="dcb73-117">L'attività successiva inizia alla fine del secondo minuto.</span><span class="sxs-lookup"><span data-stu-id="dcb73-117">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="dcb73-118">L'attività successiva inizia alla fine del terzo minuto.</span><span class="sxs-lookup"><span data-stu-id="dcb73-118">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="dcb73-119">L'attività successiva inizia alla fine del quarto minuto.</span><span class="sxs-lookup"><span data-stu-id="dcb73-119">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="dcb73-120">**Windows Server 2003, Windows XP e windows 2000:** Se si registra un'attività che contiene un trigger con un intervallo di ripetizione uguale a un minuto e una durata di ripetizione uguale a quattro minuti, l'attività verrà avviata quattro volte.</span><span class="sxs-lookup"><span data-stu-id="dcb73-120">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started four times.</span></span>

## <a name="objects-interfaces-and-xml-elements"></a><span data-ttu-id="dcb73-121">Oggetti, interfacce ed elementi XML</span><span class="sxs-lookup"><span data-stu-id="dcb73-121">Objects, Interfaces, and XML Elements</span></span>

<span data-ttu-id="dcb73-122">Per lo sviluppo di script, il modello di ripetizione viene definito utilizzando l'oggetto [**RepetitionPattern**](repetitionpattern.md) .</span><span class="sxs-lookup"><span data-stu-id="dcb73-122">For scripting development, the repetition pattern is defined using the [**RepetitionPattern**](repetitionpattern.md) object.</span></span>

<span data-ttu-id="dcb73-123">Per lo sviluppo in C++, il modello di ripetizione viene definito dall'interfaccia [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .</span><span class="sxs-lookup"><span data-stu-id="dcb73-123">For C++ development, the repetition pattern is defined by the [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) interface.</span></span>

<span data-ttu-id="dcb73-124">Durante la lettura o la scrittura di codice XML per un'attività, il modello di ripetizione viene specificato nell'elemento di [**ripetizione**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dcb73-124">When reading or writing XML for a task, the repetition pattern is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcb73-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dcb73-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcb73-126">Trigger attività</span><span class="sxs-lookup"><span data-stu-id="dcb73-126">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




