---
title: Gestione dei server DNS
description: Informazioni sulla gestione dei server DNS. Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d797e05bc326b35e48173082d9b36a2b334fd9
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010774"
---
# <a name="managing-dns-servers"></a><span data-ttu-id="66d70-104">Gestione dei server DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-104">Managing DNS Servers</span></span>

<span data-ttu-id="66d70-105">Un server DNS è un computer che completa il processo di risoluzione dei nomi in DNS.</span><span class="sxs-lookup"><span data-stu-id="66d70-105">A DNS Server is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="66d70-106">I server DNS contengono file, denominati *file di* zona, che consentono di risolvere i nomi in indirizzi IP (o viceversa).</span><span class="sxs-lookup"><span data-stu-id="66d70-106">DNS Servers contain files, called *zone files*, that enable them to resolve names to IP addresses (or vice versa).</span></span> <span data-ttu-id="66d70-107">Quando viene eseguita una query, un server DNS risponde in uno dei tre modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66d70-107">When queried, a DNS Server responds in one of three ways:</span></span>

-   <span data-ttu-id="66d70-108">Il server restituisce le informazioni di risoluzione dei nomi o IP richieste.</span><span class="sxs-lookup"><span data-stu-id="66d70-108">The server returns the requested name-resolution or IP-resolution information.</span></span>
-   <span data-ttu-id="66d70-109">Il server restituisce un puntatore a un altro server DNS in grado di eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="66d70-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="66d70-110">Il server indica che non dispone delle informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="66d70-110">The server indicates that it does not have the requested information.</span></span>

<span data-ttu-id="66d70-111">I server DNS potrebbero, durante la preparazione alla restituzione delle informazioni di risoluzione richieste, eseguire query su altri server DNS.</span><span class="sxs-lookup"><span data-stu-id="66d70-111">DNS Servers might, during the course of preparing to return the requested resolution information, query other DNS Servers.</span></span> <span data-ttu-id="66d70-112">Oltre a questo, i server DNS non eseguono operazioni diverse da quelle indicate nell'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="66d70-112">But beyond that, DNS Servers do not perform any operations other than those mentioned in the previous list.</span></span>

<span data-ttu-id="66d70-113">Esistono tre tipi principali di server DNS: server primari, server secondari e server di memorizzazione nella cache.</span><span class="sxs-lookup"><span data-stu-id="66d70-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span> <span data-ttu-id="66d70-114">Per altre informazioni su questi server DNS, vedere Server [DNS.](dns-servers.md)</span><span class="sxs-lookup"><span data-stu-id="66d70-114">See [DNS Servers](dns-servers.md) for more information on these DNS Servers.</span></span>

## <a name="administration-steps"></a><span data-ttu-id="66d70-115">Passaggi di amministrazione</span><span class="sxs-lookup"><span data-stu-id="66d70-115">Administration Steps</span></span>

<span data-ttu-id="66d70-116">Il provider WMI DNS consente l'amministrazione di server DNS dal server stesso o da host remoti.</span><span class="sxs-lookup"><span data-stu-id="66d70-116">The DNS WMI Provider enables the administration of DNS Servers from the server itself, or from remote hosts.</span></span> <span data-ttu-id="66d70-117">I passaggi generali necessari per amministrare un server DNS usando il provider WMI DNS sono:</span><span class="sxs-lookup"><span data-stu-id="66d70-117">The general steps necessary to administer a DNS Server using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="66d70-118">Connessione al provider WMI DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-118">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="66d70-119">Recupero di un'istanza del server</span><span class="sxs-lookup"><span data-stu-id="66d70-119">Getting a server instance</span></span>
-   <span data-ttu-id="66d70-120">Elenco o modifica di una proprietà del server o uso di un metodo</span><span class="sxs-lookup"><span data-stu-id="66d70-120">Listing or modifying a server property, or using a method</span></span>

<span data-ttu-id="66d70-121">Per illustrare come implementare questi passaggi di amministrazione, vengono forniti esempi.</span><span class="sxs-lookup"><span data-stu-id="66d70-121">To illustrate how to implement those administration steps, examples are provided.</span></span> <span data-ttu-id="66d70-122">Le attività seguenti sono collegate agli esempi di scripting associati.</span><span class="sxs-lookup"><span data-stu-id="66d70-122">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="66d70-123">Arresto di un server DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-123">Stopping a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="66d70-124">Avvio di un server DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-124">Starting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="66d70-125">Riavvio di un server DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-125">Restarting a DNS Server</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="66d70-126">Aggiunta di un indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="66d70-126">Adding an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="66d70-127">Rimozione di un indirizzo IP</span><span class="sxs-lookup"><span data-stu-id="66d70-127">Removing an IP Address</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="66d70-128">Elenco delle proprietà del server DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-128">Listing DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="66d70-129">Visualizzazione dei tipi di proprietà del server DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-129">Displaying DNS Server Property Types</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [<span data-ttu-id="66d70-130">Modifica delle proprietà del server DNS</span><span class="sxs-lookup"><span data-stu-id="66d70-130">Modifying DNS Server Properties</span></span>](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




