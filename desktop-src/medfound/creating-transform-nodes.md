---
description: Creazione di nodi di trasformazione
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Creazione di nodi di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524610"
---
# <a name="creating-transform-nodes"></a><span data-ttu-id="c4279-103">Creazione di nodi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="c4279-103">Creating Transform Nodes</span></span>

<span data-ttu-id="c4279-104">Un nodo Transform rappresenta una trasformazione Media Foundation (MFT), ad esempio un codificatore o un codificatore.</span><span class="sxs-lookup"><span data-stu-id="c4279-104">A transform node represents a Media Foundation transform (MFT), such as a decoder or encoder.</span></span> <span data-ttu-id="c4279-105">Esistono diversi modi per inizializzare un nodo di trasformazione:</span><span class="sxs-lookup"><span data-stu-id="c4279-105">There are several different ways to initialize a transform node:</span></span>

-   <span data-ttu-id="c4279-106">Da un puntatore a MFT.</span><span class="sxs-lookup"><span data-stu-id="c4279-106">From a pointer to the MFT.</span></span>
-   <span data-ttu-id="c4279-107">Da un CLSID per il MFT.</span><span class="sxs-lookup"><span data-stu-id="c4279-107">From a CLSID for the MFT.</span></span>
-   <span data-ttu-id="c4279-108">Da un puntatore a un oggetto di attivazione per il MFT.</span><span class="sxs-lookup"><span data-stu-id="c4279-108">From a pointer to an activation object for the MFT.</span></span>

<span data-ttu-id="c4279-109">Se si intende caricare la topologia all'interno del percorso multimediale protetto (PMP), è necessario usare il CLSID o un oggetto di attivazione, in modo che il file MFT possa essere creato all'interno del processo protetto.</span><span class="sxs-lookup"><span data-stu-id="c4279-109">If you are going to load the topology inside the protected media path (PMP), you must use either the CLSID or an activation object, so that the MFT can be created inside the protected process.</span></span> <span data-ttu-id="c4279-110">Il primo approccio (usando un puntatore a MFT) non funziona con il PMP.</span><span class="sxs-lookup"><span data-stu-id="c4279-110">The first approach (using a pointer to the MFT) does not work with the PMP.</span></span>

## <a name="creating-a-transform-node-from-an-mft"></a><span data-ttu-id="c4279-111">Creazione di un nodo Transform da un MFT</span><span class="sxs-lookup"><span data-stu-id="c4279-111">Creating a Transform Node from an MFT</span></span>

<span data-ttu-id="c4279-112">Per creare un nodo di trasformazione da un MFT, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="c4279-112">To create a transform node from an MFT, do the following:</span></span>

