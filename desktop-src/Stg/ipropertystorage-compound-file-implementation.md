---
title: IPropertyStorage-Compound'implementazione di file
description: L'implementazione COM dell'architettura structured Archiviazione è denominata file compositi.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd Stg, implementazioni, file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3c4fffe98c4bfb896f346f25ce988f75bacf1fbb194b9ec27f50e22095c8cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662611"
---
# <a name="ipropertystorage-compound-file-implementation"></a>IPropertyStorage-Compound'implementazione di file

L'implementazione COM dell'architettura structured Archiviazione è denominata [file compositi.](istorage-compound-file-implementation.md) Archiviazione oggetti implementati nei file compositi includono un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l'interfaccia che gestisce un singolo set di proprietà persistenti e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), l'interfaccia che gestisce i gruppi di set di proprietà persistenti. Per altre informazioni **sull'interfaccia IPropertyStorage,** vedere Considerazioni sulle proprietà **e IPropertyStorage** [Archiviazione proprietà](property-storage-considerations.md).

Per ottenere un puntatore all'implementazione del file composto [**di IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)chiamare [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) per creare un nuovo oggetto file composto o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) per aprire un oggetto file composto creato in precedenza. Nel caso di **StgCreateStorageEx,** il *parametro stgfmt* deve essere impostato su STGFMT \_ STORAGE. Nel caso di **StgOpenStorageEx,** il *parametro stgfmt* deve essere impostato su STGFMT \_ STORAGE o STGFMT \_ ANY. In entrambi i casi, il *parametro riid* deve essere impostato su IID \_ IPropertySetStorage. Entrambe le funzioni forniscono un puntatore [**all'interfaccia IPropertySetStorage dell'oggetto.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Chiamando il metodo [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dell'interfaccia, si otterrà un puntatore all'interfaccia **IPropertyStorage,** che è possibile usare per chiamare uno dei relativi metodi.

Un modo alternativo per ottenere un puntatore all'implementazione di file compositi [**di IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) consiste nel chiamare le funzioni [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) e [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) precedenti o specificare un parametro *riid* di IID IStorage per la \_ funzione [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**o StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) In entrambi i casi, viene restituito un puntatore [**all'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) dell'oggetto. Con i set di proprietà persistenti, chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per **l'interfaccia IPropertySetStorage,** specificando il nome definito dall'intestazione per l'IID IPropertySetStorage dell'identificatore di interfaccia \_ (IID).

## <a name="when-to-use"></a>Utilizzo

