---
description: L'helper IP fornisce funzionalità per la gestione del routing di rete. Utilizzare le seguenti funzioni per gestire la tabella di routing IP e per ottenere altre informazioni di routing.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Gestione del routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879081"
---
# <a name="managing-routing"></a><span data-ttu-id="0e1cf-104">Gestione del routing</span><span class="sxs-lookup"><span data-stu-id="0e1cf-104">Managing Routing</span></span>

<span data-ttu-id="0e1cf-105">L'helper IP fornisce funzionalità per la gestione del routing di rete.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-105">IP Helper provides features to manage network routing.</span></span> <span data-ttu-id="0e1cf-106">Utilizzare le seguenti funzioni per gestire la tabella di routing IP e per ottenere altre informazioni di routing.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-106">Use the following functions to manage the IP routing table, and to obtain other routing information.</span></span>

<span data-ttu-id="0e1cf-107">Recuperare il contenuto della tabella di routing IP effettuando una chiamata alla funzione [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) .</span><span class="sxs-lookup"><span data-stu-id="0e1cf-107">Retrieve the contents of the IP routing table by making a call to the [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) function.</span></span> <span data-ttu-id="0e1cf-108">Modificare voci specifiche nella tabella di routing IP usando le funzioni [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)e [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) .</span><span class="sxs-lookup"><span data-stu-id="0e1cf-108">Manipulate specific entries in the IP routing table using the [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry), and [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) functions.</span></span> <span data-ttu-id="0e1cf-109">Utilizzare la funzione **CreateIpForwardEntry** per aggiungere una nuova voce della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-109">Use the **CreateIpForwardEntry** function to add a new routing table entry.</span></span> <span data-ttu-id="0e1cf-110">Utilizzare la funzione **DeleteIpForwardEntry** per rimuovere una voce esistente.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-110">Use the **DeleteIpForwardEntry** function to remove an existing entry.</span></span> <span data-ttu-id="0e1cf-111">La funzione **SetIpForwardEntry** modifica una voce esistente.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-111">The **SetIpForwardEntry** function modifies an existing entry.</span></span>

<span data-ttu-id="0e1cf-112">Le funzionalità di gestione del router dell'helper IP possono essere utilizzate per recuperare informazioni sul modo in cui i datagrammi vengono instradati sulla rete.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-112">The router management capabilities of IP Helper can be used to retrieve information about how datagrams are routed over the network.</span></span> <span data-ttu-id="0e1cf-113">La funzione [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) recupera la route migliore a un indirizzo di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-113">The [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) function retrieves the best route to a specified destination address.</span></span> <span data-ttu-id="0e1cf-114">La funzione [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) recupera l'indice dell'interfaccia utilizzata dalla route migliore a un indirizzo di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-114">The [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) function retrieves the index of the interface used by the best route to a specified destination address.</span></span> <span data-ttu-id="0e1cf-115">Infine, la funzione [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) Recupera il tempo di round trip (RTT) e il numero di hop a un indirizzo di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="0e1cf-115">Lastly, the [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) function retrieves the round-trip time (RTT) and number of hops to a specified destination address.</span></span>

 

 



