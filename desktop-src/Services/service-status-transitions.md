---
description: Un servizio è responsabile della segnalazione delle modifiche apportate allo stato a gestione controllo servizi (SCM).
ms.assetid: 74a85730-6667-46fe-ae12-26561ccedb73
title: Transizioni di stato del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df7684b1ebc04aa1116b09a3ae4321f2552d7b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550539"
---
# <a name="service-state-transitions"></a>Transizioni di stato del servizio

Un servizio è responsabile della segnalazione delle modifiche apportate allo stato a gestione controllo servizi (SCM). I programmi di controllo del servizio e il sistema possono individuare lo stato di un servizio solo da SCM, quindi è importante che un servizio segnali correttamente lo stato. Un servizio segnala il proprio stato chiamando la funzione [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con un puntatore a una struttura di [**\_ stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) completamente inizializzata. Il membro **dwCurrentState** della struttura contiene lo stato del servizio da segnalare.

Lo stato iniziale di un servizio è servizio \_ interrotto. Quando SCM avvia il servizio, imposta lo stato del servizio su avvio servizio \_ \_ in sospeso e chiama la funzione [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) del servizio. Il servizio quindi completa l'inizializzazione usando una delle tecniche descritte nella [funzione ServiceMain del servizio](service-servicemain-function.md). Dopo che il servizio ha completato l'inizializzazione ed è pronto per iniziare a ricevere richieste di controllo, il servizio chiama [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) per segnalare il servizio \_ in esecuzione e specifica le richieste di controllo che il servizio è pronto ad accettare. La transizione dall'avvio del servizio in \_ \_ sospeso al servizio \_ in esecuzione indica agli strumenti SCM e di monitoraggio dei servizi che il servizio è stato avviato correttamente. Se il servizio segnala uno stato diverso dal servizio \_ in esecuzione, gli strumenti SCM o di monitoraggio dei servizi potrebbero contrassegnare il servizio come non avviato.

SCM invia al servizio solo le richieste di controllo specificate, ad eccezione della richiesta di \_ interrogazione del controllo del servizio \_ , che viene sempre inviata. Per un elenco delle richieste di controllo che un servizio può accettare, vedere il membro **dwControlsAccepted** della struttura [**\_ dello stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Per informazioni sulla registrazione per la ricezione di eventi del dispositivo, vedere la funzione [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) .

Lo stato del servizio cambia in genere in seguito alla gestione di una richiesta di controllo. Le richieste di controllo che provocano la modifica dello stato del servizio includono l'arresto del controllo del servizio, la sospensione del controllo del servizio \_ e il \_ controllo del \_ \_ servizio \_ \_ continuano Se il servizio deve eseguire un'elaborazione lunga per gestire una di queste richieste, deve creare un thread secondario per eseguire l'elaborazione lunga e segnalare lo stato in sospeso corrispondente a SCM. Per prestazioni ottimali in Windows Vista e versioni successive di Windows, il servizio deve usare un thread di lavoro da un [pool di thread](/windows/desktop/ProcThread/thread-pools) a questo scopo. Il servizio deve quindi segnalare la transizione di stato completata al termine dell'elaborazione di lunga durata. Per ulteriori informazioni sulla gestione delle richieste di controllo, vedere [funzione del gestore di controllo del servizio](service-control-handler-function.md).

Sono valide solo alcune transizioni di stato del servizio. Nel diagramma seguente vengono illustrate le transizioni valide.

![transizioni di stato del servizio valide](images/service-status-transitions.png)

Lo stato del servizio segnalato a SCM determina il modo in cui SCM interagisce con il servizio. Se, ad esempio, un servizio segnala l'arresto del servizio \_ \_ in sospeso, SCM non trasmette ulteriori richieste di controllo al servizio perché questo stato indica che il servizio è in fase di chiusura. Lo stato successivo segnalato dal servizio deve essere arrestato dal servizio \_ perché è l'unico stato valido dopo l'arresto del servizio \_ \_ in sospeso. Tuttavia, se un servizio segnala una transizione non valida, SCM non ha esito negativo per la chiamata.

Il diagramma seguente mostra le transizioni dello stato del servizio in modo più dettagliato, incluse le richieste di controllo avviate da un programma di controllo del servizio (il client del servizio) e le chiamate [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) che un servizio esegue per segnalare le modifiche di stato a SCM. Come indicato in precedenza, SCM Invia solo le richieste di controllo che il servizio ha specificato di accettare, quindi un servizio potrebbe non ricevere tutte le richieste visualizzate nel diagramma.

![informazioni dettagliate sulle transizioni di stato del servizio ](images/service-status-flow-diagram.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)
</dt> <dt>

[**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)
</dt> <dt>

[**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)
</dt> </dl>

 

 
