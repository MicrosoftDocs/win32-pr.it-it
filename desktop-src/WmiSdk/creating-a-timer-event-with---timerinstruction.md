---
description: Per creare un evento timer, creare un'istanza delle classi derivate dalla \_ \_ classe TimerInstruction in qualsiasi spazio dei nomi WMI.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Creazione di un evento timer con __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb943419a255846fbde4e17e357f8ce199824085d542d8ad300fb7e301fa3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030671"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Creazione di un evento timer \_ \_ con TimerInstruction

Per creare un evento timer, creare un'istanza delle classi derivate dalla [**\_ \_ classe TimerInstruction**](--timerinstruction.md) in qualsiasi spazio dei nomi WMI. WMI genera quindi l'evento timer all'ora appropriata. Se si perde un evento timer a causa di tempi di inattività del computer, WMI invia una notifica sull'evento perso. WMI supporta gli eventi timer per la compatibilità con le versioni precedenti e per gli scenari in cui è necessario conoscere il numero di eventi persi dall'ultimo evento recapitato. Per la maggior parte degli eventi timer, tuttavia, è necessario creare un filtro eventi per [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**Win32 \_ UTCTime.**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) Per altre informazioni, vedere [Creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime.](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)

La procedura seguente descrive come creare e ricevere un evento timer con \_ \_ TimerInstruction.

**Per creare e ricevere un evento timer con \_ \_ TimerInstruction**

1.  Creare un'istanza [**\_ \_ delle classi AbsoluteTimerInstruction**](--absolutetimerinstruction.md) [**\_ \_ o IntervalTimerInstruction.**](--intervaltimerinstruction.md)

    Le [**\_ \_ classi AbsoluteTimerInstruction**](--absolutetimerinstruction.md) e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) derivano dalla classe [**\_ \_ TimerInstruction,**](--timerinstruction.md) che contiene una stringa univoca assegnata dallo sviluppatore che identifica il tipo di evento timer. La **\_ \_ classe TimerInstruction** contiene anche un valore che specifica se WMI deve inviare una notifica tardiva se l'evento timer si verifica quando WMI non è disponibile.

    Usare [**\_ \_ AbsoluteTimerInstruction per**](--absolutetimerinstruction.md) inviare eventi timer assoluti, che si verificano in una data specifica a un'ora specifica. Usare [**\_ \_ IntervalTimerInstruction per**](--intervaltimerinstruction.md) inviare eventi timer a intervalli, che si verificano a intervalli regolari.

2.  Impostare l'applicazione per ricevere [**\_ \_ un'istanza di TimerEvent.**](--timerevent.md)

    Per generare un evento, WMI crea un'istanza della [**\_ \_ classe TimerEvent**](--timerevent.md) e inoltra l'istanza al consumer. **\_ \_ L'istanza timerEvent** contiene l'identificatore dell'istruzione timer del consumer. L'istanza contiene anche un valore che specifica quante volte WMI deve inviare la notifica degli eventi timer durante qualsiasi intervallo quando WMI non riesce a raggiungere il consumer.

 

 
