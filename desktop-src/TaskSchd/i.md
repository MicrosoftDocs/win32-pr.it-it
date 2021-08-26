---
title: I (Utilità di pianificazione)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14bec8dd745aee798ebb6aa9cb296d7a0990b85b44562fb94ea844d2d5d3397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072641"
---
# <a name="i-task-scheduler"></a>I (Utilità di pianificazione)

A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condizioni di inattività**
</dt> <dd>

Periodo di tempo in cui non è presente alcun input dell'utente nel computer. Le condizioni di inattività sono associate all'ora di inizio pianificata per l'attività.

Queste condizioni vengono impostate chiamando [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**trigger inattivi**
</dt> <dd>

Trigger basato su eventi che viene attivato quando il computer diventa inattivo per un periodo di tempo specifico.

I trigger inattivi vengono creati impostando il membro TASK TRIGGER TYPE della \_ \_ struttura TASK [**\_ TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) su TASK \_ EVENT TRIGGER ON \_ \_ \_ IDLE.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tempo di attesa inattivo**
</dt> <dd>

Intervallo di tempo (in minuti) usato da un trigger inattivo o da una condizione di inattività. I trigger inattivi sono trigger basati su eventi non associati a un'ora pianificata. Le condizioni di inattività sono associate all'ora di inizio pianificata per l'attività.

Il tempo di inattività viene impostato da una chiamata a [**IScheduledWorkItem::SetIdleWait.**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait)

</dd> </dl>

 

 




