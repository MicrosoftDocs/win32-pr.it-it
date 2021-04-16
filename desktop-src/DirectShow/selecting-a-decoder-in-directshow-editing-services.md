---
description: Selezione di un decodificatore in servizi di modifica DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Selezione di un decodificatore in servizi di modifica DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481509"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>Selezione di un decodificatore in servizi di modifica DirectShow

\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]

Quando [DirectShow editing Services](directshow-editing-services.md) (des) esegue il rendering di un progetto di modifica video, il motore di rendering seleziona automaticamente i decodificatori necessari. Questo problema può verificarsi all'interno del metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) o in modo dinamico durante il rendering.

Un utente potrebbe installare diversi decodificatori in grado di decodificare un determinato file. Quando sono disponibili più decodificatori, DES usa l'algoritmo di [connessione intelligente](intelligent-connect.md) per selezionare il decodificatore.

L'applicazione non può specificare direttamente il decoder da usare. Tuttavia, è possibile scegliere il decodificatore indirettamente tramite l'interfaccia di callback [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) . Implementando questa interfaccia nell'applicazione, è possibile ricevere notifiche durante il processo di compilazione del grafico e rifiutare determinati filtri dal grafico.

Iniziare implementando una classe che espone l'interfaccia [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :


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



Successivamente, creare il motore di rendering e chiamare il metodo [**IRenderEngine:: SetFilterGraph**](irenderengine-setfiltergraph.md) con un puntatore al gestore del grafico dei filtri. In questo modo, il motore di rendering non creerà il proprio gestore del grafo dei filtri, ma utilizzerà invece l'istanza di configurata per i callback.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



Quando viene eseguito il rendering del progetto, il metodo [**IAMGraphBuilderCallback:: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) dell'applicazione viene chiamato immediatamente prima della creazione di un nuovo filtro da parte del gestore del grafico dei filtri. Il metodo **SelectedFilter** riceve un puntatore a un'interfaccia **IMoniker** che rappresenta un moniker per il filtro. Esaminare il moniker e, se si decide di rifiutare il filtro, restituire un codice di errore dal metodo **SelectedFilter** .

La parte difficile consiste nell'identificare quali moniker rappresentano i decodificatori, e in particolare quali moniker rappresentano i decodificatori che si desidera rifiutare. Una soluzione è la seguente:

-   Prima di eseguire il rendering del progetto, usare il metodo [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) per creare un elenco di filtri registrati come accettando il tipo di input desiderato. Per i tipi di compressione video o audio, questo elenco deve essere mappato a un set di decodificatori.
-   Il metodo **EnumMatchingFilters** restituisce una raccolta di moniker. Per ogni moniker della raccolta, ottenere la proprietà **DisplayName** , come descritto in [uso del mapper dei filtri](using-the-filter-mapper.md).
-   Archiviare un elenco di nomi visualizzati, ma omettere il nome visualizzato che corrisponde al filtro che si desidera utilizzare per la decodifica. I nomi visualizzati per i filtri software hanno il formato seguente:

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

    

    è il CLSID del filtro. Per DMOs, il formato è lo stesso, ma viene modificato `sw` in `dmo` .

    L'elenco contiene ora i nomi visualizzati per ogni filtro che restituisce il tipo di supporto desiderato, ma non è il filtro preferito.

-   Nel metodo **SelectedFilter** recuperare la proprietà **DisplayName** sul moniker proposto e controllarla rispetto all'elenco archiviato. Se il nome visualizzato corrisponde a una voce dell'elenco, rifiutare tale filtro. In caso contrario, accettarlo restituendo S \_ OK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> </dl>

 

 



