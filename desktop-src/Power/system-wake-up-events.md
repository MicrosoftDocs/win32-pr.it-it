---
description: L'applicazione può ripristinare lo stato di lavoro di un computer che si trova in uno stato di sospensione utilizzando un timer pianificato o un evento del dispositivo.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: Eventi di riattivazione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13332305ef023d932f2912f7299aa12cd402733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312012"
---
# <a name="system-wake-up-events"></a>Eventi di riattivazione del sistema

Le informazioni seguenti si applicano a riattivazioni da [sospensione (S3) e ibernazione (S4)](/windows-hardware/drivers/kernel/system-sleeping-states). Per le riattivazioni da Modern standby (S0 Low Power Idle), fare riferimento alle [transizioni da Idle a attivo](/windows-hardware/design/device-experiences/transition-from-idle-to-active).

L'applicazione può ripristinare lo stato di lavoro di un computer che si trova in uno stato di sospensione utilizzando un timer pianificato o un evento del dispositivo. Questa operazione è nota come *evento di riattivazione*. Usare un [oggetto timer in attesa](/windows/desktop/Sync/waitable-timer-objects) per specificare l'ora in cui il sistema deve essere riattivato. Per creare l'oggetto, utilizzare la funzione [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Per impostare il timer, utilizzare la funzione [**SetWaitableTimer**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) . Il parametro *pDueTime* specifica quando verrà segnalato il timer. Per specificare che il sistema deve essere riattivato quando viene segnalato il timer, impostare il parametro *fResume* su **true**.

Quando il sistema viene riattivato automaticamente a causa di un evento (diverso dall'attività dell'utente o dall'interruttore di alimentazione), il sistema imposta automaticamente un timer di inattività automatica su almeno 2 minuti. Questo timer concede alle applicazioni un tempo sufficiente per chiamare la funzione [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) per indicare che sono occupate. Questo tempo consente al sistema di tornare rapidamente allo stato di sospensione dopo che il computer non è più necessario. I criteri seguenti determinano se il sistema torna allo stato di sospensione:

-   Se il sistema viene riattivato automaticamente (ovvero non è presente alcuna attività utente), si arresta non appena il timer di inattività automatico scade, presupponendo che nessuna applicazione abbia chiamato [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) per indicare che il sistema è necessario.
-   Per impostazione predefinita, le riattivazioni basate su dispositivo attivano il timer di inattività automatico a meno che il driver di dispositivo non indichi la presenza dell'utente. Se il driver indica la presenza dell'utente, viene usato il timer di inattività del sistema.
-   Se il sistema viene riattivato automaticamente, ma l'utente fornisce nuovo input mentre l'evento viene gestito, il sistema non torna automaticamente in sospensione in base al timer di inattività automatico. Al contrario, il sistema torna in sospensione in base al timer di inattività del sistema.
-   Se il sistema viene riattivato a causa dell'attività dell'utente, il sistema non torna automaticamente in sospensione in base al timer di inattività automatico. Al contrario, il sistema torna in sospensione in base al timer di inattività del sistema.

Quando il sistema viene riattivato automaticamente, trasmette l'evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) a tutte le applicazioni. Poiché l'utente non è presente, la maggior parte delle applicazioni non deve eseguire alcuna operazione. Le applicazioni che gestiscono gli eventi, ad esempio i server fax, devono gestire gli eventi. Per determinare se il sistema è in questo stato, chiamare la funzione [**IsSystemResumeAutomatic**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) . Quando il sistema viene riattivato automaticamente, la visualizzazione non viene attivata automaticamente.

Se il sistema viene riattivato a causa dell'attività dell'utente, il sistema trasmette prima l'evento [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) seguito da un evento [ \_ APMRESUMESUSPEND PBT](pbt-apmresumesuspend.md) . Il sistema, inoltre, attiverà lo schermo. L'applicazione deve riaprire i file chiusi quando il sistema entra in sospensione e prepara l'input dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> <dt>

[Criteri di sospensione del sistema](system-sleep-criteria.md)
</dt> </dl>

 

 
