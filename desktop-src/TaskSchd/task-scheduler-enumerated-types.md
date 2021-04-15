---
title: Utilità di pianificazione tipi enumerati
description: Elenca le enumerazioni usate dalle API Utilità di pianificazione.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Utilità di pianificazione Utilità di pianificazione, riferimento, tipi enumerati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517229"
---
# <a name="task-scheduler-enumerated-types"></a><span data-ttu-id="e4afa-104">Utilità di pianificazione tipi enumerati</span><span class="sxs-lookup"><span data-stu-id="e4afa-104">Task Scheduler Enumerated Types</span></span>

<span data-ttu-id="e4afa-105">Vengono descritti i tipi enumerati che definiscono le costanti utilizzate dalle API Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="e4afa-105">Describes the enumerated types that define the constants that are used by the Task Scheduler APIs.</span></span>


<span data-ttu-id="e4afa-106">I tipi enumerati seguenti sono introdotti in Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="e4afa-106">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="e4afa-107">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="e4afa-107">Enumeration</span></span>                                                                  | <span data-ttu-id="e4afa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4afa-108">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4afa-109">**\_tipo di azione attività \_**</span><span class="sxs-lookup"><span data-stu-id="e4afa-109">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="e4afa-110">Definisce il tipo di azioni che possono essere eseguite da un'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-110">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="e4afa-111">**compatibilità delle attività \_**</span><span class="sxs-lookup"><span data-stu-id="e4afa-111">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="e4afa-112">Definisce le versioni di Utilità di pianificazione o il comando AT con cui è compatibile l'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-112">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="e4afa-113">**creazione di attività \_**</span><span class="sxs-lookup"><span data-stu-id="e4afa-113">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="e4afa-114">Definisce il modo in cui il servizio di Utilità di pianificazione crea, aggiorna o Disabilita l'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-114">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="e4afa-115">**\_flag di enumerazione delle attività \_**</span><span class="sxs-lookup"><span data-stu-id="e4afa-115">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="e4afa-116">Definisce il modo in cui il Utilità di pianificazione enumera le attività registrate.</span><span class="sxs-lookup"><span data-stu-id="e4afa-116">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="e4afa-117">**\_criteri istanze \_ attività**</span><span class="sxs-lookup"><span data-stu-id="e4afa-117">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="e4afa-118">Definisce il modo in cui il Utilità di pianificazione gestisce le istanze esistenti dell'attività quando avvia una nuova istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-118">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="e4afa-119">**\_tipo di accesso attività**</span><span class="sxs-lookup"><span data-stu-id="e4afa-119">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="e4afa-120">Definisce la tecnica di accesso necessaria per eseguire un'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-120">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="e4afa-121">**\_tipo di PROCESSTOKENSID attività**</span><span class="sxs-lookup"><span data-stu-id="e4afa-121">**TASK\_PROCESSTOKENSID TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | <span data-ttu-id="e4afa-122">Definisce i tipi di SID di processo che possono essere utilizzati dalle attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-122">Defines the types of process SID that can used by tasks.</span></span>                                                         |
| [<span data-ttu-id="e4afa-123">**\_flag esecuzione \_ attività**</span><span class="sxs-lookup"><span data-stu-id="e4afa-123">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="e4afa-124">Definisce la modalità di esecuzione di un'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-124">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="e4afa-125">**\_tipo di runlevel attività \_**</span><span class="sxs-lookup"><span data-stu-id="e4afa-125">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="e4afa-126">Definisce i flag di elevazione LUA che specificano con quale livello di privilegio verrà eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-126">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="e4afa-127">**\_tipo di \_ \_ modifica stato sessione attività \_**</span><span class="sxs-lookup"><span data-stu-id="e4afa-127">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="e4afa-128">Definisce i tipi di Terminal Server modifica dello stato della sessione che è possibile usare per avviare un'attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-128">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="e4afa-129">**\_stato attività**</span><span class="sxs-lookup"><span data-stu-id="e4afa-129">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="e4afa-130">Definisce i diversi stati in cui può trovarsi un'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="e4afa-130">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="e4afa-131">**\_Trigger attività \_ tipo2**</span><span class="sxs-lookup"><span data-stu-id="e4afa-131">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="e4afa-132">Definisce il tipo di trigger che può essere utilizzato dalle attività.</span><span class="sxs-lookup"><span data-stu-id="e4afa-132">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 


> [!WARNING]
> <span data-ttu-id="e4afa-133">Le enumerazioni Utilità di pianificazione 1,0 sono disponibili solo nei sistemi operativi Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e4afa-133">The Task Scheduler 1.0 enumerations are available only in Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e4afa-134">Sono deprecati a partire da Windows Vista e possono essere rimossi completamente in futuro.</span><span class="sxs-lookup"><span data-stu-id="e4afa-134">They are deprecated as of Windows Vista and may be removed completely in the future.</span></span> <span data-ttu-id="e4afa-135">Usare invece le enumerazioni Utilità di pianificazione 2,0 elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e4afa-135">Please use the Task Scheduler 2.0 enumerations listed above instead.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e4afa-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4afa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4afa-137">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e4afa-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e4afa-138">Riferimento Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e4afa-138">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




