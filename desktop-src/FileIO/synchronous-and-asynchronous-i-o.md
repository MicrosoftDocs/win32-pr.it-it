---
description: "Esistono due tipi di sincronizzazione di input/output (I/O): I/O sincrono e I/O asincrono. L'I/O asincrono è detto anche I/O sovrapposto."
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: I/O sincrono e asincrono
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 99ab06fac66c0ff3033407326c190ce0d08e643ca30b24ff17b7420e61782222
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981826"
---
# <a name="synchronous-and-asynchronous-io"></a>I/O sincrono e asincrono

Vedere anche [Applicazioni di esempio correlate all'I/O.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io)

Esistono due tipi di sincronizzazione di input/output (I/O): I/O sincrono e I/O asincrono. L'I/O asincrono è detto anche I/O sovrapposto.

*Nell'I/O* di file sincrono, un thread avvia un'operazione di I/O e entra immediatamente in uno stato di attesa fino al completamento della richiesta di I/O. Un thread che *esegue l'I/O asincrono* dei file invia una richiesta di I/O al kernel chiamando una funzione appropriata. Se la richiesta viene accettata dal kernel, il thread chiamante continua a elaborare un altro processo fino a quando il kernel segnala al thread che l'operazione di I/O è stata completata. Interrompe quindi il processo corrente ed elabora i dati dall'operazione di I/O in base alle esigenze.

I due tipi di sincronizzazione sono illustrati nella figura seguente.

![I/O sincrono e asincrono](images/fig2bedit.png)

Nelle situazioni in cui una richiesta di I/O richiede una notevole quantità di tempo, ad esempio un aggiornamento o un backup di un database di grandi dimensioni o un collegamento di comunicazione lento, l'I/O asincrono è in genere un buon metodo per ottimizzare l'efficienza di elaborazione. Tuttavia, per le operazioni di I/O relativamente veloci, l'overhead dell'elaborazione delle richieste di I/O del kernel e dei segnali del kernel può rendere meno vantaggioso l'I/O asincrono, in particolare se è necessario eseguire molte operazioni di I/O veloci. In questo caso, l'I/O sincrono è migliore. I meccanismi e i dettagli di implementazione di come eseguire queste attività variano a seconda del tipo di handle di dispositivo usato e delle esigenze specifiche dell'applicazione. In altre parole, esistono in genere più modi per risolvere il problema.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Considerazioni sull'I/O sincrono e asincrono

Se un file o un dispositivo viene aperto per operazioni di I/O sincrone (ovvero non è specificato **FILE \_ FLAG \_ OVERLAPPED),** le chiamate successive a funzioni come [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) possono bloccare l'esecuzione del thread chiamante fino a quando non si verifica uno degli eventi seguenti:

-   L'operazione di I/O viene completata (in questo esempio, una scrittura di dati).
-   Si è verificato un errore di I/O. Ad esempio, la pipe viene chiusa dall'altra estremità.
-   Si è verificato un errore nella chiamata stessa (ad esempio, uno o più parametri non sono validi).
-   Un altro thread del processo chiama la funzione [**CancelSynchronousIo**](cancelsynchronousio-func.md) usando l'handle di thread del thread bloccato, che termina l'I/O per tale thread, interrompendo l'operazione di I/O.
-   Il thread bloccato viene terminato dal sistema. Ad esempio, il processo stesso viene terminato o un altro thread chiama la [**funzione TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) usando l'handle del thread bloccato. In genere si tratta di un'ultima risorsa e non di una buona progettazione di applicazioni.

In alcuni casi, questo ritardo può non essere accettabile per la progettazione e lo scopo dell'applicazione, pertanto i progettisti di applicazioni devono prendere in considerazione l'uso di I/O asincrono con oggetti di sincronizzazione dei thread appropriati, ad esempio le porte di completamento [di I/O](i-o-completion-ports.md). Per altre informazioni sulla sincronizzazione dei thread, vedere [Informazioni sulla sincronizzazione.](/windows/desktop/Sync/about-synchronization)

Un processo apre un file per l'I/O asincrono nella chiamata a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) specificando il flag **FILE FLAG \_ \_ OVERLAPPED** nel *parametro dwFlagsAndAttributes.* Se **\_ l'opzione FILE FLAG \_ OVERLAPPED** non è specificata, il file viene aperto per operazioni di I/O sincrone. Quando il file è stato aperto per operazioni di I/O asincrone, un puntatore a una struttura [**OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) viene passato nella chiamata a [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) [**e WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Quando si esegue l'I/O sincrono, questa struttura non è necessaria nelle chiamate a **ReadFile** **e WriteFile.**

> [!Note]  
> Se un file o un dispositivo viene aperto per operazioni di I/O asincrone, le chiamate successive a funzioni come [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) che usano tale handle in genere restituiscono immediatamente, ma possono anche comportarsi in modo sincrono per quanto riguarda l'esecuzione bloccata. Per altre informazioni, vedere [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Sebbene [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) sia la funzione più comune da usare per l'apertura di file, volumi del disco, pipe anonime e altri dispositivi simili, le operazioni di I/O possono essere eseguite anche usando un *typecast* di handle da altri oggetti di sistema, ad esempio un socket creato dal [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) o le funzioni [**accept.**](/windows/desktop/api/winsock2/nf-winsock2-accept)

Gli handle per gli oggetti directory vengono ottenuti chiamando [**la funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con l'attributo **FILE FLAG BACKUP \_ \_ \_ SEMANTICS.** Gli handle di directory non vengono quasi mai usati: le applicazioni di backup sono una delle poche applicazioni che in genere li usano.

Dopo aver aperto l'oggetto file per l'I/O asincrono, è necessario creare, inizializzare e passare correttamente una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) in ogni chiamata a funzioni come [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) [**e WriteFile.**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) Quando si usa la struttura [**OVERLAPPED**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) nelle operazioni asincrone di lettura e scrittura, tenere presente quanto segue:

-   Non deallocare o modificare la struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) o il buffer di dati fino al completamento di tutte le operazioni di I/O asincrone sull'oggetto file.
-   Se si dichiara il puntatore alla struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) come variabile locale, non uscire dalla funzione locale fino al completamento di tutte le operazioni di I/O asincrone sull'oggetto file. Se la funzione locale viene chiusa in modo prematuro, la struttura **OVERLAPPED** non rientra nell'ambito e non sarà accessibile a qualsiasi funzione [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) rilevata all'esterno di tale funzione.

