---
description: Un servizio è responsabile della segnalazione delle modifiche nello stato a Gestione controllo servizi.
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Transizioni dello stato del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039caf68ee7d9da93e86e1760e49df87667da8c16eb5ca6693cfdc7db7def2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967316"
---
# <a name="service-state-transitions"></a>Transizioni dello stato del servizio

Un servizio è responsabile della segnalazione delle modifiche nello stato a Gestione controllo servizi. I programmi di controllo dei servizi e il sistema possono individuare lo stato di un servizio solo da Gestione controllo servizi, pertanto è importante che un servizio ne reporti correttamente lo stato. Un servizio segnala lo stato chiamando la [**funzione SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con un puntatore a una struttura [**SERVICE STATUS \_ completamente**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) inizializzata. Il **membro dwCurrentState** della struttura contiene lo stato del servizio da notificare.

Lo stato iniziale di un servizio è SERVICE \_ STOPPED. Quando gestione servizi avvia il servizio, imposta lo stato del servizio su SERVICE START PENDING e chiama \_ \_ la funzione [*ServiceMain del*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) servizio. Il servizio completa quindi l'inizializzazione usando una delle tecniche descritte in [Service ServiceMain Function](service-servicemain-function.md). Dopo che il servizio ha completato l'inizializzazione ed è pronto per iniziare a ricevere richieste di controllo, il servizio chiama [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) per segnalare SERVICE RUNNING e specificare le richieste di controllo che il servizio è pronto \_ ad accettare. La transizione da SERVICE START PENDING a SERVICE RUNNING indica agli strumenti SCM e di monitoraggio dei servizi che \_ il servizio è stato avviato \_ \_ correttamente. Se il servizio segnala uno stato diverso da SERVICE RUNNING, gli strumenti SCM o di monitoraggio del servizio potrebbero contrassegnare il servizio come non \_ avviato.

Gestione controllo servizi invia solo le richieste di controllo specificate al servizio (ad eccezione della richiesta SERVICE \_ CONTROL \_ INTERROGATE, che viene sempre inviata). Per un elenco delle richieste di controllo che un servizio può accettare, vedere il **membro dwControlsAccepted** della [**struttura SERVICE \_ STATUS.**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Per informazioni sulla registrazione per ricevere eventi del dispositivo, vedere la [**funzione RegisterDeviceNotification.**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)

Lo stato del servizio viene in genere modificato in seguito alla gestione di una richiesta di controllo. Le richieste di controllo che causano la modifica dello stato del servizio includono SERVICE \_ CONTROL \_ STOP, SERVICE \_ CONTROL PAUSE e SERVICE CONTROL \_ \_ \_ CONTINUE. Se il servizio deve eseguire un'elaborazione lunga per gestire una di queste richieste, deve creare un thread secondario per eseguire l'elaborazione lunga e segnalare lo stato in sospeso corrispondente a Gestione controllo servizi. Per ottenere prestazioni ottimali in Windows Vista e versioni successive di Windows, il servizio deve usare un thread di lavoro di un pool di [thread](/windows/desktop/ProcThread/thread-pools) a questo scopo. Il servizio deve quindi segnalare la transizione di stato completata al termine dell'elaborazione lunga. Per altre informazioni sulla gestione delle richieste di controllo, vedere [Funzione del gestore di controllo del servizio](service-control-handler-function.md).

Sono valide solo determinate transizioni di stato del servizio. Il diagramma seguente illustra le transizioni valide.

![transizioni di stato del servizio valide](images/service-status-transitions.png)

Lo stato del servizio segnalato a Gestione controllo servizi determina il modo in cui SCM interagisce con il servizio. Ad esempio, se un servizio segnala SERVICE STOP PENDING, Gestione controllo servizi non trasmette ulteriori richieste di controllo al servizio perché questo stato indica che il servizio è \_ \_ in fase di arresto. Lo stato successivo segnalato dal servizio deve essere SERVICE STOPPED perché è \_ l'unico stato valido dopo SERVICE \_ STOP \_ PENDING. Tuttavia, se un servizio segnala una transizione non valida, gestione controllo servizi non ha esito negativo per la chiamata.

Il diagramma seguente illustra in modo più dettagliato le transizioni dello stato del servizio, incluse le richieste di controllo avviate da un programma di controllo del servizio (client del servizio) e le chiamate [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) effettuate da un servizio per segnalare le modifiche dello stato a Gestione controllo servizi. Come accennato in precedenza, Gestione controllo servizi invia solo richieste di controllo che il servizio ha specificato che accetterà, pertanto un servizio potrebbe non ricevere tutte le richieste visualizzate nel diagramma.

![Transizioni dello stato del servizio in dettaglio ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
