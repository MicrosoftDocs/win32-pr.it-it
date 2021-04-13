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
# <a name="working-with-usb-dv-video-devices"></a><span data-ttu-id="0cec2-103">Uso di dispositivi video USB DV</span><span class="sxs-lookup"><span data-stu-id="0cec2-103">Working with USB DV Video Devices</span></span>

<span data-ttu-id="0cec2-104">Questo argomento descrive come scrivere applicazioni per i dispositivi video USB (Universal Serial Bus) che acquisiscono video DV.</span><span class="sxs-lookup"><span data-stu-id="0cec2-104">This topic describes how to write applications for Universal Serial Bus (USB) video devices that capture DV video.</span></span>

<span data-ttu-id="0cec2-105">Il formato DV standard ha una velocità dati pari a circa 25 megabit al secondo (Mbps).</span><span class="sxs-lookup"><span data-stu-id="0cec2-105">Standard DV format has a data rate of about 25 megabits per second (Mbps).</span></span> <span data-ttu-id="0cec2-106">Quando USB è stato introdotto per la prima volta, non disponeva di una larghezza di banda sufficiente per supportare video DV.</span><span class="sxs-lookup"><span data-stu-id="0cec2-106">When USB was first introduced, it did not have enough bandwidth to support DV video.</span></span> <span data-ttu-id="0cec2-107">Tuttavia, USB 2,0 può supportare fino a 480 Mbps, che è più che sufficiente per i video DV.</span><span class="sxs-lookup"><span data-stu-id="0cec2-107">However, USB 2.0 can support up to 480 Mbps, which is more than sufficient for DV video.</span></span> <span data-ttu-id="0cec2-108">La specifica di classe dispositivo video USB (UVC), rilasciata in 2003, definisce il formato del payload per i dispositivi video USB DV.</span><span class="sxs-lookup"><span data-stu-id="0cec2-108">The USB Video Device Class (UVC) specification, released in 2003, defines the payload format for USB DV video devices.</span></span> <span data-ttu-id="0cec2-109">Un driver di classe Windows Driver Model (WDM) per i dispositivi UVC è stato introdotto in Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="0cec2-109">A Windows Driver Model (WDM) class driver for UVC devices was introduced in Windows XP Service Pack 2.</span></span>

<span data-ttu-id="0cec2-110">Nella maggior parte dei casi, il driver UVC supporta lo stesso modello di programmazione del driver MSDV per i dispositivi IEEE 1394.</span><span class="sxs-lookup"><span data-stu-id="0cec2-110">In most respects, the UVC driver supports the same programming model as the MSDV driver for IEEE 1394 devices.</span></span> <span data-ttu-id="0cec2-111">Le applicazioni scritte per MSDV devono richiedere solo modifiche minime per supportare i dispositivi UVC.</span><span class="sxs-lookup"><span data-stu-id="0cec2-111">Applications written for MSDV should require only minor modifications to support UVC devices.</span></span>

<span data-ttu-id="0cec2-112">Il driver UVC si comporta in modo diverso rispetto al driver MSDV nelle aree seguenti:</span><span class="sxs-lookup"><span data-stu-id="0cec2-112">The UVC driver behaves differently from the MSDV driver in the following areas:</span></span>

-   [<span data-ttu-id="0cec2-113">Modalità dispositivo</span><span class="sxs-lookup"><span data-stu-id="0cec2-113">Device Mode</span></span>](device-mode.md)
-   [<span data-ttu-id="0cec2-114">Formato flusso</span><span class="sxs-lookup"><span data-stu-id="0cec2-114">Stream Format</span></span>](stream-format.md)
-   [<span data-ttu-id="0cec2-115">Formato segnale</span><span class="sxs-lookup"><span data-stu-id="0cec2-115">Signal Format</span></span>](signal-format.md)
-   [<span data-ttu-id="0cec2-116">Ricerca posizione nastro</span><span class="sxs-lookup"><span data-stu-id="0cec2-116">Tape Location Search</span></span>](tape-location-search.md)
-   <span data-ttu-id="0cec2-117">[Trasmettere il DV da un file a un nastro](transmit-dv-from-file-to-tape.md).</span><span class="sxs-lookup"><span data-stu-id="0cec2-117">[Transmit DV from File to Tape](transmit-dv-from-file-to-tape.md).</span></span>

