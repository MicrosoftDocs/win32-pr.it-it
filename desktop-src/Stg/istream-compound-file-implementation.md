---
title: IStream - Implementazione di file composti
description: L'interfaccia IStream supporta la lettura e la scrittura di dati in oggetti flusso. In un oggetto di archiviazione strutturata gli oggetti flusso contengono i dati e le risorse di archiviazione forniscono la struttura.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd Stg , implementazione di file composti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57a974e44e66d8709a002f9635c41f751e80ab1d3f3875f8eb129cef2b14847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961209"
---
# <a name="istream---compound-file-implementation"></a>IStream - Implementazione di file composti

[**L'interfaccia IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supporta la lettura e la scrittura di dati in oggetti flusso. In un oggetto di archiviazione strutturata gli oggetti flusso contengono i dati e le risorse di archiviazione forniscono la struttura. I dati semplici possono essere scritti direttamente in un flusso, ma più spesso i flussi sono elementi annidati all'interno di un oggetto di archiviazione. Sono simili ai file standard.

La specifica di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) definisce più funzionalità di quelle supportate dall'implementazione COM. Ad esempio, **l'interfaccia IStream** definisce flussi di lunghezza massima di 2⁶⁴ byte che richiedono un puntatore di ricerca a 64 bit. Tuttavia, l'implementazione COM supporta solo flussi di lunghezza massima di 2 mb (4 GB) e le operazioni di lettura e scrittura sono sempre limitate a 2 mb alla volta. L'implementazione COM inoltre non supporta la transazione di flusso o il blocco dell'area.

Per creare un flusso semplice basato sulla memoria globale, ottenere un [**puntatore IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) chiamando la funzione API [**CreateStreamOnHGlobal.**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal) Per ottenere un **puntatore IStream** all'interno di un oggetto file composto, chiamare [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) [**o StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Queste funzioni recuperano un [**puntatore IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) con cui è quindi possibile chiamare [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) [**o OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) per un **puntatore IStream.** In entrambi i casi, viene usato lo stesso codice di implementazione **di IStream.**

> [!Note]  
> L'implementazione di file composti dell'archiviazione strutturata non riesce in un metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per [**ISequentialStream,**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream)ma include i metodi [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) e [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) tramite il puntatore di [**interfaccia IStream.**](/windows/desktop/api/Objidl/nn-objidl-istream)

 

## <a name="when-to-use"></a>Utilizzo

Chiamare i metodi di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per leggere e scrivere dati in un flusso.

Poiché è possibile effettuare il marshalling degli oggetti flusso in altri processi, le applicazioni possono condividere i dati negli oggetti di archiviazione senza dover usare la memoria globale. Nell'implementazione di file composti COM di oggetti flusso, le funzionalità di marshalling personalizzate in COM creano una versione remota dell'oggetto originale nel nuovo processo quando i due processi hanno accesso in memoria condivisa. Non è quindi necessario che la versione remota comunichi con il processo originale per eseguire le funzioni.

La versione remota dell'oggetto flusso condivide lo stesso puntatore di ricerca del flusso originale. Se non si vuole condividere il puntatore di ricerca, usare il metodo [**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) per fornire una copia dell'oggetto flusso per il processo remoto.

> [!Note]
> Se si crea un oggetto flusso di dimensioni maggiori dell'heap nella memoria del computer e si usa un handle **HGLOBAL** per un oggetto di memoria globale, l'oggetto flusso chiama internamente il metodo [**GlobalRealloc.**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) Poiché **GlobalRealloc** copia sempre i dati dall'origine alla destinazione, l'aumento di un oggetto flusso da 20 MB a 25 MB, ad esempio, richiede una notevole quantità di tempo. Ciò è dovuto alle dimensioni degli incrementi copiati e peggiora se nel computer è presente meno di 45 MB di memoria a causa dello scambio del disco.
>
> La soluzione preferita consiste nell'implementare [**un metodo IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) che usa la memoria allocata da [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) invece di [**GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) In questo modo è possibile riservare un grande blocco di spazio degli indirizzi virtuali e quindi eseguire il commit della memoria all'interno di tale spazio indirizzi in base alle esigenze. Non viene eseguita alcuna copia dei dati e viene eseguito il commit della memoria solo come richiesto.
>
> Un'alternativa [**a GlobalRealloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) consiste nel chiamare il metodo [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) sull'oggetto flusso per aumentare in anticipo l'allocazione di memoria. Questa operazione, tuttavia, non è efficiente quanto [**l'uso di VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), come descritto in precedenza.

 

## <a name="methods"></a>Metodi

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Legge un numero specificato di byte dall'oggetto flusso in memoria a partire dal puntatore di posizionamento corrente. Questa implementazione restituisce S \_ OK se è stata raggiunta la fine del flusso durante la lettura. Si tratta dello stesso comportamento della "fine del file" presente nella cartella FAT di MS-DOS file system.

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Scrive un numero specificato da byte nell'oggetto flusso a partire dal puntatore di ricerca corrente. In questa implementazione gli oggetti flusso non sono di tipo sparse. Tutti i byte di riempimento vengono infine allocati sul disco e assegnati al flusso.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream::Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Sposta il puntatore di posizionamento su un nuovo percorso relativo all'inizio del flusso, alla fine del flusso o al puntatore di posizionamento corrente.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Modifica la dimensione dell'oggetto flusso. In questa implementazione non è garantito che lo spazio allocato sarà contiguo.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Copia un numero specificato di byte dal puntatore di posizionamento corrente nel flusso al puntatore di posizionamento corrente in un altro flusso.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream::Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

L'implementazione di file composti [**di IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supporta l'apertura di flussi solo in modalità diretta, non in modalità transazione. Pertanto, il metodo non ha alcun effetto quando viene chiamato se non per scaricare tutti i buffer di memoria al livello di archiviazione successivo.

In questa implementazione non è importante se si esegue il commit delle modifiche ai flussi, ma è necessario eseguire il commit solo delle modifiche per gli oggetti di archiviazione.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream::Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Questa implementazione non supporta i flussi transazionati, quindi una chiamata a questo metodo non ha alcun effetto.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Il blocco di intervallo non è supportato da questa implementazione, quindi una chiamata a questo metodo non ha alcun effetto.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream::UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Rimuove la restrizione di accesso per un intervallo di byte precedentemente limitato con [**IStream::LockRegion.**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Recupera la [**struttura STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) per questo flusso

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream::Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Crea un nuovo oggetto flusso con il proprio puntatore di posizionamento che fa riferimento agli stessi byte del flusso originale.

</dd> </dl>

Un [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) in modalità semplice è soggetto ai vincoli seguenti.

-   Un flusso è una modalità semplice se è stato creato o aperto da un archivio in modalità semplice. Una modalità di archiviazione è semplice se viene creata o aperta con il flag STGM \_ SIMPLE impostato nel parametro *grfMode.*
-   I [**metodi Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) e [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) non sono supportati.
-   Il [**metodo Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) è supportato, ma è necessario specificare il valore STATFLAG \_ NONAME.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 