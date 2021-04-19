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
# <a name="idle-triggers-for-task-scheduler-10"></a>Trigger inattivi per Utilità di pianificazione 1,0

Un trigger inattivo è un trigger basato su eventi che viene attivato un numero specifico di volte dopo che il computer diventa inattivo. Sono presenti più condizioni che definiscono quando un computer diventa inattivo, ad esempio quando non si verifica alcun input della tastiera o del mouse.

I trigger inattivi vengono creati specificando trigger di evento attività in \_ \_ \_ \_ inattività nel membro del [**\_ \_ tipo di trigger attività**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) della struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Il trigger inattivo viene attivato quando il sistema diventa inattivo per la quantità di tempo specificata dal tempo di attesa inattivo dell'elemento di lavoro.

> [!Note]  
> Quando \_ \_ viene specificato il trigger dell'evento dell'attività \_ su \_ Idle, i membri **wStartHour**, **wStartMinute** e **Type** della struttura del [**\_ trigger di attività**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) vengono ignorati.

 

È possibile impostare il tempo di attesa inattivo di un elemento di lavoro chiamando il metodo [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) . Questo metodo imposta la quantità di tempo (in minuti) che il sistema deve rimanere inattivo prima che il trigger venga attivato e l'elemento di lavoro venga eseguito.

Per recuperare il tempo di inattività di un'attività, chiamare il metodo [**IScheduledWorkItem:: GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Trigger attività](task-triggers.md)
</dt> </dl>

 

 




