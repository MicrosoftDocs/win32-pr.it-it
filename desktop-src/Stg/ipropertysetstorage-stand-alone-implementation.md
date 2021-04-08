---
title: IPropertySetStorage-implementazione autonoma
description: L'implementazione autonoma fornita dal sistema di IPropertySetStorage include un'implementazione di IPropertyStorage e IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implementazioni
- IPropertySetStorage Strctd STG, implementazioni, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046851"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a>IPropertySetStorage-implementazione autonoma

L'implementazione autonoma fornita dal sistema di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) include un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) è l'interfaccia che legge e scrive le proprietà in una risorsa di archiviazione del set di proprietà. [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) è l'interfaccia che crea e apre i set di proprietà in una risorsa di archiviazione. Le interfacce [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sono inoltre disponibili nell'implementazione autonoma.

Per usare l'implementazione autonoma di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), ottenere prima un puntatore all'implementazione autonoma fornita dal sistema e associare l'implementazione fornita dal sistema all'oggetto di archiviazione. Per ottenere un puntatore all'implementazione autonoma di **IPropertySetStorage**, chiamare la funzione [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) e specificare il parametro *pStorage* che specifica l'oggetto di archiviazione che conterrà il set di proprietà. Questa funzione fornisce un puntatore alla nuova interfaccia **IPropertySetStorage** per l'oggetto di archiviazione specificato.

L'implementazione autonoma di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Crea set di proprietà per qualsiasi oggetto di archiviazione, non solo per le archiviazioni di file composte. L'implementazione autonoma non dipende dai file composti e può essere usata con qualsiasi implementazione di archivi strutturati. Tutte le restrizioni relative alle archiviazioni strutturate fornite dal chiamante si applicano a questa implementazione dei set di proprietà. Se ad esempio si fornisce un'archiviazione in modalità semplice per [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), il valore di **IPropertySetStorage** risultante sarà limitato dal [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)fornito.

Per ulteriori informazioni sull'implementazione del file composto di questa interfaccia, vedere la sezione [implementazione di file compositi IPropertySetStorage](ipropertysetstorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Utilizzo

Chiamare i metodi di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare, aprire ed eliminare set di proprietà in qualsiasi archivio strutturato. Esiste anche un metodo che fornisce un puntatore all'enumeratore [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) che può essere usato per enumerare i set di proprietà nell'archivio.

L'implementazione autonoma fornisce anche le funzioni di supporto [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) e [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , oltre ai metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , per creare e aprire i set di proprietà. Queste due funzioni aggiungono il supporto per il \_ valore non memorizzato nel buffer PROPSETFLAG, in modo che sia possibile scrivere le modifiche direttamente nel set di proprietà anziché memorizzarle nel buffer in una cache. Per altre informazioni, vedere [**costanti PROPSETFLAG**](propsetflag-constants.md).

## <a name="methods"></a>Metodi

L'implementazione autonoma di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supporta i metodi seguenti.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crea un nuovo set di proprietà nell'archivio e restituisce un puntatore all'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà.

Se si prevede di usare il valore PROPSETFLAG non \_ memorizzato nel buffer, usare invece la funzione [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) per creare e aprire il nuovo set di proprietà e ottenere un puntatore all'implementazione autonoma per l'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Apre un set di proprietà esistente nell'archiviazione e restituisce un puntatore all'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà.

Se si prevede di usare il valore PROPSETFLAG non \_ memorizzato nel buffer, usare invece la funzione [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) per ottenere un puntatore all'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà specificato.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D Elimina**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Elimina un set di proprietà in questa risorsa di archiviazione del set di proprietà.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crea un oggetto che può essere utilizzato per enumerare le strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Ogni struttura **STATPROPSETSTG** fornisce dati su un singolo set di proprietà.

> [!Note]  
> Il set di proprietà DocumentSummaryInformation e UserDefined è univoco in quanto può includere due sezioni del set di proprietà in un singolo flusso sottostante. Per ulteriori informazioni, vedere [i set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .

 

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IPropertyStorage-implementazione autonoma](ipropertystorage-stand-alone-implementation.md)
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
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**Costanti STGM**](stgm-constants.md)
</dt> </dl>

 

 