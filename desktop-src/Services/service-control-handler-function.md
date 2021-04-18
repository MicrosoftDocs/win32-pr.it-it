---
description: Ogni servizio dispone di un gestore di controllo, la funzione di gestione, che viene richiamata dal dispatcher del controllo quando il processo del servizio riceve una richiesta di controllo da un programma di controllo del servizio.
ms.assetid: 437334ed-05fa-4ab6-aab3-dc2739113e19
title: Funzione Handler di controllo dei servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1303bff45421ee7206d02be9ee30066324648823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306535"
---
# <a name="service-control-handler-function"></a>Funzione Handler di controllo dei servizi

Ogni servizio dispone di un gestore di controllo, la funzione di [**gestione**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) , che viene richiamata dal dispatcher del controllo quando il processo del servizio riceve una richiesta di controllo da un programma di controllo del servizio. Pertanto, questa funzione viene eseguita nel contesto del dispatcher del controllo. Per un esempio, vedere [scrittura di una funzione di gestione del controllo](writing-a-control-handler-function.md).

Un servizio chiama la funzione [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) o [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) per registrare la funzione del gestore di controllo del servizio.

Quando viene richiamato il gestore di controllo del servizio, il servizio deve chiamare la funzione [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) per segnalare lo stato a SCM solo se la gestione del codice di controllo causa la modifica dello stato del servizio. Se la gestione del codice di controllo non comporta la modifica dello stato del servizio, non è necessario chiamare **SetServiceStatus**.

Un programma di controllo del servizio può inviare richieste di controllo tramite la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Tutti i servizi devono accettare ed elaborare il codice di controllo per **\_ \_ interrogare** il controllo del servizio. È possibile abilitare o disabilitare l'accettazione degli altri codici di controllo chiamando [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Per ricevere il codice di controllo **\_ \_ DEVICEEVENT del controllo del servizio** , è necessario chiamare la funzione [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) . I servizi possono anche gestire ulteriori codici di controllo definiti dall'utente.

Se un servizio accetta il codice di controllo dell' **\_ \_ arresto del controllo del servizio** , deve arrestarsi alla ricezione, passando allo stato di arresto del servizio **\_ \_ in sospeso** o **\_ arrestato** . Al termine dell'invio del codice di controllo da parte di SCM, i codici di controllo non vengono inviati.

**Windows XP:** Se il servizio **non restituisce alcun \_ errore** e continua a essere eseguito, continua a ricevere i codici di controllo. Questo comportamento è stato modificato a partire da Windows Server 2003 e Windows XP con Service Pack 2 (SP2).

Il gestore di controllo deve restituire entro 30 secondi oppure l'oggetto SCM restituisce un errore. Se un servizio deve eseguire un'elaborazione lunga quando il servizio esegue il gestore di controllo, deve creare un thread secondario per eseguire l'elaborazione lunga e quindi tornare dal gestore del controllo. In questo modo si impedisce al servizio di bloccare il dispatcher del controllo. Ad esempio, quando si gestisce la richiesta di arresto per un servizio che richiede molto tempo, creare un altro thread per gestire il processo di arresto. Il gestore di controllo deve semplicemente chiamare [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con il messaggio di **arresto del servizio \_ \_ in sospeso** e restituire.

Quando l'utente arresta il sistema, tutti i gestori di controllo che hanno chiamato [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con il servizio accettano il codice di controllo **\_ \_ preshutdown** ricevono il codice di controllo della **\_ \_ prechiusura del controllo del servizio** . Gestione controllo servizi attende fino a quando il servizio non viene arrestato o il valore di timeout di prespegnimento specificato scade (questo valore può essere impostato con la funzione [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) ). Questo codice di controllo deve essere usato solo in circostanze particolari, perché un servizio che gestisce questa notifica blocca l'arresto del sistema fino a quando il servizio non viene arrestato o scade l'intervallo di timeout di prechiusura.

Una volta completate le notifiche di prechiusura, tutti i gestori di controllo che hanno chiamato [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) con il servizio accettano il codice di controllo di **\_ \_ arresto** per ricevere il codice di controllo dell' **arresto del \_ controllo \_ del servizio** . Viene inviata una notifica nell'ordine in cui sono visualizzate nel database dei servizi installati. Per impostazione predefinita, un servizio ha circa 20 secondi per eseguire attività di pulizia prima che il sistema venga arrestato. Al termine di questo periodo di tempo, l'arresto del sistema continua indipendentemente dal fatto che l'arresto del servizio sia stato completato. Si noti che se il sistema viene lasciato nello stato di arresto (non riavviato o spento), il servizio continua a essere eseguito.

Se il servizio richiede più tempo per la pulizia, invia i messaggi di stato di **arresto \_ in sospeso** , insieme a un hint di attesa, in modo che il controller di servizio conosca il tempo di attesa prima di segnalare al sistema che l'arresto del servizio è stato completato. Tuttavia, per impedire l'arresto di un servizio, è previsto un limite al tempo di attesa del controller di servizio. Se il servizio viene arrestato tramite lo snap-in servizi, il limite è di 125 secondi o 125.000 millisecondi. Se il sistema operativo viene riavviato, il limite di tempo viene specificato nel valore **WaitToKillServiceTimeout** (in millisecondi) della chiave del registro di sistema seguente:

**\_ \_ \\ Controllo CurrentControlSet del sistema del computer \\ locale \\ HKEY**

> [!IMPORTANT]
> Un servizio non deve tentare di aumentare il limite di tempo modificando questo valore. Se è necessario impostare **WaitToKillServiceTimeout** manualmente, il valore deve essere in millisecondi.

I clienti richiedono un arresto rapido del sistema operativo. Se, ad esempio, un computer in cui è in esecuzione la potenza di UPS non è in grado di completare l'arresto prima dell'esaurimento della potenza, i dati possono andare persi. I servizi devono pertanto completare le attività di pulizia nel minor tempo possibile. È consigliabile ridurre al minimo i dati non salvati salvando i dati a intervalli regolari, tenendo traccia dei dati salvati su disco e salvando solo i dati non salvati in caso di arresto. Poiché il computer è in fase di arresto, non dedicare tempo a rilasciare la memoria allocata o altre risorse di sistema. Se è necessario inviare una notifica a un server che si sta uscendo, ridurre al minimo il tempo trascorso in attesa di una risposta, perché i problemi di rete potrebbero ritardare l'arresto del servizio.

Si noti che durante l'arresto del servizio, per impostazione predefinita, SCM non prende in considerazione le dipendenze. SCM enumera l'elenco dei servizi in esecuzione e invia il comando **di \_ \_ arresto del controllo del servizio** . Pertanto, un servizio potrebbe non riuscire perché è già stato arrestato un altro servizio da cui dipende.

Per impostare l'ordine di arresto dei servizi manualmente, creare un valore di registro multistringa contenente i nomi dei servizi nell'ordine in cui devono essere arrestati e assegnarlo al valore **PreshutdownOrder** della chiave di controllo, come indicato di seguito:

**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ PreshutdownOrder = "Shutdown Order"**

Per impostare l'ordine di arresto dei servizi dipendenti dall'applicazione, usare la funzione [**SetProcessShutdownParameters**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) . Il controllo SCM usa questa funzione per assegnare alla priorità 0x1E0 del gestore. SCM Invia notifiche **di \_ \_ arresto del controllo del servizio** quando viene chiamato il gestore di controllo e attende la chiusura dei servizi prima di restituire il relativo gestore di controllo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scrittura di una funzione del gestore di controllo](writing-a-control-handler-function.md)
</dt> </dl>

 

 
