---
title: IPropertyStorage-implementazione autonoma
description: L'implementazione autonoma fornita dal sistema di IPropertySetStorage include un'implementazione di IPropertyStorage, l'interfaccia che legge e scrive le proprietà in una risorsa di archiviazione del set di proprietà.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-implementazione autonoma
- IPropertyStorage Strctd STG, implementazioni, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399194"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>IPropertyStorage-implementazione autonoma

L'implementazione autonoma fornita dal sistema di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) include un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l'interfaccia che legge e scrive le proprietà in una risorsa di archiviazione del set di proprietà. L'interfaccia **IPropertySetStorage** crea e apre i set di proprietà in una risorsa di archiviazione. Le interfacce [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sono inoltre disponibili nell'implementazione autonoma.

Per ottenere un puntatore all'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), chiamare la funzione [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) per creare un nuovo set di proprietà o [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) per ottenere il puntatore di interfaccia in un set di proprietà esistente (o chiamare i metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dell'implementazione autonoma [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Crea set di proprietà per qualsiasi oggetto di archiviazione o flusso, non solo per i flussi e le archiviazioni di file composte. L'implementazione autonoma non dipende dai file composti e può essere usata con qualsiasi implementazione di archivi strutturati. Per ulteriori informazioni sull'implementazione del file composito di questa interfaccia, vedere [IPropertyStorage-compound file implementation](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Utilizzo

Utilizzare [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) per gestire le proprietà all'interno di un singolo set di proprietà. I metodi supportano la lettura, la scrittura e l'eliminazione di entrambe le proprietà e i nomi di stringa facoltativi che possono essere associati a ID di proprietà. Altri metodi supportano le operazioni di commit e ripristino standard. Esiste anche un metodo che imposta i tempi associati all'archiviazione delle proprietà e un altro che consente l'assegnazione di un CLSID da usare per associare altro codice, ad esempio il codice dell'interfaccia utente, con il set di proprietà. Il metodo [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornisce un puntatore all'implementazione autonoma di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), che enumera le proprietà nel set.

## <a name="version-0-and-version-1-property-set-formats"></a>Formati di set di proprietà versione 0 e versione 1

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta sia la versione 0 che i formati di serializzazione del set di proprietà versione 1. Per ulteriori informazioni, vedere [serializzazione del set di proprietà](version-0-vs--version-1-property-set-serialization.md). I set di proprietà vengono creati nel formato versione 0 e rimangono in tale formato a meno che non vengano richieste nuove funzionalità. In quel momento, il formato viene aggiornato alla versione 1.

Se, ad esempio, viene creato un set di proprietà con il \_ flag predefinito PROPSETFLAG, il formato è la versione 0. Fino a quando i tipi di proprietà conformi al formato versione 0 vengono scritti e letti dal set di proprietà, il set di proprietà rimane nel formato versione 0. Se un tipo di proprietà della versione 1 viene scritto nel set di proprietà, il set di proprietà viene aggiornato automaticamente alla versione 1. Successivamente, il set di proprietà non può più essere letto dalle implementazioni che comprendono solo la versione 0.

## <a name="ipropertystorage-and-variant-types"></a>Tipi IPropertyStorage e Variant

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) non supporta i tipi Variant VT \_ Unknown o VT \_ Dispatch nel membro **VT** della struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

I tipi Variant seguenti sono supportati all'interno di SafeArray; ovvero, questi valori possono essere combinati con \_ una matrice VT nel membro **VT** della struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Tipi Variant supportati all'interno di SafeArray mediante l'implementazione del file composto di [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

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

L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta i metodi seguenti:

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Legge le proprietà specificate nella matrice *rgpspec* e fornisce i valori di tutte le proprietà valide nella matrice *rgvar* degli elementi [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Nell'implementazione autonoma fornita dal sistema, gli identificatori di proprietà duplicati che fanno riferimento a flussi o tipi di archiviazione generano più chiamate a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e l'esito positivo o negativo di [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) dipende dalla capacità dell'implementazione di archiviazione sottostante di condividere le archiviazioni aperte.

Inoltre, per garantire un'operazione thread-safe se la stessa proprietà con valori di flusso o di archiviazione viene richiesta più volte tramite lo stesso puntatore [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , l'apertura avrà esito positivo o negativo a seconda che la proprietà sia già aperta e che la file system sottostante gestisca più aperture di un flusso o di un'archiviazione. Di conseguenza, l'operazione [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) su una proprietà con valori di flusso o di archiviazione restituisce sempre una chiamata a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passando l'accesso ( \_ ad esempio, STGM ReadWrite) e i valori di condivisione (ad esempio, STGM \_ share \_ Exclusive) specificati quando il set di proprietà è stato originariamente aperto o creato.

Se il metodo ha esito negativo, i valori scritti in *rgvar* non \[ \] sono definiti. Se alcune proprietà con valori di archiviazione o flusso vengono aperte correttamente, ma si verifica un errore prima del completamento dell'esecuzione, queste proprietà devono essere rilasciate prima che il metodo venga restituito.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Scrive le proprietà specificate nella matrice *rgpspec* \[ \] , assegnando loro i tag e i valori [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) specificati in *rgvar* \[ \] . Alle proprietà già esistenti vengono assegnati i valori **PROPVARIANT** specificati e vengono create le proprietà attualmente non esistenti.

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

Elimina i nomi di stringa degli ID di proprietà specificati nella matrice *rgpropid* scrivendo **null** nel nome della proprietà.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: seclasse**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Imposta il **CLSID** del flusso del set di proprietà. Nell'implementazione autonoma, l'impostazione del CLSID su un set di proprietà non semplice, che può contenere proprietà con valori di archiviazione o flusso, come descritto in [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), imposta anche il CLSID sulla sottoarchiviazione sottostante in modo che sia possibile ottenerlo tramite una chiamata a [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Per i set di proprietà semplici e non semplici, Scarica l'immagine di memoria sul sottosistema del disco. Inoltre, per i set di proprietà in modalità transazionale non semplici, questo metodo chiama [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) sul set di proprietà.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Solo per set di proprietà non semplici, chiama il metodo [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) dell'archiviazione sottostante e riapre il flusso "Contents". Per i set di proprietà semplici, restituisce solo E \_ OK.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Crea un oggetto enumeratore che implementa [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), i metodi di cui è possibile chiamare per enumerare le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) che forniscono informazioni su ognuna delle proprietà nel set.

Questa implementazione crea una matrice in cui viene letto l'intero set di proprietà e che può essere condiviso quando viene chiamato [**IEnumSTATPROPSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) .

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Compila i membri di una struttura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , che contiene informazioni sul set di proprietà nel suo complesso. Al ritorno, fornisce un puntatore alla struttura.

Per i set di archiviazione non semplici, questa implementazione chiama [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) per ottenere le informazioni dal flusso o dall'archivio sottostante.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: setimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Solo per set di proprietà non semplici, imposta le ore supportate dall'archiviazione sottostante. Questa implementazione di [**Timers**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chiama il metodo [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) dell'archiviazione sottostante per modificare gli orari. Supporta le ore supportate dal metodo sottostante, che può essere l'ora di modifica, l'ora di accesso o l'ora di creazione.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IPropertySetStorage-implementazione autonoma](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 