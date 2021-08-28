---
title: Implementazione autonoma di IPropertyStorage
description: L'implementazione autonoma fornita dal sistema di IPropertySetStorage include un'implementazione di IPropertyStorage, l'interfaccia che legge e scrive le proprietà in un archivio del set di proprietà.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- Implementazione autonoma di IPropertyStorage
- IPropertyStorage Strctd Stg, implementazioni autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200d7f328670b8945807b7db7f742feabe58ad32847e3c56aa98a34278a71fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662551"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>Implementazione autonoma di IPropertyStorage

L'implementazione autonoma fornita dal sistema [**di IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) include un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l'interfaccia che legge e scrive le proprietà in un archivio del set di proprietà. **L'interfaccia IPropertySetStorage** crea e apre i set di proprietà in un archivio. Le [**interfacce IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) vengono fornite anche nell'implementazione autonoma.

Per ottenere un puntatore all'implementazione autonoma di [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)chiamare la funzione [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) per creare un nuovo set di proprietà o [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) per ottenere il puntatore a interfaccia su un set di proprietà esistente o chiamare i metodi [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dell'implementazione [**autonoma di IPropertySetStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crea set di proprietà su qualsiasi oggetto di archiviazione o flusso, non solo su flussi e archivi di file composti. L'implementazione autonoma non dipende dai file composti e può essere usata con qualsiasi implementazione di archivi strutturati. Per altre informazioni sull'implementazione di file compositi di questa interfaccia, vedere [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Utilizzo

Usare [**IPropertyStorage per**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gestire le proprietà all'interno di un singolo set di proprietà. I metodi supportano la lettura, la scrittura e l'eliminazione sia delle proprietà che dei nomi di stringa facoltativi che possono essere associati agli ID proprietà. Altri metodi supportano le operazioni standard di commit e ripristino dell'archiviazione. Esiste anche un metodo che imposta gli orari associati all'archiviazione delle proprietà e un altro che consente l'assegnazione di un CLSID da usare per associare altro codice, ad esempio il codice dell'interfaccia utente, al set di proprietà. Il [**metodo Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornisce un puntatore all'implementazione autonoma di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), che enumera le proprietà nel set.

## <a name="version-0-and-version-1-property-set-formats"></a>Formati dei set di proprietà versione 0 e 1

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta sia i formati di serializzazione dei set di proprietà versione 0 che versione 1. Per altre informazioni, vedere [Serializzazione di set di proprietà](version-0-vs--version-1-property-set-serialization.md). I set di proprietà vengono creati in formato versione 0 e rimangono in tale formato a meno che non vengano richieste nuove funzionalità. A quel tempo, il formato viene aggiornato alla versione 1.

Ad esempio, se un set di proprietà viene creato con il flag PROPSETFLAG \_ DEFAULT, il formato è la versione 0. Finché i tipi di proprietà conformi al formato versione 0 vengono scritti e letti da tale set di proprietà, il set di proprietà rimane nel formato versione 0. Se un tipo di proprietà versione 1 viene scritto nel set di proprietà, il set di proprietà viene aggiornato automaticamente alla versione 1. Successivamente, il set di proprietà non può più essere letto dalle implementazioni che comprendono solo la versione 0.

## <a name="ipropertystorage-and-variant-types"></a>Tipi IPropertyStorage e Variant

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) non supporta i tipi variant VT UNKNOWN o \_ VT DISPATCH nel membro \_ **vt** della [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

I tipi variant seguenti sono supportati all'interno di un oggetto SafeArray. in altri casi, questi valori possono essere combinati con VT \_ ARRAY nel **membro vt** della [**struttura PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)



Tipi variant supportati all'interno di SafeArray dall'implementazione di file compositi [ **di IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

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

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta i metodi seguenti:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Legge le proprietà specificate nella matrice *rgpspec* e fornisce i valori di tutte le proprietà valide nella matrice *rgvar* degli [**elementi PROPVARIANT.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Nell'implementazione autonoma fornita dal sistema, gli identificatori di proprietà duplicati che fanno riferimento ai tipi di flusso o di archiviazione comportano più chiamate a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e l'esito positivo o negativo di [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) dipende dalla possibilità dell'implementazione di archiviazione sottostante di condividere le risorse di archiviazione aperte.

Inoltre, per garantire un'operazione thread-safe se la stessa proprietà con valori di flusso o di archiviazione viene richiesta più volte tramite lo stesso puntatore [**IPropertyStorage,**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) l'apertura avrà esito positivo o negativo a seconda che la proprietà sia già aperta o meno e che il file system sottostante gestisca più aperti di un flusso o di un'archiviazione. Di conseguenza, l'operazione [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) su una proprietà con valori di flusso o di archiviazione comporta sempre una chiamata a [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passando l'accesso (STGM READWRITE, ad esempio) e i valori di condivisione \_ (STGM SHARE EXCLUSIVE, ad esempio) specificati quando il set di proprietà è stato originariamente aperto \_ o \_ creato.

Se il metodo ha esito negativo, i valori scritti in *rgvar* \[ \] non sono definiti. Se alcune proprietà con valori di flusso o di archiviazione vengono aperte correttamente ma si verifica un errore prima del completamento dell'esecuzione, queste proprietà devono essere rilasciate prima che il metodo venga restituito.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Scrive le proprietà specificate nella matrice *rgpspec,* assegnandole i tag \[ \] [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) e i valori specificati in *rgvar* \[ \] . Alle proprietà già esistenti vengono assegnati i valori **PROPVARIANT** specificati e vengono create le proprietà che attualmente non esistono.

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

Elimina i nomi di stringa degli ID proprietà specificati nella matrice *rgpropid* scrivendo **NULL** nel nome della proprietà.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Imposta il **CLSID** del flusso del set di proprietà. Nell'implementazione autonoma, l'impostazione del CLSID su un set di proprietà nonsimple (che può contenere proprietà di archiviazione o con valori di flusso, come descritto in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) imposta anche il CLSID nell'archivio secondario sottostante in modo che possa essere ottenuto tramite una chiamata a [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Per i set di proprietà semplici e non semplici, scarica l'immagine di memoria nel sottosistema del disco. Inoltre, per i set di proprietà in modalità transazione nonsimple, questo metodo chiama [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) sul set di proprietà.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Solo per i set di proprietà non disimple, chiama il [**metodo Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) dell'archiviazione sottostante e riapre il flusso 'contents'. Per i set di proprietà semplici, restituisce solo E \_ OK.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Crea un oggetto enumeratore che implementa [**IEnumSTATPROPSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)i cui metodi possono essere chiamati per enumerare le strutture [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) che forniscono informazioni su ognuna delle proprietà nel set.

Questa implementazione crea una matrice in cui viene letto l'intero set di proprietà e che può essere condiviso quando viene chiamato [**IEnumSTATPROPSTG::Clone.**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Compila i membri di una struttura [**STATPROPSETSTG,**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) che contiene informazioni sull'intero set di proprietà. In caso di restituzione, fornisce un puntatore alla struttura .

Per i set di archiviazione non di base, questa implementazione chiama [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) per ottenere le informazioni dall'archiviazione o dal flusso sottostante.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Solo per i set di proprietà nonsimple, imposta gli orari supportati dall'archiviazione sottostante. Questa implementazione [**di SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chiama il [**metodo IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) dell'archiviazione sottostante per modificare gli orari. Supporta gli orari supportati dal metodo sottostante, che possono essere ora di modifica, ora di accesso o ora di creazione.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione autonoma di IPropertySetStorage](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 