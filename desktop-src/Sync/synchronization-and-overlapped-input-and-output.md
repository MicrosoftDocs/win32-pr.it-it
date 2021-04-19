---
description: È possibile eseguire operazioni di I/O sincrone o asincrone, denominate anche sovrapposte, su file, named pipe e dispositivi di comunicazione seriale.
ms.assetid: db44990e-5a0f-4153-8ff6-79dd7cda48af
title: Sincronizzazione e input e output sovrapposti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e263bb39badc7cbfadd67d80eb169dc1fe6d6c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317662"
---
# <a name="synchronization-and-overlapped-input-and-output"></a>Sincronizzazione e input e output sovrapposti

È possibile eseguire operazioni di I/O sincrone o asincrone, denominate anche sovrapposte, su file, named pipe e dispositivi di comunicazione seriale. Le funzioni [**WriteFile**](/windows/win32/api/fileapi/nf-fileapi-writefile), [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile), [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol), [**WaitCommEvent**](/windows/win32/api/winbase/nf-winbase-waitcommevent), [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)e [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) possono essere eseguite in modo sincrono o asincrono. Le funzioni [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) possono essere eseguite solo in modo asincrono.

Quando una funzione viene eseguita in modo sincrono, non viene restituita fino al completamento dell'operazione. Ciò significa che l'esecuzione del thread chiamante può essere bloccata per un periodo indefinito mentre attende il completamento di un'operazione che richiede molto tempo. Le funzioni chiamate per l'operazione sovrapposta possono restituire immediatamente un risultato, anche se l'operazione non è stata completata. Ciò consente l'esecuzione in background di un'operazione di I/O che richiede molto tempo, mentre il thread chiamante è libero di eseguire altre attività. Ad esempio, un singolo thread può eseguire operazioni di I/O simultanee su handle diversi o anche operazioni simultanee di lettura e scrittura sullo stesso handle.

Per sincronizzare l'esecuzione con il completamento dell'operazione sovrapposta, il thread chiamante utilizza la funzione [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) , la funzione [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) o una delle [funzioni Wait](wait-functions.md) per determinare quando l'operazione sovrapposta è stata completata. È anche possibile usare la macro [**HasOverlappedIoCompleted**](/windows/desktop/api/WinBase/nf-winbase-hasoverlappediocompleted) per eseguire il polling per il completamento.

Per annullare tutte le operazioni di I/O asincrone in sospeso, utilizzare la funzione [**CancelIoEx**](/windows/win32/api/ioapiset/nf-ioapiset-cancelioex) e fornire una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) che specifichi la richiesta da annullare. Utilizzare la funzione [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio) per annullare le operazioni di i/O asincrone in sospeso emesse dal thread chiamante per l'handle di file specificato.

Per le operazioni sovrapposte è necessario un file, un named pipe o un dispositivo di comunicazione creato con il flag **file \_ \_ sovrapposto** . Quando un thread chiama una funzione, ad esempio la funzione [**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) , per eseguire un'operazione sovrapposta, il thread chiamante deve specificare un puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . Se questo puntatore è **null**, il valore restituito dalla funzione potrebbe indicare erroneamente che l'operazione è stata completata. Tutti i membri della struttura **sovrapposta** devono essere inizializzati su zero, a meno che non venga utilizzato un evento per segnalare il completamento di un'operazione di I/O. Se viene utilizzato un evento, il membro **hEvent** della struttura **sovrapposta** specifica un handle per l'oggetto evento allocato. Il sistema imposta lo stato dell'oggetto evento su non segnalato quando una chiamata alla funzione I/O viene restituita prima del completamento dell'operazione. Il sistema imposta lo stato dell'oggetto evento su segnalato quando l'operazione è stata completata. Un evento è necessario solo se è presente più di un'operazione di I/O in attesa nello stesso momento. Se non viene utilizzato un evento, ogni operazione di I/O completata segnalerà il file, named pipe o il dispositivo di comunicazione.

Quando una funzione viene chiamata per eseguire un'operazione sovrapposta, è possibile che l'operazione venga completata prima che la funzione restituisca. In tal caso, i risultati vengono gestiti come se l'operazione fosse stata eseguita in modo sincrono. Se l'operazione non è stata completata, tuttavia, il valore restituito della funzione è **false** e la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **errore \_ io \_ in sospeso**.