<span data-ttu-id="0cec2-118">Per determinare quale driver viene usato, chiamare [**IAMExtDevice:: Get \_ DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span><span class="sxs-lookup"><span data-stu-id="0cec2-118">To determine which driver is being used, call [**IAMExtDevice::get\_DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span></span> <span data-ttu-id="0cec2-119">Il driver MSDV restituisce il \_ flag dev port \_ 1394 e il driver UVC restituisce il \_ flag USB della porta di sviluppo \_ .</span><span class="sxs-lookup"><span data-stu-id="0cec2-119">The MSDV driver returns the DEV\_PORT\_1394 flag, and the UVC driver returns the DEV\_PORT\_USB flag.</span></span>

<span data-ttu-id="0cec2-120">**Nodi del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="0cec2-120">**Device Nodes**</span></span>

<span data-ttu-id="0cec2-121">Nella terminologia USB gli endpoint sono punti in cui i dati entrano o lasciano il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0cec2-121">In USB terminology, endpoints are the points where data enters or leaves the device.</span></span> <span data-ttu-id="0cec2-122">Un endpoint ha una direzione del flusso di dati, ovvero input (da dispositivo a host) o output (da host a dispositivo).</span><span class="sxs-lookup"><span data-stu-id="0cec2-122">An endpoint has a direction of data flow, either input (from device to host) or output (from host to device).</span></span> <span data-ttu-id="0cec2-123">Può essere utile considerare queste direzioni come relative all'host.</span><span class="sxs-lookup"><span data-stu-id="0cec2-123">It may help to think of these directions as being relative to the host.</span></span> <span data-ttu-id="0cec2-124">L'input viene indirizzato all'host. l'output deriva dall'host.</span><span class="sxs-lookup"><span data-stu-id="0cec2-124">Input goes to the host; output comes from the host.</span></span> <span data-ttu-id="0cec2-125">Il diagramma seguente illustra i due endpoint.</span><span class="sxs-lookup"><span data-stu-id="0cec2-125">The following diagram illustrates the two endpoints.</span></span>

![endpoint USB](images/ksnodes01.png)

<span data-ttu-id="0cec2-127">In un dispositivo UVC le funzioni del dispositivo sono divise logicamente in componenti denominati unità e terminali.</span><span class="sxs-lookup"><span data-stu-id="0cec2-127">In a UVC device, the functions of the device are logically divided into components called units and terminals.</span></span> <span data-ttu-id="0cec2-128">Un'unità riceve uno o più flussi di dati come input e recapita esattamente un flusso come output.</span><span class="sxs-lookup"><span data-stu-id="0cec2-128">A unit receives one or more data streams as input and delivers exactly one stream as output.</span></span> <span data-ttu-id="0cec2-129">Un terminale è il punto iniziale o finale per un flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0cec2-129">A terminal is the starting point or ending point for a data stream.</span></span> <span data-ttu-id="0cec2-130">Gli endpoint USB corrispondono ai terminali, ma le direzioni sono invertite: un endpoint di input è rappresentato da un terminale di output e viceversa.</span><span class="sxs-lookup"><span data-stu-id="0cec2-130">USB endpoints correspond to terminals, but the directions are reversed: an input endpoint is represented by an output terminal, and vice versa.</span></span> <span data-ttu-id="0cec2-131">Il diagramma seguente illustra la relazione tra terminali ed endpoint.</span><span class="sxs-lookup"><span data-stu-id="0cec2-131">The following diagram shows the relation between terminals and endpoints.</span></span>

![unità e terminali UVC](images/ksnodes02.png)

<span data-ttu-id="0cec2-133">Inoltre, non tutti i terminali corrispondono a un endpoint USB.</span><span class="sxs-lookup"><span data-stu-id="0cec2-133">Also, not every terminal corresponds to a USB endpoint.</span></span> <span data-ttu-id="0cec2-134">Il termine endpoint si riferisce in modo specifico alle connessioni USB e un dispositivo può inviare o ricevere dati tramite connessioni non USB.</span><span class="sxs-lookup"><span data-stu-id="0cec2-134">The term endpoint refers specifically to USB connections, and a device may send or receive data through non-USB connections.</span></span> <span data-ttu-id="0cec2-135">Ad esempio, una videocamera è un terminale di input e uno schermo LCD è un terminale di output.</span><span class="sxs-lookup"><span data-stu-id="0cec2-135">For example, a video camera is an input terminal and an LCD screen is an output terminal.</span></span>

<span data-ttu-id="0cec2-136">Nel filtro del proxy KS, le unità e i terminali sono rappresentati come nodi all'interno del filtro.</span><span class="sxs-lookup"><span data-stu-id="0cec2-136">In the KS Proxy filter, units and terminals are represented as nodes inside the filter.</span></span> <span data-ttu-id="0cec2-137">Il termine nodo è più generale rispetto all'unità dei termini e al terminale perché i dispositivi non USB possono anche avere nodi.</span><span class="sxs-lookup"><span data-stu-id="0cec2-137">The term node is more general than the terms unit and terminal because non-USB devices can also have nodes.</span></span> <span data-ttu-id="0cec2-138">Per ottenere informazioni sui nodi in un filtro, eseguire una query sul filtro per l'interfaccia [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .</span><span class="sxs-lookup"><span data-stu-id="0cec2-138">To get information about the nodes in a filter, query the filter for the [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) interface.</span></span> <span data-ttu-id="0cec2-139">I tipi di nodo sono identificati da GUID.</span><span class="sxs-lookup"><span data-stu-id="0cec2-139">Node types are identified by GUIDs.</span></span> <span data-ttu-id="0cec2-140">I nodi del selettore sono nodi che possono spostarsi tra due o più input.</span><span class="sxs-lookup"><span data-stu-id="0cec2-140">Selector nodes are nodes that can switch between two or more inputs.</span></span> <span data-ttu-id="0cec2-141">I nodi del selettore espongono l'interfaccia dell' [**eleggente**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) .</span><span class="sxs-lookup"><span data-stu-id="0cec2-141">Selector nodes expose the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface.</span></span>

<span data-ttu-id="0cec2-142">Il codice seguente verifica se un pin di output in un filtro riceve l'input da un nodo di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="0cec2-142">The following code tests whether an output pin on a filter receives input from a node of a given type.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0cec2-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cec2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cec2-144">Video digitale in DirectShow</span><span class="sxs-lookup"><span data-stu-id="0cec2-144">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



