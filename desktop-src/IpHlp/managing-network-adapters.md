---
description: L'helper IP fornisce funzionalità per la gestione delle schede di rete. Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer. Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.
ms.assetid: fbb32941-2add-4f74-90c4-1dc1bfebd64c
title: Gestione delle schede di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8f42cf1499ee7873d13334d0edbc9f954794f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525891"
---
# <a name="managing-network-adapters"></a><span data-ttu-id="9e6ea-105">Gestione delle schede di rete</span><span class="sxs-lookup"><span data-stu-id="9e6ea-105">Managing Network Adapters</span></span>

<span data-ttu-id="9e6ea-106">L'helper IP fornisce funzionalità per la gestione delle schede di rete.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-106">IP Helper provides capabilities for managing network adapters.</span></span> <span data-ttu-id="9e6ea-107">Esiste una corrispondenza uno-a-uno tra le interfacce e gli adapter in un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-107">There is a one-to-one correspondence between the interfaces and adapters on a given computer.</span></span> <span data-ttu-id="9e6ea-108">Un'interfaccia è un'astrazione a livello di IP, mentre un adapter è un'astrazione a livello di Datalink.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-108">An interface is an IP-level abstraction, whereas an adapter is a datalink-level abstraction.</span></span>

<span data-ttu-id="9e6ea-109">Utilizzare le funzioni descritte nei paragrafi seguenti per recuperare informazioni sulle schede di rete nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-109">Use the functions described in the following paragraphs to retrieve information about the network adapters in the local computer.</span></span>

<span data-ttu-id="9e6ea-110">La funzione [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) restituisce una matrice di strutture di [**\_ \_ informazioni della scheda IP**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) , una per ogni scheda nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-110">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns an array of [**IP\_ADAPTER\_INFO**](/windows/desktop/api/Iptypes/ns-iptypes-ip_adapter_info) structures, one for each adapter in the local computer.</span></span> <span data-ttu-id="9e6ea-111">La funzione [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) restituisce informazioni aggiuntive su un adapter specifico.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-111">The [**GetPerAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getperadapterinfo) function returns additional information about a specific adapter.</span></span> <span data-ttu-id="9e6ea-112">La funzione **GetPerAdapterInfo** richiede che il chiamante specifichi l'indice dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-112">The **GetPerAdapterInfo** function requires the caller to specify the index of the adapter.</span></span> <span data-ttu-id="9e6ea-113">Per ottenere l'indice dell'adapter dal nome dell'adapter, utilizzare la funzione [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) .</span><span class="sxs-lookup"><span data-stu-id="9e6ea-113">To obtain the adapter index from the adapter name, use the [**GetAdapterIndex**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadapterindex) function.</span></span>

<span data-ttu-id="9e6ea-114">Alcune applicazioni utilizzano Adapter che ricevono datagrammi, ma non possono trasmetterli.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-114">Some applications use adapters that receive datagrams, but cannot transmit them.</span></span> <span data-ttu-id="9e6ea-115">Per ottenere informazioni su questi adapter, utilizzare la funzione [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) .</span><span class="sxs-lookup"><span data-stu-id="9e6ea-115">To obtain information about these adapters, use the [**GetUniDirectionalAdapterInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo) function.</span></span>

<span data-ttu-id="9e6ea-116">La funzione [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) consente di recuperare gli indirizzi IP associati a un particolare adapter.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-116">The [**GetAdaptersAddresses**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersaddresses) function enables you to retrieve the IP addresses associated with a particular adapter.</span></span> <span data-ttu-id="9e6ea-117">Questa funzione supporta l'indirizzamento sia IPv4 che IPv6.</span><span class="sxs-lookup"><span data-stu-id="9e6ea-117">This function supports both IPv4 and IPv6 addressing.</span></span>

-   <span data-ttu-id="9e6ea-118">Per esempi di codice che coinvolgono [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) , vedere [gestione delle schede di rete con GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span><span class="sxs-lookup"><span data-stu-id="9e6ea-118">For code samples involving [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

 

 



