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
# <a name="selecting-a-decoder-in-directshow-editing-services"></a><span data-ttu-id="c3ac6-103">Selezione di un decodificatore in servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="c3ac6-103">Selecting a Decoder in DirectShow Editing Services</span></span>

<span data-ttu-id="c3ac6-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="c3ac6-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="c3ac6-105">Quando [DirectShow editing Services](directshow-editing-services.md) (des) esegue il rendering di un progetto di modifica video, il motore di rendering seleziona automaticamente i decodificatori necessari.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-105">When [DirectShow Editing Services](directshow-editing-services.md) (DES) renders a video editing project, the Rendering Engine automatically selects the necessary decoders.</span></span> <span data-ttu-id="c3ac6-106">Questo problema può verificarsi all'interno del metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) o in modo dinamico durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-106">This may happen inside the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method, or else dynamically during rendering.</span></span>

<span data-ttu-id="c3ac6-107">Un utente potrebbe installare diversi decodificatori in grado di decodificare un determinato file.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-107">A user might install several decoders that are capable of decoding a particular file.</span></span> <span data-ttu-id="c3ac6-108">Quando sono disponibili più decodificatori, DES usa l'algoritmo di [connessione intelligente](intelligent-connect.md) per selezionare il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-108">When multiple decoders are available, DES uses the [Intelligent Connect](intelligent-connect.md) algorithm to select the decoder.</span></span>

<span data-ttu-id="c3ac6-109">L'applicazione non può specificare direttamente il decoder da usare.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-109">There is no way for the application to specify directly which decoder to use.</span></span> <span data-ttu-id="c3ac6-110">Tuttavia, è possibile scegliere il decodificatore indirettamente tramite l'interfaccia di callback [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) .</span><span class="sxs-lookup"><span data-stu-id="c3ac6-110">However, you can choose the decoder indirectly through the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) callback interface.</span></span> <span data-ttu-id="c3ac6-111">Implementando questa interfaccia nell'applicazione, è possibile ricevere notifiche durante il processo di compilazione del grafico e rifiutare determinati filtri dal grafico.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-111">By implementing this interface in your application, you can receive notifications during the graph-building process and reject certain filters from the graph.</span></span>

<span data-ttu-id="c3ac6-112">Iniziare implementando una classe che espone l'interfaccia [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :</span><span class="sxs-lookup"><span data-stu-id="c3ac6-112">Start by implementing a class that exposes the [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) interface:</span></span>


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



<span data-ttu-id="c3ac6-113">Creare quindi un'istanza di Filter Graph Manager e registrare la classe per ricevere le notifiche di callback:</span><span class="sxs-lookup"><span data-stu-id="c3ac6-113">Then create an instance of the Filter Graph Manager and register your class to receive callback notifications:</span></span>


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



<span data-ttu-id="c3ac6-114">Successivamente, creare il motore di rendering e chiamare il metodo [**IRenderEngine:: SetFilterGraph**](irenderengine-setfiltergraph.md) con un puntatore al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-114">Next, create the Render Engine and call the [**IRenderEngine::SetFilterGraph**](irenderengine-setfiltergraph.md) method with a pointer to the Filter Graph Manager.</span></span> <span data-ttu-id="c3ac6-115">In questo modo, il motore di rendering non creerà il proprio gestore del grafo dei filtri, ma utilizzerà invece l'istanza di configurata per i callback.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-115">This ensures that the Render Engine does not create its own Filter Graph Manager, but instead uses the instance that you have configured for callbacks.</span></span>


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



<span data-ttu-id="c3ac6-116">Quando viene eseguito il rendering del progetto, il metodo [**IAMGraphBuilderCallback:: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) dell'applicazione viene chiamato immediatamente prima della creazione di un nuovo filtro da parte del gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-116">When the project is rendered, the application's [**IAMGraphBuilderCallback::SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) method is called immediately before the Filter Graph Manager creates a new filter.</span></span> <span data-ttu-id="c3ac6-117">Il metodo **SelectedFilter** riceve un puntatore a un'interfaccia **IMoniker** che rappresenta un moniker per il filtro.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-117">The **SelectedFilter** method receives a pointer to an **IMoniker** interface that represents a moniker for the filter.</span></span> <span data-ttu-id="c3ac6-118">Esaminare il moniker e, se si decide di rifiutare il filtro, restituire un codice di errore dal metodo **SelectedFilter** .</span><span class="sxs-lookup"><span data-stu-id="c3ac6-118">Examine the moniker, and if you decide to reject the filter, return a failure code from the **SelectedFilter** method.</span></span>

