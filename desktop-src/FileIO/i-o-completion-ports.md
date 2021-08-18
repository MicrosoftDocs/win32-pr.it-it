---
description: Le porte di completamento I/O forniscono un modello di threading efficiente per l'elaborazione di più richieste di I/O asincrone in un sistema multiprocessore.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: Porte di completamento I/O
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2133bb14c661580eaf8004bd92c6f947b3b8777a4b1a5f6b330fe631b2be6c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050831"
---
# <a name="io-completion-ports"></a>Porte di completamento I/O

Le porte di completamento I/O forniscono un modello di threading efficiente per l'elaborazione di più richieste di I/O asincrone in un sistema multiprocessore. Quando un processo crea una porta di completamento I/O, il sistema crea un oggetto coda associato per le richieste il cui unico scopo è quello di eseguire queste richieste. I processi che gestiscono molte richieste di I/O asincrone simultanee possono eseguire questa operazione in modo più rapido ed efficiente usando le porte di completamento I/O in combinazione con un pool di thread preallocato piuttosto che creando thread nel momento in cui ricevono una richiesta di I/O.

## <a name="how-io-completion-ports-work"></a>Funzionamento delle porte di completamento I/O

La [**funzione CreateIoCompletionPort**](createiocompletionport.md) crea una porta di completamento I/O e associa uno o più handle di file a tale porta. Al termine di un'operazione di I/O asincrona su uno di questi handle di file, un pacchetto di completamento I/O viene accodato in ordine FIFO (First-In-First-Out) alla porta di completamento I/O associata. Un uso efficace di questo meccanismo è combinare il punto di sincronizzazione per più handle di file in un singolo oggetto, anche se sono disponibili anche altre applicazioni utili. Si noti che, mentre i pacchetti vengono accodati in ordine FIFO, possono essere deaccodati in un ordine diverso.

> [!Note]
>
> Il termine *handle di file* usato qui si riferisce a un'astrazione di sistema che rappresenta un endpoint di I/O sovrapposto, non solo un file su disco. Ad esempio, può essere un endpoint di rete, un socket TCP, un named pipe o uno slot di posta elettronica. È possibile usare qualsiasi oggetto di sistema che supporta operazioni di I/O sovrapposte. Per un elenco delle funzioni di I/O correlate, vedere la fine di questo argomento.

 

Quando un handle di file è associato a una porta di completamento, il blocco di stato passato non verrà aggiornato fino a quando il pacchetto non viene rimosso dalla porta di completamento. L'unica eccezione è se l'operazione originale restituisce in modo sincrono un errore. Un thread creato dal thread principale o dal thread principale stesso usa la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per attendere che un pacchetto di completamento sia accodato alla porta di completamento I/O, anziché attendere direttamente il completamento dell'I/O asincrono. I thread che bloccano l'esecuzione su una porta di completamento I/O vengono rilasciati in ordine LIFO (Last-In-First-Out) e il pacchetto di completamento successivo viene estratto dalla coda FIFO della porta di completamento I/O per il thread. Ciò significa che, quando un pacchetto di completamento viene rilasciato a un thread, il sistema rilascia l'ultimo thread (più recente) associato a tale porta, passando le informazioni di completamento per il completamento I/O meno recente.

