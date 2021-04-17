---
title: Single-Threaded Apartment
description: Single-Threaded Apartment
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0a8cb1422b6866d9e0d043fdd46c895e6d335b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399761"
---
# <a name="single-threaded-apartments"></a>Single-Threaded Apartment

L'uso di Apartment a thread singolo (il processo del modello di Apartment) offre un paradigma basato su messaggi per la gestione simultanea di più oggetti. Consente di scrivere codice più efficiente consentendo a un thread di attendere il completamento di un'operazione che richiede molto tempo, per consentire l'esecuzione di un altro thread.

Ogni thread in un processo inizializzato come processo del modello di Apartment e che recupera e invia messaggi della finestra è un thread apartment a thread singolo. Ogni thread risiede all'interno del proprio Apartment. All'interno di un Apartment, i puntatori all'interfaccia possono essere passati senza marshalling e, di conseguenza, tutti gli oggetti in un thread apartment a thread singolo comunicano direttamente.

Un raggruppamento logico di oggetti correlati che tutti vengono eseguiti sullo stesso thread e pertanto deve avere un'esecuzione sincrona può risiedere nello stesso thread apartment a thread singolo. Tuttavia, un oggetto modello di Apartment non può trovarsi in più di un thread. Le chiamate a oggetti in altri thread devono essere effettuate all'interno del contesto del thread proprietario, in modo che i commutatori COM distribuiti automaticamente i thread quando si chiama su un proxy.

I modelli interprocesso e interthreading sono simili. Quando è necessario passare un puntatore di interfaccia a un oggetto in un altro Apartment (in un altro thread) nello stesso processo, si usa lo stesso modello di marshalling utilizzato dagli oggetti in processi diversi per passare i puntatori attraverso i limiti del processo. Ottenendo un puntatore all'oggetto di marshalling standard, è possibile effettuare il marshalling di puntatori di interfaccia tra i limiti dei thread (tra Apartment) nello stesso modo in cui si esegue tra i processi. (È necessario effettuare il marshalling di puntatori a interfaccia se passati tra Apartment).

Le regole per gli Apartment a thread singolo sono semplici, ma è importante seguirle attentamente:

-   Ogni oggetto deve risiedere su un solo thread (all'interno di un Apartment a thread singolo).
-   Inizializzare la libreria COM per ogni thread.
-   Eseguire il marshalling di tutti i puntatori a oggetti quando vengono passati tra Apartment.
-   Ogni Apartment a thread singolo deve disporre di un ciclo di messaggi per gestire le chiamate da altri processi e Apartment nello stesso processo. Gli Apartment a thread singolo senza oggetti (solo client) necessitano anche di un ciclo di messaggi per inviare i messaggi di trasmissione utilizzati da alcune applicazioni.
-   Gli oggetti basati su DLL o in-process non chiamano le funzioni di inizializzazione COM. al contrario, registrano il modello di threading con il valore denominato **ThreadingModel** sotto la chiave [InprocServer32](inprocserver32.md) nel registro di sistema. Gli oggetti compatibili con l'Apartment devono anche scrivere attentamente i punti di ingresso della DLL. Esistono considerazioni speciali che si applicano al threading nei server in-process. Per ulteriori informazioni, vedere [problemi di threading del server in-process](in-process-server-threading-issues.md).

Mentre più oggetti possono risiedere in un singolo thread, nessun oggetto modello di Apartment può risiedere in più di un thread.

Ogni thread di un processo client o di un server out-of-process deve chiamare [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize)oppure chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) e specificare CoInit \_ ApartmentThreaded per il parametro *dwCoInit* . L'Apartment principale è il thread che chiama prima **CoInitializeEx** . Per informazioni sui server in-process, vedere [problemi di threading del server in-process](in-process-server-threading-issues.md).

Tutte le chiamate a un oggetto devono essere effettuate sul relativo thread (all'interno dell'Apartment). Non è consentito chiamare un oggetto direttamente da un altro thread. l'uso di oggetti in questo modo a thread libero può causare problemi per le applicazioni. L'implicazione di questa regola è che tutti i puntatori agli oggetti devono essere sottoposti a marshalling quando passati tra Apartment. COM fornisce le due funzioni seguenti a questo scopo:

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) esegue il marshalling di un'interfaccia in un oggetto flusso restituito al chiamante.
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) esegue l'unmarshalling di un puntatore a interfaccia da un oggetto flusso e lo rilascia.