1.  <span data-ttu-id="c4279-113">Creare un'istanza di MFT e ottenere un puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del MFT.</span><span class="sxs-lookup"><span data-stu-id="c4279-113">Create an instance of the MFT and get a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface of the MFT.</span></span>
2.  <span data-ttu-id="c4279-114">Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ trasformazione \_ della topologia MF** per creare il nodo Transform.</span><span class="sxs-lookup"><span data-stu-id="c4279-114">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="c4279-115">Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il puntatore [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="c4279-115">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer.</span></span>
4.  <span data-ttu-id="c4279-116">Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.</span><span class="sxs-lookup"><span data-stu-id="c4279-116">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="c4279-117">Nell'esempio seguente viene creato e inizializzato un nodo Transform da un MFT.</span><span class="sxs-lookup"><span data-stu-id="c4279-117">The following example creates and initializes a transform node from an MFT.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a><span data-ttu-id="c4279-118">Creazione di un nodo Transform da un CLSID</span><span class="sxs-lookup"><span data-stu-id="c4279-118">Creating a Transform Node from a CLSID</span></span>

<span data-ttu-id="c4279-119">Per creare un nodo di trasformazione da un CLSID, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c4279-119">To create a transform node from a CLSID, do the following:</span></span>

1.  <span data-ttu-id="c4279-120">Trovare il CLSID del MFT.</span><span class="sxs-lookup"><span data-stu-id="c4279-120">Find the CLSID of the MFT.</span></span> <span data-ttu-id="c4279-121">È possibile usare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) per trovare i CLSID di MFTS per categoria, ad esempio decodificatori o codificatori.</span><span class="sxs-lookup"><span data-stu-id="c4279-121">You can use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function to find the CLSIDs of MFTs by category, such as decoders or encoders.</span></span> <span data-ttu-id="c4279-122">È anche possibile che si conosca il CLSID di un particolare MFT che si vuole usare (ad esempio se è stata implementata una MFT personalizzata).</span><span class="sxs-lookup"><span data-stu-id="c4279-122">You might also know the CLSID of a particular MFT that you want to use (for example, if you implemented your own custom MFT).</span></span>
2.  <span data-ttu-id="c4279-123">Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ trasformazione \_ della topologia MF** per creare il nodo Transform.</span><span class="sxs-lookup"><span data-stu-id="c4279-123">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="c4279-124">Impostare l'attributo **MF \_ TOPONODE \_ Transform \_ ObjectID** nel nodo.</span><span class="sxs-lookup"><span data-stu-id="c4279-124">Set the **MF\_TOPONODE\_TRANSFORM\_OBJECTID** attribute on the node.</span></span> <span data-ttu-id="c4279-125">Il valore dell'attributo è il CLSID.</span><span class="sxs-lookup"><span data-stu-id="c4279-125">The attribute value is the CLSID.</span></span>
4.  <span data-ttu-id="c4279-126">Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.</span><span class="sxs-lookup"><span data-stu-id="c4279-126">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="c4279-127">Nell'esempio seguente viene creato e inizializzato un nodo Transform da un CLSID.</span><span class="sxs-lookup"><span data-stu-id="c4279-127">The following example creates and initializes a transform node from a CLSID.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a><span data-ttu-id="c4279-128">Creazione di un nodo Transform da un oggetto Activation</span><span class="sxs-lookup"><span data-stu-id="c4279-128">Creating a Transform Node from an Activation Object</span></span>

<span data-ttu-id="c4279-129">Alcuni MFTs forniscono oggetti attivazione.</span><span class="sxs-lookup"><span data-stu-id="c4279-129">Some MFTs provide activation objects.</span></span> <span data-ttu-id="c4279-130">Ad esempio, la funzione [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) restituisce un oggetto Activation per il codificatore Windows Media Audio (WMA).</span><span class="sxs-lookup"><span data-stu-id="c4279-130">For example, the [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) function returns an activation object for the Windows Media Audio (WMA) encoder.</span></span> <span data-ttu-id="c4279-131">La funzione Exact dipende dalla MFT.</span><span class="sxs-lookup"><span data-stu-id="c4279-131">The exact function depends on the MFT.</span></span> <span data-ttu-id="c4279-132">Non ogni MFT fornisce un oggetto attivazione.</span><span class="sxs-lookup"><span data-stu-id="c4279-132">Not every MFT provides an activation object.</span></span> <span data-ttu-id="c4279-133">Per altre informazioni, vedere [oggetti Activation](activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c4279-133">For more information, see [Activation Objects](activation-objects.md).</span></span>

<span data-ttu-id="c4279-134">È anche possibile ottenere un oggetto di attivazione MFT chiamando la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="c4279-134">You can also get an MFT activation object by calling the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="c4279-135">Per creare un nodo Transform da un oggetto Activation, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="c4279-135">To create a transform node from an activation object, do the following:</span></span>

1.  <span data-ttu-id="c4279-136">Creare l'oggetto attivazione e ottenere un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) dell'oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="c4279-136">Create the activation object and get a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface of the activation object.</span></span>
2.  <span data-ttu-id="c4279-137">Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ trasformazione \_ della topologia MF** per creare il nodo Transform.</span><span class="sxs-lookup"><span data-stu-id="c4279-137">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_TRANSFORM\_NODE** flag to create the transform node.</span></span>
3.  <span data-ttu-id="c4279-138">Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="c4279-138">Call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) and pass in the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer.</span></span>
4.  <span data-ttu-id="c4279-139">Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.</span><span class="sxs-lookup"><span data-stu-id="c4279-139">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="c4279-140">Nell'esempio seguente viene creato e inizializzato un nodo Transform da un oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="c4279-140">The following example creates and initializes a transform node from an activation object.</span></span>


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c4279-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4279-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4279-142">Creazione di topologie</span><span class="sxs-lookup"><span data-stu-id="c4279-142">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="c4279-143">Topologie</span><span class="sxs-lookup"><span data-stu-id="c4279-143">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="c4279-144">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c4279-144">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