Un thread può gestire le operazioni sovrapposte mediante uno dei due metodi seguenti:

-   Utilizzare la funzione [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex) per attendere il completamento dell'operazione sovrapposta. Se si usa **GetOverlappedResultEx** , il thread chiamante può specificare un timeout per l'operazione sovrapposta o eseguire un'attesa di avviso.
-   Specificare un handle per l'oggetto evento di reimpostazione manuale della struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) in una delle [funzioni di attesa](wait-functions.md) e quindi, dopo la restituzione della funzione Wait, chiamare [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) o [**GetOverlappedResultEx**](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex). La funzione restituisce i risultati dell'operazione sovrapposta completata e per le funzioni in cui tali informazioni sono appropriate, indica il numero effettivo di byte trasferiti.

Quando si eseguono più operazioni sovrapposte simultanee in un singolo thread, il thread chiamante deve specificare una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) per ogni operazione. Ogni struttura **sovrapposta** deve specificare un handle per un diverso oggetto evento di reimpostazione manuale. Per attendere il completamento di una qualsiasi delle operazioni sovrapposte, il thread specifica tutti gli handle di eventi di reimpostazione manuale come criteri di attesa in una delle funzioni di [attesa](wait-functions.md)di più oggetti. Il valore restituito della funzione di attesa di più oggetti indica quale oggetto evento di reimpostazione manuale è stato segnalato, in modo che il thread possa determinare quale operazione sovrapposta ha causato il completamento dell'operazione di attesa.

È più sicuro usare un oggetto evento separato per ogni operazione sovrapposta, anziché specificare alcun oggetto evento o riutilizzare lo stesso oggetto evento per più operazioni. Se nella struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) non è specificato alcun oggetto evento, il sistema segnala lo stato del file, named pipe o dispositivo di comunicazione quando l'operazione di sovrapposizione è stata completata. Pertanto, è possibile specificare questi handle come oggetti di sincronizzazione in una funzione Wait, sebbene il loro utilizzo a questo scopo possa essere difficile da gestire perché, quando si eseguono operazioni sovrapposte simultanee nello stesso file, named pipe o dispositivo di comunicazione, non esiste alcun modo per stabilire quale operazione ha causato la segnalazione dello stato dell'oggetto.

Un thread non deve riutilizzare un evento presumendo che l'evento venga segnalato solo dall'operazione sovrapposta del thread. Un evento viene segnalato nello stesso thread dell'operazione sovrapposta che viene completata. L'uso dello stesso evento su più thread può causare un race condition in cui l'evento viene segnalato correttamente per il thread la cui operazione viene completata prima e prematuramente per gli altri thread che usano tale evento. Quindi, al termine della successiva operazione sovrapposta, l'evento viene segnalato di nuovo per tutti i thread che usano tale evento e così via fino al completamento di tutte le operazioni sovrapposte.

Per esempi che illustrano l'uso delle operazioni sovrapposte, le routine di completamento e la funzione [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) , vedere [using Pipes](../ipc/using-pipes.md).

* * Windows Vista, Windows Server 2003 e Windows XP: * *

Prestare attenzione quando si riutilizzano le strutture [**sovrapposte**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . Se le strutture **sovrapposte** vengono riutilizzate in più thread e [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) viene chiamato con il parametro *bWait* impostato su **true**, il thread chiamante deve garantire che l'evento associato venga segnalato prima di riutilizzare la struttura. Questa operazione può essere eseguita tramite la funzione [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) dopo aver chiamato **GetOverlappedResult** per forzare il thread ad attendere il completamento dell'operazione. Si noti che l'oggetto evento deve essere un oggetto evento di reimpostazione manuale. Se viene usato un oggetto evento di autoreset, la chiamata di **GetOverlappedResult** con il parametro *BWait* impostato su **true** comporta il blocco della funzione a tempo indefinito. Questo comportamento è stato modificato a partire da Windows 7 e Windows Server 2008 R2 per le applicazioni che specificano Windows 7 come sistema operativo supportato nel manifesto dell'applicazione. Per altre informazioni, vedere [manifesti dell'applicazione](/previous-versions/windows/desktop/adrms_sdk/application-manifests).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di I/O](../fileio/i-o-concepts.md)
</dt> </dl>

 

 
