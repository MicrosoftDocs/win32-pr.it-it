---
description: "Esistono due tipi di sincronizzazione di input/output (I/O): I/o sincrono e I/O asincrono. L'I/O asincrono è noto anche come I/O sovrapposto."
ms.assetid: ade51d98-cc9d-4b33-9c52-559a9cb14707
title: I/O sincrono e asincrono
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 071dd2943537dcb6aff67a95cb5e2c3d514f4c1a
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323901"
---
# <a name="synchronous-and-asynchronous-io"></a>I/O sincrono e asincrono

Vedere anche [applicazioni di esempio correlate all'I/O](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winbase/io).

Esistono due tipi di sincronizzazione di input/output (I/O): I/o sincrono e I/O asincrono. L'I/O asincrono è noto anche come I/O sovrapposto.

Nell' *I/o di file sincrono*, un thread avvia un'operazione di i/o e immette immediatamente uno stato di attesa fino al completamento della richiesta di i/o. Un thread che esegue l' *i/o di file asincrono* invia una richiesta di i/o al kernel chiamando una funzione appropriata. Se la richiesta viene accettata dal kernel, il thread chiamante continua a elaborare un altro processo finché il kernel non segnala al thread che l'operazione di I/O è stata completata. Interrompe quindi il processo corrente ed elabora i dati dall'operazione di I/O, se necessario.

Nella figura seguente sono illustrati i due tipi di sincronizzazione.

![i/o sincrono e asincrono](images/fig2bedit.png)

Nelle situazioni in cui una richiesta di I/O richiede una quantità di tempo elevata, ad esempio un aggiornamento o un backup di un database di grandi dimensioni o di un collegamento di comunicazione lenta, l'I/O asincrono è in genere un metodo efficace per ottimizzare l'efficienza di elaborazione. Tuttavia, per le operazioni di I/O relativamente veloci, l'overhead dell'elaborazione delle richieste di I/o del kernel e dei segnali del kernel può rendere meno vantaggioso l'I/O asincrono, in particolare se è necessario eseguire molte operazioni di I/O rapide. In questo caso, l'I/O sincrono sarebbe migliore. I meccanismi e i dettagli di implementazione di come eseguire queste attività variano a seconda del tipo di handle di dispositivo usato e delle esigenze specifiche dell'applicazione. In altre parole, esistono in genere diversi modi per risolvere il problema.

## <a name="synchronous-and-asynchronous-io-considerations"></a>Considerazioni sui/O sincrone e asincrone

Se un file o un dispositivo viene aperto per l'I/O sincrono (ovvero, il **\_ flag file \_ sovrapposto** non è specificato), le chiamate successive a funzioni come [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) possono bloccare l'esecuzione del thread chiamante fino a quando non si verifica uno degli eventi seguenti:

-   L'operazione di I/O è stata completata, in questo esempio una scrittura di dati.
-   Si è verificato un errore di I/O. Ad esempio, la pipe viene chiusa dall'altra estremità.
-   Si è verificato un errore nella chiamata stessa (ad esempio, uno o più parametri non sono validi).
-   Un altro thread del processo chiama la funzione [**CancelSynchronousIo**](cancelsynchronousio-func.md) usando l'handle di thread del thread bloccato, che termina l'i/o per quel thread, in caso di errore dell'operazione di i/o.
-   Il thread bloccato viene terminato dal sistema. ad esempio, il processo stesso viene terminato o un altro thread chiama la funzione [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) usando l'handle del thread bloccato. Si tratta in genere di un'ultima soluzione e non di una corretta progettazione delle applicazioni.

In alcuni casi, questo ritardo può essere inaccettabile per la progettazione e lo scopo dell'applicazione, quindi i progettisti di applicazioni devono prendere in considerazione l'utilizzo di I/O asincrono con gli oggetti di sincronizzazione dei thread appropriati, ad esempio le [porte di completamento i/o](i-o-completion-ports.md). Per ulteriori informazioni sulla sincronizzazione dei thread, vedere [informazioni sulla sincronizzazione](/windows/desktop/Sync/about-synchronization).

Un processo apre un file per l'I/O asincrono nella chiamata a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) specificando il **flag \_ file \_ sovrapposto** nel parametro *dwFlagsAndAttributes* . Se **il \_ flag di file \_ sovrapposto** non è specificato, il file viene aperto per l'i/O sincrono. Quando il file è stato aperto per l'I/O asincrono, un puntatore a una struttura [**sovrapposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) viene passato nella chiamata a [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Quando si eseguono operazioni di I/O sincrone, questa struttura non è obbligatoria nelle chiamate a **ReadFile** e **WriteFile**.

> [!Note]  
> Se un file o un dispositivo viene aperto per l'I/O asincrono, le chiamate successive a funzioni come [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) che usano tale handle in genere restituiscono immediatamente, ma possono anche comportarsi in modo sincrono rispetto all'esecuzione bloccata. Per altre informazioni, vedere [https://support.microsoft.com/kb/156932](https://support.microsoft.com/kb/156932).

 

Sebbene [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) sia la funzione più comune da usare per l'apertura di file, volumi di dischi, pipe anonime e altri dispositivi simili, le operazioni di I/O possono essere eseguite anche usando un handle *typecast* da altri oggetti di sistema, ad esempio un socket creato dal [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) o da funzioni [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) .

Gli handle per gli oggetti directory vengono ottenuti chiamando la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con l'attributo della **\_ \_ \_ semantica di backup del flag di file** . Gli handle di directory non vengono mai usati. le applicazioni di backup sono una delle poche applicazioni che li utilizzeranno in genere.

Dopo l'apertura dell'oggetto file per l'I/O asincrono, è necessario creare, inizializzare e passare correttamente una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) a ogni chiamata a funzioni quali [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile). Quando si utilizza la struttura [**sovrapposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) nelle operazioni di lettura e scrittura asincrone, tenere presente quanto segue:

-   Non deallocare o modificare la struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) o il buffer di dati finché non sono state completate tutte le operazioni di i/O asincrone nell'oggetto file.
-   Se si dichiara il puntatore alla struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) come variabile locale, non chiudere la funzione locale finché non sono state completate tutte le operazioni di i/O asincrone nell'oggetto file. Se la funzione locale viene chiusa in modo anomalo, la struttura **sovrapposta** uscirà dall'ambito e non sarà accessibile a tutte le funzioni [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) rilevate al di fuori di tale funzione.

