---
description: È possibile eseguire operazioni di I/O sincrone o asincrone (denominate anche sovrapposte) su file, named pipe e dispositivi di comunicazione seriale.
ms.assetid: db44990e-5a0f-4153-8ff6-79dd7cda48af
title: Sincronizzazione e input e output sovrapposti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e462e4c2cffa3f1c9dee9bc33a7c75b910ce8139dbdfab9c190b4691c4b6bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975911"
---
# <a name="synchronization-and-overlapped-input-and-output"></a>Sincronizzazione e input e output sovrapposti

È possibile eseguire operazioni di I/O sincrone o asincrone (denominate anche sovrapposte) su file, named pipe e dispositivi di comunicazione seriale. Le [**funzioni WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol), [**WaitCommEvent**](/windows/win32/api/winbase/nf-winbase-waitcommevent), [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)e [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) possono essere eseguite in modo sincrono o asincrono. Le [**funzioni ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex) [**e WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) possono essere eseguite solo in modo asincrono.

Quando una funzione viene eseguita in modo sincrono, non viene restituita fino al completamento dell'operazione. Ciò significa che l'esecuzione del thread chiamante può essere bloccata per un periodo indefinito mentre è in attesa del completamento di un'operazione dispendiosa in termini di tempo. Le funzioni chiamate per l'operazione sovrapposta possono restituire immediatamente un valore, anche se l'operazione non è stata completata. Ciò consente l'esecuzione in background di un'operazione di I/O dispendiosa in termini di tempo mentre il thread chiamante è libero di eseguire altre attività. Ad esempio, un singolo thread può eseguire operazioni di I/O simultanee su handle diversi o anche operazioni simultanee di lettura e scrittura sullo stesso handle.

Per sincronizzare l'esecuzione con il completamento dell'operazione sovrapposta, il thread chiamante usa la funzione [**GetOverlappedResult,**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) [**getOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) o una delle funzioni di attesa per determinare quando l'operazione sovrapposta è stata completata. [](wait-functions.md) È anche possibile usare la macro [**HasOverlappedIoCompleted**](/windows/desktop/api/WinBase/nf-winbase-hasoverlappediocompleted) per eseguire il polling del completamento.

Per annullare tutte le operazioni di I/O asincrone in sospeso, usare la funzione [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) e fornire una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) che specifica la richiesta di annullamento. Usare la [**funzione CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio) per annullare le operazioni di I/O asincrone in sospeso eseguite dal thread chiamante per l'handle di file specificato.

Le operazioni sovrapposte richiedono un file, named pipe o un dispositivo di comunicazione creato con il flag **FILE \_ FLAG \_ OVERLAPPED.** Quando un thread chiama una funzione ,ad esempio la funzione [**ReadFile,**](/windows/win32/api/fileapi/nf-fileapi-readfile) per eseguire un'operazione sovrapposta, il thread chiamante deve specificare un puntatore a una [**struttura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Se questo puntatore è **NULL,** il valore restituito dalla funzione potrebbe indicare erroneamente che l'operazione è stata completata. Tutti i membri della struttura **OVERLAPPED** devono essere inizializzati su zero, a meno che non venga usato un evento per segnalare il completamento di un'operazione di I/O. Se si usa un evento, il **membro hEvent** della struttura **OVERLAPPED** specifica un handle per l'oggetto evento allocato. Il sistema imposta lo stato dell'oggetto evento su non associato quando una chiamata alla funzione di I/O viene restituita prima del completamento dell'operazione. Il sistema imposta lo stato dell'oggetto evento su segnalato quando l'operazione è stata completata. Un evento è necessario solo se sarà presente più di un'operazione di I/O in attesa contemporaneamente. Se non viene usato un evento, ogni operazione di I/O completata segnalerà il file, il named pipe o il dispositivo di comunicazione.

Quando viene chiamata una funzione per eseguire un'operazione sovrapposta, l'operazione potrebbe essere completata prima che la funzione venga restituita. In questo caso, i risultati vengono gestiti come se l'operazione fosse stata eseguita in modo sincrono. Se l'operazione non è stata completata, tuttavia, il valore restituito della funzione è **FALSE** e la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR IO \_ \_ PENDING.**

