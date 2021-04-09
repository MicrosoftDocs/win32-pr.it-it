---
description: L'helper IP fornisce funzionalità di recupero delle informazioni utili per l'amministrazione di rete del computer locale.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Recupero di informazioni sul protocollo Internet e sul Internet Control Message Protocol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966433"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a><span data-ttu-id="96cff-103">Recupero di informazioni sul protocollo Internet e sul Internet Control Message Protocol</span><span class="sxs-lookup"><span data-stu-id="96cff-103">Retrieving Information on the Internet Protocol and the Internet Control Message Protocol</span></span>

<span data-ttu-id="96cff-104">L'helper IP fornisce funzionalità di recupero delle informazioni utili per l'amministrazione di rete del computer locale.</span><span class="sxs-lookup"><span data-stu-id="96cff-104">IP Helper provides information retrieval capabilities that are useful for the network administration of the local computer.</span></span> <span data-ttu-id="96cff-105">Le funzioni seguenti recuperano le statistiche per il protocollo IP (Internet Protocol) e il Internet Control Message Protocol (ICMP).</span><span class="sxs-lookup"><span data-stu-id="96cff-105">The following functions retrieve statistics for the Internet Protocol (IP) and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="96cff-106">È anche possibile usare queste funzioni per impostare determinati parametri di configurazione per l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="96cff-106">You can also use these functions to set certain configuration parameters for IP.</span></span>

<span data-ttu-id="96cff-107">La funzione [**GetIPStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) recupera le statistiche IP correnti per il computer locale.</span><span class="sxs-lookup"><span data-stu-id="96cff-107">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function retrieves the current IP statistics for the local computer.</span></span> <span data-ttu-id="96cff-108">Per esempi di codice che coinvolgono **GetIPStatistics** , vedere [recupero di informazioni con GetIPStatistics](retrieving-information-using-getipstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="96cff-108">For code samples involving **GetIpStatistics** see [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md).</span></span>

<span data-ttu-id="96cff-109">La funzione [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) recupera le statistiche ICMP correnti.</span><span class="sxs-lookup"><span data-stu-id="96cff-109">The [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) function retrieves the current ICMP statistics.</span></span>

<span data-ttu-id="96cff-110">Usare la funzione [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) per abilitare o disabilitare l'invio di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="96cff-110">Use the [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) function to enable or disable IP forwarding.</span></span> <span data-ttu-id="96cff-111">Questa funzione consente inoltre di impostare la durata (TTL) predefinita per i datagrammi IP.</span><span class="sxs-lookup"><span data-stu-id="96cff-111">This function also makes it possible for you to set the default time-to-live (TTL) for IP datagrams.</span></span> <span data-ttu-id="96cff-112">In alternativa, è possibile impostare la durata (TTL) utilizzando la funzione [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .</span><span class="sxs-lookup"><span data-stu-id="96cff-112">Alternatively, you can set the TTL by using the [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) function.</span></span>

 

 