È anche possibile creare un evento e inserire l'handle nella struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) ; le [funzioni Wait](/windows/desktop/Sync/wait-functions) possono quindi essere usate per attendere il completamento dell'operazione di i/O in attesa dell'handle dell'evento.

Come indicato in precedenza, quando si lavora con un handle asincrono, le applicazioni devono prestare attenzione quando si determinano quando liberare le risorse associate a un'operazione di I/O specificata su tale handle. Se l'handle viene deallocato in modo anomalo, è possibile che [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) o [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) segnali erroneamente che l'operazione di i/O è stata completata. Inoltre, la funzione **WriteFile** a volte restituisce **true** con un [**valore GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) con **\_ esito positivo errore**, anche se utilizza un handle asincrono (che può restituire anche **false** con **errore \_ io \_ in sospeso**). I programmatori abituati alla progettazione di I/O sincrona in genere rilasceranno le risorse del buffer di dati in questo momento perché **true** e **Error \_ Success** indicano che l'operazione è stata completata. Tuttavia, se si utilizzano le [porte di completamento i/o](i-o-completion-ports.md) con questo handle asincrono, verrà inviato anche un pacchetto di completamento anche se l'operazione di i/o è stata completata immediatamente. In altre parole, se l'applicazione libera risorse dopo che **WriteFile** restituisce **true** con **l' \_ esito positivo dell'errore** , oltre che nella routine della porta di completamento i/O, avrà una condizione di errore double-free. In questo esempio, si consiglia di consentire alla routine della porta di completamento di essere interamente responsabile di tutte le operazioni di liberazione per tali risorse.

Il sistema non mantiene il puntatore del file sugli handle asincroni per i file e i dispositivi che supportano i puntatori a file (ovvero la ricerca di dispositivi), pertanto la posizione del file deve essere passata alle funzioni di lettura e scrittura nei membri dati offset correlati della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Per ulteriori informazioni, vedere [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) e [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile).

La posizione del puntatore del file per un handle sincrono viene gestita dal sistema quando i dati vengono letti o scritti e possono essere aggiornati anche tramite la funzione [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) o [**SetFilePointerEx**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointerex) .

Un'applicazione può inoltre attendere l'handle di file per sincronizzare il completamento di un'operazione di I/O, ma è necessario prestare estrema cautela. Ogni volta che viene avviata un'operazione di I/O, il sistema operativo imposta l'handle di file sullo stato non segnalato. Ogni volta che viene completata un'operazione di I/O, il sistema operativo imposta l'handle di file sullo stato segnalato. Pertanto, se un'applicazione avvia due operazioni di I/O e attende l'handle di file, non è possibile determinare quale operazione è terminata quando l'handle è impostato sullo stato segnalato. Se un'applicazione deve eseguire più operazioni di I/O asincrone su un singolo file, deve attendere l'handle di evento nella struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) specifica per ogni operazione di i/o, anziché nell'handle di file comune.

Per annullare tutte le operazioni di I/O asincrone in sospeso, usare:

-   [**CancelIo**](cancelio.md): questa funzione Annulla solo le operazioni rilasciate dal thread chiamante per l'handle di file specificato.
-   [**CancelIoEx**](cancelioex-func.md): questa funzione Annulla tutte le operazioni rilasciate dai thread per l'handle di file specificato.

Usare [**CancelSynchronousIo**](cancelsynchronousio-func.md) per annullare le operazioni di I/O sincrone in sospeso.

Le funzioni [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) consentono a un'applicazione di specificare una routine da eseguire (vedere [**FileIOCompletionRoutine**](/windows/win32/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine)) quando viene completata la richiesta di i/O asincrona.

 

 
