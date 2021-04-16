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
# <a name="creating-transform-nodes"></a>Creazione di nodi di trasformazione

Un nodo Transform rappresenta una trasformazione Media Foundation (MFT), ad esempio un codificatore o un codificatore. Esistono diversi modi per inizializzare un nodo di trasformazione:

-   Da un puntatore a MFT.
-   Da un CLSID per il MFT.
-   Da un puntatore a un oggetto di attivazione per il MFT.

Se si intende caricare la topologia all'interno del percorso multimediale protetto (PMP), è necessario usare il CLSID o un oggetto di attivazione, in modo che il file MFT possa essere creato all'interno del processo protetto. Il primo approccio (usando un puntatore a MFT) non funziona con il PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Creazione di un nodo Transform da un MFT

Per creare un nodo di trasformazione da un MFT, seguire questa procedura:

1.  Creare un'istanza di MFT e ottenere un puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del MFT.
2.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ trasformazione \_ della topologia MF** per creare il nodo Transform.
3.  Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il puntatore [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .
4.  Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo Transform da un MFT.


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



## <a name="creating-a-transform-node-from-a-clsid"></a>Creazione di un nodo Transform da un CLSID

Per creare un nodo di trasformazione da un CLSID, eseguire le operazioni seguenti:

1.  Trovare il CLSID del MFT. È possibile usare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) per trovare i CLSID di MFTS per categoria, ad esempio decodificatori o codificatori. È anche possibile che si conosca il CLSID di un particolare MFT che si vuole usare (ad esempio se è stata implementata una MFT personalizzata).
2.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ trasformazione \_ della topologia MF** per creare il nodo Transform.
3.  Impostare l'attributo **MF \_ TOPONODE \_ Transform \_ ObjectID** nel nodo. Il valore dell'attributo è il CLSID.
4.  Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo Transform da un CLSID.


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



## <a name="creating-a-transform-node-from-an-activation-object"></a>Creazione di un nodo Transform da un oggetto Activation

Alcuni MFTs forniscono oggetti attivazione. Ad esempio, la funzione [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) restituisce un oggetto Activation per il codificatore Windows Media Audio (WMA). La funzione Exact dipende dalla MFT. Non ogni MFT fornisce un oggetto attivazione. Per altre informazioni, vedere [oggetti Activation](activation-objects.md).

È anche possibile ottenere un oggetto di attivazione MFT chiamando la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Per creare un nodo Transform da un oggetto Activation, procedere come segue:

1.  Creare l'oggetto attivazione e ottenere un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) dell'oggetto Activation.
2.  Chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) con il flag del **\_ nodo di \_ trasformazione \_ della topologia MF** per creare il nodo Transform.
3.  Chiamare [**IMFTopologyNode:: seobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) e passare il puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
4.  Chiamare [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) per aggiungere il nodo alla topologia.

Nell'esempio seguente viene creato e inizializzato un nodo Transform da un oggetto Activation.


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

 

 



