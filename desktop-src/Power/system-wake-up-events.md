---
description: L'applicazione può ripristinare un computer in stato di sospensione allo stato di lavoro usando un timer pianificato o un evento del dispositivo.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: Eventi di riattivazione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f67ec53b474e303bada3a27bda1adea8170d5be2d6a84354fc17094ddec7da2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143224"
---
# <a name="system-wake-up-events"></a>Eventi di riattivazione del sistema

Le informazioni seguenti si applicano alle riattivazioni dalla sospensione [(S3) e all'ibernazione (S4).](/windows-hardware/drivers/kernel/system-sleeping-states) Per le riattivazioni da Modern Standby (S0 Low Power Idle), fare riferimento alle transizioni [da inattive ad attive.](/windows-hardware/design/device-experiences/transition-from-idle-to-active)

L'applicazione può ripristinare un computer in stato di sospensione allo stato di lavoro usando un timer pianificato o un evento del dispositivo. Questo evento è noto come *evento di riattivazione.* Usare un [oggetto timer in attesa](/windows/desktop/Sync/waitable-timer-objects) per specificare l'ora in cui il sistema deve essere riattivato. Per creare l'oggetto, usare [**la funzione CreateWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) Per impostare il timer, usare la [**funzione SetWaitableTimer.**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) Il *parametro pDueTime* specifica quando verrà segnalato il timer. Per specificare che il sistema deve essere riattivato quando viene segnalato il timer, impostare il *parametro fResume* su **TRUE.**

Quando il sistema viene riattivato automaticamente a causa di un evento (diverso dall'interruttore di alimentazione o dall'attività dell'utente), il sistema imposta automaticamente un timer di inattività automatica su almeno 2 minuti. Questo timer offre alle applicazioni tempo sufficiente per chiamare [**la funzione SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) per indicare che sono occupate. Questa volta consente al sistema di tornare rapidamente allo stato di sospensione quando il computer non è più necessario. I criteri seguenti determinano se il sistema torna allo stato di sospensione:

-   Se il sistema si riattiva automaticamente,ovvero non è presente alcuna attività dell'utente, si arresta non appena scade il timer di inattività automatica, presupponendo che nessuna applicazione abbia chiamato [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) per indicare che il sistema è necessario.
-   Le riattivazioni basate su dispositivo attivano il timer di inattività automatica per impostazione predefinita, a meno che il driver di dispositivo non indichi la presenza dell'utente. Se il driver indica la presenza dell'utente, viene usato il timer di inattività del sistema.
-   Se il sistema viene riattivato automaticamente, ma l'utente fornisce nuovo input durante la gestione dell'evento, il sistema non torna automaticamente in sospensione in base al timer di inattività automatica. Al contrario, il sistema torna in sospensione in base al timer di inattività del sistema.
-   Se il sistema si riattiva a causa dell'attività dell'utente, il sistema non torna automaticamente in stato di sospensione in base al timer di inattività automatica. Il sistema torna invece in sospensione in base al timer di inattività del sistema.

Quando il sistema si riattiva automaticamente, trasmette l'evento [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) a tutte le applicazioni. Poiché l'utente non è presente, la maggior parte delle applicazioni non deve eseguire alcuna operazione. Le applicazioni di gestione degli eventi, ad esempio i server fax, devono gestire i relativi eventi. Per determinare se il sistema è in questo stato, chiamare la [**funzione IsSystemResumeAutomatic.**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) Quando il sistema viene riattivato automaticamente, lo schermo non viene attivato automaticamente.

Se il sistema si riattiva a causa dell'attività dell'utente, il sistema trasmetterà innanzitutto l'evento [ \_ PBT APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) seguito da un evento [PBT \_ APMRESUMESUSPEND.](pbt-apmresumesuspend.md) Inoltre, il sistema attiva lo schermo. L'applicazione deve riaprire i file che ha chiuso quando il sistema è stato in sospensione e preparare l'input dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> <dt>

[Criteri di sospensione del sistema](system-sleep-criteria.md)
</dt> </dl>

 

 
