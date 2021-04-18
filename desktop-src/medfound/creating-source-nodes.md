---
description: Creazione di nodi di origine
ms.assetid: 44c26bcd-04a9-48c3-b536-25c2b18c34c1
title: Creazione di nodi di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b1e882dd6f8e9345244b56eace332c2fad4bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305465"
---
# <a name="creating-source-nodes"></a><span data-ttu-id="15843-103">Creazione di nodi di origine</span><span class="sxs-lookup"><span data-stu-id="15843-103">Creating Source Nodes</span></span>

<span data-ttu-id="15843-104">Un nodo di origine rappresenta un flusso da un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="15843-104">A source node represents one stream from a media source.</span></span> <span data-ttu-id="15843-105">Il nodo di origine deve contenere puntatori all'origine multimediale, al descrittore di presentazione e al descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="15843-105">The source node must contain pointers to the media source, the presentation descriptor, and the stream descriptor.</span></span>

<span data-ttu-id="15843-106">Per aggiungere un nodo di origine a una topologia, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="15843-106">To add a source node to a topology, do the following:</span></span>

1.  <span data-ttu-id="15843-107">Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ \_ \_ nodo SOURCESTREAM della topologia MF** per creare il nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="15843-107">Call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) with the **MF\_TOPOLOGY\_SOURCESTREAM\_NODE** flag to create the source node.</span></span>
2.  <span data-ttu-id="15843-108">Impostare l'attributo di [**\_ \_ origine MF TOPONODE**](mf-toponode-source-attribute.md) sul nodo con un puntatore all'origine supporto.</span><span class="sxs-lookup"><span data-stu-id="15843-108">Set the [**MF\_TOPONODE\_SOURCE**](mf-toponode-source-attribute.md) attribute on the node, with a pointer to the media source.</span></span>
3.  <span data-ttu-id="15843-109">Impostare l'attributo del [**\_ \_ \_ descrittore di presentazione MF TOPONODE**](mf-toponode-presentation-descriptor-attribute.md) sul nodo con un puntatore al descrittore di presentazione dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="15843-109">Set the [**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**](mf-toponode-presentation-descriptor-attribute.md) attribute on the node, with a pointer to the presentation descriptor of the media source.</span></span>
4.  <span data-ttu-id="15843-110">Impostare l'attributo del [**\_ \_ \_ descrittore di flusso MF TOPONODE**](mf-toponode-stream-descriptor-attribute.md) nel nodo, con un puntatore al descrittore del flusso per il flusso.</span><span class="sxs-lookup"><span data-stu-id="15843-110">Set the [**MF\_TOPONODE\_STREAM\_DESCRIPTOR**](mf-toponode-stream-descriptor-attribute.md) attribute on the node, with a pointer to the stream descriptor for the stream.</span></span>
5.  <span data-ttu-id="15843-111">Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.</span><span class="sxs-lookup"><span data-stu-id="15843-111">Call [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) to add the node to the topology.</span></span>

<span data-ttu-id="15843-112">Nell'esempio seguente viene creato e inizializzato un nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="15843-112">The following example creates and initializes a source node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
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



## <a name="related-topics"></a><span data-ttu-id="15843-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="15843-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15843-114">Creazione di topologie</span><span class="sxs-lookup"><span data-stu-id="15843-114">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="15843-115">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="15843-115">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="15843-116">Topologie</span><span class="sxs-lookup"><span data-stu-id="15843-116">Topologies</span></span>](topologies.md)
</dt> <dt>

[<span data-ttu-id="15843-117">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="15843-117">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



