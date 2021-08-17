---
title: IPropertySetStorage-Compound'implementazione del file di configurazione
description: L'implementazione dell'oggetto di archiviazione file composta COM include un'implementazione di IPropertyStorage, l'interfaccia che gestisce un singolo set di proprietà persistenti e IPropertySetStorage, l'interfaccia che gestisce i gruppi di set di proprietà persistenti.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd Stg , implementazioni, file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3bc0d423b304b6d456ccddab158a48ba0b6d5f3f310d293c6aed0dedb2a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662661"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>IPropertySetStorage-Compound'implementazione del file di configurazione

L'implementazione dell'oggetto di archiviazione file composta [COM](ipropertystorage-compound-file-implementation.md) include un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l'interfaccia che gestisce un singolo set di proprietà persistenti e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), l'interfaccia che gestisce i gruppi di set di proprietà persistenti.

Per ottenere un puntatore all'implementazione del file composto [**di IPropertySetStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)specificare il nome definito dall'intestazione per l'identificatore IID IStorage come parametro riid oppure usare le funzioni \_ [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)  In entrambi i casi specificare STGFMT \_ STORAGE come *parametro stgfmt.* (STGFMT \_ È possibile specificare ANY in alternativa nel caso di **StgOpenStorageEx.** Specificare anche il nome definito dall'intestazione per l'IID (Interface Identifier) \_ IPropertySetStorage come *parametro riid.* Entrambe le funzioni forniscono un puntatore **all'interfaccia IPropertySetStorage dell'oggetto.**

Un altro modo per ottenere un puntatore all'implementazione del file composto è specificare il nome definito dall'intestazione per l'identificatore IID IStorage come parametro riid o usare le funzioni \_ [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)  Verrà fornito un puntatore all'interfaccia [**IStorage dell'oggetto.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Per gestire i set di proprietà persistenti, chiamare [**IStorage::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per [**l'interfaccia IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

## <a name="when-to-use-ipropertysetstorage"></a>Quando usare IPropertySetStorage

Chiamare i metodi di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare, aprire o eliminare set di proprietà nell'archiviazione corrente del set di proprietà dei file composti. Esiste anche un metodo, [**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), che fornisce un puntatore a un enumeratore che può essere usato per enumerare i set di proprietà nell'archiviazione.

## <a name="methods"></a>Metodi

[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Crea un nuovo set di proprietà nell'archivio file composto corrente e, in caso di restituzione, fornisce un puntatore a interfaccia all'implementazione del file composto [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) In questa implementazione, i set di proprietà possono essere transazionati solo se si specifica PROPSETFLAG \_ NONSIMPLE. Questo metodo richiede che la modalità di condivisione specificata nel parametro *grfMode* sia STGM SHARE EXCLUSIVE e che la modalità di accesso sia STGM READ o \_ \_ \_ STGM \_ READWRITE (modalità STGM WRITE non \_ supportata).

[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Apre un set di proprietà esistente nell'archivio delle proprietà corrente. In caso di restituzione, fornisce un puntatore a interfaccia all'implementazione del file composto [**di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Questo metodo richiede che la modalità di condivisione specificata nel parametro *grfMode* sia STGM SHARE EXCLUSIVE e che la modalità di accesso sia STGM READ o \_ \_ \_ STGM \_ READWRITE (STGM WRITE non è \_ supportata).

[**IPropertySetStorage::D elete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Elimina un set di proprietà in questa archiviazione di proprietà.

[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Crea un oggetto utilizzato per enumerare [**le strutture STATPROPSETSTG.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) Ogni **struttura STATPROPSETSTG** fornisce dati su un singolo set di proprietà.

## <a name="remarks"></a>Commenti

A partire da Windows 2000, l'implementazione di file compositi [**di IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supporta la modalità semplice. La modalità semplice viene indicata specificando il flag STGM \_ SIMPLE per le funzioni [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) e [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Se il file composto viene aperto in modalità semplice, l'implementazione **IPropertySetStorage** associata è limitata come segue:

-   È possibile creare solo set di proprietà semplici. Ciò significa che se si specifica il valore PROPSETFLAG NONSIMPLE nel parametro \_ *grfFlags* per il metodo [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) viene generato un errore.
-   Dopo aver creato un file composto con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) usando STGM SIMPLE ed eseguire una query per l'interfaccia \_ [**IPropertySetStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) è possibile chiamare [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) una sola volta. È quindi necessario rilasciare [**l'interfaccia IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prima di chiamare **nuovamente il metodo Create.** Per altre informazioni sulla modalità semplice, vedere [**Costanti STGM.**](stgm-constants.md)
-   Non è possibile usare il [**metodo IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) per aprire un set di proprietà dopo aver utilizzato [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) per creare l'oggetto di archiviazione. È invece necessario usare [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) prima di eseguire una query [**per IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e chiamare il **metodo Open.**
-   Dopo aver aperto un file composto con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) usando il flag STGM SIMPLE ed eseguire una query per l'interfaccia IPropertySetStorage, è possibile aprire un set di proprietà alla volta \_ usando [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). [](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Inoltre, potrebbe non essere possibile aumentare le dimensioni totali del set di proprietà mentre il set di proprietà è aperto.

I set di proprietà semplici non possono essere transazionati. Non è possibile specificare STGM TRANSACTED nel parametro grfmode dei metodi Create e Open a meno che non si specifica anche \_ PROPSETFLAG NONSIMPLE nel parametro  [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) [](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) \_ *grfFlags.* Tenere presente che i set di proprietà semplici e non semplici non sono correlati ai set di proprietà in modalità semplice descritti in precedenza. Per altre informazioni sui set di proprietà semplici e non semplici, vedere Archiviazione e Oggetti di flusso [per un set di proprietà](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> I set di proprietà DocumentSummaryInformation e UserDefined sono univoci in quanto possono avere due sezioni del set di proprietà. Per altre informazioni, vedere [DocumentSummaryInformation e Set di proprietà definite dall'utente](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IPropertyStorage - Implementazione di file compositi](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Costanti PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 