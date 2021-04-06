---
description: Di seguito è riportata una guida dettagliata per iniziare a programmare con l'helper IP Application Programming Interface (API). È progettato per fornire informazioni sulle funzioni di supporto IP di base e sulle strutture dei dati e sul modo in cui interagiscono.
ms.assetid: 3280d6cf-2741-40fe-8aa5-9f5be96d9fb8
title: Introduzione con helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 566ed4503c9bbafaee846aebf30c31993f7ce7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885713"
---
# <a name="getting-started-with-ip-helper"></a><span data-ttu-id="92b2f-104">Introduzione con helper IP</span><span class="sxs-lookup"><span data-stu-id="92b2f-104">Getting Started with IP Helper</span></span>

<span data-ttu-id="92b2f-105">Di seguito è riportata una guida dettagliata per iniziare a programmare con l'helper IP Application Programming Interface (API).</span><span class="sxs-lookup"><span data-stu-id="92b2f-105">The following is a step-by-step guide to getting started programming using the IP Helper application programming interface (API).</span></span> <span data-ttu-id="92b2f-106">È progettato per fornire informazioni sulle funzioni di supporto IP di base e sulle strutture dei dati e sul modo in cui interagiscono.</span><span class="sxs-lookup"><span data-stu-id="92b2f-106">It is designed to provide an understanding of basic IP Helper functions and data structures, and how they work together.</span></span>

<span data-ttu-id="92b2f-107">L'applicazione usata per l'illustrazione è un'applicazione helper IP di base.</span><span class="sxs-lookup"><span data-stu-id="92b2f-107">The application that is used for illustration is a very basic IP Helper application.</span></span> <span data-ttu-id="92b2f-108">Negli esempi inclusi nel Software Development Kit (SDK) di Microsoft Windows sono inclusi esempi di codice più avanzati.</span><span class="sxs-lookup"><span data-stu-id="92b2f-108">More advanced code examples are included in the samples included with the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="92b2f-109">Il primo passaggio è identico per la maggior parte delle applicazioni helper IP.</span><span class="sxs-lookup"><span data-stu-id="92b2f-109">The first step is the same for most IP Helper applications.</span></span>

