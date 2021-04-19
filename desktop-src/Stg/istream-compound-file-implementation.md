---
title: Implementazione del file composto IStream
description: L'interfaccia IStream supporta la lettura e la scrittura di dati negli oggetti flusso. In un oggetto di archiviazione strutturato gli oggetti flusso contengono i dati e le archiviazioni forniscono la struttura.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320215"
---
# <a name="istream---compound-file-implementation"></a>Implementazione del file composto IStream

L'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supporta la lettura e la scrittura di dati negli oggetti flusso. In un oggetto di archiviazione strutturato gli oggetti flusso contengono i dati e le archiviazioni forniscono la struttura. I dati semplici possono essere scritti direttamente in un flusso, ma con maggiore frequenza, i flussi sono elementi annidati all'interno di un oggetto di archiviazione. Sono simili ai file standard.

La specifica di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) definisce più funzionalità rispetto a quelle supportate dall'implementazione com. Ad esempio, l'interfaccia **IStream** definisce i flussi fino a 2 ⁶ ⁴ byte di lunghezza che richiedono un puntatore di ricerca a 64 bit. Tuttavia, l'implementazione COM supporta solo flussi fino a 2 ³ ² di lunghezza (4 GB), mentre le operazioni di lettura e scrittura sono sempre limitate a 2 ³ ² byte alla volta. Anche l'implementazione COM non supporta la transazione di flusso o il blocco dell'area.

Per creare un flusso semplice basato sulla memoria globale, ottenere un puntatore [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) chiamando la funzione API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal). Per ottenere un puntatore **IStream** in un oggetto file composto, chiamare [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Queste funzioni recuperano un puntatore [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , con cui è possibile chiamare [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) o [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) per un puntatore **IStream** . In entrambi i casi, viene usato lo stesso codice di implementazione di **IStream** .

> [!Note]  
> L'implementazione del file composto di archiviazione strutturata non ha esito positivo su un metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), ma include i metodi [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) e [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) tramite il puntatore all'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .

 

## <a name="when-to-use"></a>Utilizzo

Chiamare i metodi di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per leggere e scrivere dati in un flusso.

Poiché è possibile effettuare il marshalling di oggetti flusso ad altri processi, le applicazioni possono condividere i dati negli oggetti di archiviazione senza dover usare la memoria globale. Nell'implementazione del file composto COM di oggetti Stream, le funzionalità di marshalling personalizzate in COM creano una versione remota dell'oggetto originale nel nuovo processo quando i due processi hanno accesso a memoria condivisa. Quindi, non è necessario che la versione remota comunichi con il processo originale per eseguire le relative funzioni.

La versione remota dell'oggetto flusso condivide lo stesso puntatore di ricerca del flusso originale. Se non si desidera condividere il puntatore Seek, utilizzare il metodo [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) per fornire una copia dell'oggetto flusso per il processo remoto.

> [!Note]
> Se si crea un oggetto flusso di dimensioni maggiori dell'heap nella memoria del computer e si usa un handle **HGLOBAL** per un oggetto memoria globale, l'oggetto flusso chiama il metodo [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) internamente, in modo che richieda più memoria. Poiché **GlobalReAlloc** copia sempre i dati dall'origine alla destinazione, l'aumento di un oggetto flusso da 20 MB a 25 MB, ad esempio, richiede una notevole quantità di tempo. Ciò è dovuto alla dimensione degli incrementi copiati e viene peggiorata se nel computer sono presenti meno di 45 MB di memoria a causa dello scambio del disco.
>
> La soluzione migliore consiste nell'implementare un metodo [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) che utilizza la memoria allocata da [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) anziché [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc). Questo può riservare una grande quantità di spazio degli indirizzi virtuali e quindi eseguire il commit della memoria all'interno di tale spazio di indirizzi in modo obbligatorio. Non viene eseguita la copia dei dati e viene eseguito il commit della memoria solo se necessario.
>
> Un'alternativa a [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) consiste nel chiamare il metodo [**IStream:: sesize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) sull'oggetto Stream per aumentare in anticipo l'allocazione di memoria. Questa operazione non è tuttavia efficace quanto l'utilizzo di [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), come descritto in precedenza.

 

## <a name="methods"></a>Metodi

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Legge un numero specificato di byte dall'oggetto flusso in memoria a partire dal puntatore di posizionamento corrente. Questa implementazione restituisce \_ OK se è stata raggiunta la fine del flusso durante la lettura. Questo comportamento è identico a quello del "fine del file" trovato nella file system FAT di MS-DOS.

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Scrive un numero specificato da byte nell'oggetto flusso a partire dal puntatore di ricerca corrente. In questa implementazione gli oggetti flusso non sono di tipo sparse. Tutti i byte di riempimento vengono infine allocati sul disco e assegnati al flusso.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Sposta il puntatore di posizionamento su un nuovo percorso relativo all'inizio del flusso, alla fine del flusso o al puntatore di posizionamento corrente.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: sesize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Modifica la dimensione dell'oggetto flusso. In questa implementazione, non vi è alcuna garanzia che lo spazio allocato sarà contiguo.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Copia un numero specificato di byte dal puntatore di posizionamento corrente nel flusso al puntatore di posizionamento corrente in un altro flusso.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

L'implementazione del file composto di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) supporta l'apertura dei flussi solo in modalità diretta, non in modalità transazionale. Pertanto, il metodo non ha alcun effetto quando viene chiamato diverso da per svuotare tutti i buffer di memoria al livello di archiviazione successivo.

In questa implementazione, non è importante se si esegue il commit delle modifiche nei flussi, è necessario eseguire solo le modifiche di commit per gli oggetti di archiviazione.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Questa implementazione non supporta i flussi transazionali, pertanto una chiamata a questo metodo non ha alcun effetto.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Il blocco dell'intervallo non è supportato da questa implementazione, quindi una chiamata a questo metodo non ha alcun effetto.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Rimuove la restrizione di accesso in un intervallo di byte precedentemente limitati con [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Recupera la struttura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) per questo flusso

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Crea un nuovo oggetto flusso con il proprio puntatore di posizionamento che fa riferimento agli stessi byte del flusso originale.

</dd> </dl>

Un [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) in modalità semplice è soggetto ai vincoli seguenti.

-   Un flusso è una modalità semplice se è stato creato o aperto da un'archiviazione in modalità semplice. Un archivio è una modalità semplice se viene creato o aperto con il \_ flag semplice STGM impostato nel parametro *grfMode* .
-   I metodi [**Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) e [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) non sono supportati.
-   Il metodo [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) è supportato, ma è \_ necessario specificare il valore StatFlag Noname.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 