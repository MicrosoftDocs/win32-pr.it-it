---
description: Uso di dispositivi video DV USB
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Uso di dispositivi video DV USB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd1f83fb490f4bd1e71714dcb0658d01a41d6e45af6f3e89436f6e32c1cdc985
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071746"
---
# <a name="working-with-usb-dv-video-devices"></a>Uso di dispositivi video DV USB

Questo argomento descrive come scrivere applicazioni per dispositivi video USB (Universal Serial Bus) che acquisiscono video DV.

Il formato DV Standard ha una velocità dati di circa 25 megabit al secondo (Mbps). Quando è stata introdotta per la prima volta, USB non aveva larghezza di banda sufficiente per supportare video DV. TUTTAVIA, USB 2.0 può supportare fino a 480 Mbps, che è più che sufficiente per i video DV. La specifica USB Video Device Class (UVC), rilasciata nel 2003, definisce il formato di payload per i dispositivi video USB DV. Un driver Windows Driver Model (WDM) per dispositivi UVC è stato introdotto in Windows XP Service Pack 2.

Nella maggior parte dei casi, il driver UVC supporta lo stesso modello di programmazione del driver MSDV per IEEE 1394 dispositivi. Le applicazioni scritte per MSDV devono richiedere solo piccole modifiche per supportare i dispositivi UVC.

Il driver UVC si comporta in modo diverso rispetto al driver MSDV nelle aree seguenti:

-   [Modalità dispositivo](device-mode.md)
-   [Formato flusso](stream-format.md)
-   [Formato del segnale](signal-format.md)
-   [Ricerca percorso nastro](tape-location-search.md)
-   [Trasmettere DV da file a nastro](transmit-dv-from-file-to-tape.md).

Per determinare quale driver viene usato, chiamare [**IAMExtDevice::get \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport). Il driver MSDV restituisce il flag DEV \_ PORT \_ 1394 e il driver UVC restituisce il flag DEV \_ PORT \_ USB.

**Nodi del dispositivo**

Nella terminologia USB, gli endpoint sono i punti in cui i dati entrano o lasciano il dispositivo. Un endpoint ha una direzione del flusso di dati, ovvero l'input (da dispositivo a host) o l'output (dall'host al dispositivo). Può essere utile pensare che queste direzioni siano relative all'host. L'input passa all'host. L'output proviene dall'host. Il diagramma seguente illustra i due endpoint.

![Endpoint usb](images/ksnodes01.png)

In un dispositivo UVC le funzioni del dispositivo sono suddivise logicamente in componenti denominati unità e terminali. Un'unità riceve uno o più flussi di dati come input e fornisce esattamente un flusso come output. Un terminale è il punto iniziale o finale per un flusso di dati. Gli endpoint USB corrispondono ai terminali, ma le direzioni sono invertte: un endpoint di input è rappresentato da un terminale di output e viceversa. Il diagramma seguente illustra la relazione tra terminali ed endpoint.

![Unità e terminali uvc](images/ksnodes02.png)

Inoltre, non tutti i terminali corrispondono a un endpoint USB. Il termine endpoint si riferisce in modo specifico alle connessioni USB e un dispositivo può inviare o ricevere dati tramite connessioni non USB. Ad esempio, una videocamera è un terminale di input e uno schermo LCD è un terminale di output.

Nel filtro KS Proxy le unità e i terminali sono rappresentati come nodi all'interno del filtro. Il termine nodo è più generale rispetto ai termini unità e terminale perché anche i dispositivi non USB possono avere nodi. Per ottenere informazioni sui nodi in un filtro, eseguire una query sul filtro per [**l'interfaccia IKsTopologyInfo.**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) I tipi di nodo sono identificati dai GUID. I nodi del selettore sono nodi che possono alternare due o più input. I nodi del selettore espongono [**l'interfaccia ISelector.**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector)

Il codice seguente verifica se un pin di output in un filtro riceve l'input da un nodo di un determinato tipo.


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

 

 



