---
title: Server Active Directory e DNS dinamico
description: I server Active Directory pubblicano i relativi indirizzi in modo che i client possano individuarli conoscendo solo il nome di dominio.
ms.assetid: b4928d53-2629-4ddb-bb43-ce7a187b41e2
ms.tgt_platform: multiple
keywords:
- Active Directory DNS dinamici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971987cb73b65e46b36eda4c713054ba2796e63b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707222"
---
# <a name="active-directory-servers-and-dynamic-dns"></a><span data-ttu-id="88e74-104">Server Active Directory e DNS dinamico</span><span class="sxs-lookup"><span data-stu-id="88e74-104">Active Directory Servers and Dynamic DNS</span></span>

<span data-ttu-id="88e74-105">I server Active Directory pubblicano i relativi indirizzi in modo che i client possano individuarli conoscendo solo il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="88e74-105">The Active Directory servers publish their addresses such that clients can find them knowing only the domain name.</span></span> <span data-ttu-id="88e74-106">I server Active Directory vengono pubblicati usando i record di risorse del servizio (SRV RR) in DNS.</span><span class="sxs-lookup"><span data-stu-id="88e74-106">Active Directory servers are published using the Service Resource Records (SRV RRs) in DNS.</span></span> <span data-ttu-id="88e74-107">SRV RR è un record DNS utilizzato per eseguire il mapping del nome di un servizio all'indirizzo di un server che offre il servizio.</span><span class="sxs-lookup"><span data-stu-id="88e74-107">The SRV RR is a DNS record used to map the name of a service to the address of a server that offers the service.</span></span> <span data-ttu-id="88e74-108">Il nome di un record SRV è nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="88e74-108">The name of a SRV RR is in this form:</span></span>


```C++
<service>.<protocol>.<domain>
```



<span data-ttu-id="88e74-109">I server Active Directory offrono il servizio LDAP sul protocollo TCP, in modo che i nomi pubblicati siano "LDAP. <domain> TCP".</span><span class="sxs-lookup"><span data-stu-id="88e74-109">Active Directory servers offer the LDAP service over the TCP protocol so that published names are "ldap.tcp.<domain>".</span></span> <span data-ttu-id="88e74-110">Pertanto, l'RR SRV per fabrikam.com è "ldap.tcp.fabrikam.com".</span><span class="sxs-lookup"><span data-stu-id="88e74-110">Thus, the SRV RR for fabrikam.com is "ldap.tcp.fabrikam.com".</span></span> <span data-ttu-id="88e74-111">I dati aggiuntivi sull'RR SRV indicano la priorità e il peso per il server, consentendo ai client di scegliere il server migliore per le proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="88e74-111">Additional data about the SRV RR indicates the priority and weight for the server, enabling clients to choose the best server for their needs.</span></span>

<span data-ttu-id="88e74-112">Quando si installa un server di Active Directory, viene utilizzato il DNS dinamico per la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="88e74-112">When an Active Directory server is installed, it uses Dynamic DNS to publish itself.</span></span> <span data-ttu-id="88e74-113">Poiché gli indirizzi TCP/IP sono soggetti a modifiche, i server verificano periodicamente le registrazioni per assicurarsi che siano corretti e aggiornarli, se necessario.</span><span class="sxs-lookup"><span data-stu-id="88e74-113">Because TCP/IP addresses are subject to change, servers periodically verify their registrations to be sure they are correct, and update them if necessary.</span></span>

<span data-ttu-id="88e74-114">Il DNS dinamico è una recente aggiunta allo standard DNS.</span><span class="sxs-lookup"><span data-stu-id="88e74-114">Dynamic DNS is a recent addition to the DNS standard.</span></span> <span data-ttu-id="88e74-115">DNS dinamico definisce un protocollo per l'aggiornamento dinamico di un server DNS con nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="88e74-115">Dynamic DNS defines a protocol for dynamically updating a DNS server with new data.</span></span> <span data-ttu-id="88e74-116">Prima del DNS dinamico, agli amministratori veniva richiesto di configurare manualmente i record archiviati dai server DNS.</span><span class="sxs-lookup"><span data-stu-id="88e74-116">Prior to Dynamic DNS, administrators were required to manually configure the records stored by DNS servers.</span></span>

 

 