Anche se un numero qualsiasi di thread può chiamare [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per una porta di completamento I/O specificata, quando un thread specificato chiama **GetQueuedCompletionStatus** la prima volta, viene associato alla porta di completamento I/O specificata fino a quando non si verifica una delle tre operazioni seguenti: il thread viene chiuso, specifica una porta di completamento I/O diversa o chiude la porta di completamento I/O. In altre parole, un singolo thread può essere associato al massimo a una porta di completamento I/O.

Quando un pacchetto di completamento viene accodato a una porta di completamento I/O, il sistema controlla innanzitutto il numero di thread associati a tale porta in esecuzione. Se il numero di thread in esecuzione è inferiore al valore di concorrenza (illustrato nella sezione successiva), uno dei thread in attesa (quello più recente) è autorizzato a elaborare il pacchetto di completamento. Quando un thread in esecuzione completa l'elaborazione, in genere chiama [**nuovamente GetQueuedCompletionStatus,**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) a questo punto restituisce con il pacchetto di completamento successivo o attende se la coda è vuota.

I thread possono usare [**la funzione PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) per inserire i pacchetti di completamento nella coda di una porta di completamento I/O. In questo modo, la porta di completamento può essere usata per ricevere comunicazioni da altri thread del processo, oltre a ricevere pacchetti di completamento I/O dal sistema di I/O. La **funzione PostQueuedCompletionStatus** consente a un'applicazione di accodare i propri pacchetti di completamento per scopi speciali alla porta di completamento di I/O senza avviare un'operazione di I/O asincrona. Ciò è utile per notificare ai thread di lavoro eventi esterni, ad esempio.

L'handle della porta di completamento I/O e ogni handle di file associato a tale porta di completamento di I/O specifica sono noti come riferimenti alla porta di completamento *I/O.* La porta di completamento I/O viene rilasciata quando non sono presenti altri riferimenti. Pertanto, tutti questi handle devono essere chiusi correttamente per rilasciare la porta di completamento I/O e le risorse di sistema associate. Dopo aver soddisfatto queste condizioni, un'applicazione deve chiudere l'handle della porta di completamento I/O chiamando la [**funzione CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

> [!Note]
>
> Una porta di completamento I/O è associata al processo che l'ha creata e non è gestibile da un processo all'altro. Tuttavia, un singolo handle è sharable tra i thread nello stesso processo.

 

## <a name="threads-and-concurrency"></a>Thread e concorrenza

La proprietà più importante di una porta di completamento di I/O da considerare con attenzione è il valore di concorrenza. Il valore di concorrenza di una porta di completamento viene specificato quando viene creata con [**CreateIoCompletionPort**](createiocompletionport.md) tramite il *parametro NumberOfConcurrentThreads.* Questo valore limita il numero di thread runnable associati alla porta di completamento. Quando il numero totale di thread runnable associati alla porta di completamento raggiunge il valore di concorrenza, il sistema blocca l'esecuzione di tutti i thread successivi associati a tale porta di completamento fino a quando il numero di thread runnable scende al di sotto del valore di concorrenza.

Lo scenario più efficiente si verifica quando sono presenti pacchetti di completamento in attesa nella coda, ma non è possibile soddisfatte attese perché la porta ha raggiunto il limite di concorrenza. Si consideri cosa accade con un valore di concorrenza di uno e più thread in attesa nella chiamata di funzione [**GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) In questo caso, se la coda dispone sempre di pacchetti di completamento in attesa, quando il thread in esecuzione chiama **GetQueuedCompletionStatus**, non bloccherà l'esecuzione perché, come accennato in precedenza, la coda di thread è LIFO. Al contrario, questo thread preleverà immediatamente il successivo pacchetto di completamento in coda. Non si verificheranno commutazioni di contesto del thread, perché il thread in esecuzione continua a raccogliere pacchetti di completamento e gli altri thread non possono essere eseguiti.

> [!Note]
>
> Nell'esempio precedente, i thread aggiuntivi sembrano inutili e non vengono mai eseguiti, ma ciò presuppone che il thread in esecuzione non venga mai inserito in uno stato di attesa da un altro meccanismo, termini o chiuda in altro modo la porta di completamento I/O associata. Prendere in considerazione tutte queste ramificazioni di esecuzione dei thread durante la progettazione dell'applicazione.

 

Il valore massimo complessivo migliore da selezionare per il valore di concorrenza è il numero di CPU nel computer. Se la transazione richiede un calcolo lungo, un valore di concorrenza maggiore consentirà l'esecuzione di più thread. Il completamento di ogni pacchetto di completamento può richiedere più tempo, ma verranno elaborati più pacchetti di completamento contemporaneamente. È possibile sperimentare con il valore di concorrenza in combinazione con gli strumenti di profilatura per ottenere l'effetto migliore per l'applicazione.

Il sistema consente inoltre a un thread in attesa in [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) di elaborare un pacchetto di completamento se un altro thread in esecuzione associato alla stessa porta di completamento I/O entra in uno stato di attesa per altri motivi, ad esempio la funzione [**SuspendThread.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) Quando il thread nello stato di attesa inizia di nuovo a essere in esecuzione, può verificarsi un breve periodo in cui il numero di thread attivi supera il valore di concorrenza. Tuttavia, il sistema riduce rapidamente questo numero non consentendo nuovi thread attivi fino a quando il numero di thread attivi non scende al di sotto del valore di concorrenza. Questo è uno dei motivi per cui l'applicazione crea più thread nel pool di thread rispetto al valore di concorrenza. La gestione del pool di thread non è in linea con l'ambito di questo argomento, ma una buona regola generale è avere almeno il doppio dei thread nel pool di thread rispetto ai processori nel sistema. Per altre informazioni sul pool di thread, vedere [Pool di thread](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Funzioni di I/O supportate

Le funzioni seguenti possono essere usate per avviare operazioni di I/O completate tramite porte di completamento I/O. È necessario passare alla funzione un'istanza della struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e un handle di file associato in precedenza a una porta di completamento I/O (tramite una chiamata a [**CreateIoCompletionPort**](createiocompletionport.md)) per abilitare il meccanismo di porta di completamento I/O:

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
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

[**BindIoCompletionCallback**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
