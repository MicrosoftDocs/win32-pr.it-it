---
title: Implementazione di IStorage-Compound file
description: L'implementazione del file composto di IStorage consente di creare e gestire i flussi e le sottoarchiviazioni in un oggetto di archiviazione che risiede in un oggetto file composto.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299988"
---
# <a name="istorage-compound-file-implementation"></a>Implementazione di IStorage-Compound file

L'implementazione del file composto di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) consente di creare e gestire i flussi e le sottoarchiviazioni in un oggetto di archiviazione che risiede in un oggetto file composto. Per creare un oggetto file composto e ottenere un puntatore **IStorage** , chiamare la funzione API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Per aprire un oggetto file composto esistente e ottenere il puntatore **IStorage** radice, chiamare [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Le applicazioni che usano l'archiviazione composta devono essere registrate nelle \_ classi HKEY \_ radice \\ SystemFileAssociations e devono fornire i propri gestori di proprietà. Per ulteriori informazioni, vedere la sezione "registrazione di verbi e altre informazioni sull'associazione di file" della [registrazione dell'applicazione](/windows/desktop/shell/app-registration).

## <a name="when-to-use"></a>Utilizzo

La maggior parte delle applicazioni usa questa implementazione per creare e gestire le archiviazioni e i flussi.

## <a name="methods"></a>Metodi

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Crea e apre un oggetto flusso con il nome specificato contenuto in questo oggetto di archiviazione. Il nome non deve superare i 31 caratteri (escluso il carattere di terminazione della stringa). I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM del metodo [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) non supporta i comportamenti seguenti:

-   Il \_ flag DELETEONRELEASE di STGM non è supportato.
-   La modalità transazionale (STGM \_ transazionale) non è supportata per gli oggetti flusso.
-   L'apertura dello stesso flusso più di una volta dallo stesso spazio di archiviazione non è supportata. Il \_ flag della \_ modalità di condivisione esclusiva di condivisione STGM deve essere specificato nel parametro *grfMode* .

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Apre un oggetto flusso esistente in questo oggetto di archiviazione utilizzando le modalità di accesso specificate nel parametro *grfMode* . I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM del metodo [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) non supporta il comportamento seguente:

-   \_Flag DELETEONRELEASE di STGM.
-   Modalità transazionale (STGM transazionale \_ ) per gli oggetti flusso.
-   Apertura dello stesso flusso più di una volta dallo stesso spazio di archiviazione. \_ \_ È necessario specificare il flag STGM Share Exclusive.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Crea e apre un nuovo oggetto di archiviazione con il nome specificato nella modalità di accesso specificata. Il nome non deve superare i 31 caratteri (escluso il carattere di terminazione della stringa). I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM del metodo [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) non supporta il comportamento seguente:

-   \_Flag di priorità STGM per le archiviazioni non radice.
-   Apertura dello stesso oggetto di archiviazione più di una volta dallo stesso archivio padre. \_ \_ È necessario specificare il flag STGM Share Exclusive.
-   \_Flag DELETEONRELEASE di STGM. Se questo flag è specificato, la funzione restituisce STG \_ E \_ INVALIDFLAG.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Apre un oggetto di archiviazione esistente con il nome specificato nella modalità di accesso specificata. I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato. L'implementazione del file composto fornito da COM del metodo [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) non supporta il comportamento seguente:

-   \_Flag di priorità STGM per le archiviazioni non radice.
-   Apertura dello stesso oggetto di archiviazione più di una volta dallo stesso archivio padre. \_ \_ È necessario specificare il flag STGM Share Exclusive.
-   \_Flag DELETEONRELEASE di STGM. Se questo flag è specificato, la funzione restituisce STG \_ E \_ INVALIDFUNCTION.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Copia solo le sottoarchiviazioni e i flussi di questo oggetto di archiviazione aperti in un altro oggetto di archiviazione. Il parametro *rgiidExclude* può essere impostato su IID \_ IStream per copiare solo le sottoarchiviazioni o per l'IID \_ IStorage per copiare solo i flussi.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Copia o sposta un sottoarchivio o un flusso da questo oggetto di archiviazione a un altro oggetto di archiviazione.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Garantisce che tutte le modifiche apportate a un oggetto di archiviazione aperte in modalità transazionale si riflettano nell'archivio padre. per un archivio radice, riflette le modifiche nel dispositivo effettivo. ad esempio, un file su disco. Per un oggetto di archiviazione radice aperto in modalità diretta, questo metodo non ha alcun effetto tranne che per svuotare tutti i buffer di memoria sul disco. Per gli oggetti di archiviazione non radice in modalità diretta, questo metodo non ha alcun effetto.

L'implementazione dei file compositi fornita da COM usa un processo di commit in due fasi, a meno che non \_ venga specificato STGC overwrite nel parametro *grfCommitFlags* . Questo processo in due fasi garantisce l'affidabilità dei dati, nel caso in cui l'operazione di commit abbia esito negativo. In primo luogo, tutti i nuovi dati vengono scritti nello spazio inutilizzato nel file sottostante. Se necessario, al file viene allocato un nuovo spazio. Al termine di questo passaggio, una tabella nel file viene aggiornata usando un'operazione di scrittura a settore singolo per indicare che i nuovi dati devono essere usati al posto del vecchio. I dati obsoleti diventano spazio libero da usare alla successiva operazione di commit. Pertanto, i dati precedenti sono disponibili e possono essere ripristinati se si verifica un errore durante il commit delle modifiche. Se \_ si specifica STGC overwrite, viene utilizzata una singola operazione di commit della fase. Per ulteriori informazioni sui flag della modalità transazionale, vedere enumerazione [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) .

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Elimina tutte le modifiche apportate all'oggetto di archiviazione dall'ultima operazione di commit.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Crea e recupera un puntatore a un oggetto enumeratore che può essere usato per enumerare gli oggetti di archiviazione e di flusso contenuti in questo oggetto di archiviazione. L'implementazione del file composto fornito da COM acquisisce uno snapshot di tali informazioni. Pertanto, le modifiche apportate ai flussi e alle archiviazioni non vengono riflesse nell'enumeratore fino a quando non viene ottenuto un nuovo enumeratore.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Rimuove l'elemento specificato (substorage o Stream) da questo oggetto di archiviazione.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage:: RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Rinomina il flusso o lo spazio di archiviazione specificato in questo oggetto di archiviazione. I caratteri da 000 a 01f, che fungono da primo carattere del nome del flusso/archivio, sono riservati all'OLE. Si tratta di una limitazione del file composto, non della restrizione di un archivio strutturato.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Imposta la modifica, l'accesso e l'ora di creazione dell'elemento di archiviazione specificato. L'implementazione del file composto fornito da COM mantiene gli orari di modifica e modifica per gli oggetti di archiviazione interni. Gli oggetti di archiviazione radice supportano qualsiasi elemento supportato dalla file system sottostante (o da [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)). L'implementazione del file composto non mantiene alcun timestamp per i flussi interni. I timestamp non supportati vengono segnalati come zero, consentendo al chiamante di verificare il supporto.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage:: seclasse**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Assegna il CLSID specificato a questo oggetto di archiviazione.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage:: SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Archivia fino a 32 bit di informazioni sullo stato in questo oggetto di archiviazione. Lo stato impostato da questo metodo è solo per uso esterno. L'implementazione del file composto fornito da COM non esegue alcuna azione in base allo stato.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Recupera la struttura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) per questo oggetto di archiviazione aperto.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se l'oggetto di archiviazione viene aperto in modalità semplice, l'utilizzo dei metodi precedenti è limitato. Una risorsa di archiviazione è in modalità semplice se viene aperta con l' \_ elemento semplice STGM specificato nel parametro *grfMode* della funzione [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Per altre informazioni sulle archiviazioni in modalità semplice, vedere [**costanti STGM**](stgm-constants.md). Se l'oggetto di archiviazione in modalità semplice è stato ottenuto dalla funzione **StgCreateStorageEx** , è possibile chiamare il metodo [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) , ma il metodo [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) non può. Se l'oggetto di archiviazione in modalità semplice è stato ottenuto dalla funzione **StgOpenStorageEx** , è possibile chiamare il metodo **OpenStream** , ma il metodo **CreateStream** non può.

Quando si usa un oggetto di archiviazione in modalità semplice per creare un flusso, le dimensioni minime del flusso sono in genere pari a 4096 byte. Se nel flusso vengono scritti meno dati, le dimensioni vengono arrotondate per eccesso a 4096 byte.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di implementazione dei file composti](structured-storage-interfaces.md)
</dt> <dt>

[**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 