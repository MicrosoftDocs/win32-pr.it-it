---
title: Informazioni sull'API di Network List Manager
description: Informazioni sull'API di Network List Manager
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713588"
---
# <a name="about-the-network-list-manager-api"></a><span data-ttu-id="2c676-103">Informazioni sull'API di Network List Manager</span><span class="sxs-lookup"><span data-stu-id="2c676-103">About the Network List Manager API</span></span>

<span data-ttu-id="2c676-104">L'ambiente di rete di Microsoft Windows consente ai computer multihomed di connettersi contemporaneamente a più reti.</span><span class="sxs-lookup"><span data-stu-id="2c676-104">The Microsoft Windows networking environment allows multihomed computers to connect to several networks simultaneously.</span></span> <span data-ttu-id="2c676-105">È possibile che siano disponibili più reti wireless insieme alle connessioni LAN e remote.</span><span class="sxs-lookup"><span data-stu-id="2c676-105">There may be multiple wireless networks available along with LAN and dial-up connections.</span></span> <span data-ttu-id="2c676-106">Network List Manager identifica le reti disponibili e restituisce i dati degli attributi di rete per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2c676-106">Network List Manager identifies available networks and returns network attribute data to the application.</span></span>

<span data-ttu-id="2c676-107">L'API Network List Manager interagisce con il servizio Network List Manager per identificare e recuperare le proprietà di ogni rete a cui il PC si connette.</span><span class="sxs-lookup"><span data-stu-id="2c676-107">The Network List Manager API interacts with the Network List Manager service to identify and retrieve properties of each network that the PC connects to.</span></span> <span data-ttu-id="2c676-108">Ogni rete viene identificata in modo univoco con una firma di rete basata sulle proprietà identificabili in modo univoco della rete.</span><span class="sxs-lookup"><span data-stu-id="2c676-108">Each network is uniquely identified with a network signature based on the uniquely identifiable properties of that network.</span></span> <span data-ttu-id="2c676-109">Quando un'applicazione viene registrata per le notifiche di Network List Manager, l'applicazione riceve notifiche sulla disponibilità di nuove connessioni di rete o modifiche alle connessioni di rete esistenti.</span><span class="sxs-lookup"><span data-stu-id="2c676-109">When an application registers for Network List Manager notifications, the application receives notifications about the availability of new network connections or changes to existing network connections.</span></span> <span data-ttu-id="2c676-110">Le applicazioni possono regolare la logica a seconda della rete a cui sono connesse. connessione di rete a cui sono connesse. o le proprietà di rete.</span><span class="sxs-lookup"><span data-stu-id="2c676-110">Applications can adjust their logic depending on: which network they are connected to; which network connection they are connected to; or what the network properties are.</span></span> <span data-ttu-id="2c676-111">Con queste informazioni le applicazioni possono ottimizzare le proprie azioni in base alle condizioni correnti della rete</span><span class="sxs-lookup"><span data-stu-id="2c676-111">With this information applications can fine tune their actions based on current network conditions</span></span>

<span data-ttu-id="2c676-112">In Windows Vista sono state introdotte nuove interfacce che è possibile utilizzare per ottenere informazioni dettagliate su queste caratteristiche di rete e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="2c676-112">Windows Vista introduces new interfaces that can be used to obtain detailed information about these network characteristics and more.</span></span> <span data-ttu-id="2c676-113">Con l'interfaccia [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) è facile enumerare tutte le reti ([**inett**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) visualizzate da un computer o solo le reti connesse o solo le reti disconnesse.</span><span class="sxs-lookup"><span data-stu-id="2c676-113">With the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface it is easy to enumerate all networks ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) a computer has ever seen, or just the connected networks, or just the disconnected networks.</span></span> <span data-ttu-id="2c676-114">L'interfaccia **INetworkListManager** consente inoltre di enumerare facilmente le interfacce di rete in un computer.</span><span class="sxs-lookup"><span data-stu-id="2c676-114">The **INetworkListManager** interface also makes it easy to enumerate the network interfaces on a computer.</span></span>

<span data-ttu-id="2c676-115">Per determinare le proprietà di una connessione di rete, viene utilizzata l'interfaccia di [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) , ovvero nome, descrizione, ID, gestito/autenticato, connesso/disconnesso e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="2c676-115">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface is used to determine the properties of a network connection: name, description, ID, managed/authenticated, connected/disconnected, and more.</span></span> <span data-ttu-id="2c676-116">È possibile che una singola rete sia connessa a diverse interfacce, quindi tramite un'interfaccia di **inet** è possibile anche enumerare **le istanze dell'interfaccia di** questo sistema.</span><span class="sxs-lookup"><span data-stu-id="2c676-116">It is possible that a single network is connected to several interfaces, so through an **INetwork** interface you can also enumerate the instances of the **INetwork** interface being used.</span></span>

<span data-ttu-id="2c676-117">L'interfaccia di tipo [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) indica le proprietà pertinenti di un'interfaccia: ID, Guid, tipo (gestito, autenticato) e stato (connesso, disconnesso, V4 locale, V4 Internet, V6 locale, V6 Internet).</span><span class="sxs-lookup"><span data-stu-id="2c676-117">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface tells you the relevant properties of an interface: ID, GUID, Type (managed, authenticated), and State (connected, disconnected, V4 Local, V4 Internet, V6 Local, V6 Internet).</span></span> <span data-ttu-id="2c676-118">V4 local indica l'accesso locale IPv4 (Internet Protocol versione 4).</span><span class="sxs-lookup"><span data-stu-id="2c676-118">V4 Local means Internet Protocol version 4 (IPv4) local access.</span></span> <span data-ttu-id="2c676-119">V4 Internet significa IPv4 con accesso a Internet.</span><span class="sxs-lookup"><span data-stu-id="2c676-119">V4 Internet means IPv4 with internet access.</span></span> <span data-ttu-id="2c676-120">Il protocollo Internet V6 locale e V6 media sono IPv6.</span><span class="sxs-lookup"><span data-stu-id="2c676-120">V6 Local and V6 Internet mean IPv6.</span></span>

<span data-ttu-id="2c676-121">La radice della struttura ad albero di oggetti per il percorso di rete è l'interfaccia [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) .</span><span class="sxs-lookup"><span data-stu-id="2c676-121">The root of the object tree for Network Location is the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface.</span></span> <span data-ttu-id="2c676-122">Questa interfaccia è implementata nella coclasse **CLSID \_ NetworkListManager** .</span><span class="sxs-lookup"><span data-stu-id="2c676-122">This interface is implemented on the **CLSID\_NetworkListManager** coclass.</span></span> <span data-ttu-id="2c676-123">Per utilizzare questa interfaccia, è necessario creare l'oggetto com **CLSID \_ NetworkListManager** come dimostrato:</span><span class="sxs-lookup"><span data-stu-id="2c676-123">In order to use this interface, it is necessary to create the **CLSID\_NetworkListManager** COM object as demonstrated:</span></span>


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




