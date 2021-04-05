---
title: Implementazione di IPropertyStorage-Compound file
description: L'implementazione COM dell'architettura di archiviazione strutturata è denominata file composti.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd STG, implementazioni, file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d927b0145077f12e5ba508ca65554ca33633a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872650"
---
# <a name="ipropertystorage-compound-file-implementation"></a>Implementazione di IPropertyStorage-Compound file

L'implementazione COM dell'architettura di archiviazione strutturata è denominata [file composti](istorage-compound-file-implementation.md). Gli oggetti di archiviazione implementati nei file composti includono un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l'interfaccia che gestisce un singolo set di proprietà permanenti e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), l'interfaccia che gestisce i gruppi di set di proprietà permanenti. Per ulteriori informazioni sull'interfaccia **IPropertyStorage** , vedere [considerazioni sull'archiviazione delle proprietà](property-storage-considerations.md)e di **IPropertyStorage** .

Per ottenere un puntatore all'implementazione del file composto di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), chiamare [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) per creare un nuovo oggetto file composto o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) per aprire un oggetto file composto creato in precedenza. Nel caso di **StgCreateStorageEx**, il parametro *stgfmt* deve essere impostato su stgfmt \_ storage. Nel caso di **StgOpenStorageEx**, il parametro *stgfmt* deve essere impostato su stgfmt \_ storage o stgfmt \_ any. In entrambi i casi, il parametro *riid* deve essere impostato su IID \_ IPropertySetStorage. Entrambe le funzioni forniscono un puntatore all'interfaccia [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) dell'oggetto. Chiamando il metodo [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dell'interfaccia, si otterrà un puntatore all'interfaccia **IPropertyStorage** , che è possibile usare per chiamare uno dei metodi.

Un metodo alternativo per ottenere un puntatore all'implementazione del file composto di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) consiste nel chiamare le funzioni [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) e [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) precedenti oppure per specificare un parametro *riid* di IID \_ IStorage per la funzione [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . In entrambi i casi, viene restituito un puntatore all'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) dell'oggetto. Con i set di proprietà permanenti, chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per l'interfaccia **IPropertySetStorage** , specificando il nome definito dall'intestazione per l'IID dell'identificatore di interfaccia (IID) \_ IPropertySetStorage.

## <a name="when-to-use"></a>Utilizzo

Utilizzare [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) per gestire le proprietà all'interno di un singolo set di proprietà. I metodi supportano la lettura, la scrittura e l'eliminazione di entrambe le proprietà e i nomi di stringa facoltativi che possono essere associati a identificatori di proprietà. Altri metodi supportano le operazioni di commit e ripristino standard. È inoltre disponibile un metodo che consente di impostare gli orari associati all'archiviazione delle proprietà e un altro che consente l'assegnazione di un CLSID che può essere utilizzato per associare altro codice, ad esempio il codice dell'interfaccia utente, con il set di proprietà. La chiamata al metodo [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornisce un puntatore all'implementazione del file composto di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), che consente di enumerare le proprietà nel set.

