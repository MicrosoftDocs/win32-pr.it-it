---
description: Creazione di nodi di output
ms.assetid: 6e548f2a-77cd-460e-9ffd-c098f6ee75eb
title: Creazione di nodi di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6af2842458fb360374d34583b15bfbf5005b2f2bbdd8b32332bc6756ca4e8157
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943021"
---
# <a name="creating-output-nodes"></a>Creazione di nodi di output

Un nodo di output rappresenta un sink di flusso in un sink multimediale. Esistono due modi per inizializzare un nodo di output:

-   Da un puntatore al sink di flusso.
-   Da un puntatore a un oggetto di attivazione per il sink multimediale.

Se si desidera caricare la topologia all'interno del percorso del supporto protetto (PMP), è necessario usare un oggetto di attivazione, in modo che il sink multimediale possa essere creato all'interno del processo protetto. Il primo approccio (usando un puntatore al sink di flusso) non funziona con il PMP.

## <a name="creating-an-output-node-from-a-stream-sink"></a>Creazione di un nodo di output da un sink di flusso

Per creare un nodo di output da un sink di flusso, eseguire le operazioni seguenti:

1.  Creare un'istanza del sink multimediale.
2.  Usare l'interfaccia [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) del sink di supporto per ottenere un puntatore al sink di flusso desiderato. **L'interfaccia IMFMediaSink** include diversi metodi che restituiscono puntatori a un sink di flusso.
3.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag **MF \_ TOPOLOGY \_ OUTPUT \_ NODE** per creare il nodo di output.
4.  Chiamare [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare un puntatore [**all'interfaccia IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del sink di flusso.
5.  Impostare [**l'attributo MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) su **FALSE** (facoltativo ma consigliato).
6.  Chiamare [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo di output da un sink di flusso.


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



Quando l'applicazione arresta la sessione multimediale, la sessione multimediale arresta automaticamente il sink multimediale. Pertanto, non è possibile usare nuovamente il sink multimediale con un'altra istanza della sessione multimediale.

## <a name="creating-an-output-node-from-an-activation-object"></a>Creazione di un nodo di output da un oggetto di attivazione

Qualsiasi sink di supporto attendibile deve fornire un oggetto di attivazione, in modo che possa essere creato all'interno del processo protetto. Per altre informazioni, vedere [Oggetti di attivazione](activation-objects.md). La funzione specifica che crea l'oggetto di attivazione dipenderà dal sink multimediale.

Per creare un nodo di output da un oggetto di attivazione, eseguire le operazioni seguenti:

1.  Creare l'oggetto di attivazione e ottenere un puntatore [**all'interfaccia IMFActivate dell'oggetto**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) di attivazione.
2.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag **MF \_ TOPOLOGY \_ OUTPUT \_ NODE** per creare il nodo di output.
3.  Facoltativamente, impostare [**l'attributo \_ MF TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md) nel nodo per specificare l'identificatore di flusso del sink di flusso. Se si omette questo attributo, per impostazione predefinita il nodo usa il sink di flusso 0.
4.  Impostare [**l'attributo MF \_ TOPONODE \_ NOSHUTDOWN \_ ON \_ REMOVE**](mf-toponode-noshutdown-on-remove-attribute.md) su **TRUE** (facoltativo ma consigliato).
5.  Chiamare [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il [**puntatore IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
6.  Chiamare [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo di output da un oggetto di attivazione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Creazione di topologie](creating-topologies.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



