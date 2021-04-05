---
title: Server DNS
description: Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Server DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712241"
---
# <a name="dns-servers"></a><span data-ttu-id="30b60-104">Server DNS</span><span class="sxs-lookup"><span data-stu-id="30b60-104">DNS Servers</span></span>

<span data-ttu-id="30b60-105">Un *server DNS* è un computer che completa il processo di risoluzione dei nomi in DNS.</span><span class="sxs-lookup"><span data-stu-id="30b60-105">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="30b60-106">I server DNS contengono [*file di zona*](z-gly.md) che consentono di risolvere i nomi in indirizzi IP e indirizzi IP in nomi.</span><span class="sxs-lookup"><span data-stu-id="30b60-106">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="30b60-107">Quando viene eseguita una query, un server DNS risponderà in uno dei tre modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="30b60-107">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="30b60-108">Il server restituisce i dati richiesti per la risoluzione dei nomi o la risoluzione IP.</span><span class="sxs-lookup"><span data-stu-id="30b60-108">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="30b60-109">Il server restituisce un puntatore a un altro server DNS che può servire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="30b60-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="30b60-110">Il server indica che non sono presenti i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="30b60-110">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="30b60-111">I server DNS potrebbero, durante la preparazione della restituzione dei dati di risoluzione richiesti, eseguire una query su altri server DNS, ma, oltre a questo, i server DNS non eseguono altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="30b60-111">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="30b60-112">Sono disponibili tre tipi principali di server DNS: server primari, server secondari e server di memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="30b60-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="30b60-113">Server primario</span><span class="sxs-lookup"><span data-stu-id="30b60-113">Primary Server</span></span>

<span data-ttu-id="30b60-114">Il *server primario* è il server autorevole per la zona.</span><span class="sxs-lookup"><span data-stu-id="30b60-114">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="30b60-115">Tutte le attività amministrative associate alla zona, ad esempio la creazione di sottodomini all'interno della zona o altre attività amministrative simili, devono essere eseguite sul server primario.</span><span class="sxs-lookup"><span data-stu-id="30b60-115">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="30b60-116">Inoltre, le eventuali modifiche associate alla zona o alle eventuali modifiche o aggiunte a RRs nei file di zona devono essere effettuate sul server primario.</span><span class="sxs-lookup"><span data-stu-id="30b60-116">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="30b60-117">Per qualsiasi zona, esiste un server primario, tranne quando si integra Active Directory Services e il server DNS Microsoft.</span><span class="sxs-lookup"><span data-stu-id="30b60-117">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="30b60-118">Server secondari</span><span class="sxs-lookup"><span data-stu-id="30b60-118">Secondary Servers</span></span>

<span data-ttu-id="30b60-119">I *server secondari* sono server DNS di backup.</span><span class="sxs-lookup"><span data-stu-id="30b60-119">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="30b60-120">I server secondari ricevono tutti i file di zona dai file di zona del server primario in un trasferimento di zona.</span><span class="sxs-lookup"><span data-stu-id="30b60-120">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="30b60-121">Per qualsiasi zona specificata possono esistere più server secondari, il numero necessario per fornire [*bilanciamento del carico*](l-gly.md), [*tolleranza di errore*](f-gly.md)e riduzione del traffico.</span><span class="sxs-lookup"><span data-stu-id="30b60-121">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="30b60-122">Inoltre, qualsiasi server DNS specificato può essere un server secondario per più zone.</span><span class="sxs-lookup"><span data-stu-id="30b60-122">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="30b60-123">Oltre ai server DNS primari e secondari, è possibile usare ruoli del server DNS aggiuntivi quando tali server sono appropriati per un'infrastruttura DNS.</span><span class="sxs-lookup"><span data-stu-id="30b60-123">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="30b60-124">Questi server aggiuntivi memorizzano nella cache server e server d' [*inoltri*](f-gly.md).</span><span class="sxs-lookup"><span data-stu-id="30b60-124">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="30b60-125">Server di memorizzazione nella cache</span><span class="sxs-lookup"><span data-stu-id="30b60-125">Caching Servers</span></span>

<span data-ttu-id="30b60-126">I [*server di memorizzazione nella cache*](c-gly.md), noti anche come server solo caching, eseguono come suggerito il nome; forniscono solo il servizio di query memorizzato nella cache per le risposte DNS.</span><span class="sxs-lookup"><span data-stu-id="30b60-126">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="30b60-127">Anziché gestire i file di zona come altri server secondari, la memorizzazione nella cache dei server DNS esegue query, memorizza nella cache le risposte e restituisce i risultati al client di query.</span><span class="sxs-lookup"><span data-stu-id="30b60-127">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="30b60-128">La differenza principale tra i server di memorizzazione nella cache e gli altri server secondari è che altri server secondari gestiscono i file di zona (ed eseguono trasferimenti di zona quando appropriato, generando così il traffico di rete associato al trasferimento), i server di memorizzazione nella cache non lo sono.</span><span class="sxs-lookup"><span data-stu-id="30b60-128">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




