---
title: Implementazione di IEnumSTATPROPSTG-Compound file
description: L'implementazione del file composto dell'interfaccia IEnumSTATPROPSTG viene utilizzata per enumerare le proprietà, ottenendo le strutture Campo STATPROPSTG, che contengono dati statistici sulle proprietà.
ms.assetid: 8fa536f4-cce6-47e4-a860-2f43e48fa469
keywords:
- IEnumSTATPROPSTG Strctd STG, implementazione del file composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbffce14016efdb4e2a77d60096b6776e6c2189
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963357"
---
# <a name="ienumstatpropstg-compound-file-implementation"></a>Implementazione di IEnumSTATPROPSTG-Compound file

L'implementazione del file composto dell'interfaccia [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) viene utilizzata per enumerare le proprietà, ottenendo le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) , che contengono dati statistici sulle proprietà. L'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) gestisce i dati statistici ed è associata a un oggetto di archiviazione file composto corrente.

Il costruttore nell'implementazione COM di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) crea una classe che legge l'intero set di proprietà e crea una matrice statica che può essere condivisa quando viene chiamato **IEnumSTATPROPSTG:: Clone** .

## <a name="when-to-use"></a>Utilizzo

Chiamare l'implementazione del file composto di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) per enumerare le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) che contengono dati sulle proprietà all'interno del set di proprietà corrente. Quando si usa l'implementazione del file composto delle interfacce di archiviazione delle proprietà, chiamare [**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) per restituire un puntatore a **IEnumSTATPROPSTG** per gestire l'oggetto di archiviazione della proprietà e gli elementi al suo interno.

## <a name="remarks"></a>Commenti

<dl> <dt>

<span id="IEnumSTATPROPSTG__Next"></span><span id="ienumstatpropstg__next"></span><span id="IENUMSTATPROPSTG__NEXT"></span>[**IEnumSTATPROPSTG:: Next**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Ottiene le successive strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) (il numero viene specificato dal parametro *celt* ). Restituisce \_ OK se ha esito positivo.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Skip"></span><span id="ienumstatpropstg__skip"></span><span id="IENUMSTATPROPSTG__SKIP"></span>[**IEnumSTATPROPSTG:: Skip**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Ignora il numero di elementi specificato in *celt*. L'elemento successivo da enumerare tramite una chiamata a Next diventa quindi l'elemento dopo gli elementi ignorati. Restituisce \_ OK se gli elementi *celt* sono stati ignorati. restituisce \_ false se il numero di elementi *celt* è stato ignorato.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Reset"></span><span id="ienumstatpropstg__reset"></span><span id="IENUMSTATPROPSTG__RESET"></span>[**IEnumSTATPROPSTG:: Reset**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Imposta il cursore all'inizio dell'enumerazione. Se ha esito positivo, restituisce S \_ OK. in caso contrario, restituisce STG \_ E \_ INVALIDHANDLE.

</dd> <dt>

<span id="IEnumSTATPROPSTG__Clone"></span><span id="ienumstatpropstg__clone"></span><span id="IENUMSTATPROPSTG__CLONE"></span>[**IEnumSTATPROPSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dd>

Usa il costruttore per [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) per creare una copia della matrice. Poiché la classe che costruisce la matrice statica contiene effettivamente l'oggetto, questa funzione aggiunge principalmente al conteggio dei riferimenti.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg)
</dt> <dt>

[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> </dl>

 

 