Usare [**IPropertyStorage per**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gestire le proprietà all'interno di un singolo set di proprietà. I metodi supportano la lettura, la scrittura e l'eliminazione sia delle proprietà che dei nomi di stringa facoltativi che possono essere associati agli identificatori di proprietà. Altri metodi supportano le operazioni standard di commit e ripristino dell'archiviazione. Esiste anche un metodo che consente di impostare gli orari associati all'archiviazione delle proprietà e un altro che consente l'assegnazione di un CLSID che può essere usato per associare altro codice, ad esempio il codice dell'interfaccia utente, al set di proprietà. La chiamata [**al metodo Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornisce un puntatore all'implementazione del file composto [**di IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), che consente di enumerare le proprietà nel set.

> [!Note]  
> Se si ottiene un puntatore a [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) chiamando [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) o [**StgOpenStorageEx in**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) un archivio di set di proprietà in modalità semplice, i metodi **IPropertyStorage** rispettano le regole dei flussi in modalità semplice. L'archiviazione del set di proprietà è in modalità semplice se è stata ottenuta per un file creato o aperto con il flag STGM \_ SIMPLE. In questo caso, non è sempre possibile rendere più grande il flusso sottostante e non è possibile sostituire le proprietà esistenti con proprietà più grandi. Per altre informazioni, vedere [Implementazione di file compositi IPropertySetStorage.](ipropertysetstorage-compound-file-implementation.md)

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage e Caching

L'implementazione di file [**compositi di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) memorizza nella cache i set di proprietà aperti in memoria per migliorare le prestazioni. Di conseguenza, le modifiche apportate a un set di proprietà non vengono scritte nel file composto fino a quando non vengono chiamati i metodi [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o **Release** (ultimo riferimento).

## <a name="simple-mode-property-sets"></a>Set di proprietà in modalità semplice

Un oggetto di archiviazione delle proprietà è in modalità semplice se viene creato da un oggetto di archiviazione del set di proprietà in modalità semplice. Ad esempio, un oggetto di archiviazione del set di proprietà sarebbe in modalità semplice se fosse stato ottenuto dalla funzione [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) con il flag STGM SIMPLE impostato nel \_ *parametro grfMode.* Si noti che la "modalità semplice" non è correlata ai "set di proprietà semplici". Un set di proprietà è semplice se viene creato chiamando [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) con il flag PROPSETFLAG \_ NONSIMPLE impostato nel parametro *grfFlags.* Per altre informazioni sui set di proprietà semplici e non semplici, vedere Archiviazione e Oggetti di flusso [per un set di proprietà](storage-vs--stream-for-a-property-set.md).

Quando viene creato un oggetto di archiviazione delle proprietà in modalità semplice, non sono presenti restrizioni per l'utilizzo. Quando viene aperto un oggetto di archiviazione delle proprietà in modalità semplice esistente, l'oggetto flusso sottostante in cui è archiviato il set di proprietà non può essere aumentato. Di conseguenza, non è sempre possibile modificare un oggetto di archiviazione di proprietà di questo tipo se la modifica richiede un flusso più grande.

## <a name="property-set-formats"></a>Formati dei set di proprietà

L'implementazione di [**file compositi di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta sia la versione 0 che i formati di serializzazione del set di proprietà versione 1. Il formato versione 1 è supportato nei computer che eseguono Windows 2000. Per altre informazioni, vedere [Serializzazione di set di proprietà](version-0-vs--version-1-property-set-serialization.md). I set di proprietà vengono creati in formato versione 0 e rimangono in tale formato, a meno che non vengano richieste nuove funzionalità. In questo caso, il formato viene aggiornato alla versione 1.

Ad esempio, se un set di proprietà viene creato con il flag PROPSETFLAG \_ DEFAULT, il formato è la versione 0. Finché i tipi di proprietà conformi al formato versione 0 vengono scritti e letti da tale set di proprietà, il set di proprietà rimane nel formato versione 0. Se un tipo di proprietà versione 1 viene scritto nel set di proprietà, il set di proprietà viene aggiornato automaticamente alla versione 1. Successivamente, il set di proprietà non può più essere letto dalle implementazioni che riconoscono solo la versione 0.

## <a name="ipropertystorage-and-variant-types"></a>Tipi IPropertyStorage e Variant

L'implementazione del file composto [**di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) non supporta i tipi variant VT UNKNOWN o \_ VT DISPATCH nel membro \_ **vt** della [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Nella tabella seguente sono elencati i tipi variant supportati all'interno di un oggetto SafeArray. in altri casi, questi valori possono essere combinati con VT \_ ARRAY nel **membro vt** della [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)



Tipi variant supportati all'interno di SafeArray dall'implementazione di file compositi di IPropertyStorage

VT \_ I1

VT \_ UI1

VT \_ I2

Interfaccia utente \_ VT 2

VT \_ I4

Interfaccia utente \_ VT4

VT \_ INT

VT \_ UINT

VT \_ R4

VT \_ R8

VT \_ CY

DATA \_ VT

VT \_ BSTR

VT \_ BOOL

VT \_ DECIMAL

ERRORE \_ VT

VARIANTE \_ VT

 



 

Quando VT \_ VARIANT viene combinato con VT \_ ARRAY, SafeArray contiene strutture [**PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) Tuttavia, i tipi di questi elementi devono essere presi dall'elenco precedente, non possono essere VT VARIANT e non possono includere gli indicatori \_ VT \_ VECTOR, VT ARRAY o \_ VT \_ BYREF.

## <a name="ipropertystorage-methods"></a>Metodi IPropertyStorage

L'implementazione di [**file compositi di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta i metodi seguenti:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Legge le proprietà specificate nella matrice *rgpspec* e fornisce i valori di tutte le proprietà valide nella matrice *rgvar* di PROPVARIANT. Nell'implementazione del file composto COM, gli identificatori di proprietà duplicati che fanno riferimento ai tipi di flusso o di archiviazione comportano più chiamate a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e l'esito positivo o negativo di **ReadMultiple** dipende dalla capacità dell'implementazione di archiviazione sottostante di condividere le operazioni di apertura. Poiché in un file composto STGM \_ SHARE \_ EXCLUSIVE è forzato, più tentativi di apertura avranno esito negativo. L'apertura dello stesso oggetto di archiviazione più volte dalla stessa archiviazione padre non è supportata. È necessario specificare il flag STGM \_ SHARE \_ EXCLUSIVE.

Inoltre, per garantire un'operazione thread-safe se la stessa proprietà con valori di flusso o di archiviazione viene richiesta più volte tramite lo stesso puntatore [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nell'implementazione del file composto COM, l'operazione di apertura avrà esito positivo o negativo a seconda che la proprietà sia già aperta e se il file system sottostante gestisca più aperture di un flusso o di un archivio. Di conseguenza, l'operazione **ReadMultiple** su una proprietà con valori di flusso o di archiviazione comporta sempre una chiamata a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), che passa l'accesso (STGM READWRITE e così via) e i flag di condivisione (STGM SHARE EXCLUSIVE e così via) specificati quando il set di proprietà originale è stato aperto o \_ \_ \_ creato.

Se il metodo ha esito negativo, i valori scritti in *rgvar* \[ \] non sono definiti. Se alcune proprietà con valori di flusso o di archiviazione vengono aperte correttamente ma si verifica un errore prima del completamento dell'esecuzione, queste devono essere rilasciate prima che il metodo venga restituito.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Scrive le proprietà specificate nella matrice *rgpspec,* assegnandole i tag \[ \] [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) e i valori specificati in *rgvar* \[ \] . Alle proprietà già esistenti vengono assegnati i **valori PROPVARIANT** specificati. Vengono create proprietà attualmente inesistenti.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Elimina le proprietà specificate in *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Legge i nomi di stringa esistenti associati agli ID proprietà specificati nella matrice *rgpropid.* \[ \]

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Assegna i nomi di stringa specificati nella matrice *rglpwstrName* agli ID proprietà specificati nella matrice *rgpropid.*

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Elimina i nomi delle proprietà per le proprietà specificate nella matrice *rgpropid.* \[ \]

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Imposta il **CLSID** del flusso del set di proprietà. Nell'implementazione del file composto, l'impostazione del CLSID su un set di proprietà nonsimple (che può legalmente contenere proprietà di archiviazione o con valori di flusso, come descritto in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) imposta anche il CLSID nell'archivio secondario sottostante in modo che possa essere ottenuto tramite una chiamata a [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Per i set di proprietà semplici e non semplici, scarica l'immagine di memoria del set di proprietà nell'archiviazione sottostante. Inoltre, per i set di proprietà in modalità transazione non semplice, questo metodo esegue un commit (come in [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) nella memoria che contiene il set di proprietà.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Solo per i set di proprietà non standard, chiama il [**metodo Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) dell'archiviazione sottostante e riapre il flusso 'contents'. Per i set di proprietà semplici, questa interfaccia restituisce sempre S \_ OK. I set di proprietà nonsimple sono quelli creati usando il flag PROPSETFLAG \_ NONSIMPLE nel [**metodo IPropertySetStorage::Create.**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) Per altre informazioni, vedere oggetti [Archiviazione e Stream per un set di proprietà.](storage-vs--stream-for-a-property-set.md)

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Costruisce un'istanza di [**IEnumSTATPROPSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)i cui metodi possono essere chiamati per enumerare le strutture [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) che forniscono informazioni su ognuna delle proprietà nel set. Questa implementazione crea una matrice in cui viene letto l'intero set di proprietà e che può essere condiviso quando viene chiamato **IEnumSTATPROPSTG::Clone.** Le modifiche apportate al set di proprietà non vengono riflesse in **un'istanza IEnumSTATPROPSTG** aperta. Per visualizzare tali modifiche, è necessario costruire una nuova istanza di questo enumeratore.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Inserisce i membri di una [**struttura STATPROPSETSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) che contiene i dati relativi al set di proprietà nel suo complesso. In caso di restituzione, fornisce un puntatore alla struttura . Per i set di archiviazione nonsimple, questa implementazione chiama [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) per ottenere gli orari dall'archiviazione o dal flusso sottostante. Per i set di archiviazione semplici, non vengono mantenuti orari.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Solo per i set di proprietà non di base, imposta gli orari supportati dall'archiviazione sottostante. L'implementazione dell'archiviazione file composta supporta tutti e tre: modifica, accesso e creazione. Questa implementazione [**di SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chiama [**il metodo IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) dell'archiviazione sottostante per recuperare questi orari.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 