---
description: Si crea un evento timer creando un'istanza delle classi derivate dalla \_ \_ classe TimerInstruction in qualsiasi spazio dei nomi WMI.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Creazione di un evento timer con __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e502678525569dae272edb7b03c0916db25edfd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233468"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Creazione di un evento timer con \_ \_ TimerInstruction

Si crea un evento timer creando un'istanza delle classi derivate dalla classe [**\_ \_ TimerInstruction**](--timerinstruction.md) in qualsiasi spazio dei nomi WMI. WMI genera quindi l'evento timer al momento appropriato. Se si perde un evento timer a causa di tempi di inattività del computer, WMI invia una notifica all'utente sull'evento mancante. WMI supporta gli eventi timer per la compatibilità con le versioni precedenti e per gli scenari in cui è necessario verificare il numero di eventi mancanti dall'ultimo evento recapitato. Per la maggior parte degli eventi timer, tuttavia, è necessario creare un filtro eventi per [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [**\_ UTCTime Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime). Per ulteriori informazioni, vedere [creazione di un evento timer con Win32 \_ LocalTime o Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

Nella procedura seguente viene descritto come creare e ricevere un evento timer con \_ \_ TimerInstruction.

**Per creare e ricevere un evento timer con \_ \_ TimerInstruction**

1.  Creare un'istanza delle classi [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) o [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) .

    Le classi [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) e [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) sono derivate dalla classe [**\_ \_ TimerInstruction**](--timerinstruction.md) , che contiene una stringa assegnata dallo sviluppatore univoca che identifica il tipo di evento del timer. La classe **\_ \_ TimerInstruction** contiene inoltre un valore che specifica se WMI deve inviare una notifica tardiva se l'evento timer si verifica quando WMI non è disponibile.

    Usare [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) per inviare eventi del timer assoluti, che si verificano in una data specifica in un momento specifico. Usare [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) per inviare eventi timer di intervallo, che si verificano regolarmente.

2.  Impostare l'applicazione in modo che riceva un'istanza di [**\_ \_ TimerEvent**](--timerevent.md) .

    Per generare un evento, WMI crea un'istanza della classe [**\_ \_ TimerEvent**](--timerevent.md) e la trasmette al consumer. L'istanza di **\_ \_ TimerEvent** contiene l'identificatore dell'istruzione del timer del consumer. L'istanza contiene inoltre un valore che specifica il numero di volte in cui WMI deve inviare la notifica degli eventi del timer durante qualsiasi intervallo quando WMI non riesce a raggiungere il consumer.

 

 