È anche possibile creare un evento e inserire l'handle nella [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Le [funzioni di attesa](/windows/desktop/Sync/wait-functions) possono quindi essere usate per attendere il completamento dell'operazione di I/O attendendo l'handle dell'evento.

Come indicato in precedenza, quando si lavora con un handle asincrono, le applicazioni devono fare attenzione quando determinano quando liberare le risorse associate a un'operazione di I/O specificata su tale handle. Se l'handle viene deallocato prematuramente, [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) potrebbe segnalare erroneamente che l'operazione di I/O è stata completata. Inoltre, la **funzione WriteFile** restituisce talvolta **TRUE** con un valore [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) di **ERROR \_ SUCCESS,** anche se usa un handle asincrono (che può anche restituire **FALSE** con ERROR **IO \_ \_ PENDING).** I programmatori abituati alla progettazione di I/O sincrona rilasceranno in genere le risorse del buffer di dati a questo punto perché **TRUE** e **ERROR \_ SUCCESS** significano che l'operazione è stata completata. Tuttavia, se [le porte di completamento I/O](i-o-completion-ports.md) vengono usate con questo handle asincrono, verrà inviato anche un pacchetto di completamento anche se l'operazione di I/O viene completata immediatamente. In altre parole, se l'applicazione libera le risorse dopo **che WriteFile** restituisce **TRUE** con **ERROR \_ SUCCESS** oltre che nella routine della porta di completamento I/O, avrà una condizione di errore doppia. In questo esempio, si consiglia di consentire alla routine della porta di completamento di essere l'unica responsabile di tutte le operazioni di liberamento per tali risorse.

Il sistema non mantiene il puntatore del file su handle asincroni per file e dispositivi che supportano i puntatori ai file (ovvero la ricerca di dispositivi), pertanto la posizione del file deve essere passata alle funzioni di lettura e scrittura nei membri dati offset correlati della struttura [**OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Per altre informazioni, vedere [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) [**e ReadFile.**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)

La posizione del puntatore del file per un handle sincrono viene gestita dal sistema durante la lettura o la scrittura dei dati e può essere aggiornata anche usando la [**funzione SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) o [**SetFilePointerEx.**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex)

Un'applicazione può anche attendere l'handle di file per sincronizzare il completamento di un'operazione di I/O, ma questa operazione richiede estrema cautela. Ogni volta che viene avviata un'operazione di I/O, il sistema operativo imposta l'handle di file sullo stato nonsignaled. Ogni volta che viene completata un'operazione di I/O, il sistema operativo imposta l'handle di file sullo stato segnalato. Pertanto, se un'applicazione avvia due operazioni di I/O e attende l'handle di file, non è possibile determinare quale operazione viene completata quando l'handle è impostato sullo stato segnalato. Se un'applicazione deve eseguire più operazioni di I/O asincrone su un singolo file, deve attendere l'handle dell'evento nella struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) specifica per ogni operazione di I/O, anziché sull'handle di file comune.

Per annullare tutte le operazioni di I/O asincrone in sospeso, usare:

-   [**CancelIo:**](cancelio.md)questa funzione annulla solo le operazioni eseguite dal thread chiamante per l'handle di file specificato.
-   [**CancelIoEx:**](cancelioex-func.md)questa funzione annulla tutte le operazioni eseguite dai thread per l'handle di file specificato.

Usare [**CancelSynchronousIo per**](cancelsynchronousio-func.md) annullare le operazioni di I/O sincrone in sospeso.

Le [**funzioni ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) consentono a un'applicazione di specificare una routine da eseguire (vedere [**FileIOCompletionRoutine)**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)al termine della richiesta di I/O asincrona.

 

 