Un thread può gestire le operazioni sovrapposte con uno dei due metodi seguenti:

-   Usare la [**funzione GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) per attendere il completamento dell'operazione sovrapposta. Se **si usa GetOverlappedResultEx,** il thread chiamante può specificare un timeout per l'operazione sovrapposta o eseguire un'attesa avvisabile.
-   Specificare un handle per l'oggetto evento di reimpostazione [](wait-functions.md) manuale della struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) in una delle funzioni di attesa e quindi, dopo il completamento della funzione di attesa, chiamare [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetOverlappedResultEx.**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) La funzione restituisce i risultati dell'operazione sovrapposta completata e, per le funzioni in cui tali informazioni sono appropriate, segnala il numero effettivo di byte trasferiti.

Quando si eseguono più operazioni sovrapposte simultanee in un singolo thread, il thread chiamante deve specificare una [**struttura OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) per ogni operazione. Ogni **struttura OVERLAPPED** deve specificare un handle per un oggetto evento di reimpostazione manuale diverso. Per attendere il completamento di una delle operazioni sovrapposte, il thread specifica tutti gli handle di evento di reimpostazione manuale come criteri di attesa in una delle funzioni di attesa a [più oggetti](wait-functions.md). Il valore restituito della funzione di attesa a più oggetti indica quale oggetto evento di reimpostazione manuale è stato segnalato, in modo che il thread possa determinare quale operazione sovrapposta ha causato il completamento dell'operazione di attesa.

È più sicuro usare un oggetto evento separato per ogni operazione sovrapposta, anziché non specificare alcun oggetto evento o riutilizzare lo stesso oggetto evento per più operazioni. Se nella struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) non è specificato alcun oggetto evento, il sistema segnala lo stato del file, del named pipe o del dispositivo di comunicazione quando l'operazione sovrapposta è stata completata. Pertanto, è possibile specificare questi handle come oggetti di sincronizzazione in una funzione di attesa, anche se il loro uso a questo scopo può essere difficile da gestire perché, quando si eseguono simultaneamente operazioni sovrapposte sullo stesso file, named pipe o dispositivo di comunicazione, non è possibile sapere quale operazione ha causato la segnalazione dello stato dell'oggetto.

Un thread non deve riutilizzare un evento presupponendo che l'evento verrà segnalato solo dall'operazione sovrapposta di tale thread. Un evento viene segnalato sullo stesso thread dell'operazione sovrapposta che viene completata. L'uso dello stesso evento su più thread può causare un race condition in cui l'evento viene segnalato correttamente per il thread la cui operazione viene completata per prima e prematuramente per gli altri thread che usano tale evento. Quindi, al termine dell'operazione sovrapposta successiva, l'evento viene segnalato nuovamente per tutti i thread che usano tale evento e così via fino al completamento di tutte le operazioni sovrapposte.

Per esempi che illustrano l'uso di operazioni sovrapposte, routine di completamento e [**la funzione GetOverlappedResult,**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) vedere [Uso di pipe.](../ipc/using-pipes.md)

**Windows Vista, Windows Server 2003 e Windows XP: **

Prestare attenzione quando si riutilizzano [**le strutture OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Se le strutture **OVERLAPPED** vengono riutilizzate in più thread e [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) viene chiamato con il parametro *bWait* impostato su **TRUE,** il thread chiamante deve assicurarsi che l'evento associato venga segnalato prima di riutilizzare la struttura. Questa operazione può essere eseguita usando la funzione [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) dopo aver chiamato **GetOverlappedResult** per forzare il thread ad attendere il completamento dell'operazione. Si noti che l'oggetto evento deve essere un oggetto evento di reimpostazione manuale. Se viene usato un oggetto evento impostato automaticamente, la chiamata a **GetOverlappedResult** con il parametro *bWait* impostato su **TRUE** causa il blocco indefinito della funzione. Questo comportamento è cambiato a partire da Windows 7 e Windows Server 2008 R2 per le applicazioni che specificano Windows 7 come sistema operativo supportato nel manifesto dell'applicazione. Per altre informazioni, vedere [Manifesti dell'applicazione.](/previous-versions/windows/desktop/adrms_sdk/application-manifests)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di I/O](../fileio/i-o-concepts.md)
</dt> </dl>

 

 
