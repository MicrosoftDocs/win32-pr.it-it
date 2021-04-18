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
# <a name="creating-source-nodes"></a>Creazione di nodi di origine

Un nodo di origine rappresenta un flusso da un'origine multimediale. Il nodo di origine deve contenere puntatori all'origine multimediale, al descrittore di presentazione e al descrittore del flusso.

Per aggiungere un nodo di origine a una topologia, effettuare le operazioni seguenti:

1.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ \_ \_ nodo SOURCESTREAM della topologia MF** per creare il nodo di origine.
2.  Impostare l'attributo di [**\_ \_ origine MF TOPONODE**](mf-toponode-source-attribute.md) sul nodo con un puntatore all'origine supporto.
3.  Impostare l'attributo del [**\_ \_ \_ descrittore di presentazione MF TOPONODE**](mf-toponode-presentation-descriptor-attribute.md) sul nodo con un puntatore al descrittore di presentazione dell'origine multimediale.
4.  Impostare l'attributo del [**\_ \_ \_ descrittore di flusso MF TOPONODE**](mf-toponode-stream-descriptor-attribute.md) nel nodo, con un puntatore al descrittore del flusso per il flusso.
5.  Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo di origine.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di topologie](creating-topologies.md)
</dt> <dt>

[Origini supporti](media-sources.md)
</dt> <dt>

[Topologie](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



