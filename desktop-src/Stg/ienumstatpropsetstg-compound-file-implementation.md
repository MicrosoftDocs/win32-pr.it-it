---
title: Implementazione di IEnumSTATPROPSETSTG-Compound file
description: L'implementazione del file composto dell'interfaccia IEnumSTATPROPSETSTG viene utilizzata per enumerare una matrice di strutture STATPROPSETSTG che contengono dati statistici della proprietà.
ms.assetid: 1ce36e40-518c-411b-be5a-835a2dd0995e
keywords:
- IEnumSTATPROPSETSTG Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9566af1a1956b3a951a996b6198f4a3161680042
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337742"
---
# <a name="ienumstatpropsetstg-compound-file-implementation"></a>Implementazione di IEnumSTATPROPSETSTG-Compound file

L'implementazione del file composto dell'interfaccia [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) viene utilizzata per enumerare una matrice di strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) che contengono dati statistici della proprietà. L'implementazione di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) gestisce i dati statistici ed è associata a un oggetto di archiviazione file composto corrente.

## <a name="when-to-use"></a>Utilizzo

Chiamare i metodi di [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) per enumerare le strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , ognuna delle quali fornisce dati su uno dei set di proprietà associati all'oggetto di archiviazione file composto.

## <a name="remarks"></a>Commenti

<dl> <dt>

<span id="IEnumSTATPROPSETSTG__Next"></span><span id="ienumstatpropsetstg__next"></span><span id="IENUMSTATPROPSETSTG__NEXT"></span>[**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Ottiene le successive strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) (il numero viene specificato dal parametro *celt* ). Gli elementi **STATPROPSETSTG** forniti tramite una chiamata all'implementazione del file composto di [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) seguono le regole seguenti:

-   Se [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) non è in grado di fornire STATPROPSETSTG. fmtid, gli zeri vengono scritti in quel membro. Questo errore si verifica quando il set di proprietà non dispone di un nome predefinito, ad esempio \\ 005SummaryInformation, e non è un valore valido.
-   Il set di proprietà DocumentSummaryInformation e UserDefined è speciale, in quanto può includere due sezioni set di proprietà. Questo set di proprietà è descritto nella sezione [set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md). La seconda sezione è indicata come proprietà User-Defined. Ogni sezione viene identificata con un identificatore di formato univoco (FMTID). Quando [**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum) viene usato per enumerare i set di proprietà, il set di proprietà User-Defined non verrà enumerato.

> [!Note]  
> Se si crea sempre un set di proprietà usando [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), quindi, poiché viene creato un "GUID di tipo carattere" per il nome di archiviazione, [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) restituirà un fmtid valido diverso da zero per il set di proprietà \[ STATPROPSETSTG. fmtid \] .

 

-   Il membro STATPROPSETSTG. grfFlags non riflette necessariamente se il set di proprietà è ANSI o meno. Se \_ è impostato PROPSETFLAG ANSI, il set di proprietà è sicuramente ANSI. Se PROPSETFLAG \_ ANSI è chiaro, il set di proprietà potrebbe essere Unicode o non Unicode, perché non è possibile stabilire se è ANSI senza aprirlo.
-   Il membro STATPROPSETSTG. grfFlags riflette se il set di proprietà è semplice o meno, quindi l'impostazione del flag PROPSETFLAG non \_ semplice è sempre valida.
-   Se [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) non è in grado di fornire STATPROPSETSTG. CLSID, viene impostato su tutti zeri (CLSID \_ null). Nell'implementazione del file composto COM, questo errore si verifica quando il set di proprietà è semplice (il \_ flag PROPSETFLAG non semplice non è impostato) o è non semplice, ma il CLSID non è stato impostato in modo esplicito. Per i set di proprietà non semplici, il CLSID ricevuto è quello gestito dal [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)sottostante.
-   Se [**IEnumSTATPROPSETSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) non è in grado di fornire i campi di tempo \[ **CTime**, **mtime**, **dell'atime** \] , ogni ora non supportata verrà impostata su zero. Nell'implementazione del file composto COM, ottenere questi valori dipende dal recupero dall'implementazione [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) sottostante.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Skip"></span><span id="ienumstatpropsetstg__skip"></span><span id="IENUMSTATPROPSETSTG__SKIP"></span>[**IEnumSTATPROPSETSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Ignora il numero di elementi specificato in *celt*. Restituisce \_ OK se il numero di elementi specificato viene ignorato, restituisce \_ false se vengono ignorati meno elementi di quelli richiesti. In tutti gli altri casi, restituisce l'errore appropriato.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Reset"></span><span id="ienumstatpropsetstg__reset"></span><span id="IENUMSTATPROPSETSTG__RESET"></span>[**IEnumSTATPROPSETSTG:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Imposta il cursore all'inizio dell'enumerazione. Se ha esito positivo, restituisce S \_ OK. in caso contrario, restituisce STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSETSTG__Clone"></span><span id="ienumstatpropsetstg__clone"></span><span id="IENUMSTATPROPSETSTG__CLONE"></span>[**IEnumSTATPROPSETSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dd>

Copia lo stato di enumerazione corrente dell'enumeratore.

</dd> </dl>

 

 