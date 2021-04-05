---
title: Implementazione di IPropertySetStorage-Compound file
description: L'implementazione dell'oggetto di archiviazione file composto COM include un'implementazione di IPropertyStorage, l'interfaccia che gestisce un singolo set di proprietà permanenti e IPropertySetStorage, l'interfaccia che gestisce i gruppi di set di proprietà permanenti.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd STG, implementazioni, file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9053a7cf6bf1ae7e4230b15eb0117c428acb08da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729082"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>Implementazione di IPropertySetStorage-Compound file

L' [implementazione dell'oggetto di archiviazione file composto com](ipropertystorage-compound-file-implementation.md) include un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l'interfaccia che gestisce un singolo set di proprietà permanenti e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), l'interfaccia che gestisce i gruppi di set di proprietà permanenti.

Per ottenere un puntatore all'implementazione del file composto di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), specificare il nome definito dall'intestazione per l'identificatore IID \_ IStorage come parametro *riid* oppure utilizzare le funzioni [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . In entrambi i casi, specificare STGFMT \_ storage come parametro *STGFMT* . (STGFMT \_ In alternativa, è possibile specificare qualsiasi nel caso di **StgOpenStorageEx**. Specificare anche il nome definito dall'intestazione per l'IID (Interface Identifier) IID \_ IPropertySetStorage come parametro *riid* . Entrambe le funzioni forniscono un puntatore all'interfaccia **IPropertySetStorage** dell'oggetto.

Un altro modo per ottenere un puntatore all'implementazione del file composto è quello di specificare il nome definito dall'intestazione per l'identificatore IID \_ IStorage come parametro *riid* o di usare le funzioni [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) o [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) . Verrà fornito un puntatore all'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) dell'oggetto. Quando si desidera gestire i set di proprietà permanenti, chiamare [**IStorage:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

## <a name="when-to-use-ipropertysetstorage"></a>Quando usare IPropertySetStorage

Chiamare i metodi di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare, aprire o eliminare set di proprietà nella risorsa di archiviazione del set di proprietà del file composto corrente. Esiste anche un metodo, [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), che fornisce un puntatore a un enumeratore che può essere usato per enumerare i set di proprietà nell'archivio.

## <a name="methods"></a>Metodi

[**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Crea un nuovo set di proprietà nell'archivio file composto corrente e, al ritorno, fornisce un puntatore di interfaccia all'implementazione del file composto [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . In questa implementazione i set di proprietà possono essere sottoposti a transazione solo se \_ viene specificato PROPSETFLAG non semplice. Questo metodo richiede che la modalità di condivisione specificata nel parametro *grfMode* sia STGM \_ share \_ Exclusive e che la modalità di accesso sia STGM \_ Read o STGM \_ ReadWrite ( \_ la modalità di scrittura STGM non è supportata).

[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Apre un set di proprietà esistente nell'archivio della proprietà corrente. Al ritorno, fornisce un puntatore di interfaccia all'implementazione del file composito di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Questo metodo richiede che la modalità di condivisione specificata nel parametro *grfMode* sia STGM \_ share \_ Exclusive e che la modalità di accesso sia STGM \_ Read o STGM \_ ReadWrite (STGM \_ Write non è supportata).

[**IPropertySetStorage::D Elimina**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Elimina un set di proprietà in questo archivio delle proprietà.

[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Crea un oggetto utilizzato per enumerare le strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Ogni struttura **STATPROPSETSTG** fornisce dati su un singolo set di proprietà.

## <a name="remarks"></a>Commenti

A partire da Windows 2000, l'implementazione del file composto di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supporta la modalità semplice. La modalità semplice è indicata specificando il \_ flag semplice STGM per le funzioni [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) e [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Se il file composto viene aperto in modalità semplice, l'implementazione di **IPropertySetStorage** associata è limitata come segue:

-   È possibile creare solo set di proprietà semplici. Ovvero, se si specifica il \_ valore PROPSETFLAG non semplice nel parametro *grfFlags* per il metodo [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) viene restituito un errore.
-   Dopo aver creato un file composto con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) usando STGM \_ Simple ed eseguendo una query per l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , è possibile chiamare solo [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) una sola volta. Quindi è necessario rilasciare l'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prima di chiamare di nuovo il metodo **create** . Per altre informazioni sulla modalità semplice, vedere [**costanti STGM**](stgm-constants.md).
-   Non è possibile usare il metodo [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) per aprire un set di proprietà dopo l'uso di [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) per creare l'oggetto di archiviazione. È invece necessario usare [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) prima di eseguire una query su [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e chiamare il metodo **Open** .
-   Dopo aver aperto un file composto con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) usando il \_ flag semplice STGM e la query per l'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , è possibile aprire un set di proprietà alla volta usando [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). Inoltre, potrebbe non essere possibile aumentare la dimensione totale del set di proprietà quando il set di proprietà è aperto.

I set di proprietà semplici non possono essere sottoposti a transazione. Non è possibile specificare STGM \_ transazionale nel parametro *grfMode* dei metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , a meno che non si specifichi anche PROPSETFLAG \_ nonsimple nel parametro *grfFlags* . Tenere presente che i set di proprietà semplici e non semplici non sono correlati ai set di proprietà in modalità semplice descritti in precedenza. Per altre informazioni sui set di proprietà semplici e non semplici, vedere [oggetti di archiviazione e di flusso per un set di proprietà](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> I set di proprietà DocumentSummaryInformation e UserDefined sono univoci in quanto possono avere due sezioni set di proprietà. Per ulteriori informazioni, vedere [i set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IPropertyStorage-implementazione del file composto](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Costanti PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 