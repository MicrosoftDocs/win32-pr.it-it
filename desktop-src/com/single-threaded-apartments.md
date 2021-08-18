---
title: Single-Threaded Apartment
description: Single-Threaded Apartment
ms.assetid: 2f345ae2-8314-4067-a6d6-5a0275941ed4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f9b969a48fd83ac82307c42bf4e801168bcf97f83536045fc078b19e3eb77d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129823"
---
# <a name="single-threaded-apartments"></a>Single-Threaded Apartment

L'uso di apartment a thread singolo (processo del modello apartment) offre un paradigma basato su messaggi per gestire più oggetti in esecuzione contemporaneamente. Consente di scrivere codice più efficiente consentendo a un thread, mentre attende il completamento di un'operazione dispendiosa in termini di tempo, per consentire l'esecuzione di un altro thread.

Ogni thread in un processo inizializzato come processo del modello di apartment e che recupera e invia messaggi di finestra è un thread apartment a thread singolo. Ogni thread si trova all'interno del proprio apartment. All'interno di un apartment, i puntatori a interfaccia possono essere passati senza marshalling e pertanto tutti gli oggetti in un thread apartment a thread singolo comunicano direttamente.

Un raggruppamento logico di oggetti correlati che vengono tutti eseguiti sullo stesso thread e pertanto deve avere un'esecuzione sincrona può essere attivo nello stesso thread di apartment a thread singolo. Tuttavia, un oggetto modello apartment non può risiedere in più di un thread. Le chiamate a oggetti in altri thread devono essere effettuate all'interno del contesto del thread proprietario, in modo che COM distribuito commuti automaticamente i thread quando si chiama su un proxy.

I modelli interprocesso e interthread sono simili. Quando è necessario passare un puntatore a interfaccia a un oggetto in un altro apartment (in un altro thread) all'interno dello stesso processo, si usa lo stesso modello di marshalling utilizzato da oggetti in processi diversi per passare puntatori attraverso i limiti del processo. Ottenendo un puntatore all'oggetto di marshalling standard, è possibile effettuare il marshalling dei puntatori di interfaccia attraverso i limiti dei thread (tra gli apartment) nello stesso modo in cui si effettuano tra i processi. È necessario effettuare il marshalling dei puntatori a interfaccia quando vengono passati tra apartment.

Le regole per gli apartment a thread singolo sono semplici, ma è importante seguirle attentamente:

-   Ogni oggetto deve essere attivo in un solo thread (all'interno di un apartment a thread singolo).
-   Inizializzare la libreria COM per ogni thread.
-   Effettua il marshalling di tutti i puntatori agli oggetti quando li passa tra gli apartment.
-   Ogni apartment a thread singolo deve avere un ciclo di messaggi per gestire le chiamate da altri processi e apartment all'interno dello stesso processo. Anche gli apartment a thread singolo senza oggetti (solo client) necessitano di un ciclo di messaggi per inviare i messaggi trasmessi utilizzati da alcune applicazioni.
-   Gli oggetti basati su DLL o in-process non chiamano le funzioni di inizializzazione COM. ma registrano il modello di threading con il valore denominato **ThreadingModel** nella chiave [InprocServer32](inprocserver32.md) del Registro di sistema. Gli oggetti che sono in grado di riconoscere apartment devono anche scrivere con attenzione i punti di ingresso dll. Esistono considerazioni speciali che si applicano ai server in-process di threading. Per altre informazioni, vedere [Problemi di threading del server in-process.](in-process-server-threading-issues.md)

Mentre più oggetti possono essere presenti in un singolo thread, nessun oggetto modello apartment può essere attivo in più di un thread.

Ogni thread di un processo client o di un server out-of-process deve chiamare [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize)oppure [**chiamare CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) e specificare COINIT APARTMENTTHREADED per il \_ parametro *dwCoInit.* L'apartment principale è il thread che chiama **prima CoInitializeEx.** Per informazioni sui server in-process, vedere [Problemi di threading del server in-process.](in-process-server-threading-issues.md)

Tutte le chiamate a un oggetto devono essere effettuate sul relativo thread (all'interno del relativo apartment). Non è consentito chiamare un oggetto direttamente da un altro thread. L'uso di oggetti in questo modo a thread libero può causare problemi per le applicazioni. L'implicazione di questa regola è che tutti i puntatori agli oggetti devono essere sottoposti a marshalling quando vengono passati tra apartment. COM fornisce le due funzioni seguenti a questo scopo:

-   [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) effettua il marshalling di un'interfaccia in un oggetto flusso restituito al chiamante.
-   [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) unmarshals un puntatore a interfaccia da un oggetto flusso e lo rilascia.

Queste funzioni eseguano il wrapping delle chiamate alle funzioni [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) e [**CoUnmarshalInterface,**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface) che richiedono l'uso del \_ flag INPROC MSHCTX.

In generale, il marshalling viene eseguito automaticamente da COM. Ad esempio, quando si passa un puntatore a interfaccia come parametro in una chiamata al metodo su un proxy a un oggetto in un altro apartment o quando si chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), COM esegue automaticamente il marshalling. Tuttavia, in alcuni casi speciali, in cui il writer dell'applicazione passa puntatori a interfaccia tra apartment senza usare i normali meccanismi COM, il writer deve gestire manualmente il marshalling.

Se un apartment (Apartment 1) in un processo ha un puntatore a interfaccia e un altro apartment (Apartment 2) ne richiede l'uso, Apartment 1 deve chiamare [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) per effettuare il marshalling dell'interfaccia. Il flusso creato da questa funzione è thread-safe e deve essere archiviato in una variabile accessibile da Apartment 2. L'apartment 2 deve passare questo flusso a [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream) per eseguire l'unmarshaling dell'interfaccia e otterrà un puntatore a un proxy tramite il quale può accedere all'interfaccia. L'apartment principale deve rimanere attivo fino a quando il client non ha completato tutte le operazioni COM (perché alcuni oggetti in-process vengono caricati nell'apartment principale, come descritto in Problemi di threading del [server in-process).](in-process-server-threading-issues.md) Dopo che un oggetto è stato passato tra thread in questo modo, è molto facile passare puntatori a interfaccia come parametri. In questo modo, COM distribuito esegue il marshalling e il cambio di thread per l'applicazione.