<span data-ttu-id="c3ac6-119">La parte difficile consiste nell'identificare quali moniker rappresentano i decodificatori, e in particolare quali moniker rappresentano i decodificatori che si desidera rifiutare.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-119">The difficult part is to identify which monikers represent decoders — and in particular, which monikers represent decoders that you want to reject.</span></span> <span data-ttu-id="c3ac6-120">Una soluzione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="c3ac6-120">One solution is the following:</span></span>

-   <span data-ttu-id="c3ac6-121">Prima di eseguire il rendering del progetto, usare il metodo [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) per creare un elenco di filtri registrati come accettando il tipo di input desiderato.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-121">Before rendering the project, use the [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method to create a list of filters that are registered as accepting the desired input type.</span></span> <span data-ttu-id="c3ac6-122">Per i tipi di compressione video o audio, questo elenco deve essere mappato a un set di decodificatori.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-122">For video or audio compression types, this list should map to a set of decoders.</span></span>
-   <span data-ttu-id="c3ac6-123">Il metodo **EnumMatchingFilters** restituisce una raccolta di moniker.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-123">The **EnumMatchingFilters** method returns a collection of monikers.</span></span> <span data-ttu-id="c3ac6-124">Per ogni moniker della raccolta, ottenere la proprietà **DisplayName** , come descritto in [uso del mapper dei filtri](using-the-filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="c3ac6-124">For each moniker in the collection, get the **DisplayName** property, as described in [Using the Filter Mapper](using-the-filter-mapper.md).</span></span>
-   <span data-ttu-id="c3ac6-125">Archiviare un elenco di nomi visualizzati, ma omettere il nome visualizzato che corrisponde al filtro che si desidera utilizzare per la decodifica.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-125">Store a list of the display names, but omit the display name that matches the filter you want to use for decoding.</span></span> <span data-ttu-id="c3ac6-126">I nomi visualizzati per i filtri software hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="c3ac6-126">Display names for software filters have the following form:</span></span>

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    <span data-ttu-id="c3ac6-127">dove</span><span class="sxs-lookup"><span data-stu-id="c3ac6-127">where</span></span>

    ```C++
    CategoryGUID
    ```

    

    <span data-ttu-id="c3ac6-128">è il GUID della categoria di filtro e</span><span class="sxs-lookup"><span data-stu-id="c3ac6-128">is the GUID of the filter category, and</span></span>

    ```C++
    FilterCLSID
    ```

    

    <span data-ttu-id="c3ac6-129">è il CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-129">is the filter's CLSID.</span></span> <span data-ttu-id="c3ac6-130">Per DMOs, il formato è lo stesso, ma viene modificato `sw` in `dmo` .</span><span class="sxs-lookup"><span data-stu-id="c3ac6-130">For DMOs, the format is the same, but change `sw` to `dmo`.</span></span>

    <span data-ttu-id="c3ac6-131">L'elenco contiene ora i nomi visualizzati per ogni filtro che restituisce il tipo di supporto desiderato, ma non è il filtro preferito.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-131">The list now contains display names for every filter that outputs the desired media type but is not your preferred filter.</span></span>

-   <span data-ttu-id="c3ac6-132">Nel metodo **SelectedFilter** recuperare la proprietà **DisplayName** sul moniker proposto e controllarla rispetto all'elenco archiviato.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-132">In the **SelectedFilter** method, get the **DisplayName** property on the proposed moniker and check it against the stored list.</span></span> <span data-ttu-id="c3ac6-133">Se il nome visualizzato corrisponde a una voce dell'elenco, rifiutare tale filtro.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-133">If the display name matches an entry in the list, reject that filter.</span></span> <span data-ttu-id="c3ac6-134">In caso contrario, accettarlo restituendo S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3ac6-134">Otherwise, accept it by returning S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3ac6-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c3ac6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3ac6-136">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="c3ac6-136">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



