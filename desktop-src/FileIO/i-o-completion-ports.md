---
description: Le porte di completamento i/O forniscono un modello di threading efficiente per l'elaborazione di più richieste di I/O asincrone in un sistema multiprocessore.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: Porte di completamento I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882363ef99821a0b0b40810f45d609c5b5f7760c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317783"
---
# <a name="io-completion-ports"></a>Porte di completamento I/O

Le porte di completamento i/O forniscono un modello di threading efficiente per l'elaborazione di più richieste di I/O asincrone in un sistema multiprocessore. Quando un processo crea una porta di completamento di I/O, il sistema crea un oggetto Queue associato per le richieste il cui unico scopo è quello di soddisfare tali richieste. I processi che gestiscono molte richieste di I/O asincrone simultanee possono eseguire questa operazione in modo più rapido ed efficiente usando le porte di completamento I/O insieme a un pool di thread preallocato rispetto alla creazione di thread al momento della ricezione di una richiesta di I/O.

## <a name="how-io-completion-ports-work"></a>Funzionamento delle porte di completamento I/O

La funzione [**CreateIoCompletionPort**](createiocompletionport.md) crea una porta di completamento di I/o e associa uno o più handle di file a tale porta. Quando viene completata un'operazione di I/O asincrona su uno di questi handle di file, un pacchetto di completamento I/O viene accodato in ordine FIFO (First-in-First-out) alla porta di completamento I/O associata. Un utilizzo efficace di questo meccanismo consiste nel combinare il punto di sincronizzazione per più handle di file in un singolo oggetto, sebbene ci siano anche altre applicazioni utili. Si noti che mentre i pacchetti sono accodati in ordine FIFO, è possibile che vengano rimossi dalla coda in un ordine diverso.

> [!Note]
>
> Il termine *handle di file* usato qui si riferisce a un'astrazione di sistema che rappresenta un endpoint I/O sovrapposto, non solo a un file su disco. Può ad esempio essere un endpoint di rete, un socket TCP, un named pipe o uno slot di posta elettronica. È possibile utilizzare qualsiasi oggetto di sistema che supporta I/O sovrapposti. Per un elenco delle funzioni di I/O correlate, vedere la fine di questo argomento.

 

Quando un handle di file è associato a una porta di completamento, il blocco di stato passato in non verrà aggiornato finché il pacchetto non verrà rimosso dalla porta di completamento. L'unica eccezione è rappresentata dal caso in cui l'operazione originale restituisce in modo sincrono un errore. Un thread (uno creato dal thread principale o il thread principale stesso) usa la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per attendere che un pacchetto di completamento venga accodato alla porta di completamento i/o, anziché attendere il completamento dell'i/o asincrono. I thread che bloccano l'esecuzione su una porta di completamento di I/O vengono rilasciati nell'ordine LIFO (Last-in-First-out) e il pacchetto di completamento successivo viene estratto dalla coda FIFO della porta di completamento I/O per quel thread. Ciò significa che, quando un pacchetto di completamento viene rilasciato a un thread, il sistema rilascia l'ultimo thread (più recente) associato a tale porta, passando le informazioni di completamento per il completamento I/O meno recente.