Per gestire le chiamate da altri processi e apartment all'interno dello stesso processo, ogni apartment a thread singolo deve avere un ciclo di messaggi. Ciò significa che la funzione di lavoro del thread deve avere un ciclo GetMessage/DispatchMessage. Se vengono usate altre primitive di sincronizzazione per comunicare tra i thread, è possibile usare la funzione [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) per attendere i messaggi e gli eventi di sincronizzazione dei thread. La documentazione per questa funzione include un esempio di questo tipo di ciclo combinato.

COM crea una finestra nascosta usando Windows classe "OleMainThreadWndClass" in ogni apartment a thread singolo. Una chiamata a un oggetto viene ricevuta come messaggio di finestra per questa finestra nascosta. Quando l'apartment dell'oggetto recupera e invia il messaggio, la finestra nascosta lo riceverà. La routine della finestra chiamerà quindi il metodo di interfaccia corrispondente dell'oggetto .

Quando più client chiamano un oggetto, le chiamate vengono accodati nella coda di messaggi e l'oggetto riceverà una chiamata ogni volta che l'apartment recupera e invia messaggi. Poiché le chiamate vengono sincronizzate da COM e le chiamate vengono sempre recapitate dal thread che appartiene all'apartment dell'oggetto, le implementazioni dell'interfaccia dell'oggetto non devono fornire la sincronizzazione. Gli apartment a thread singolo possono implementare [**IMessageFilter**](/windows/desktop/api/ObjIdl/nn-objidl-imessagefilter) per consentire loro di annullare chiamate o ricevere messaggi di finestra quando necessario.

L'oggetto può essere rientrato se una delle implementazioni del metodo di interfaccia recupera e invia messaggi o effettua una chiamata ORPC a un altro thread, causando così il recapito di un'altra chiamata all'oggetto (dallo stesso apartment). OLE non impedisce la reentrancy nello stesso thread, ma può essere utile per thread safety. Questo è identico al modo in cui una routine della finestra può essere rientrata se recupera e invia messaggi durante l'elaborazione di un messaggio. Tuttavia, la chiamata di un server apartment a thread singolo out-of-process che chiama un altro server apartment a thread singolo consentirà di rientrare nel primo server.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alle interfacce tra apartment](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Scelta del modello di threading](choosing-the-threading-model.md)
</dt> <dt>

[Apartment multithreading](multithreaded-apartments.md)
</dt> <dt>

[Problemi di threading del server in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processi, thread e apartment](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicazione a thread singolo e multithreading](single-threaded-and-multithreaded-communication.md)
</dt> </dl>

 

 