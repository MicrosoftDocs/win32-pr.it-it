---
title: Strutture e unioni Utilità di pianificazione
description: Elenca le strutture e le unioni usate dalle API Utilità di pianificazione 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Utilità di pianificazione Utilità di pianificazione, riferimento, strutture e unioni
- attiva Utilità di pianificazione, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221043"
---
# <a name="task-scheduler-structures-and-unions"></a><span data-ttu-id="590b8-105">Strutture e unioni Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="590b8-105">Task Scheduler Structures and Unions</span></span>

<span data-ttu-id="590b8-106">In questa sezione vengono descritte le strutture e le unioni utilizzate dalle API di Utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="590b8-106">This section describes the structures and unions used by the Task Scheduler APIs.</span></span>

<span data-ttu-id="590b8-107">Tutte le strutture e le unioni seguenti vengono usate da Utilità di pianificazione 1,0.</span><span class="sxs-lookup"><span data-stu-id="590b8-107">All the structures and unions below are used by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="590b8-108">Nome</span><span class="sxs-lookup"><span data-stu-id="590b8-108">Name</span></span>                                               | <span data-ttu-id="590b8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="590b8-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="590b8-110">**GIORNALIERA**</span><span class="sxs-lookup"><span data-stu-id="590b8-110">**DAILY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-daily)                             | <span data-ttu-id="590b8-111">Definisce l'intervallo, in giorni, in cui viene eseguita un'attività.</span><span class="sxs-lookup"><span data-stu-id="590b8-111">Defines the interval, in days, at which a task is run.</span></span>                                                                          |
| [<span data-ttu-id="590b8-112">**MONTHLYDATE**</span><span class="sxs-lookup"><span data-stu-id="590b8-112">**MONTHLYDATE**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | <span data-ttu-id="590b8-113">Definisce il giorno del mese in cui l'attività viene eseguita.</span><span class="sxs-lookup"><span data-stu-id="590b8-113">Defines the day of the month the task will run.</span></span>                                                                                 |
| [<span data-ttu-id="590b8-114">**MONTHLYDOW**</span><span class="sxs-lookup"><span data-stu-id="590b8-114">**MONTHLYDOW**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | <span data-ttu-id="590b8-115">Definisce la data o le date in cui l'attività viene eseguita per mese, settimana e giorno della settimana.</span><span class="sxs-lookup"><span data-stu-id="590b8-115">Defines the date(s) that the task runs by month, week, and day of the week.</span></span>                                                     |
| [<span data-ttu-id="590b8-116">**\_trigger attività**</span><span class="sxs-lookup"><span data-stu-id="590b8-116">**TASK\_TRIGGER**</span></span>](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | <span data-ttu-id="590b8-117">Definisce gli orari per l'esecuzione di un [*elemento di lavoro*](w.md)pianificato.</span><span class="sxs-lookup"><span data-stu-id="590b8-117">Defines the times to run a scheduled [*work item*](w.md).</span></span>                                                  |
| [<span data-ttu-id="590b8-118">**\_Unione del tipo di trigger \_**</span><span class="sxs-lookup"><span data-stu-id="590b8-118">**TRIGGER\_TYPE\_UNION**</span></span>](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | <span data-ttu-id="590b8-119">Definisce la pianificazione della chiamata del trigger all'interno del membro del **tipo** di una struttura di [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="590b8-119">Defines the invocation schedule of the trigger within the **Type** member of a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> |
| [<span data-ttu-id="590b8-120">**SETTIMANALE**</span><span class="sxs-lookup"><span data-stu-id="590b8-120">**WEEKLY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | <span data-ttu-id="590b8-121">Definisce l'intervallo, in settimane, tra le chiamate di un'attività.</span><span class="sxs-lookup"><span data-stu-id="590b8-121">Defines the interval, in weeks, between invocations of a task.</span></span>                                                                  |



 

 

 




