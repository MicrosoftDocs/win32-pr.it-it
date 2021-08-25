---
description: Le funzioni globali e locali sono supportate per il porting da codice a 16 bit o per la gestione della compatibilità del codice sorgente con le versioni a 16 bit Windows.
ms.assetid: 97707ce7-4c65-4d0e-ba69-47fdaee73a9b
title: Funzioni globali e locali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d7832f90a420e6be87fe6599cc8c9e4722ddf45b789663ed9b39eab4e5449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869696"
---
# <a name="global-and-local-functions"></a>Funzioni globali e locali

Le funzioni globali e locali sono supportate per il porting da codice a 16 bit o per la gestione della compatibilità del codice sorgente con le versioni a 16 bit Windows. A partire da Windows a 32 bit, le funzioni globali e locali vengono implementate come funzioni wrapper che chiamano le funzioni [heap](heap-functions.md) corrispondenti usando un handle per l'heap predefinito del processo. Pertanto, le funzioni globali e locali hanno un sovraccarico maggiore rispetto ad altre funzioni di gestione della memoria.

Le [funzioni heap](heap-functions.md) forniscono più funzionalità e controllo rispetto alle funzioni globali e locali. Le nuove applicazioni devono usare le funzioni heap, a meno che la documentazione non dica in modo specifico che deve essere usata una funzione globale o locale. Ad esempio, alcune Windows allocano memoria che deve essere liberata con [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree)e le funzioni globali vengono ancora usate con Dynamic Data Exchange (DDE), le funzioni degli Appunti e gli oggetti dati OLE. Per un elenco completo delle funzioni globali e locali, vedere la tabella in [Funzioni di gestione della memoria](memory-management-functions.md).

Windows gestione della memoria non fornisce un heap locale e un heap globale separati, come Windows a 16 bit. Di conseguenza, le famiglie di funzioni globali e locali sono equivalenti e la scelta tra di esse è una questione di preferenza personale. Si noti che la modifica da un modello di memoria segmentata a 16 bit a un modello di memoria virtuale a 32 bit ha reso inutili o senza significato alcune delle funzioni globali e locali correlate e delle relative opzioni. Ad esempio, non sono più presenti puntatori vicini e lontani, perché le allocazioni locali e globali restituiscono indirizzi virtuali a 32 bit.

Gli oggetti di memoria allocati [**da GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) sono in pagine private di cui è stato eseguito il commit con accesso in lettura/scrittura a cui non è possibile accedere da altri processi. La memoria allocata usando **GlobalAlloc** con **GMEM \_ DDESHARE** non viene effettivamente condivisa a livello globale, come nel caso di applicazioni a 16 bit Windows. Questo valore non ha alcun effetto ed è disponibile solo per la compatibilità. Le applicazioni che richiedono memoria condivisa per altri scopi devono usare oggetti di mapping dei file. Più processi possono eseguire il mapping di una vista dello stesso oggetto di mapping dei file per fornire la memoria condivisa denominata. Per altre informazioni, vedere [Mapping dei file](file-mapping.md).

Le allocazioni di memoria sono limitate solo dalla memoria fisica disponibile, inclusa l'archiviazione nel file di paging su disco. Quando si alloca memoria fissa, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) restituiscono un puntatore che il processo chiamante può usare immediatamente per accedere alla memoria. Quando si alloca memoria spostabile, il valore restituito è un handle. Per ottenere un puntatore a un oggetto di memoria mobile, usare le [**funzioni GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock) [**e LocalLock.**](/windows/desktop/api/WinBase/nf-winbase-locallock)

Le dimensioni effettive della memoria allocata possono essere maggiori delle dimensioni richieste. Per determinare il numero effettivo di byte allocati, usare la [**funzione GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize) [**o LocalSize.**](/windows/desktop/api/WinBase/nf-winbase-localsize) Se l'importo allocato è superiore a quello richiesto, il processo può usare l'intero importo.

Le [**funzioni GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc) [**e LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) modificano le dimensioni o gli attributi di un oggetto di memoria allocato da [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) [**e LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc). Le dimensioni possono aumentare o diminuire.

Le [**funzioni GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree) [**e LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) rilasciano la memoria allocata da [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc)o [**LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc). Per eliminare l'oggetto memoria specificato senza invalidare l'handle, usare la [**funzione GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) [**o LocalDiscard.**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) L'handle può essere usato in un secondo momento da **GlobalReAlloc** o **LocalReAlloc** per allocare un nuovo blocco di memoria associato allo stesso handle.

Per restituire informazioni su un oggetto di memoria specificato, usare la [**funzione GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags) [**o LocalFlags.**](/windows/desktop/api/WinBase/nf-winbase-localflags) Le informazioni includono il numero di blocchi dell'oggetto e indicano se l'oggetto è eliminabile o è già stato eliminato. Per restituire un handle all'oggetto di memoria associato a un puntatore specificato, usare la [**funzione GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle) [**o LocalHandle.**](/windows/desktop/api/WinBase/nf-winbase-localhandle)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Confronto dei metodi di allocazione di memoria](comparing-memory-allocation-methods.md)
</dt> </dl>

 

 
