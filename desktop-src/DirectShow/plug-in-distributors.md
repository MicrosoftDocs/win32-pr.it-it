---
description: Distributori di plug-in
ms.assetid: 80ff713d-f704-40d3-9317-cbf33d932207
title: Distributori di plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7817e5e31b29444cc596b0be583be2198adc018
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303935"
---
# <a name="plug-in-distributors"></a>Distributori di plug-in

I distributori di plug-in (PID) rappresentano un modo per estendere la funzionalità di gestione del grafo dei filtri. Un server di distribuzione plug-in è un oggetto COM che viene aggregato da gestione grafo del filtro in fase di esecuzione. Le applicazioni ottengono l'accesso al PID tramite Filter Graph Manager.

Quando viene eseguita una query sul gestore del grafico di filtri per un'interfaccia non supportata, viene eseguita una ricerca nel registro di sistema di una chiave con il formato seguente:


```C++
HKEY_CLASSES_ROOT\Interface\IID\Distributor
```



`IID` stringa che contiene l'identificatore di interfaccia. Se la voce del registro di sistema esiste, il valore della voce definisce l'identificatore di classe (CLSID) di un PID che supporta l'interfaccia. Filter Graph Manager aggrega il PID e restituisce un puntatore a interfaccia, che funge quindi da **IUnknown** esterno per il PID. Quando l'applicazione chiama i metodi nell'interfaccia, li chiama effettivamente nel PID. Tuttavia, l'esistenza del PID è trasparente per l'applicazione.

Il termine *server di distribuzione* deriva dal fatto che un PID può eseguire query sul puntatore **IUnknown** esterno per le interfacce in gestione grafico dei filtri. Chiamando il metodo [**IFilterGraph:: EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) , il PID può enumerare i filtri nel grafico e distribuire le chiamate al metodo a tali filtri. In questo modo, un PID può fungere da singolo punto di controllo per l'applicazione per chiamare i metodi sui filtri.

Quando il gestore del grafico del filtro aggrega un PID, esegue una query sul PID per l'interfaccia [**IDistributorNotify**](/windows/desktop/api/Strmif/nn-strmif-idistributornotify) . Se il PID supporta questa interfaccia, il gestore del grafo del filtro lo utilizza per notificare al PID le modifiche apportate al grafo:

-   Quando il grafico di filtro passa tra gli Stati Run, Paused e Stopped, viene chiamato [**IDistributorNotify:: Run**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-run), [**IDistributorNotify::P ause**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-pause)o [**IDistributorNotify:: Stop**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-stop).
-   Quando viene impostato un clock di riferimento, il gestore del grafo dei filtri chiama [**IDistributorNotify:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-setsyncsource).
-   Quando si aggiungono o rimuovono i filtri o si modificano le connessioni pin, il gestore del grafo dei filtri chiama [**IDistributorNotify:: NotifyGraphChange**](/windows/desktop/api/Strmif/nf-strmif-idistributornotify-notifygraphchange).

Per implementare un PID personalizzato, creare un oggetto COM che supporta l'aggregazione. Deve supportare un'interfaccia che non è ancora supportata da gestione grafo del filtro. Facoltativamente, può supportare l'interfaccia **IDistributorNotify** .

Se il PID ottiene tutti i puntatori di interfaccia dal gestore del grafico dei filtri, dovrebbe rilasciarli immediatamente. In caso contrario, potrebbe creare un conteggio dei riferimenti circolari, che potrebbe impedire l'eliminazione definitiva del gestore del grafico del filtro. Il mantenimento di un conteggio dei riferimenti in gestione grafico dei filtri non è necessario in alcun caso, perché il gestore del grafico dei filtri controlla la durata del PID.

Poiché un PID è progettato specificamente per l'aggregazione da parte del gestore del grafo del filtro, è possibile applicare questa operazione nel metodo del costruttore del PID. Controllare se il puntatore **IUnknown** esterno è **null** e, in caso affermativo, restituire il codice di errore VFW \_ E \_ need \_ owner. Vedere [codici di errore e di esito positivo](error-and-success-codes.md). Per impedire ad altri oggetti di aggregare il PID, è inoltre possibile eseguire una query sul puntatore **IUnknown** esterno per l'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) . Restituisce un codice di errore se l'oggetto non espone **IGraphBuilder**.

 

 



