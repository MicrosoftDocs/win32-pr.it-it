---
title: Utilità di pianificazione 2,0 tipi enumerati
description: Vengono descritti i tipi enumerati che definiscono le costanti utilizzate dalle API di Utilità di pianificazione 2,0.
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339762"
---
# <a name="task-scheduler-20-enumerated-types"></a><span data-ttu-id="e0857-103">Utilità di pianificazione 2,0 tipi enumerati</span><span class="sxs-lookup"><span data-stu-id="e0857-103">Task Scheduler 2.0 Enumerated Types</span></span>

<span data-ttu-id="e0857-104">Vengono descritti i tipi enumerati che definiscono le costanti utilizzate dalle API di Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0857-104">Describes the enumerated types that define the constants that are used by the Task Scheduler 2.0 APIs.</span></span>


<span data-ttu-id="e0857-105">I tipi enumerati seguenti sono introdotti in Utilità di pianificazione 2,0.</span><span class="sxs-lookup"><span data-stu-id="e0857-105">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="e0857-106">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="e0857-106">Enumeration</span></span>                                                                  | <span data-ttu-id="e0857-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0857-107">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0857-108">**\_tipo di azione attività \_**</span><span class="sxs-lookup"><span data-stu-id="e0857-108">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="e0857-109">Definisce il tipo di azioni che possono essere eseguite da un'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-109">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="e0857-110">**compatibilità delle attività \_**</span><span class="sxs-lookup"><span data-stu-id="e0857-110">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="e0857-111">Definisce le versioni di Utilità di pianificazione o il comando AT con cui è compatibile l'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-111">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="e0857-112">**creazione di attività \_**</span><span class="sxs-lookup"><span data-stu-id="e0857-112">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="e0857-113">Definisce il modo in cui il servizio di Utilità di pianificazione crea, aggiorna o Disabilita l'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-113">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="e0857-114">**\_flag di enumerazione delle attività \_**</span><span class="sxs-lookup"><span data-stu-id="e0857-114">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="e0857-115">Definisce il modo in cui il Utilità di pianificazione enumera le attività registrate.</span><span class="sxs-lookup"><span data-stu-id="e0857-115">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="e0857-116">**\_criteri istanze \_ attività**</span><span class="sxs-lookup"><span data-stu-id="e0857-116">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="e0857-117">Definisce il modo in cui il Utilità di pianificazione gestisce le istanze esistenti dell'attività quando avvia una nuova istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-117">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="e0857-118">**\_tipo di accesso attività**</span><span class="sxs-lookup"><span data-stu-id="e0857-118">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="e0857-119">Definisce la tecnica di accesso necessaria per eseguire un'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-119">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="e0857-120">**\_tipo di PROCESSTOKENSID attività \_**</span><span class="sxs-lookup"><span data-stu-id="e0857-120">**TASK\_PROCESSTOKENSID\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | <span data-ttu-id="e0857-121">Definisce i tipi di SID del processo che possono essere utilizzati dalle attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-121">Defines the types of process SID that can be used by tasks.</span></span>                                                      |
| [<span data-ttu-id="e0857-122">**\_flag esecuzione \_ attività**</span><span class="sxs-lookup"><span data-stu-id="e0857-122">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="e0857-123">Definisce la modalità di esecuzione di un'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-123">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="e0857-124">**\_tipo di runlevel attività \_**</span><span class="sxs-lookup"><span data-stu-id="e0857-124">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="e0857-125">Definisce i flag di elevazione LUA che specificano con quale livello di privilegio verrà eseguita l'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-125">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="e0857-126">**\_tipo di \_ \_ modifica stato sessione attività \_**</span><span class="sxs-lookup"><span data-stu-id="e0857-126">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="e0857-127">Definisce i tipi di Terminal Server modifica dello stato della sessione che è possibile usare per avviare un'attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-127">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="e0857-128">**\_stato attività**</span><span class="sxs-lookup"><span data-stu-id="e0857-128">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="e0857-129">Definisce i diversi stati in cui può trovarsi un'attività registrata.</span><span class="sxs-lookup"><span data-stu-id="e0857-129">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="e0857-130">**\_Trigger attività \_ tipo2**</span><span class="sxs-lookup"><span data-stu-id="e0857-130">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="e0857-131">Definisce il tipo di trigger che può essere utilizzato dalle attività.</span><span class="sxs-lookup"><span data-stu-id="e0857-131">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="e0857-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e0857-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0857-133">Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e0857-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e0857-134">Riferimento Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="e0857-134">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




