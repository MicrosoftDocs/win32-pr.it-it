---
description: Creazione di nodi di output
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Creazione di nodi di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4388258c82c12f8473dc07df83ba3b9467eed7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878458"
---
# <a name="creating-output-nodes"></a><span data-ttu-id="52beb-103">Creazione di nodi di output</span><span class="sxs-lookup"><span data-stu-id="52beb-103">Creating Output Nodes</span></span>

<span data-ttu-id="52beb-104">Un nodo di output rappresenta un sink del flusso in un sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="52beb-104">An output node represents a stream sink on a media sink.</span></span> <span data-ttu-id="52beb-105">Esistono due modi per inizializzare un nodo di output:</span><span class="sxs-lookup"><span data-stu-id="52beb-105">There are two ways to initialize an output node:</span></span>

-   <span data-ttu-id="52beb-106">Da un puntatore al sink del flusso.</span><span class="sxs-lookup"><span data-stu-id="52beb-106">From a pointer to the stream sink.</span></span>
-   <span data-ttu-id="52beb-107">Da un puntatore a un oggetto di attivazione per il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="52beb-107">From a pointer to an activation object for the media sink.</span></span>

<span data-ttu-id="52beb-108">Se si intende caricare la topologia all'interno del percorso multimediale protetto (PMP), è necessario usare un oggetto attivazione, in modo che il sink multimediale possa essere creato all'interno del processo protetto.</span><span class="sxs-lookup"><span data-stu-id="52beb-108">If you are going to load the topology inside the protected media path (PMP), you must use an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="52beb-109">Il primo approccio (usando un puntatore al sink di flusso) non funziona con il PMP.</span><span class="sxs-lookup"><span data-stu-id="52beb-109">The first approach (using a pointer to the stream sink) does not work with the PMP.</span></span>

## <a name="creating-an-output-node-from-a-stream-sink"></a><span data-ttu-id="52beb-110">Creazione di un nodo di output da un sink di flusso</span><span class="sxs-lookup"><span data-stu-id="52beb-110">Creating an Output Node from a Stream Sink</span></span>

<span data-ttu-id="52beb-111">Per creare un nodo di output da un sink di flusso, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="52beb-111">To create an output node from a stream sink, do the following:</span></span>

