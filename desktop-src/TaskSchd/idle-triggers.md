---
title: Trigger inattivi per Utilità di pianificazione 1.0
description: Un trigger inattivo è un trigger basato su eventi che viene attivato un numero specifico di volte dopo che il computer diventa inattivo. Esistono più condizioni che definiscono quando un computer diventa inattivo, ad esempio quando non si verifica alcun input da tastiera o mouse.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349b6ce078479df841773661bfe07b098f95d1124a68803b8b472b226d9b5df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760087"
---
# <a name="idle-triggers-for-task-scheduler-10"></a>Trigger inattivi per Utilità di pianificazione 1.0

Un trigger inattivo è un trigger basato su eventi che viene attivato un numero specifico di volte dopo che il computer diventa inattivo. Esistono più condizioni che definiscono quando un computer diventa inattivo, ad esempio quando non si verifica alcun input da tastiera o mouse.

I trigger inattivi vengono creati specificando TASK EVENT TRIGGER ON IDLE nel \_ \_ membro TASK TRIGGER \_ \_ [**\_ \_ TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) della [**struttura TASK \_ TRIGGER.**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) Il trigger inattivo viene attivato quando il sistema diventa inattivo per la quantità di tempo specificata dal tempo di attesa inattivo dell'elemento di lavoro.

> [!Note]  
> Quando si specifica TASK EVENT TRIGGER ON IDLE, i membri \_ \_ \_ \_ **wStartHour**, **wStartMinute** [**\_**](/windows/desktop/api/Mstask/ns-mstask-task_trigger)  e Type della struttura TASK TRIGGER vengono ignorati.

 

È possibile impostare il tempo di attesa inattivo di un elemento di lavoro chiamando il [**metodo IScheduledWorkItem::SetIdleWait.**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) Questo metodo imposta la quantità di tempo (in minuti) in cui il sistema deve rimanere inattivo prima che venga attivato il trigger e venga eseguito l'elemento di lavoro.

Per recuperare il tempo di inattività di un'attività, chiamare il [**metodo IScheduledWorkItem::GetIdleWait.**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger di attività](task-triggers.md)
</dt> </dl>

 

 