Sebbene un numero qualsiasi di thread possa chiamare [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per una porta di completamento di i/o specificata, quando un thread specificato chiama **GetQueuedCompletionStatus** la prima volta, diventa associato alla porta di completamento di i/o specificata fino a quando non si verifica una delle tre situazioni seguenti: il thread viene chiuso, specifica una porta di completamento di i/o diversa o chiude la porta di completamento i/o. In altre parole, un singolo thread può essere associato, al massimo, una porta di completamento di I/O.

Quando un pacchetto di completamento viene accodato a una porta di completamento di I/O, il sistema controlla prima di tutto il numero di thread associati alla porta in esecuzione. Se il numero di thread in esecuzione è inferiore al valore di concorrenza (descritto nella sezione successiva), uno dei thread in attesa (quello più recente) può elaborare il pacchetto di completamento. Quando un thread in esecuzione ne completa l'elaborazione, in genere chiama di nuovo [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) , a quel punto restituisce con il pacchetto di completamento successivo o resta in attesa se la coda è vuota.

I thread possono utilizzare la funzione [**PostQueuedCompletionStatus ha provocato**](postqueuedcompletionstatus.md) per inserire i pacchetti di completamento in una coda della porta di completamento I/O. In questo modo, è possibile usare la porta di completamento per ricevere le comunicazioni da altri thread del processo, oltre a ricevere pacchetti di completamento I/O dal sistema I/O. La funzione **PostQueuedCompletionStatus ha provocato** consente a un'applicazione di accodare i propri pacchetti di completamento per scopi specifici alla porta di completamento i/o senza avviare un'operazione di i/o asincrona. Questa operazione è utile per inviare notifiche ai thread di lavoro degli eventi esterni, ad esempio.

Il punto di controllo della porta di completamento I/O e ogni handle di file associato alla porta di completamento I/O specifica sono noti come *riferimenti alla porta di completamento i/o*. La porta di completamento I/O viene rilasciata quando non vi sono altri riferimenti. È pertanto necessario chiudere correttamente tutti questi handle per rilasciare la porta di completamento I/O e le risorse di sistema associate. Una volta soddisfatte queste condizioni, un'applicazione deve chiudere l'handle della porta di completamento I/O chiamando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

> [!Note]
>
> Una porta di completamento I/O è associata al processo che lo ha creato e non è condivisibile tra i processi. Tuttavia, un singolo handle è condivisibile tra i thread nello stesso processo.

 

## <a name="threads-and-concurrency"></a>Thread e concorrenza

La proprietà più importante di una porta di completamento I/O da considerare con attenzione è il valore di concorrenza. Il valore di concorrenza di una porta di completamento viene specificato quando viene creato con [**CreateIoCompletionPort**](createiocompletionport.md) tramite il parametro *NumberOfConcurrentThreads* . Questo valore limita il numero di thread eseguibili associati alla porta di completamento. Quando il numero totale di thread eseguibili associati alla porta di completamento raggiunge il valore di concorrenza, il sistema blocca l'esecuzione di tutti i thread successivi associati alla porta di completamento finché il numero di thread eseguibili scende sotto il valore di concorrenza.

Lo scenario più efficiente si verifica quando i pacchetti di completamento sono in attesa nella coda, ma non è possibile soddisfare le attese perché la porta ha raggiunto il limite di concorrenza. Si consideri cosa accade con un valore di concorrenza di uno e più thread in attesa nella chiamata di funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . In questo caso, se la coda include sempre pacchetti di completamento in attesa, quando il thread in esecuzione chiama **GetQueuedCompletionStatus**, l'esecuzione non verrà bloccata perché, come indicato in precedenza, la coda di thread è LIFO. Al contrario, il thread rileverà immediatamente il successivo pacchetto di completamento in coda. Non si verificheranno commutazioni di contesto dei thread perché il thread in esecuzione continua a raccogliere i pacchetti di completamento e gli altri thread non possono essere eseguiti.

> [!Note]
>
> Nell'esempio precedente, i thread aggiuntivi sembrano inutili e non vengono mai eseguiti, ma ciò presuppone che il thread in esecuzione non venga mai inserito in uno stato di attesa da un altro meccanismo, termina o chiude la porta di completamento di I/O associata. Prendere in considerazione tutte le ramificazioni di esecuzione dei thread durante la progettazione dell'applicazione.

 

Il valore massimo complessivo migliore da selezionare per il valore di concorrenza è il numero di CPU nel computer. Se la transazione richiede un calcolo lungo, un valore di concorrenza maggiore consentirà l'esecuzione di più thread. Ogni pacchetto di completamento potrebbe richiedere più tempo, ma più pacchetti di completamento verranno elaborati contemporaneamente. È possibile provare a usare il valore di concorrenza insieme agli strumenti di profilatura per ottenere l'effetto migliore per l'applicazione.

Il sistema consente inoltre a un thread in attesa di [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) di elaborare un pacchetto di completamento se un altro thread in esecuzione associato alla stessa porta di completamento di I/O entra in uno stato di attesa per altri motivi, ad esempio la funzione [**SuspendThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) . Quando inizia a eseguire di nuovo il thread nello stato di attesa, potrebbe verificarsi un breve periodo di tempo in cui il numero di thread attivi supera il valore di concorrenza. Tuttavia, il sistema riduce rapidamente questo numero non consentendo alcun nuovo thread attivo fino a quando il numero di thread attivi non scende al di sotto del valore di concorrenza. Questo è uno dei motivi per cui l'applicazione crea più thread nel pool di thread rispetto al valore di concorrenza. La gestione dei pool di thread esula dall'ambito di questo argomento, ma una regola empirica consiste nel disporre di un minimo di due volte il numero di thread nel pool di thread, perché sono presenti processori nel sistema. Per ulteriori informazioni sul pool di thread, vedere [pool di thread](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Funzioni di I/O supportate

Le funzioni seguenti possono essere utilizzate per avviare le operazioni di I/O che vengono completate utilizzando le porte di completamento I/O. È necessario passare alla funzione un'istanza della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e un handle di file precedentemente associato a una porta di completamento i/o (tramite una chiamata a [**CreateIoCompletionPort**](createiocompletionport.md)) per abilitare il meccanismo della porta di completamento i/o:

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**WSASendTo**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**WSASend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**WSARecvFrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[Informazioni su processi e thread](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**BindIoCompletionCallback ha provocato**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus ha provocato**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
