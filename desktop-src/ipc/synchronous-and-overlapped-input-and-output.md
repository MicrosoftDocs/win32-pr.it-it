---
description: I/o della pipe sincrona e I/O della pipe asincrona. Le funzioni ReadFile, WriteFile, TransactNamedPipe e ConnectNamedPipe possono eseguire operazioni di input e output su una pipe in modo sincrono o asincrono.
ms.assetid: 5ab9bb7f-1f99-4041-bba8-2863f34dbcaf
title: I/O della pipe sincrona e sovrapposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3becfb19dfe5fa49d4121246a576fb3200226b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318430"
---
# <a name="synchronous-and-overlapped-pipe-io"></a>I/O della pipe sincrona e sovrapposta

Le funzioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) possono eseguire operazioni di input e output su una pipe in modo sincrono o asincrono. Quando una funzione viene eseguita in modo sincrono, non viene restituita finché non viene completata l'operazione che sta eseguendo. Ciò significa che l'esecuzione del thread chiamante può essere bloccata per un periodo indefinito mentre è in attesa del completamento di un'operazione che richiede molto tempo. Quando una funzione viene eseguita in modo asincrono, viene restituito immediatamente, anche se l'operazione non è stata completata. In questo modo è possibile eseguire un'operazione che richiede molto tempo in background, mentre il thread chiamante è libero di eseguire altre attività.

L'utilizzo di operazioni di I/O asincrone consente a un server pipe di utilizzare un ciclo che esegue i passaggi seguenti:

1.  Specificare più oggetti evento in una chiamata alla funzione Wait e attendere che uno degli oggetti sia impostato sullo stato segnalato.
2.  Usare il valore restituito della funzione wait per determinare quale operazione sovrapposta è stata completata.
3.  Eseguire le attività necessarie per pulire l'operazione completata e avviare l'operazione successiva per tale handle della pipe. Questo può implicare l'avvio di un'altra operazione sovrapposta per lo stesso handle di pipe.

Le operazioni sovrapposte consentono a una pipe di leggere e scrivere dati contemporaneamente e per un singolo thread di eseguire operazioni di I/O simultanee su più handle di pipe. In questo modo un server pipe a thread singolo è in grado di gestire le comunicazioni con più client pipe in modo efficiente. Per un esempio, vedere [named pipe server con I/O sovrapposti](named-pipe-server-using-overlapped-i-o.md).

Per consentire a un server pipe di utilizzare operazioni sincrone per comunicare con più di un client, è necessario creare un thread distinto per ogni client pipe in modo da poter eseguire uno o più thread mentre altri thread sono in attesa. Per un esempio di server pipe multithreading che usa operazioni sincrone, vedere [server pipe multithreading](multithreaded-pipe-server.md).

## <a name="enabling-asynchronous-operation"></a>Abilitazione dell'operazione asincrona

Le funzioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) possono essere eseguite in modo asincrono solo se si Abilita la modalità sovrapposta per l'handle della pipe specificato e si specifica un puntatore valido a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . Se il puntatore **sovrapposto** è **null**, il valore restituito dalla funzione può indicare erroneamente che l'operazione è stata completata. Pertanto, è consigliabile che se si crea un handle con il flag di \_ file \_ sovrapposto e si desidera un comportamento asincrono, è sempre necessario specificare una struttura **sovrapposta** valida.

Il membro **hEvent** della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) specificata deve contenere un handle per un oggetto evento di reimpostazione manuale. Si tratta di un oggetto di sincronizzazione creato dalla funzione [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) . Il thread che avvia l'operazione sovrapposta usa l'oggetto evento per determinare il momento in cui l'operazione è stata completata. Non è consigliabile usare l'handle di pipe per la sincronizzazione quando si eseguono operazioni simultanee sullo stesso handle perché non esiste alcun modo per sapere quale completamento dell'operazione ha causato la segnalazione dell'handle della pipe. L'unica tecnica affidabile per l'esecuzione di operazioni simultanee sullo stesso handle di pipe consiste nell'usare una struttura **sovrapposta** separata con il proprio oggetto evento per ogni operazione. Per ulteriori informazioni sugli oggetti evento, vedere [sincronizzazione](/windows/desktop/Sync/synchronization).

Inoltre, è possibile ricevere una notifica quando un'operazione sovrapposta viene completata usando le funzioni [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) o [**GetQueuedCompletionStatusEx**](/windows/desktop/FileIO/getqueuedcompletionstatusex-func) . In questo caso, non è necessario assegnare l'evento di reimpostazione manuale nella struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e il completamento viene eseguito sull'handle della pipe nello stesso modo di un'operazione di lettura o scrittura asincrona. Per ulteriori informazioni, vedere [porte di completamento I/O](/windows/desktop/FileIO/i-o-completion-ports).

Quando le operazioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) vengono eseguite in modo asincrono, si verifica una delle condizioni seguenti:

-   Se l'operazione viene completata quando la funzione restituisce, il valore restituito indica l'esito positivo o negativo dell'operazione. Se si verifica un errore, il valore restituito è zero e la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un valore diverso da Error \_ io \_ Pending.
-   Se l'operazione non è terminata quando la funzione restituisce, il valore restituito è zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l'errore \_ io \_ in sospeso. In questo caso, il thread chiamante deve attendere il completamento dell'operazione. Il thread chiamante deve quindi chiamare la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare i risultati.

## <a name="using-completion-routines"></a>Uso delle routine di completamento

Le funzioni [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) forniscono un'altra forma di i/O sovrapposti. Diversamente dalle funzioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) sovrapposte, che usano un oggetto evento per segnalare il completamento, le funzioni estese specificano una *routine di completamento*. Una routine di completamento è una funzione accodata per l'esecuzione al termine dell'operazione di lettura o scrittura. La routine di completamento non viene eseguita fino a quando il thread che ha chiamato **ReadFileEx** e **WriteFileEx** avvia un' *operazione di attesa segnalabile* chiamando una delle [funzioni di attesa alertable](/windows/desktop/Sync/wait-functions) con il parametro *fAlertable* impostato su **true**. In un'operazione di attesa di avviso, le funzioni restituiscono anche quando una routine di completamento **ReadFileEx** o **WriteFileEx** viene accodata per l'esecuzione. Un server pipe può utilizzare le funzioni estese per eseguire una sequenza di operazioni di lettura e scrittura per ogni client che si connette a tale server. Ogni operazione di lettura o scrittura nella sequenza specifica una routine di completamento e ogni routine di completamento avvia il passaggio successivo della sequenza. Per un esempio, vedere [named pipe server usando le routine di completamento](named-pipe-server-using-completion-routines.md).

 

 
