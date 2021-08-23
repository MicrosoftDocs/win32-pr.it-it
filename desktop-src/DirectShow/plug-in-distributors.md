---
description: Server di distribuzione plug-in
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Server di distribuzione plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70d253066fdde4f082a964c56a221331cfd127c0984db2a7b1933a0bb352425
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583661"
---
# <a name="plug-in-distributors"></a>Server di distribuzione plug-in

I distributori di plug-in (PID) sono un modo per estendere la funzionalità di gestione dei grafi di filtro. Un server di distribuzione plug-in è un oggetto COM aggregato dal gestore del grafo dei filtri in fase di esecuzione. Le applicazioni ottengono l'accesso al PID tramite il gestore del grafico dei filtri.

Quando viene eseguita una query sul gestore del grafo del filtro per trovare un'interfaccia che non supporta, cerca nel Registro di sistema una chiave nel formato seguente:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` è una stringa contenente l'identificatore di interfaccia. Se la voce del Registro di sistema esiste, il valore della voce definisce l'identificatore di classe (CLSID) di un PID che supporta l'interfaccia. Il gestore del grafico dei filtri aggrega il PID e restituisce un puntatore a interfaccia, fungendo quindi da **IUnknown** esterno per il PID. Quando l'applicazione chiama metodi sull'interfaccia, li chiama effettivamente sul PID. Tuttavia, l'esistenza del PID è trasparente per l'applicazione.

Il termine *distributore* deriva dal fatto che un PID può eseguire una query sul puntatore **IUnknown** esterno per le interfacce nel gestore del grafico dei filtri. Chiamando il [**metodo IFilterGraph::EnumFilters,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) il PID può enumerare i filtri nel grafico e distribuire le chiamate al metodo a tali filtri. In questo modo, un PID può fungere da singolo punto di controllo per l'applicazione per chiamare metodi sui filtri.

Quando il gestore del grafo dei filtri aggrega un PID, esegue una query sul PID per [**l'interfaccia IDistributorNotify.**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) Se il PID supporta questa interfaccia, il gestore del grafo dei filtri la usa per notificare al PID le modifiche nel grafico:

-   Quando il grafico dei filtri passa tra gli stati di esecuzione, sospensione e arresto, chiama [**IDistributorNotify::Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)o [**IDistributorNotify::Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).
-   Quando viene impostato un clock di riferimento, il gestore del grafico dei filtri chiama [**IDistributorNotify::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).
-   Quando i filtri vengono aggiunti o rimossi o vengono modificate le connessioni pin, il gestore del grafo dei filtri chiama [**IDistributorNotify::NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).

Per implementare un PID personalizzato, creare un oggetto COM che supporti l'aggregazione. Deve supportare un'interfaccia che il gestore dei grafi di filtro non supporta già. Facoltativamente, può supportare **l'interfaccia IDistributorNotify.**

Se il PID ottiene puntatori a interfaccia dal gestore del grafico dei filtri, deve rilasciarli immediatamente. In caso contrario, potrebbe creare un conteggio dei riferimenti circolare, che potrebbe impedire l'eliminazione del gestore del grafo del filtro. In ogni caso, non è necessario mantenere un conteggio dei riferimenti nel gestore del grafo dei filtri, perché il gestore del grafo dei filtri controlla la durata del PID.

Poiché un PID è progettato specificamente per l'aggregazione da parte del gestore del grafo dei filtri, può essere necessario applicare questa impostazione nel metodo del costruttore del PID. Controllare se il puntatore **IUnknown** esterno è **NULL** e, in tal caso, restituire il codice di errore VFW \_ E NEED \_ \_ OWNER. Vedere Codici [di errore e di esito](error-and-success-codes.md)positivo. Inoltre, per impedire ad altri oggetti di aggregare il PID, è possibile eseguire una query sul puntatore **IUnknown** esterno per [**l'interfaccia IGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) Restituisce un codice di errore se l'oggetto non espone **IGraphBuilder.**

 

 



