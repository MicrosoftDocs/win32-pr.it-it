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
# <a name="i-task-scheduler"></a>I (Utilità di pianificazione)

A B C D [E](e.md) F G H i J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condizioni di inattività**
</dt> <dd>

Un periodo di tempo in cui non è presente alcun input utente nel computer. Le condizioni di inattività sono associate all'ora di inizio pianificata per l'attività.

Queste condizioni vengono impostate chiamando [**IScheduledWorkItem:: Flags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**trigger inattivi**
</dt> <dd>

Trigger basato su eventi generato quando il computer diventa inattivo per un periodo di tempo specifico.

I trigger inattivi vengono creati impostando \_ il \_ membro del tipo di trigger attività della struttura del [**\_ trigger**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) di attività \_ \_ su trigger evento attività \_ su \_ inattivo.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tempo di attesa inattivo**
</dt> <dd>

Intervallo di tempo (in minuti) utilizzato da un trigger inattivo o da una condizione di inattività. I trigger inattivi sono trigger basati su eventi che non sono associati a un'ora pianificata. Le condizioni di inattività sono associate all'ora di inizio pianificata per l'attività.

Il tempo di inattività viene impostato da una chiamata a [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).

</dd> </dl>

 

 




