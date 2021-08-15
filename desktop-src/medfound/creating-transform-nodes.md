---
description: Creazione di nodi di trasformazione
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Creazione di nodi di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc6cc0aff2d429cee2d9d3b175c57dacd773dc865f702e043386127b9104833d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346901"
---
# <a name="creating-transform-nodes"></a>Creazione di nodi di trasformazione

Un nodo di trasformazione rappresenta una Media Foundation (MFT), ad esempio un decodificatore o un codificatore. Esistono diversi modi per inizializzare un nodo di trasformazione:

-   Da un puntatore a MFT.
-   Da un CLSID per MFT.
-   Da un puntatore a un oggetto di attivazione per MFT.

Se si sta per caricare la topologia all'interno del percorso del supporto protetto (PMP), è necessario usare il CLSID o un oggetto di attivazione, in modo che il MFT possa essere creato all'interno del processo protetto. Il primo approccio (usando un puntatore a MFT) non funziona con il PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Creazione di un nodo di trasformazione da un MFT

Per creare un nodo di trasformazione da un MFT, eseguire le operazioni seguenti:

1.  Creare un'istanza di MFT e ottenere un puntatore [**all'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) di MFT.
2.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag **MF \_ TOPOLOGY \_ TRANSFORM \_ NODE** per creare il nodo di trasformazione.
3.  Chiamare [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il [**puntatore IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
4.  Chiamare [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo di trasformazione da un MFT.


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



## <a name="creating-a-transform-node-from-a-clsid"></a>Creazione di un nodo di trasformazione da un CLSID

Per creare un nodo di trasformazione da un CLSID, eseguire le operazioni seguenti:

1.  Trovare il CLSID dell'MFT. È possibile usare la [**funzione MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) per trovare i CLSID di MFT per categoria, ad esempio decodificatori o codificatori. È anche possibile conoscere il CLSID di un particolare MFT che si vuole usare, ad esempio se è stato implementato un MFT personalizzato.
2.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag **MF \_ TOPOLOGY \_ TRANSFORM \_ NODE** per creare il nodo di trasformazione.
3.  Impostare **l'attributo \_ \_ \_ OBJECTID MF TOPONODE TRANSFORM** nel nodo. Il valore dell'attributo è il CLSID.
4.  Chiamare [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo di trasformazione da un CLSID.


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



## <a name="creating-a-transform-node-from-an-activation-object"></a>Creazione di un nodo di trasformazione da un oggetto di attivazione

Alcuni MFT forniscono oggetti di attivazione. Ad esempio, la [**funzione MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) restituisce un oggetto di attivazione per il Windows Media Audio (WMA). La funzione esatta dipende da MFT. Non ogni MFT fornisce un oggetto di attivazione. Per altre informazioni, vedere [Oggetti di attivazione](activation-objects.md).

È anche possibile ottenere un oggetto di attivazione MFT chiamando la [**funzione MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Per creare un nodo di trasformazione da un oggetto di attivazione, eseguire le operazioni seguenti:

1.  Creare l'oggetto di attivazione e ottenere un puntatore [**all'interfaccia IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) dell'oggetto di attivazione.
2.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag **MF \_ TOPOLOGY \_ TRANSFORM \_ NODE** per creare il nodo di trasformazione.
3.  Chiamare [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il [**puntatore IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
4.  Chiamare [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo di trasformazione da un oggetto di attivazione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di topologie](creating-topologies.md)
</dt> <dt>

[Topologie](topologies.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



