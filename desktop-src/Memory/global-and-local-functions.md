---
description: Le funzioni globali e locali sono supportate per il porting dal codice a 16 bit o per la gestione della compatibilità del codice sorgente con Windows a 16 bit.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Funzioni globali e locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf356647f92f0e7d82e914a91020c438363ff082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879069"
---
# <a name="global-and-local-functions"></a>Funzioni globali e locali

Le funzioni globali e locali sono supportate per il porting dal codice a 16 bit o per la gestione della compatibilità del codice sorgente con Windows a 16 bit. A partire da Windows a 32 bit, le funzioni globali e locali vengono implementate come funzioni wrapper che chiamano le [funzioni heap](heap-functions.md) corrispondenti usando un handle per l'heap predefinito del processo. Pertanto, le funzioni globali e locali hanno un sovraccarico maggiore rispetto ad altre funzioni di gestione della memoria.

Le [funzioni heap](heap-functions.md) forniscono maggiori funzionalità e controllo rispetto alle funzioni globali e locali. Le nuove applicazioni devono usare le funzioni di heap, a meno che la documentazione non riferisca specificamente la funzione globale o locale da usare. Alcune funzioni di Windows, ad esempio, allocano memoria che deve essere liberata con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree)e le funzioni globali vengono ancora utilizzate con Dynamic Data Exchange (DDE), le funzioni degli Appunti e gli oggetti dati OLE. Per un elenco completo delle funzioni globali e locali, vedere la tabella in [funzioni di gestione della memoria](memory-management-functions.md).

Gestione memoria Windows non fornisce un heap locale e un heap globale distinti, come avviene in Windows a 16 bit. Di conseguenza, le famiglie globali e locali di funzioni sono equivalenti e la scelta tra di esse è una questione di preferenza personale. Si noti che la modifica da un modello di memoria segmentata a 16 bit a un modello di memoria virtuale a 32 bit ha fatto in modo che alcune delle funzioni globali e locali correlate e le relative opzioni non siano necessarie o non significative. Ad esempio, non ci sono più puntatori quasi e lontani, perché le allocazioni locali e globali restituiscono indirizzi virtuali a 32 bit.

Gli oggetti memoria allocati da [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) si trovano in pagine private di cui è stato eseguito il commit con accesso in lettura/scrittura a cui non è possibile accedere da altri processi. La memoria allocata usando **GlobalAlloc** con **GMEM \_ DDESHARE** non è effettivamente condivisa globalmente come in Windows a 16 bit. Questo valore non ha alcun effetto ed è disponibile solo per la compatibilità. Le applicazioni che richiedono memoria condivisa per altri scopi devono usare oggetti di mapping di file. Più processi possono eseguire il mapping di una visualizzazione dello stesso oggetto mapping di file per fornire la memoria condivisa denominata. Per ulteriori informazioni, vedere [mapping di file](file-mapping.md).

Le allocazioni di memoria sono limitate solo dalla memoria fisica disponibile, inclusa l'archiviazione nel file di paging su disco. Quando si alloca memoria fissa, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) restituiscono un puntatore che il processo chiamante può utilizzare immediatamente per accedere alla memoria. Quando si alloca memoria mobile, il valore restituito è un handle. Per ottenere un puntatore a un oggetto di memoria mobile, usare le funzioni [**funzione GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) e [**LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) .

Le dimensioni effettive della memoria allocata possono essere maggiori delle dimensioni richieste. Per determinare il numero effettivo di byte allocati, usare la funzione [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) o [**LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) . Se la quantità allocata è maggiore della quantità richiesta, il processo può utilizzare l'intero importo.

Le funzioni [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) e [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) modificano le dimensioni o gli attributi di un oggetto Memory allocato da [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc). È possibile aumentare o diminuire le dimensioni.

Le funzioni [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) e [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) rilasciano memoria allocata da [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)o [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc). Per rimuovere l'oggetto di memoria specificato senza invalidare l'handle, utilizzare la funzione [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) o [**LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) . L'handle può essere usato in un secondo momento da **GlobalReAlloc** o **LocalReAlloc** per allocare un nuovo blocco di memoria associato allo stesso handle.

Per restituire informazioni su un oggetto di memoria specificato, utilizzare la funzione [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) o [**LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) . Le informazioni includono il conteggio dei blocchi dell'oggetto e indica se l'oggetto è rimossa o se è già stato rimosso. Per restituire un handle all'oggetto Memory associato a un puntatore specificato, utilizzare la funzione [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) o [**LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Confronto tra i metodi di allocazione della memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
