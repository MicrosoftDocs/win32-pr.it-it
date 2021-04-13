---
description: Uso di dispositivi video USB DV
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Uso di dispositivi video USB DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226493"
---
# <a name="working-with-usb-dv-video-devices"></a>Uso di dispositivi video USB DV

Questo argomento descrive come scrivere applicazioni per i dispositivi video USB (Universal Serial Bus) che acquisiscono video DV.

Il formato DV standard ha una velocità dati pari a circa 25 megabit al secondo (Mbps). Quando USB è stato introdotto per la prima volta, non disponeva di una larghezza di banda sufficiente per supportare video DV. Tuttavia, USB 2,0 può supportare fino a 480 Mbps, che è più che sufficiente per i video DV. La specifica di classe dispositivo video USB (UVC), rilasciata in 2003, definisce il formato del payload per i dispositivi video USB DV. Un driver di classe Windows Driver Model (WDM) per i dispositivi UVC è stato introdotto in Windows XP Service Pack 2.

Nella maggior parte dei casi, il driver UVC supporta lo stesso modello di programmazione del driver MSDV per i dispositivi IEEE 1394. Le applicazioni scritte per MSDV devono richiedere solo modifiche minime per supportare i dispositivi UVC.

Il driver UVC si comporta in modo diverso rispetto al driver MSDV nelle aree seguenti:

-   [Modalità dispositivo](device-mode.md)
-   [Formato flusso](stream-format.md)
-   [Formato segnale](signal-format.md)
-   [Ricerca posizione nastro](tape-location-search.md)
-   [Trasmettere il DV da un file a un nastro](transmit-dv-from-file-to-tape.md).

Per determinare quale driver viene usato, chiamare [**IAMExtDevice:: Get \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport). Il driver MSDV restituisce il \_ flag dev port \_ 1394 e il driver UVC restituisce il \_ flag USB della porta di sviluppo \_ .

**Nodi del dispositivo**

Nella terminologia USB gli endpoint sono punti in cui i dati entrano o lasciano il dispositivo. Un endpoint ha una direzione del flusso di dati, ovvero input (da dispositivo a host) o output (da host a dispositivo). Può essere utile considerare queste direzioni come relative all'host. L'input viene indirizzato all'host. l'output deriva dall'host. Il diagramma seguente illustra i due endpoint.

![endpoint USB](images/ksnodes01.png)

In un dispositivo UVC le funzioni del dispositivo sono divise logicamente in componenti denominati unità e terminali. Un'unità riceve uno o più flussi di dati come input e recapita esattamente un flusso come output. Un terminale è il punto iniziale o finale per un flusso di dati. Gli endpoint USB corrispondono ai terminali, ma le direzioni sono invertite: un endpoint di input è rappresentato da un terminale di output e viceversa. Il diagramma seguente illustra la relazione tra terminali ed endpoint.

![unità e terminali UVC](images/ksnodes02.png)

Inoltre, non tutti i terminali corrispondono a un endpoint USB. Il termine endpoint si riferisce in modo specifico alle connessioni USB e un dispositivo può inviare o ricevere dati tramite connessioni non USB. Ad esempio, una videocamera è un terminale di input e uno schermo LCD è un terminale di output.

Nel filtro del proxy KS, le unità e i terminali sono rappresentati come nodi all'interno del filtro. Il termine nodo è più generale rispetto all'unità dei termini e al terminale perché i dispositivi non USB possono anche avere nodi. Per ottenere informazioni sui nodi in un filtro, eseguire una query sul filtro per l'interfaccia [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) . I tipi di nodo sono identificati da GUID. I nodi del selettore sono nodi che possono spostarsi tra due o più input. I nodi del selettore espongono l'interfaccia dell' [**eleggente**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) .

Il codice seguente verifica se un pin di output in un filtro riceve l'input da un nodo di un tipo specificato.


