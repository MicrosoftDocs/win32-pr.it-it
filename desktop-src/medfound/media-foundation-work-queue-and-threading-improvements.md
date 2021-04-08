---
description: Questo argomento descrive i miglioramenti apportati a Windows 8 per le code di lavoro e il threading nella piattaforma Microsoft Media Foundation.
ms.assetid: 9E2A1D94-BF82-488E-8297-D524683ABE17
title: Miglioramenti della coda di lavoro e del threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b307cb00316696e075e9e9cc2a138e98e149be
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104058466"
---
# <a name="work-queue-and-threading-improvements"></a>Miglioramenti della coda di lavoro e del threading

Questo argomento descrive i miglioramenti apportati a Windows 8 per le code di lavoro e il threading nella piattaforma Microsoft Media Foundation.

-   [Comportamento di Windows 7](#windows-7-behavior)
    -   [Code di lavoro](#work-queues)
    -   [Supporto di MMCSS](#mmcss-support)
    -   [IMFRealTimeClient](#imfrealtimeclientex)
-   [Miglioramenti di Windows 8](#windows-8-improvements)
    -   [Code di lavoro multithreading](#multithreaded-work-queues)
    -   [Code di lavoro delle attività condivise](#shared-task-work-queues)
    -   [Coda di attesa](#wait-queue)
    -   [Miglioramenti al supporto di MMCSS](#enhancements-to-mmcss-support)
    -   [IMFRealTimeClientEx](#imfrealtimeclientex)
    -   [Branch topologia](#topology-branches)
-   [Indicazioni](#recommendations)
-   [Summary](#summary)
-   [Argomenti correlati](#related-topics)

## <a name="windows-7-behavior"></a>Comportamento di Windows 7

In questa sezione viene riepilogato il comportamento di Media Foundation code di lavoro in Windows 7.

### <a name="work-queues"></a>Code di lavoro

La piattaforma Media Foundation crea diverse code di lavoro standard. Solo due sono documentati come utilizzo generale dell'applicazione:

-   **MFASYNC \_ coda di callback \_ \_ standard**
-   **\_ \_ \_ funzione Long coda callback \_ MFASYNC**

Un'applicazione o un componente può allocare nuove code di lavoro chiamando [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) o [**MFAllocateWorkQueueEx**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex). La funzione **MFAllocateWorkQueueEx** definisce due tipi di coda di lavoro:

-   **MF \_ \_WORKQUEUE standard** crea una coda di lavoro senza un ciclo di messaggi.
-   **MF \_ La finestra \_ WORKQUEUE** crea una coda di lavoro con un ciclo di messaggi.

Per accodare un elemento di lavoro, chiamare [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) o [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). La piattaforma esegue l'elemento di lavoro richiamando l'implementazione fornita dal chiamante di [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback). In Windows 7 e versioni precedenti, la piattaforma crea un thread per ogni coda di lavoro.

### <a name="mmcss-support"></a>Supporto di MMCSS

Il [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) gestisce le priorità dei thread in modo che le applicazioni multimediali ottengano intervalli regolari di tempo della CPU, senza negare le risorse della CPU alle applicazioni con priorità più bassa. MMCSS definisce un set di *attività* con profili di utilizzo della CPU diversi. Quando un thread unisce un'attività MMCSS, MMCSS imposta la priorità del thread in base a diversi fattori:

-   Priorità di base dell'attività, impostata nel registro di sistema.
-   Priorità del thread relativa, impostata in fase di esecuzione chiamando [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).
-   Diverse caratteristiche in fase di esecuzione, ad esempio se l'applicazione è in primo piano e quanto tempo CPU viene utilizzato dai thread in ogni classe MMCSS.

Un'applicazione può registrare una coda di lavoro con MMCSS chiamando [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss). Questa funzione accetta un ID coda di lavoro, una classe MMCSS (nome attività) e l'identificatore attività MMCSS. Internamente, chiama [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) con il nome dell'attività e l'ID attività. Dopo la registrazione di una coda di lavoro con MMCSS, è possibile ottenere la classe e l'ID attività chiamando [**MFGetWorkQueueMMCSSClass**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcssclass) e [**MFGetWorkQueueMMCSSTaskId**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsstaskid).

La [sessione multimediale](media-session.md) fornisce un accesso di livello superiore a queste API tramite l'interfaccia [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices) . Questa interfaccia fornisce due metodi principali:

| Metodo                                                                                                            | Descrizione                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss)   | Registra una coda di lavoro con un'attività MMCSS. Questo metodo è essenzialmente un thin wrapper per [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss), ma è possibile passare il valore **MFASYNC \_ coda di callback \_ \_ All** per registrare tutte le code di lavoro della piattaforma in una sola volta. |
| [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) | Registra un ramo della topologia con una coda di lavoro.                                                                                                                                                                                                                                         |



 

Per registrare un ramo della topologia, effettuare le operazioni seguenti.

1.  Impostare l'attributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) nel nodo di origine per il ramo. Usare qualsiasi valore definito dall'applicazione.
2.  Facoltativamente, impostare la **\_ classe MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS** per aggiungere la coda di lavoro a un'attività MMCSS.
3.  Chiamare [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sulla topologia risolta.

La sessione multimediale alloca una nuova coda di lavoro per ogni valore univoco di [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md). Per ogni ramo della topologia, le operazioni asincrone della pipeline vengono eseguite nella coda di lavoro assegnata al ramo.

### <a name="imfrealtimeclient"></a>IMFRealTimeClient

L'interfaccia [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient) è destinata ai componenti della pipeline che creano i propri thread o utilizzano le code di lavoro per le operazioni asincrone. La sessione multimediale usa questa interfaccia per notificare al componente della pipeline il comportamento corretto, come indicato di seguito:

-   Se il componente della pipeline crea un thread di lavoro, il metodo [**IMFRealTimeClient:: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads) invia una notifica al componente a cui è stata aggiunta la classe MMCSS.
-   Se il componente della pipeline usa una coda di lavoro, il metodo [**IMFRealTimeClient:: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue) indica al componente la coda di lavoro da usare.

In genere, un componente della pipeline utilizza un thread o una coda di lavoro per eseguire attività asincrone, ma non entrambe.

## <a name="windows-8-improvements"></a>Miglioramenti di Windows 8

### <a name="multithreaded-work-queues"></a>Code di lavoro multithreading

In Windows 8, Media Foundation supporta un nuovo tipo di coda di lavoro denominata *coda multithread*. Una coda multithread usa un pool di thread di sistema per la distribuzione degli elementi di lavoro. La coda con multithreading si ridimensiona meglio rispetto alle code a thread singolo precedenti. Ad esempio,

-   Diversi componenti possono condividere una coda multithread senza bloccarsi un altro, richiedendo la creazione di un numero inferiore di thread.

-   Gli elementi di lavoro sono ottimizzati per evitare cambi di contesto se è già impostato un evento. Questa operazione è più efficiente rispetto alla creazione di thread personalizzati per l'attesa degli eventi.

Quando si usa [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex), le applicazioni devono evitare la filatura dei thread, ma devono usare le code di lavoro. A tale scopo, le applicazioni devono implementare [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex) e non usare [**RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) e [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads).

Quando la piattaforma Media Foundation viene inizializzata, viene creata una coda con multithreading con l'identificatore **MFASYNC \_ coda di callback \_ \_ multithreading**.

Una coda multithread non serializza gli elementi di lavoro. Ogni volta che un thread dal pool di thread diventa disponibile, viene inviato il successivo elemento di lavoro nella coda. Il chiamante deve garantire che il lavoro venga serializzato correttamente. Per semplificare questa operazione, Media Foundation definisce una *coda di lavoro seriale*. Una coda seriale esegue il wrapping di un'altra coda di lavoro, ma garantisce l'esecuzione completamente serializzata. L'elemento successivo della coda non viene inviato finché non viene completato l'elemento precedente.

Il codice seguente crea una coda del serializzatore sulla coda multithreading della piattaforma.


```C++
DWORD workQueueID;
hr = MFAllocateSerialWorkQueue(MFASYNC_CALLBACK_QUEUE_MULTITHREADED, &workQueueID); 
```



Più di una coda seriale può eseguire il wrapping della stessa coda multithread. Le code seriali condividono lo stesso pool di thread e l'esecuzione serializzata viene applicata all'interno di ogni coda.

Le code di lavoro standard esistenti prima di Windows 8 sono ora implementate come code di lavoro seriali che eseguono il wrapping della coda multithreading della piattaforma. Questa modifica conserva la compatibilità con le versioni precedenti.

### <a name="shared-task-work-queues"></a>Code di lavoro delle attività condivise

Per funzionare correttamente con l'utilità di pianificazione del kernel, è necessario disporre di una coda di lavoro a thread multipli per ogni attività MMCSS usata. La piattaforma Media Foundation alloca tali richieste, fino a una per ogni attività MMCSS, per processo. Per ottenere la coda di lavoro condivisa per una particolare attività MMCSS, chiamare [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) e specificare il nome dell'attività. La funzione Cerca il nome dell'attività in una tabella. Se per questa attività non esiste già una coda di lavoro, la funzione alloca una nuova coda di lavoro MT e la aggiunge immediatamente all'attività MMCSS. Se per l'attività esiste già una coda di lavoro, la funzione restituisce l'identificatore della coda di lavoro esistente.

### <a name="wait-queue"></a>Coda di attesa

La *coda di attesa* è una coda di lavoro della piattaforma speciale che attende la segnalazione degli eventi. Se un componente deve attendere la segnalazione di un evento, può usare la coda di attesa anziché creare un thread di lavoro per attendere l'evento.

Per utilizzare la coda di attesa, chiamare [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem). I parametri includono l'handle di evento e un puntatore [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Quando l'evento viene segnalato, la coda di attesa richiama il callback. È presente una singola coda di attesa della piattaforma; le applicazioni non possono creare le proprie code di attesa.

### <a name="enhancements-to-mmcss-support"></a>Miglioramenti al supporto di MMCSS

Le nuove funzioni della piattaforma Media Foundation seguenti sono correlate a MMCSS.



| Funzione                                                                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex) | Registra una coda di lavoro con MMCSS. Questa funzione include un parametro per specificare la priorità relativa del thread. Internamente, questo valore viene convertito in una chiamata a [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).                                                                                                                                                                               |
| [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)                 | Esegue una query sulla priorità di una coda di lavoro.                                                                                                                                                                                                                                                                                                                                                                 |
| [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)                 | Registra tutte le code di lavoro della piattaforma con un'attività MMCSS. Questa funzione è simile al metodo [**IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) , ma può essere usata senza creare un'istanza della sessione multimediale. Inoltre, la funzione include un parametro per specificare la priorità del thread di base. |



 

Per le applicazioni che usano la sessione multimediale è necessario impostare l'attributo della [ \_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) su "audio" per il ramo di rendering audio. Impostare l'attributo su "Playback" per il ramo di rendering video.

### <a name="imfrealtimeclientex"></a>IMFRealTimeClientEx

Interfaccia [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex) che sostituisce IMFRealTimeClient per i componenti della pipeline che eseguono operazioni asincrone.



| Metodo                                                             | Descrizione                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RegisterThreadsEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) | Notifica al componente di registrare i thread con MMCSS. Questo metodo è equivalente a [**IMFRealTimeClient:: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads), ma aggiunge un parametro per la priorità del thread di base. |
| [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex)       | Notifica al componente di utilizzare una coda di lavoro specifica. Questo metodo è equivalente a [**IMFReadTimeClient:: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue), ma aggiunge un parametro per la priorità dell'elemento di lavoro.               |
| [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads) | Notifica al componente di annullare la registrazione dei thread da MMCSS. Questo metodo è identico al metodo [**IMFRealTimeClient:: UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-unregisterthreads) .                                       |



 

I componenti della pipeline devono usare le code di lavoro e non devono creare thread di lavoro per i motivi seguenti:

-   Le code di lavoro si adattano meglio, perché usano i pool di thread del sistema operativo.
-   La piattaforma gestisce i dettagli della registrazione delle code di lavoro con MMCSS.
-   Un thread di lavoro può facilmente causare un deadlock che è difficile eseguire il debug.

Si consiglia inoltre di utilizzare la coda di lavoro del serializzatore se è necessario serializzare le operazioni asincrone.

### <a name="topology-branches"></a>Branch topologia

Se l'attributo della [ \_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) registra un ramo della topologia con MMCSS, in Windows 8 la sessione multimediale usa le code di lavoro mt condivise. Nelle versioni precedenti di Windows, la sessione multimediale ha allocato una nuova coda di lavoro.

Vengono definiti due nuovi attributi per la registrazione di un ramo della topologia con MMCSS.



| Attributo                                                                            | Descrizione                         |
|--------------------------------------------------------------------------------------|-------------------------------------|
| [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Priority](mf-toponode-workqueue-mmcss-priority.md) | Specifica la priorità del thread di base. |
| [\_ \_ \_ priorità elemento WORKQUEUE MF \_ TOPONODE](mf-toponode-workqueue-item-priority.md)   | Specifica la priorità dell'elemento di lavoro.   |



 

## <a name="recommendations"></a>Consigli

-   Le applicazioni che usano la sessione multimediale devono impostare la [ \_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) su "audio" per il ramo di rendering audio e la "riproduzione" per il ramo di rendering video.
-   Per le applicazioni che usano la sessione multimediale è necessario chiamare [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) nella topologia.
-   Per i componenti della pipeline, le code di lavoro sono consigliate al posto dei thread di lavoro. Se il componente USA code di lavoro o thread di lavoro, implementare [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex).
-   Non creare code di lavoro private, in quanto in questo modo si vanifica lo scopo delle code di lavoro della piattaforma. Usare la coda multithreading della piattaforma o una coda seriale che esegue il wrapping della coda multithreading della piattaforma.
-   Se è necessario serializzare le operazioni asincrone, usare una coda seriale.

## <a name="summary"></a>Riepilogo

Le seguenti API della piattaforma Media Foundation correlate ai thread e alle code di lavoro sono nuove per Windows 8.

-   [\_ \_ \_ priorità elemento WORKQUEUE MF \_ TOPONODE](mf-toponode-workqueue-item-priority.md)
-   [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Priority](mf-toponode-workqueue-mmcss-priority.md)
-   [**MFAllocateSerialWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue)
-   [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex)
-   [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)
-   [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem)
-   [**MFPutWorkItem2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2)
-   [**MFPutWorkItemEx2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2)
-   [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)
-   [**MFUnregisterPlatformFromMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfunregisterplatformfrommmcss)
-   [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue)
-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 