Queste funzioni incapsulano le chiamate alle funzioni [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) , che richiedono l'uso del \_ flag InProc di MSHCTX.

In generale, il marshalling viene eseguito automaticamente da COM. Ad esempio, quando si passa un puntatore di interfaccia come parametro in una chiamata al metodo su un proxy a un oggetto in un altro Apartment o quando si chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), com esegue automaticamente il marshalling. Tuttavia, in alcuni casi particolari, in cui il writer dell'applicazione passa i puntatori di interfaccia tra gli Apartment senza usare i normali meccanismi COM, il writer deve gestire manualmente il marshalling.

Se un Apartment (Apartment 1) in un processo dispone di un puntatore a interfaccia e un altro Apartment (Apartment 2) ne richiede l'uso, l'Apartment 1 deve chiamare [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) per effettuare il marshalling dell'interfaccia. Il flusso creato da questa funzione è thread-safe e deve essere archiviato in una variabile accessibile dall'Apartment 2. L'Apartment 2 deve passare questo flusso a [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) per annullare il marshalling dell'interfaccia e ottenere un puntatore a un proxy tramite il quale può accedere all'interfaccia. L'Apartment principale deve rimanere attivo fino a quando il client non ha completato tutte le operazioni COM (poiché alcuni oggetti in-process vengono caricati nell'Apartment principale, come descritto in [problemi di threading del server in-process](in-process-server-threading-issues.md)). Dopo che un oggetto è stato passato tra i thread in questo modo, è molto facile passare i puntatori all'interfaccia come parametri. In questo modo, Distributed COM esegue il marshalling e il cambio di thread per l'applicazione.

Per gestire le chiamate da altri processi e appartamenti nello stesso processo, ogni Apartment a thread singolo deve avere un ciclo di messaggi. Ciò significa che la funzione lavoro del thread deve avere un ciclo GetMessage/DispatchMessage. Se vengono utilizzate altre primitive di sincronizzazione per la comunicazione tra thread, è possibile usare la funzione [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) per attendere sia per i messaggi sia per gli eventi di sincronizzazione dei thread. La documentazione relativa a questa funzione presenta un esempio di questo tipo di ciclo combinato.

COM crea una finestra nascosta usando la classe Windows "OleMainThreadWndClass" in ogni Apartment a thread singolo. Una chiamata a un oggetto viene ricevuta come messaggio di finestra in questa finestra nascosta. Quando l'Apartment dell'oggetto recupera e invia il messaggio, la finestra nascosta lo riceverà. La routine della finestra chiamerà quindi il metodo di interfaccia corrispondente dell'oggetto.

Quando più client chiamano un oggetto, le chiamate vengono accodate nella coda di messaggi e l'oggetto riceve una chiamata ogni volta che l'Apartment recupera e invia i messaggi. Poiché le chiamate sono sincronizzate da COM e le chiamate vengono sempre recapitate dal thread che appartiene all'Apartment dell'oggetto, le implementazioni dell'interfaccia dell'oggetto non devono fornire la sincronizzazione. Gli Apartment a thread singolo possono implementare [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) per consentire loro di annullare chiamate o ricevere messaggi della finestra quando necessario.

L'oggetto può essere riavviato se una delle implementazioni del metodo di interfaccia recupera e invia messaggi o esegue una chiamata ORPC a un altro thread, causando così l'invio di un'altra chiamata all'oggetto (dallo stesso Apartment). OLE non impedisce la rientranza sullo stesso thread, ma può aiutare a fornire thread safety. Si tratta di un metodo identico al modo in cui è possibile immettere nuovamente una routine della finestra se recupera e invia messaggi durante l'elaborazione di un messaggio. Tuttavia, la chiamata a un server Apartment a thread singolo out-of-process che chiama un altro Apartment server a thread singolo consentirà di reimmettere il primo server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra gli Apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartment con multithreading](multithreaded-apartments.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e Apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 