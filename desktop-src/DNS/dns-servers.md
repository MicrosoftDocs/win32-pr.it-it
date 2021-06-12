---
title: Server DNS
description: Informazioni sui server DNS. Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Server DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011254"
---
# <a name="dns-servers"></a><span data-ttu-id="5a0b3-105">Server DNS</span><span class="sxs-lookup"><span data-stu-id="5a0b3-105">DNS Servers</span></span>

<span data-ttu-id="5a0b3-106">Un *server DNS* è un computer che completa il processo di risoluzione dei nomi in DNS.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-106">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="5a0b3-107">I server DNS [*contengono file di*](z-gly.md) zona che consentono di risolvere i nomi in indirizzi IP e indirizzi IP in nomi.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-107">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="5a0b3-108">Quando viene eseguita una query, un server DNS risponderà in uno dei tre modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a0b3-108">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="5a0b3-109">Il server restituisce i dati di risoluzione dei nomi o IP richiesti.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-109">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="5a0b3-110">Il server restituisce un puntatore a un altro server DNS in grado di eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-110">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="5a0b3-111">Il server indica che non dispone dei dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-111">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="5a0b3-112">I server DNS potrebbero, durante la preparazione alla restituzione dei dati di risoluzione richiesti, eseguire query su altri server DNS, ma oltre a questo, i server DNS non eseguono altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-112">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="5a0b3-113">Esistono tre tipi principali di server DNS: server primari, server secondari e server di memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="5a0b3-114">Server primario</span><span class="sxs-lookup"><span data-stu-id="5a0b3-114">Primary Server</span></span>

<span data-ttu-id="5a0b3-115">Il *server primario* è il server autorevole per la zona.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-115">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="5a0b3-116">Tutte le attività amministrative associate alla zona, ad esempio la creazione di sottodomini all'interno della zona o altre attività amministrative simili, devono essere eseguite nel server primario.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-116">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="5a0b3-117">Inoltre, tutte le modifiche associate alla zona o eventuali modifiche o aggiunte alle richiesteri nei file di zona devono essere apportate nel server primario.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-117">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="5a0b3-118">Per ogni zona è presente un server primario, tranne quando si integrano i servizi Active Directory e il server DNS Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-118">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="5a0b3-119">Server secondari</span><span class="sxs-lookup"><span data-stu-id="5a0b3-119">Secondary Servers</span></span>

<span data-ttu-id="5a0b3-120">*I server secondari* sono server DNS di backup.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-120">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="5a0b3-121">I server secondari ricevono tutti i relativi file di zona dai file di zona del server primario in un trasferimento di zona.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-121">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="5a0b3-122">Per qualsiasi zona possono esistere più server secondari, tutti necessari per garantire il bilanciamento del [*carico,*](l-gly.md)la tolleranza di [*errore*](f-gly.md)e la riduzione del traffico.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-122">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="5a0b3-123">Inoltre, qualsiasi server DNS specificato può essere un server secondario per più zone.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-123">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="5a0b3-124">Oltre ai server DNS primari e secondari, è possibile usare ruoli server DNS aggiuntivi quando tali server sono appropriati per un'infrastruttura DNS.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-124">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="5a0b3-125">Questi server aggiuntivi memorizzano nella cache server e [*server d'inoltro*](f-gly.md).</span><span class="sxs-lookup"><span data-stu-id="5a0b3-125">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="5a0b3-126">Memorizzazione nella cache dei server</span><span class="sxs-lookup"><span data-stu-id="5a0b3-126">Caching Servers</span></span>

<span data-ttu-id="5a0b3-127">[*I server di memorizzazione*](c-gly.md)nella cache, noti anche come server di sola memorizzazione nella cache, vengono eseguono come suggerisce il nome; forniscono solo il servizio query memorizzate nella cache per le risposte DNS.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-127">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="5a0b3-128">Invece di gestire i file di zona come fanno altri server secondari, la memorizzazione nella cache dei server DNS esegue query, memorizza nella cache le risposte e restituisce i risultati al client che esegue le query.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-128">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="5a0b3-129">La differenza principale tra i server di memorizzazione nella cache e gli altri server secondari è che altri server secondari gestiscono i file di zona (e, se appropriato, e, se appropriato, generano traffico di rete associato al trasferimento), i server di memorizzazione nella cache non lo fanno.</span><span class="sxs-lookup"><span data-stu-id="5a0b3-129">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




