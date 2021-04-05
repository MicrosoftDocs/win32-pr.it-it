---
title: Gestione dei server DNS
description: Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712427"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="ddbed-103">Gestione dei server DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-103">Managing DNS Servers</span></span>

<span data-ttu-id="ddbed-104">Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.</span><span class="sxs-lookup"><span data-stu-id="ddbed-104">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="ddbed-105">I server DNS contengono file, denominati *file di zona*, che consentono di risolvere i nomi in indirizzi IP (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="ddbed-105">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="ddbed-106">Quando viene eseguita una query, un server DNS risponde in uno dei tre modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ddbed-106">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="ddbed-107">Il server restituisce le informazioni richieste per la risoluzione dei nomi o la risoluzione IP.</span><span class="sxs-lookup"><span data-stu-id="ddbed-107">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="ddbed-108">Il server restituisce un puntatore a un altro server DNS che può servire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="ddbed-108">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="ddbed-109">Il server indica che non sono disponibili le informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="ddbed-109">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="ddbed-110">I server DNS potrebbero, durante la preparazione della restituzione delle informazioni di risoluzione richieste, eseguire una query su altri server DNS.</span><span class="sxs-lookup"><span data-stu-id="ddbed-110">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="ddbed-111">Tuttavia, oltre a questo, i server DNS non eseguono alcuna operazione diversa da quella indicata nell'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="ddbed-111">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="ddbed-112">Sono disponibili tre tipi principali di server DNS: server primari, server secondari e server di memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="ddbed-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="ddbed-113">Per ulteriori informazioni su questi server DNS, vedere [server DNS](dns-servers.md) .</span><span class="sxs-lookup"><span data-stu-id="ddbed-113">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="ddbed-114">Procedura di amministrazione</span><span class="sxs-lookup"><span data-stu-id="ddbed-114">Administration Steps</span></span>

<span data-ttu-id="ddbed-115">Il provider WMI DNS consente l'amministrazione dei server DNS dal server stesso o da host remoti.</span><span class="sxs-lookup"><span data-stu-id="ddbed-115">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="ddbed-116">I passaggi generali necessari per amministrare un server DNS tramite il provider WMI DNS sono:</span><span class="sxs-lookup"><span data-stu-id="ddbed-116">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="ddbed-117">Connessione al provider WMI DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-117">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="ddbed-118">Recupero di un'istanza del server</span><span class="sxs-lookup"><span data-stu-id="ddbed-118">Getting a server instance</span></span>
-   <span data-ttu-id="ddbed-119">Elenco o modifica di una proprietà del server o utilizzo di un metodo</span><span class="sxs-lookup"><span data-stu-id="ddbed-119">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="ddbed-120">Per illustrare come implementare tali passaggi di amministrazione, vengono forniti alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="ddbed-120">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="ddbed-121">Le attività seguenti sono collegate agli esempi di script associati.</span><span class="sxs-lookup"><span data-stu-id="ddbed-121">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="ddbed-122">Arresto di un server DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-122">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="ddbed-123">Avvio di un server DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-123">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="ddbed-124">Riavvio di un server DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-124">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="ddbed-125">Aggiunta di un indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="ddbed-125">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="ddbed-126">Rimozione di un indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="ddbed-126">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="ddbed-127">Elenco delle proprietà del server DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-127">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="ddbed-128">Visualizzazione di tipi di proprietà del server DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-128">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="ddbed-129">Modifica delle proprietà del server DNS</span><span class="sxs-lookup"><span data-stu-id="ddbed-129">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




