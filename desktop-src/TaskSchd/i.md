---
title: I (Utilità di pianificazione)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517259"
---
# <a name="i-task-scheduler"></a><span data-ttu-id="33b18-103">I (Utilità di pianificazione)</span><span class="sxs-lookup"><span data-stu-id="33b18-103">I (Task Scheduler)</span></span>

<span data-ttu-id="33b18-104">A B C D [E](e.md) F G H i J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="33b18-104">A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="33b18-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condizioni di inattività**</span><span class="sxs-lookup"><span data-stu-id="33b18-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**idle conditions**</span></span>
</dt> <dd>

<span data-ttu-id="33b18-106">Un periodo di tempo in cui non è presente alcun input utente nel computer.</span><span class="sxs-lookup"><span data-stu-id="33b18-106">A period of time in which there is no user input on the computer.</span></span> <span data-ttu-id="33b18-107">Le condizioni di inattività sono associate all'ora di inizio pianificata per l'attività.</span><span class="sxs-lookup"><span data-stu-id="33b18-107">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="33b18-108">Queste condizioni vengono impostate chiamando [**IScheduledWorkItem:: Flags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span><span class="sxs-lookup"><span data-stu-id="33b18-108">These conditions are set by calling [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span></span>

</dd> <dt>

<span data-ttu-id="33b18-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**trigger inattivi**</span><span class="sxs-lookup"><span data-stu-id="33b18-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**idle triggers**</span></span>
</dt> <dd>

<span data-ttu-id="33b18-110">Trigger basato su eventi generato quando il computer diventa inattivo per un periodo di tempo specifico.</span><span class="sxs-lookup"><span data-stu-id="33b18-110">An event-based trigger that is fired when the computer becomes idle for a specific amount of time.</span></span>

<span data-ttu-id="33b18-111">I trigger inattivi vengono creati impostando \_ il \_ membro del tipo di trigger attività della struttura del [**\_ trigger**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) di attività \_ \_ su trigger evento attività \_ su \_ inattivo.</span><span class="sxs-lookup"><span data-stu-id="33b18-111">Idle triggers are created by setting the TASK\_TRIGGER\_TYPE member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure to TASK\_EVENT\_TRIGGER\_ON\_IDLE.</span></span>

</dd> <dt>

<span data-ttu-id="33b18-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tempo di attesa inattivo**</span><span class="sxs-lookup"><span data-stu-id="33b18-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**idle wait time**</span></span>
</dt> <dd>

<span data-ttu-id="33b18-113">Intervallo di tempo (in minuti) utilizzato da un trigger inattivo o da una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="33b18-113">The time interval (in minutes) used by an idle trigger or idle condition.</span></span> <span data-ttu-id="33b18-114">I trigger inattivi sono trigger basati su eventi che non sono associati a un'ora pianificata.</span><span class="sxs-lookup"><span data-stu-id="33b18-114">Idle triggers are event-based triggers that are not associated with a scheduled time.</span></span> <span data-ttu-id="33b18-115">Le condizioni di inattività sono associate all'ora di inizio pianificata per l'attività.</span><span class="sxs-lookup"><span data-stu-id="33b18-115">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="33b18-116">Il tempo di inattività viene impostato da una chiamata a [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span><span class="sxs-lookup"><span data-stu-id="33b18-116">The idle time is set by a call to [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span></span>

</dd> </dl>

 

 