```C++
// Structure to hold topology information.
struct TopologyConnections
{
    KSTOPOLOGY_CONNECTION *connections; // Array of connections
    DWORD count;  // Number of elements in the array
};

/////////////////////////////////////////////////////////////////////
// Name: GetTopologyConnections
// Desc: Gets the topology information from a filter.
//
// pTopo:       Pointer to the filter's IKsTopologyInfo interface.
// connectInfo: Pointer to a TopologyConnections structure. The 
//              function fills in this structure.
//
// Note: If the function succeeds, call CoTaskMemFree to free the
//       pConnectInfo->connections array.
/////////////////////////////////////////////////////////////////////

HRESULT GetTopologyConnections(
    IKsTopologyInfo *pTopo, 
    TopologyConnections *pConnectInfo
    )
{
    DWORD count;
    HRESULT hr = pTopo->get_NumConnections(&count);
    if (FAILED(hr))
    {
        return hr;
    }

    pConnectInfo->count = count;
    pConnectInfo->connections = NULL;
    if (count > 0)
    {
        // Allocate an array for the connection information.
        SIZE_T cb = sizeof(KSTOPOLOGY_CONNECTION) * count;
        KSTOPOLOGY_CONNECTION *pConnections = 
            (KSTOPOLOGY_CONNECTION*) CoTaskMemAlloc(cb);
        if (pConnections == NULL)
        {
            return E_OUTOFMEMORY;
        }
        // Fill the array.
        for (DWORD ix = 0; ix < count; ix++)
        {
            hr = pTopo->get_ConnectionInfo(ix, &pConnections[ix]);
            if (FAILED(hr))
            {
                break;
            }
        }
        if (SUCCEEDED(hr))
        {
            pConnectInfo->connections = pConnections;
        }
        else
        {
           CoTaskMemFree(pConnections);
        }
    }
    return hr;
}

/////////////////////////////////////////////////////////////////////
// Name: IsNodeDownstreamFromNode
// Desc: Searches upstream from a node for a specified node type.
//
// pTopo:        Pointer to the filter's IKsTopologyInfo interface.
// connectInfo:  Contains toplogy information. To fill in this
//               structure, call GetTopologyConnections.
// nodeID:       ID of the starting node in the search.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected, or false otherwise.
//
// Note: If the source node matches the type, this function returns 
//       true without searching upstream.
/////////////////////////////////////////////////////////////////////

HRESULT IsNodeDownstreamFromNode(
    IKsTopologyInfo *pTopo,
    const TopologyConnections& connectInfo, 
    DWORD nodeID,
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    *pIsConnected = false;
    // Base case for recursion: check the source node.
    GUID type;
    HRESULT hr = pTopo->get_NodeType(nodeID, &type);
    if (FAILED(hr))
    {
        return hr;
    }
    if (type == nodeType)
    {
        *pIsConnected = true;
        return S_OK;
    }

    // If the source node is a selector, get the input node.
    CComPtr<ISelector> pSelector;
    hr = pTopo->CreateNodeInstance(nodeID, __uuidof(ISelector), 
        (void**)&pSelector);
    if (SUCCEEDED(hr))
    {
        DWORD sourceNodeID;
        hr = pSelector->get_SourceNodeId(&sourceNodeID);
        if (SUCCEEDED(hr))
        {
            // Recursive call with the selector's input node.
            return IsNodeDownstreamFromNode(pTopo, connectInfo, 
                       sourceNodeID, nodeType, pIsConnected);
        }
    }
    else if (hr == E_NOINTERFACE)
    {
        hr = S_OK;  // This node is not a selector. Not a failure.
    }
    else
    {
        return hr;
    }

    // Test all of the upstream connections on this pin. 
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == nodeID) &&
            (connectInfo.connections[ix].FromNode != KSFILTER_NODE))
        {
            // FromNode is connected to the source node.
            DWORD fromNode = connectInfo.connections[ix].FromNode;

            // Recursive call with the upstream node.
            bool bIsConnected;
            hr = IsNodeDownstreamFromNode(pTopo, connectInfo, 
                fromNode, nodeType, &bIsConnected);
            if (FAILED(hr))
            {
                break;
            }
            if (bIsConnected)
            {
                *pIsConnected = true;
                break;
            }
        }
    }
    return hr;
}


/////////////////////////////////////////////////////////////////////
// Name: GetNodeUpstreamFromPin
// Desc: Finds the node connected to an output pin.
//
// connectInfo: Contains toplogy information. To fill in this
//              structure, call GetTopologyConnections.
// nPinIndex:   Index of the output pin.
// pNodeID:     Receives the ID of the connected node.
/////////////////////////////////////////////////////////////////////

HRESULT GetNodeUpstreamFromPin(
    const TopologyConnections& connectInfo, 
    UINT nPinIndex, 
    DWORD *pNodeID
    )
{
    bool bFound = false;
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == KSFILTER_NODE) &&
            (connectInfo.connections[ix].ToNodePin == nPinIndex))
        {
            *pNodeID = connectInfo.connections[ix].FromNode;
            bFound = true;
            break;
        }
    }
    if (bFound)
    {
        return S_OK;
    }
    else
    {
        return E_FAIL;
    }
}


/////////////////////////////////////////////////////////////////////
// Name: IsPinDownstreamFromNode
// Desc: Tests whether an output pin gets data from a node of
//       a specified type.
// 
// pFilter:      Pointer to the filter's IBaseFilter interface.
// UINT:         Index of the output pin to test.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected; false otherwise.
/////////////////////////////////////////////////////////////////////

HRESULT IsPinDownstreamFromNode(
    IBaseFilter *pFilter, 
    UINT nPinIndex, 
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    CComQIPtr<IKsTopologyInfo> pTopo(pFilter);
    if (pTopo == NULL)
    {
        return E_NOINTERFACE;
    }

    // Get the topology connection information.
    TopologyConnections connectionInfo;
    HRESULT hr = GetTopologyConnections(pTopo, &connectionInfo);
    if (FAILED(hr))
    {
        return hr;
    }

    // Find the node upstream from this pin.
    DWORD nodeID;
    hr = GetNodeUpstreamFromPin(connectionInfo, nPinIndex, &nodeID);
    if (SUCCEEDED(hr))
    {
        bool isConnected;
        hr = IsNodeDownstreamFromNode(pTopo, connectionInfo, 
            nodeID, nodeType, &isConnected);
        if (SUCCEEDED(hr))
        {
            *pIsConnected = isConnected;
        }
    }
    CoTaskMemFree(connectionInfo.connections);
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Video digitale in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



