---
title: IStorage-Compound'implementazione del file di configurazione
description: L'implementazione di file compositi di IStorage consente di creare e gestire archivi secondari e flussi all'interno di un oggetto di archiviazione che risiede in un oggetto file composto.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd Stg , implementazione di file compositi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab243189d5a8cfb3e053c66bcd752d05bb65ab965657778a3bc3250c30ef8e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992414"
---
# <a name="istorage-compound-file-implementation"></a>IStorage-Compound'implementazione del file di configurazione

L'implementazione di file compositi [**di IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) consente di creare e gestire archivi secondari e flussi all'interno di un oggetto di archiviazione che risiede in un oggetto file composto. Per creare un oggetto file composto e ottenere un **puntatore IStorage,** chiamare la funzione API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Per aprire un oggetto file composto esistente e ottenere il puntatore **IStorage** radice, chiamare [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Le applicazioni che usano l'archiviazione composta devono essere registrate in HKEY \_ CLASSES \_ ROOT \\ SystemFileAssociations e devono fornire i propri gestori delle proprietà. Per altre informazioni, vedere la sezione "Registrazione di verbi e altre informazioni sull'associazione di file" di [Registrazione dell'applicazione](/windows/desktop/shell/app-registration).

## <a name="when-to-use"></a>Utilizzo

La maggior parte delle applicazioni usa questa implementazione per creare e gestire archivi e flussi.

## <a name="methods"></a>Metodi

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Crea e apre un oggetto flusso con il nome specificato contenuto in questo oggetto di archiviazione. Il nome non deve superare i 31 caratteri (senza includere il carattere di terminazione della stringa). I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM [**del metodo IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) non supporta i comportamenti seguenti:

-   Il flag STGM \_ DELETEONRELEASE non è supportato.
-   La modalità transazione (STGM \_ TRANSACTED) non è supportata per gli oggetti flusso.
-   L'apertura dello stesso flusso più volte dalla stessa archiviazione non è supportata. Il flag STGM \_ SHARE \_ EXCLUSIVE sharing-mode deve essere specificato nel *parametro grfMode.*

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Apre un oggetto flusso esistente all'interno di questo oggetto di archiviazione usando le modalità di accesso specificate nel *parametro grfMode.* I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM [**del metodo IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) non supporta il comportamento seguente:

-   Flag STGM \_ DELETEONRELEASE.
-   Modalità transazione (STGM \_ TRANSACTED) per gli oggetti flusso.
-   Apertura dello stesso flusso più di una volta dalla stessa archiviazione. È necessario specificare il flag STGM \_ SHARE \_ EXCLUSIVE.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Crea e apre un nuovo oggetto di archiviazione con il nome specificato nella modalità di accesso specificata. Il nome non deve superare i 31 caratteri (senza includere il carattere di terminazione della stringa). I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM [**del metodo IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) non supporta il comportamento seguente:

-   Flag STGM \_ PRIORITY per le risorse di archiviazione nonroot.
-   Apertura dello stesso oggetto di archiviazione più volte dalla stessa archiviazione padre. È necessario specificare il flag STGM \_ SHARE \_ EXCLUSIVE.
-   Flag STGM \_ DELETEONRELEASE. Se si specifica questo flag, la funzione restituisce STG \_ E \_ INVALIDFLAG.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Apre un oggetto di archiviazione esistente con il nome specificato nella modalità di accesso specificata. I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM [**del metodo IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) non supporta il comportamento seguente:

-   Flag STGM \_ PRIORITY per le risorse di archiviazione nonroot.
-   Apertura dello stesso oggetto di archiviazione più volte dalla stessa archiviazione padre. È necessario specificare il flag STGM \_ SHARE \_ EXCLUSIVE.
-   Flag STGM \_ DELETEONRELEASE. Se si specifica questo flag, la funzione restituisce STG \_ E \_ INVALIDFUNCTION.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Copia solo le sottocartelle e i flussi di questo oggetto di archiviazione aperto in un altro oggetto di archiviazione. Il *parametro rgiidExclude* può essere impostato su IID IStream per copiare solo le sottocartelle o su ISTORAGE IID per copiare \_ solo i \_ flussi.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage::MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Copia o sposta un'archiviazione secondaria o un flusso da questo oggetto di archiviazione a un altro oggetto di archiviazione.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Garantisce che tutte le modifiche apportate a un oggetto di archiviazione aperto in modalità transazione siano riflesse nell'archiviazione padre. per un archivio radice, riflette le modifiche nel dispositivo effettivo; ad esempio un file su disco. Per un oggetto di archiviazione radice aperto in modalità diretta, questo metodo non ha alcun effetto se non per scaricare tutti i buffer di memoria sul disco. Per gli oggetti di archiviazione nonroot in modalità diretta, questo metodo non ha alcun effetto.

L'implementazione di file compositi forniti da COM usa un processo di commit in due fasi a meno che STGC OVERWRITE non sia specificato \_ nel *parametro grfCommitFlags.* Questo processo in due fasi garantisce l'affidabilità dei dati, nel caso in cui l'operazione di commit non riesca. In primo luogo, tutti i nuovi dati vengono scritti nello spazio inutilizzato nel file sottostante. Se necessario, viene allocato nuovo spazio al file. Al termine di questo passaggio, una tabella nel file viene aggiornata usando un'operazione di scrittura a settore singolo per indicare che i nuovi dati devono essere usati al posto del vecchio. I dati vecchi diventano spazio libero da usare alla successiva operazione di commit. Di conseguenza, i dati vecchi sono disponibili e possono essere ripristinati se si verifica un errore durante il commit delle modifiche. Se si imposta STGC \_ OVERWRITE, viene usata un'operazione di commit a fase singola. Per altre informazioni sui flag in modalità transazione, vedere [**Enumerazione STGC.**](/windows/win32/api/wtypes/ne-wtypes-stgc)

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Rimuove tutte le modifiche apportate all'oggetto di archiviazione dall'ultima operazione di commit.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Crea e recupera un puntatore a un oggetto enumeratore che può essere usato per enumerare gli oggetti di archiviazione e flusso contenuti in questo oggetto di archiviazione. L'implementazione di file compositi fornita da COM consente di creare uno snapshot di queste informazioni. Pertanto, le modifiche ai flussi e alle risorse di archiviazione non vengono riflesse nell'enumeratore fino a quando non viene ottenuto un nuovo enumeratore.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Rimuove l'elemento specificato (archivio secondario o flusso) da questo oggetto di archiviazione.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage::RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Rinomina l'archivio secondario o il flusso specificato in questo oggetto di archiviazione. I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Imposta le ore di modifica, accesso e creazione dell'elemento di archiviazione specificato. L'implementazione di file compositi fornita da COM mantiene i tempi di modifica e di modifica per gli oggetti di archiviazione interni. Gli oggetti di archiviazione radice supportano qualsiasi elemento supportato dal file system sottostante (o [**da ILockBytes).**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) L'implementazione del file composto non mantiene alcun timestamp per i flussi interni. I timestamp non supportati vengono segnalati come zero, che consente al chiamante di testare il supporto.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Assegna il CLSID specificato a questo oggetto di archiviazione.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage::SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Archivia fino a 32 bit di informazioni sullo stato in questo oggetto di archiviazione. Lo stato impostato da questo metodo è solo per uso esterno. L'implementazione del file composto fornito da COM non esegue alcuna azione in base allo stato.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Recupera la struttura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) per questo oggetto di archiviazione aperto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se l'oggetto di archiviazione viene aperto in modalità semplice, l'uso dei metodi precedenti è limitato. Un'archiviazione è in modalità semplice se viene aperta con l'elemento STGM SIMPLE specificato nel parametro \_ *grfMode* della [**funzione StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Per altre informazioni sulle risorse di archiviazione in modalità semplice, vedere [**Costanti STGM.**](stgm-constants.md) Se l'oggetto di archiviazione in modalità semplice è stato ottenuto dalla funzione **StgCreateStorageEx,** è possibile chiamare il metodo [**CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ma non il [**metodo OpenStream.**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) Se l'oggetto di archiviazione in modalità semplice è stato ottenuto dalla funzione **StgOpenStorageEx,** è possibile chiamare il metodo **OpenStream,** ma non il **metodo CreateStream.**

Quando un oggetto di archiviazione in modalità semplice viene usato per creare un flusso, le dimensioni minime del flusso in genere sono 4096 byte. Se nel flusso vengono scritti meno dati, le dimensioni vengono arrotondate per es.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di implementazione dei file compositi](structured-storage-interfaces.md)
</dt> <dt>

[**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**Istream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 