1.  <span data-ttu-id="52beb-112">Creare un'istanza del sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="52beb-112">Create an instance of the media sink.</span></span>
2.  <span data-ttu-id="52beb-113">Usare l'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del sink multimediale per ottenere un puntatore al sink di flusso desiderato.</span><span class="sxs-lookup"><span data-stu-id="52beb-113">Use the media sink's [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) interface to get a pointer to the desired stream sink.</span></span> <span data-ttu-id="52beb-114">(L'interfaccia **IMFMediaSink** dispone di diversi metodi che restituiscono puntatori a un sink di flusso).</span><span class="sxs-lookup"><span data-stu-id="52beb-114">(The **IMFMediaSink** interface has several methods that return pointers to a stream sink.)</span></span>
3.  <span data-ttu-id="52beb-115">Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ output \_ della topologia MF** per creare il nodo di output.</span><span class="sxs-lookup"><span data-stu-id="52beb-115">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
4.  <span data-ttu-id="52beb-116">Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare un puntatore all'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="52beb-116">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in a pointer to the stream sink's [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface.</span></span>
5.  <span data-ttu-id="52beb-117">Impostare [**MF \_ TOPONODE \_ noshutdown \_ sull'attributo \_ Remove su**](mf-toponode-noshutdown-on-remove-attribute.md) **false** (facoltativo ma consigliato).</span><span class="sxs-lookup"><span data-stu-id="52beb-117">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **FALSE** (optional but recommended).</span></span>
6.  <span data-ttu-id="52beb-118">Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.</span><span class="sxs-lookup"><span data-stu-id="52beb-118">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="52beb-119">Nell'esempio seguente viene creato e inizializzato un nodo di output da un sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="52beb-119">The following example creates and initializes an output node from a stream sink.</span></span>


```C++
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFStreamSink *pStreamSink, // Stream sink.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    IMFTopologyNode *pNode = NULL;
    HRESULT hr = S_OK;
    
    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pStreamSink);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, TRUE);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    if (pNode)
    {
        pNode->Release();
    }
    return hr;
}
```



<span data-ttu-id="52beb-120">Quando l'applicazione arresta la sessione multimediale, la sessione multimediale arresta automaticamente il sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="52beb-120">When the application shuts down the Media Session, the Media Session automatically shuts down the media sink.</span></span> <span data-ttu-id="52beb-121">Non è pertanto possibile riutilizzare il sink multimediale con un'altra istanza della sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="52beb-121">Therefore, you cannot re-use the media sink with another instance of the Media Session.</span></span>

## <a name="creating-an-output-node-from-an-activation-object"></a><span data-ttu-id="52beb-122">Creazione di un nodo di output da un oggetto Activation</span><span class="sxs-lookup"><span data-stu-id="52beb-122">Creating an Output Node from an Activation Object</span></span>

<span data-ttu-id="52beb-123">Qualsiasi sink multimediale attendibile deve fornire un oggetto attivazione, in modo che il sink multimediale possa essere creato all'interno del processo protetto.</span><span class="sxs-lookup"><span data-stu-id="52beb-123">Any trusted media sink must provide an activation object, so that the media sink can be created inside the protected process.</span></span> <span data-ttu-id="52beb-124">Per altre informazioni, vedere [oggetti Activation](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="52beb-124">For more information, see [Activation Objects](activation-objects.md).</span></span> <span data-ttu-id="52beb-125">La funzione specifica che crea l'oggetto attivazione dipenderà dal sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="52beb-125">The particular function that creates the activation object will depend on the media sink.</span></span>

<span data-ttu-id="52beb-126">Per creare un nodo di output da un oggetto Activation, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="52beb-126">To create an output node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="52beb-127">Creare l'oggetto attivazione e ottenere un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) dell'oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="52beb-127">Create the activation object and get a pointer to the activation object's [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="52beb-128">Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ output \_ della topologia MF** per creare il nodo di output.</span><span class="sxs-lookup"><span data-stu-id="52beb-128">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_OUTPUT\_NODE** flag to create the output node.</span></span>
3.  <span data-ttu-id="52beb-129">Facoltativamente, impostare l'attributo [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) nel nodo per specificare l'identificatore di flusso del sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="52beb-129">Optionally, set the [**MF\_TOPONODE\_STREAMID**](mf-toponode-streamid-attribute.md) attribute on the node to specify the stream identifier of the stream sink.</span></span> <span data-ttu-id="52beb-130">Se si omette questo attributo, il valore predefinito del nodo sarà Using Stream sink 0.</span><span class="sxs-lookup"><span data-stu-id="52beb-130">If you omit this attribute, the node defaults to using stream sink 0.</span></span>
4.  <span data-ttu-id="52beb-131">Impostare [**MF \_ TOPONODE \_ noshutdown \_ sull'attributo \_ Remove su**](mf-toponode-noshutdown-on-remove-attribute.md) **true** (facoltativo ma consigliato).</span><span class="sxs-lookup"><span data-stu-id="52beb-131">Set the [**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) attribute to **TRUE** (optional but recommended).</span></span>
5.  <span data-ttu-id="52beb-132">Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="52beb-132">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
6.  <span data-ttu-id="52beb-133">Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.</span><span class="sxs-lookup"><span data-stu-id="52beb-133">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="52beb-134">Nell'esempio seguente viene creato e inizializzato un nodo di output da un oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="52beb-134">The following example creates and initializes an output node from an activation object.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="52beb-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52beb-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52beb-136">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="52beb-136">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="52beb-137">Creazione di topologie</span><span class="sxs-lookup"><span data-stu-id="52beb-137">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="52beb-138">Sink di supporti</span><span class="sxs-lookup"><span data-stu-id="52beb-138">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="52beb-139">Topologie</span><span class="sxs-lookup"><span data-stu-id="52beb-139">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