> [!Note]  
> Se si ottiene un puntatore a [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) chiamando [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) o [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) in una risorsa di archiviazione con set di proprietà in modalità semplice, i metodi **IPropertyStorage** rispettano le regole dei flussi in modalità semplice. La modalità di archiviazione del set di proprietà è semplice se è stata ottenuta per un file che è stato creato o aperto con il \_ flag semplice STGM. In questo caso, non è sempre possibile rendere il flusso sottostante più grande e non è possibile sostituire le proprietà esistenti con proprietà più grandi. Per altre informazioni, vedere [IPropertySetStorage-implementazione del file composto](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage e Caching

L'implementazione del file composto di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) memorizza nella cache i set di proprietà aperti in memoria per migliorare le prestazioni. Di conseguenza, le modifiche apportate a un set di proprietà non vengono scritte nel file composto fino a quando non vengono chiamati i metodi di [**commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) o di **rilascio** (ultimo riferimento).

## <a name="simple-mode-property-sets"></a>Set di proprietà in modalità semplice

Un oggetto di archiviazione proprietà è in modalità semplice se viene creato da un oggetto di archiviazione del set di proprietà in modalità semplice. Ad esempio, un oggetto di archiviazione del set di proprietà è in modalità semplice se è stato ottenuto dalla funzione [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) con il \_ flag STGM Simple impostato nel parametro *grfMode* . Si noti che "Simple Mode" non è correlato a "Simple Property Sets". Un set di proprietà è semplice se viene creato chiamando [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) con il flag PROPSETFLAG non \_ semplice impostato nel parametro *grfFlags* . Per altre informazioni sui set di proprietà semplici e non semplici, vedere [oggetti di archiviazione e di flusso per un set di proprietà](storage-vs--stream-for-a-property-set.md).

Quando viene creato un oggetto di archiviazione della proprietà in modalità semplice, non sono previste restrizioni per l'utilizzo. Quando viene aperto un oggetto di archiviazione proprietà in modalità semplice esistente, l'oggetto flusso sottostante che archivia il set di proprietà non può essere aumentato. Di conseguenza, non è sempre possibile modificare tale oggetto di archiviazione proprietà se la modifica richiede un flusso più grande.

## <a name="property-set-formats"></a>Formati di set di proprietà

L'implementazione del file composto di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta sia la versione 0 che i formati di serializzazione del set di proprietà versione 1. Il formato versione 1 è supportato nei computer che eseguono Windows 2000. Per ulteriori informazioni, vedere [serializzazione del set di proprietà](version-0-vs--version-1-property-set-serialization.md). I set di proprietà vengono creati nel formato versione 0 e rimangono in tale formato a meno che non vengano richieste nuove funzionalità. In tal caso, il formato verrà aggiornato alla versione 1.

Se, ad esempio, viene creato un set di proprietà con il \_ flag predefinito PROPSETFLAG, il formato è la versione 0. Fino a quando i tipi di proprietà conformi al formato versione 0 vengono scritti e letti dal set di proprietà, il set di proprietà rimane nel formato versione 0. Se un tipo di proprietà della versione 1 viene scritto nel set di proprietà, il set di proprietà viene aggiornato automaticamente alla versione 1. Successivamente, il set di proprietà non può più essere letto dalle implementazioni che riconoscono solo la versione 0.

## <a name="ipropertystorage-and-variant-types"></a>Tipi IPropertyStorage e Variant

L'implementazione del file composito di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) non supporta i tipi varianti VT \_ Unknown o VT \_ Dispatch nel membro **VT** della struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Nella tabella seguente sono elencati i tipi Variant supportati all'interno di SafeArray; ovvero, questi valori possono essere combinati con \_ una matrice VT nel membro **VT** della struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Tipi Variant supportati all'interno di SafeArray mediante l'implementazione del file composto di IPropertyStorage

VT \_ I1

\_Ui1 VT

\_I2 VT

\_UI2 VT

VT \_ I4

\_UI4 VT

\_int VT

\_uint VT

\_R4 VT

VT \_ R8

\_CY VT

\_Data VT

\_BSTR VT

\_bool VT

\_decimale VT

\_errore VT

\_variante VT

 



 

Quando \_ la variante VT viene combinata con \_ la matrice VT, il SAFEARRAY stesso include le strutture [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Tuttavia, i tipi di questi elementi devono essere ricavati dall'elenco precedente, non possono essere \_ varianti VT e non possono includere gli \_ indicatori del vettore VT, dell'array VT o del \_ \_ ByRef VT.

## <a name="ipropertystorage-methods"></a>Metodi IPropertyStorage

L'implementazione del file composto di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta i metodi seguenti:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Legge le proprietà specificate nella matrice *rgpspec* e fornisce i valori di tutte le proprietà valide nella matrice *rgvar* di PROPVARIANTs. Nell'implementazione del file composto COM, gli identificatori di proprietà duplicati che fanno riferimento ai tipi di flusso o di archiviazione generano più chiamate a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e l'esito positivo o negativo di **ReadMultiple** dipende dalla capacità dell'implementazione di archiviazione sottostante di condividere le operazioni di apertura. Poiché in un file composto \_ è stata forzata la condivisione \_ esclusiva, più tentativi di apertura non riusciranno. Non è possibile aprire lo stesso oggetto di archiviazione più di una volta dallo stesso archivio padre. \_ \_ È necessario specificare il flag STGM Share Exclusive.

Inoltre, per garantire un'operazione thread-safe se la stessa proprietà con valori di flusso o di archiviazione viene richiesta più volte tramite lo stesso puntatore [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nell'implementazione del file composto com, l'operazione di apertura avrà esito positivo o negativo a seconda che la proprietà sia già aperta e che il file system sottostante gestisca più aperture di un flusso o di un'archiviazione. Pertanto, l'operazione **ReadMultiple** su una proprietà con valori di flusso o di archiviazione restituisce sempre una chiamata a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), che passa l'accesso (STGM \_ ReadWrite e così via) e i flag di condivisione (STGM \_ share \_ Exclusive e così via) specificati al momento dell'apertura o della creazione del set di proprietà originale.

Se il metodo ha esito negativo, i valori scritti in *rgvar* non \[ \] sono definiti. Se alcune proprietà con valori di flusso o di archiviazione vengono aperte correttamente, ma si verifica un errore prima del completamento dell'esecuzione, questi devono essere rilasciati prima che il metodo venga restituito.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Scrive le proprietà specificate nella matrice *rgpspec* \[ \] , assegnando loro i tag e i valori [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) specificati in *rgvar* \[ \] . Alle proprietà già esistenti vengono assegnati i valori **PROPVARIANT** specificati. Vengono create proprietà che attualmente non esistono.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Elimina le proprietà specificate in *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage:: ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Legge i nomi di stringa esistenti associati agli ID di proprietà specificati nella matrice *rgpropid* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Assegna i nomi di stringa specificati nella matrice *rglpwstrName* agli ID di proprietà specificati nella matrice *rgpropid* .

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Elimina i nomi di proprietà per le proprietà specificate nella matrice *rgpropid* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: seclasse**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Imposta il **CLSID** del flusso del set di proprietà. Nell'implementazione del file composto, impostando il CLSID su un set di proprietà non semplice, che può contenere legalmente proprietà con valori di archiviazione o flusso, come descritto in [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), imposta anche il CLSID sulla sottoarchiviazione sottostante in modo che sia possibile ottenerlo tramite una chiamata a [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Per i set di proprietà semplici e non semplici, Scarica l'immagine della memoria del set di proprietà nell'archivio sottostante. Inoltre, per i set di proprietà non semplici in modalità transazionale, questo metodo esegue un commit (come in [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) nella risorsa di archiviazione che contiene il set di proprietà.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Solo per set di proprietà non semplici, chiama il metodo [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) dell'archiviazione sottostante e riapre il flusso "Contents". Per i set di proprietà semplici, questa interfaccia restituisce sempre \_ OK. I set di proprietà non semplici sono quelli creati usando il flag PROPSETFLAG non \_ semplice nel metodo [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) . Per altre informazioni, vedere [oggetti di archiviazione e di flusso per un set di proprietà](storage-vs--stream-for-a-property-set.md) .

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Costruisce un'istanza di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), i metodi di cui è possibile chiamare per enumerare le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) che forniscono informazioni su ognuna delle proprietà nel set. Questa implementazione crea una matrice in cui viene letto l'intero set di proprietà e che può essere condiviso quando viene chiamato **IEnumSTATPROPSTG:: Clone** . Le modifiche apportate al set di proprietà non vengono riflesse in un'istanza di **IEnumSTATPROPSTG** aperta. Per visualizzare tali modifiche, è necessario costruire una nuova istanza di questo enumeratore.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Compila i membri di una struttura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , che contiene i dati relativi al set di proprietà nel suo complesso. Al ritorno, fornisce un puntatore alla struttura. Per i set di archiviazione non semplici, questa implementazione chiama [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) per ottenere gli orari dall'archiviazione o dal flusso sottostante. Per i set di archiviazione semplici, non vengono mantenuti orari.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: setimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Solo per set di proprietà non semplici, imposta le ore supportate dall'archiviazione sottostante. L'implementazione dell'archiviazione file composta supporta tutte e tre le operazioni: modifica, accesso e creazione. Questa implementazione di [**Timers**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chiama il metodo [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) dell'archiviazione sottostante per recuperare tali orari.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 