-   [<span data-ttu-id="92b2f-110">Creazione di un'applicazione helper IP di base</span><span class="sxs-lookup"><span data-stu-id="92b2f-110">Creating a Basic IP Helper Application</span></span>](creating-a-basic-ip-helper-application.md)

<span data-ttu-id="92b2f-111">Le sezioni seguenti descrivono i passaggi rimanenti per la creazione di questa applicazione helper IP di base.</span><span class="sxs-lookup"><span data-stu-id="92b2f-111">The following sections describe the remaining steps for creating this basic IP Helper application.</span></span>

-   [<span data-ttu-id="92b2f-112">Recupero di informazioni tramite GetNetworkParams</span><span class="sxs-lookup"><span data-stu-id="92b2f-112">Retrieving Information Using GetNetworkParams</span></span>](retrieving-information-using-getnetworkparams.md)
-   [<span data-ttu-id="92b2f-113">Gestione delle schede di rete con GetAdaptersInfo</span><span class="sxs-lookup"><span data-stu-id="92b2f-113">Managing Network Adapters Using GetAdaptersInfo</span></span>](managing-network-adapters-using-getadaptersinfo.md)
-   [<span data-ttu-id="92b2f-114">Gestione delle interfacce mediante GetInterfaceInfo</span><span class="sxs-lookup"><span data-stu-id="92b2f-114">Managing Interfaces Using GetInterfaceInfo</span></span>](managing-interfaces-using-getinterfaceinfo.md)
-   [<span data-ttu-id="92b2f-115">Gestione degli indirizzi IP tramite GetIpAddrTable</span><span class="sxs-lookup"><span data-stu-id="92b2f-115">Managing IP Addresses Using GetIpAddrTable</span></span>](managing-ip-addresses-using-getipaddrtable.md)
-   [<span data-ttu-id="92b2f-116">Gestione dei lease DHCP con IpReleaseAddress e IpRenewAddress</span><span class="sxs-lookup"><span data-stu-id="92b2f-116">Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress</span></span>](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)
-   [<span data-ttu-id="92b2f-117">Gestione degli indirizzi IP con AddIPAddress e DeleteIPAddress</span><span class="sxs-lookup"><span data-stu-id="92b2f-117">Managing IP Addresses Using AddIPAddress and DeleteIPAddress</span></span>](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)
-   [<span data-ttu-id="92b2f-118">Recupero di informazioni tramite GetIpStatistics</span><span class="sxs-lookup"><span data-stu-id="92b2f-118">Retrieving Information Using GetIpStatistics</span></span>](retrieving-information-using-getipstatistics.md)
-   [<span data-ttu-id="92b2f-119">Recupero di informazioni tramite GetTcpStatistics</span><span class="sxs-lookup"><span data-stu-id="92b2f-119">Retrieving Information Using GetTcpStatistics</span></span>](retrieving-information-using-gettcpstatistics.md)

<span data-ttu-id="92b2f-120">Il codice sorgente completo per questo esempio di helper IP di base.</span><span class="sxs-lookup"><span data-stu-id="92b2f-120">The complete source code for this basic IP Helper example.</span></span>

-   [<span data-ttu-id="92b2f-121">Codice sorgente completo dell'applicazione helper IP</span><span class="sxs-lookup"><span data-stu-id="92b2f-121">Complete IP Helper Application Source Code</span></span>](complete-ip-helper-application-source-code.md)

## <a name="advanced-ip-helper-samples"></a><span data-ttu-id="92b2f-122">Esempi avanzati di helper IP</span><span class="sxs-lookup"><span data-stu-id="92b2f-122">Advanced IP Helper Samples</span></span>

<span data-ttu-id="92b2f-123">Con Microsoft Windows Software Development Kit (SDK) sono inclusi diversi esempi di helper IP più avanzati.</span><span class="sxs-lookup"><span data-stu-id="92b2f-123">Several more advanced IP Helper samples are included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="92b2f-124">Per impostazione predefinita, il codice sorgente di esempio dell'helper IP viene installato dalla Windows SDK rilasciata per Windows 7 nella seguente directory:</span><span class="sxs-lookup"><span data-stu-id="92b2f-124">By default, the IP Helper sample source code is installed by the Windows SDK released for Windows 7 in the following directory:</span></span>

<span data-ttu-id="92b2f-125">*C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi \\ NetDs \\ IPHelp*</span><span class="sxs-lookup"><span data-stu-id="92b2f-125">*C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\IPHelp*</span></span>

<span data-ttu-id="92b2f-126">Gli esempi più avanzati elencati di seguito sono disponibili nelle directory seguenti:</span><span class="sxs-lookup"><span data-stu-id="92b2f-126">The more advanced samples listed below are found in the following directories:</span></span>

-   <span data-ttu-id="92b2f-127">EnableRouter</span><span class="sxs-lookup"><span data-stu-id="92b2f-127">EnableRouter</span></span>

    <span data-ttu-id="92b2f-128">Questa directory contiene un esempio che illustra come usare le funzioni di supporto IP [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) e [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) per abilitare e disabilitare l'invio IPv4 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="92b2f-128">This directory contains a sample that demonstrates how to use the [**EnableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-enablerouter) and [**UnenableRouter**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-unenablerouter) IP Helper functions to enable and disable IPv4 forwarding on the local computer.</span></span>

-   <span data-ttu-id="92b2f-129">iparp</span><span class="sxs-lookup"><span data-stu-id="92b2f-129">iparp</span></span>

    <span data-ttu-id="92b2f-130">Questa directory contiene un programma di esempio che illustra come usare le funzioni helper IP per visualizzare e modificare le voci nella tabella ARP IPv4 nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="92b2f-130">This directory contains a sample program that demonstrates how to use the IP Helper functions to display and manipulate entries in the IPv4 ARP table on the local computer.</span></span>

-   <span data-ttu-id="92b2f-131">ipchange</span><span class="sxs-lookup"><span data-stu-id="92b2f-131">ipchange</span></span>

    <span data-ttu-id="92b2f-132">Questa directory contiene un programma di esempio che illustra come usare le funzioni di supporto IP per modificare a livello di codice un indirizzo IP per una scheda di rete specifica nel computer.</span><span class="sxs-lookup"><span data-stu-id="92b2f-132">This directory contains a sample program that demonstrates how to use IP Helper functions to programmatically change an IP address for a specific network adapter on your machine.</span></span> <span data-ttu-id="92b2f-133">Questo programma illustra anche come recuperare le informazioni di configurazione IP della scheda di rete esistente.</span><span class="sxs-lookup"><span data-stu-id="92b2f-133">This program also demonstrates how to retrieve existing network adapter IP configuration information.</span></span>

-   <span data-ttu-id="92b2f-134">IPConfig</span><span class="sxs-lookup"><span data-stu-id="92b2f-134">IPConfig</span></span>

    <span data-ttu-id="92b2f-135">Questa directory contiene un programma di esempio che illustra come recuperare a livello di codice le informazioni di configurazione IPv4 simili all'utilità IPCONFIG.EXE.</span><span class="sxs-lookup"><span data-stu-id="92b2f-135">This directory contains a sample program that demonstrates how to programmatically retrieve IPv4 configuration information similar to the IPCONFIG.EXE utility.</span></span> <span data-ttu-id="92b2f-136">Viene illustrato come usare le funzioni [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) e [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) .</span><span class="sxs-lookup"><span data-stu-id="92b2f-136">It demonstrates how to use the [**GetNetworkParams**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getnetworkparams) and [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) functions.</span></span> <span data-ttu-id="92b2f-137">Si noti che la funzione **GetAdaptersInfo** recupera solo le informazioni IPv4.</span><span class="sxs-lookup"><span data-stu-id="92b2f-137">Note that the **GetAdaptersInfo** function only retrieves IPv4 information.</span></span>

-   <span data-ttu-id="92b2f-138">IPRenew</span><span class="sxs-lookup"><span data-stu-id="92b2f-138">IPRenew</span></span>

    <span data-ttu-id="92b2f-139">Questa directory contiene un programma di esempio in cui viene illustrato come rilasciare e rinnovare gli indirizzi IPv4 ottenuti tramite DHCP a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="92b2f-139">This directory contains a sample program that demonstrates how to programmatically release and renew IPv4 addresses obtained through DHCP.</span></span> <span data-ttu-id="92b2f-140">Questo programma illustra anche come recuperare le informazioni di configurazione delle schede di rete esistenti.</span><span class="sxs-lookup"><span data-stu-id="92b2f-140">This program also demonstrates how to retrieve existing network adapter configuration information.</span></span>

-   <span data-ttu-id="92b2f-141">IPRoute</span><span class="sxs-lookup"><span data-stu-id="92b2f-141">IPRoute</span></span>

    <span data-ttu-id="92b2f-142">Questa directory contiene un programma di esempio che illustra come usare le funzioni di supporto IP per modificare la tabella di routing IPv4.</span><span class="sxs-lookup"><span data-stu-id="92b2f-142">This directory contains a sample program that demonstrates how to use the IP Helper functions to manipulate the IPv4 routing table.</span></span>

-   <span data-ttu-id="92b2f-143">ipstat</span><span class="sxs-lookup"><span data-stu-id="92b2f-143">ipstat</span></span>

    <span data-ttu-id="92b2f-144">Questa directory contiene un programma di esempio che illustra come usare le funzioni di supporto IP per visualizzare le connessioni IPv4 per un protocollo.</span><span class="sxs-lookup"><span data-stu-id="92b2f-144">This directory contains a sample program that demonstrates how to use the IP Helper functions to show IPv4 connections for a protocol.</span></span> <span data-ttu-id="92b2f-145">Per impostazione predefinita, vengono visualizzate le statistiche per IP, ICMP, TCP e UDP.</span><span class="sxs-lookup"><span data-stu-id="92b2f-145">By default, statistics are shown for IP, ICMP, TCP and UDP.</span></span>

-   <span data-ttu-id="92b2f-146">NetInfo</span><span class="sxs-lookup"><span data-stu-id="92b2f-146">Netinfo</span></span>

    <span data-ttu-id="92b2f-147">Questa directory contiene un programma di esempio che illustra come usare le nuove API helper IP introdotte in Windows Vista e versioni successive per visualizzare/modificare le informazioni sull'indirizzo e sull'interfaccia per IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="92b2f-147">This directory contains a sample program that demonstrates how to the use the new IP Helper APIs introduced on Windows Vista and later to display/change address and interface information for IPv4 and IPv6.</span></span>

 

 



