---
description: Informazioni sul generatore di grafici di acquisizione
ms.assetid: 9399a06e-7305-41e8-aefe-3d158052a8ed
title: Informazioni sul generatore di grafici di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae321665e0eae65a1d464bf87a12ac33e935d7ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965795"
---
# <a name="about-the-capture-graph-builder"></a><span data-ttu-id="68eb2-103">Informazioni sul generatore di grafici di acquisizione</span><span class="sxs-lookup"><span data-stu-id="68eb2-103">About the Capture Graph Builder</span></span>

<span data-ttu-id="68eb2-104">Un grafico di filtro che esegue l'acquisizione video o audio è denominato *grafico di acquisizione*.</span><span class="sxs-lookup"><span data-stu-id="68eb2-104">A filter graph that performs video or audio capture is called a *capture graph*.</span></span> <span data-ttu-id="68eb2-105">I grafici di acquisizione sono spesso più complicati dei grafici per la riproduzione di file.</span><span class="sxs-lookup"><span data-stu-id="68eb2-105">Capture graphs are often more complicated than file playback graphs.</span></span> <span data-ttu-id="68eb2-106">Per semplificare la creazione di grafici di acquisizione da parte delle applicazioni, DirectShow fornisce un oggetto helper denominato generatore grafico di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="68eb2-106">To make it easier for applications to build capture graphs, DirectShow provides a helper object called the Capture Graph Builder.</span></span> <span data-ttu-id="68eb2-107">Il generatore di grafici di acquisizione espone l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) , che contiene i metodi per la compilazione e il controllo di un grafico di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="68eb2-107">The Capture Graph Builder exposes the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, which contains methods for building and controlling a capture graph.</span></span> <span data-ttu-id="68eb2-108">Il diagramma seguente illustra il generatore Graph di acquisizione e l'interfaccia **ICaptureGraphBuilder2** .</span><span class="sxs-lookup"><span data-stu-id="68eb2-108">The following diagram illustrates the Capture Graph Builder and the **ICaptureGraphBuilder2** interface.</span></span>

![uso del generatore di grafici di acquisizione](images/cgb01.png)

<span data-ttu-id="68eb2-110">Per iniziare, chiamare CoCreateInstance per creare nuove istanze del generatore del grafico di acquisizione e del gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="68eb2-110">Start by calling CoCreateInstance to create new instances of the Capture Graph Builder and the Filter Graph Manager.</span></span> <span data-ttu-id="68eb2-111">Inizializzare quindi il generatore Graph di acquisizione chiamando [**ICaptureGraphBuilder2:: SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) con un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="68eb2-111">Then initialize the Capture Graph Builder by calling [**ICaptureGraphBuilder2::SetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setfiltergraph) with a pointer to the Filter Graph Manager's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="68eb2-112">La figura seguente illustra questo processo.</span><span class="sxs-lookup"><span data-stu-id="68eb2-112">The following diagram illustrates this process.</span></span>

![inizializzazione del generatore di grafici di acquisizione](images/cgb03.png)

<span data-ttu-id="68eb2-114">Il codice seguente illustra una funzione helper per eseguire questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="68eb2-114">The following code shows a helper function to perform these steps:</span></span>


```C++
HRESULT InitCaptureGraphBuilder(
  IGraphBuilder **ppGraph,  // Receives the pointer.
  ICaptureGraphBuilder2 **ppBuild  // Receives the pointer.
)
{
    if (!ppGraph || !ppBuild)
    {
        return E_POINTER;
    }
    IGraphBuilder *pGraph = NULL;
    ICaptureGraphBuilder2 *pBuild = NULL;

    // Create the Capture Graph Builder.
    HRESULT hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICaptureGraphBuilder2, (void**)&pBuild );
    if (SUCCEEDED(hr))
    {
        // Create the Filter Graph Manager.
        hr = CoCreateInstance(CLSID_FilterGraph, 0, CLSCTX_INPROC_SERVER,
            IID_IGraphBuilder, (void**)&pGraph);
        if (SUCCEEDED(hr))
        {
            // Initialize the Capture Graph Builder.
            pBuild->SetFiltergraph(pGraph);

            // Return both interface pointers to the caller.
            *ppBuild = pBuild;
            *ppGraph = pGraph; // The caller must release both interfaces.
            return S_OK;
        }
        else
        {
            pBuild->Release();
        }
    }
    return hr; // Failed
}
```



<span data-ttu-id="68eb2-115">In questa sezione sull'acquisizione video si presuppone che si stia usando il generatore del grafico di acquisizione per creare il grafico di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="68eb2-115">Throughout this section on video capture, it is assumed that you are using the Capture Graph Builder to create the capture graph.</span></span> <span data-ttu-id="68eb2-116">Tuttavia, è possibile compilare i grafici di acquisizione interamente usando i metodi IGraphBuilder.</span><span class="sxs-lookup"><span data-stu-id="68eb2-116">However, it is possible to build capture graphs entirely by using IGraphBuilder methods.</span></span> <span data-ttu-id="68eb2-117">Questo argomento è tuttavia considerato un argomento avanzato e i metodi di acquisizione del generatore di grafici sono preferiti.</span><span class="sxs-lookup"><span data-stu-id="68eb2-117">This is considered an advanced topic, however, and the Capture Graph Builder methods are preferred.</span></span> <span data-ttu-id="68eb2-118">Per altre informazioni, vedere [argomenti di acquisizione avanzati](advanced-capture-topics.md).</span><span class="sxs-lookup"><span data-stu-id="68eb2-118">For more information, see [Advanced Capture Topics](advanced-capture-topics.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68eb2-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68eb2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68eb2-120">Informazioni su acquisizione video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="68eb2-120">About Video Capture in DirectShow</span></span>](about-video-capture-in-directshow.md)
</dt> </dl>

 

 



