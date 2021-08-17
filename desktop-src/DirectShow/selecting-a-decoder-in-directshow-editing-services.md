---
description: Selezione di un decodificatore nei DirectShow di modifica
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Selezione di un decodificatore nei DirectShow di modifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcff63d44918a189f49e11527fe6fef35d108b7f20c1dadefa0a045e2c895b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341271"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>Selezione di un decodificatore nei DirectShow di modifica

\[Questa API non è supportata e potrebbe essere modificata o non disponibile in futuro.\]

Quando [DirectShow servizi](directshow-editing-services.md) di modifica (DES) esegue il rendering di un progetto di modifica video, il motore di rendering seleziona automaticamente i decodificatori necessari. Questa operazione può verificarsi [**all'interno del metodo IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) o in modo dinamico durante il rendering.

Un utente potrebbe installare diversi decodificatori in grado di decodificare un file specifico. Quando sono disponibili più decodificatori, DES usa l'algoritmo [Intelligent Connessione](intelligent-connect.md) per selezionare il decodificatore.

L'applicazione non può specificare direttamente quale decodificatore usare. Tuttavia, è possibile scegliere il decodificatore indirettamente tramite l'interfaccia di callback [**IAMGraphBuilderCallback.**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) Implementando questa interfaccia nell'applicazione, è possibile ricevere notifiche durante il processo di creazione del grafo e rifiutare determinati filtri dal grafo.

Per iniziare, implementare una classe che espone [**l'interfaccia IAMGraphBuilderCallback:**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback)


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



Creare quindi un'istanza di Filter Graph Manager e registrare la classe per ricevere le notifiche di callback:


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



Creare quindi il motore di rendering e chiamare il metodo [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) con un puntatore a Filter Graph Manager. In questo modo si garantisce che il motore di rendering non crei il proprio Gestore Graph Filtri, ma usi invece l'istanza configurata per i callback.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



Quando viene eseguito il rendering del progetto, il metodo [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) dell'applicazione viene chiamato immediatamente prima che Filter Graph Manager crei un nuovo filtro. Il **metodo SelectedFilter** riceve un puntatore a **un'interfaccia IMoniker** che rappresenta un moniker per il filtro. Esaminare il moniker e, se si decide di rifiutare il filtro, restituire un codice di errore dal **metodo SelectedFilter.**

La parte difficile è identificare i moniker che rappresentano i decodificatori e, in particolare, i moniker che rappresentano i decodificatori che si desidera rifiutare. Una soluzione è la seguente:

-   Prima di eseguire il rendering del progetto, usare il metodo [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) per creare un elenco di filtri registrati come accettando il tipo di input desiderato. Per i tipi di compressione video o audio, questo elenco deve essere mappato a un set di decodificatori.
-   Il **metodo EnumMatchingFilters** restituisce una raccolta di moniker. Per ogni moniker nella raccolta, ottenere la **proprietà DisplayName,** come descritto in [Using the Filter Mapper](using-the-filter-mapper.md).
-   Archiviare un elenco dei nomi visualizzati, ma omettere il nome visualizzato corrispondente al filtro da usare per la decodifica. I nomi visualizzati per i filtri software hanno il formato seguente:

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    dove

    ```C++
    CategoryGUID
    ```

    

    è il GUID della categoria di filtro e

    ```C++
    FilterCLSID
    ```

    

    è il CLSID del filtro. Per le DMO, il formato è lo stesso, ma cambiare `sw` in `dmo` .

    L'elenco contiene ora nomi visualizzati per ogni filtro che restituisce il tipo di supporto desiderato, ma non è il filtro preferito.

-   Nel metodo **SelectedFilter** ottenere la **proprietà DisplayName** nel moniker proposto e verificarlo rispetto all'elenco archiviato. Se il nome visualizzato corrisponde a una voce nell'elenco, rifiutare il filtro. In caso contrario, accettarlo restituindo S \_ OK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un Project](rendering-a-project.md)
</dt> </dl>

 

 



