---
description: Il servizio dischi virtuali (VDS) gestisce un'ampia gamma di configurazioni di archiviazione, da desktop su disco singolo ad array di archiviazione esterni. Il servizio espone un Application Programming Interface (API).
ms.assetid: 536aafd2-cc04-48cc-8ee7-920efbba2a5f
title: Servizio dischi virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcfef0c5a73fcb2e6911395c829380c4bdfe56ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312706"
---
# <a name="virtual-disk-service"></a><span data-ttu-id="04497-104">Servizio dischi virtuali</span><span class="sxs-lookup"><span data-stu-id="04497-104">Virtual Disk Service</span></span>

<span data-ttu-id="04497-105">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia COM del servizio dischi virtuali viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04497-105">\[Beginning with Windows 8 and Windows Server 2012, the Virtual Disk Service COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="04497-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="04497-106">Purpose</span></span>

<span data-ttu-id="04497-107">Il servizio dischi virtuali (VDS) gestisce un'ampia gamma di configurazioni di archiviazione, da desktop su disco singolo ad array di archiviazione esterni.</span><span class="sxs-lookup"><span data-stu-id="04497-107">The Virtual Disk Service (VDS) manages a wide range of storage configurations, from single-disk desktops to external storage arrays.</span></span> <span data-ttu-id="04497-108">Il servizio espone un Application Programming Interface (API).</span><span class="sxs-lookup"><span data-stu-id="04497-108">The service exposes an application programming interface (API).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="04497-109">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="04497-109">Where applicable</span></span>

<span data-ttu-id="04497-110">A partire da Windows 8 e Windows Server 8, l'interfaccia COM del servizio dischi virtuali viene sostituita dall'API di gestione dell'archiviazione, un'interfaccia di programmazione basata su WMI.</span><span class="sxs-lookup"><span data-stu-id="04497-110">Beginning with Windows 8 and Windows Server 8, the Virtual Disk Service COM interface is superseded by the Storage Management API, a WMI-based programming interface.</span></span> <span data-ttu-id="04497-111">Per gestire i sottosistemi di archiviazione (Windows), i dischi, le partizioni e i volumi, si consiglia vivamente di usare l'API di gestione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="04497-111">For managing storage subsystems, (Windows) disks, partitions, and volumes, we strongly recommend using the Storage Management API.</span></span> <span data-ttu-id="04497-112">Per ulteriori informazioni, vedere l' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span><span class="sxs-lookup"><span data-stu-id="04497-112">For more information, see the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).</span></span>

<span data-ttu-id="04497-113">Per tutti gli utilizzi tranne i volumi di avvio speculare (usando un volume mirror per ospitare il sistema operativo), i dischi dinamici sono deprecati.</span><span class="sxs-lookup"><span data-stu-id="04497-113">For all usages except mirror boot volumes (using a mirror volume to host the operating system ), dynamic disks are deprecated.</span></span> <span data-ttu-id="04497-114">Per i dati che richiedono resilienza in caso di errore dell'unità, usare spazi di archiviazione, una soluzione di virtualizzazione dell'archiviazione resiliente.</span><span class="sxs-lookup"><span data-stu-id="04497-114">For data that requires resiliency against drive failure, use Storage Spaces, a resilient storage virtualization solution.</span></span> <span data-ttu-id="04497-115">Per altre informazioni, vedere [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="04497-115">For more information, see [Storage Spaces Technical Preview](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831739(v=ws.11)).</span></span>

<span data-ttu-id="04497-116">Gli sviluppatori di applicazioni che utilizzano le interfacce descritte in questa guida possono eseguire query e configurare un set eterogeneo di archiviazione gestita internamente e fornita dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="04497-116">Application developers who use the interfaces described in this guide can query and configure a heterogeneous set of vendor-supplied and internally managed storage.</span></span> <span data-ttu-id="04497-117">VDS nasconde dalle applicazioni le complessità associate all'archiviazione, rendendo il servizio sia indipendente dal fornitore che dalla tecnologia.</span><span class="sxs-lookup"><span data-stu-id="04497-117">VDS hides from applications the complexities associated with storage, making the service both vendor and technology neutral.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="04497-118">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="04497-118">Developer audience</span></span>

<span data-ttu-id="04497-119">Questa documentazione è destinata agli sviluppatori di applicazioni che hanno familiarità con le funzionalità di archiviazione delle piattaforme Microsoft Windows e che conoscono lo sviluppo COM.</span><span class="sxs-lookup"><span data-stu-id="04497-119">This documentation is intended for application developers who are familiar with the storage capabilities of Microsoft Windows platforms and who are knowledgeable about COM development.</span></span>

<span data-ttu-id="04497-120">La guida è destinata anche ai produttori di sottosistemi hardware che sviluppano e supportano i programmi del provider hardware VDS.</span><span class="sxs-lookup"><span data-stu-id="04497-120">The guide is also intended for hardware subsystem manufacturers who develop and support VDS hardware provider programs.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="04497-121">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="04497-121">Run-time requirements</span></span>

<span data-ttu-id="04497-122">VDS è supportato in Windows Server 2003, Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="04497-122">VDS is supported on Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="04497-123">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della documentazione relativa a tale elemento.</span><span class="sxs-lookup"><span data-stu-id="04497-123">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="04497-124">L'esecuzione di applicazioni VDS a 32 bit in WOW64 è supportata, ma i provider VDS a 64 bit devono essere eseguiti come applicazioni native nelle versioni di Windows a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="04497-124">Running 32-bit VDS applications under WOW64 is supported, but 64-bit VDS providers must run as native applications on 64-bit Windows versions.</span></span>

<span data-ttu-id="04497-125">VDS è disponibile nel Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="04497-125">VDS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="04497-126">È possibile installare l'SDK per Windows 7 e Windows Server 2008 R2 dall' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="04497-126">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="04497-127">Questa versione di Windows SDK può essere usata per sviluppare applicazioni VDS per Windows Server 2003, Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="04497-127">This version of the Windows SDK can be used to develop VDS applications for Windows Server 2003, Windows Vista, and later.</span></span> <span data-ttu-id="04497-128">È anche possibile scaricare la [versione ISO](https://www.microsoft.com/download/details.aspx?id=8442) dell'SDK dall'area download di Windows.</span><span class="sxs-lookup"><span data-stu-id="04497-128">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="04497-129">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="04497-129">In this section</span></span>



| <span data-ttu-id="04497-130">Argomento</span><span class="sxs-lookup"><span data-stu-id="04497-130">Topic</span></span>                                         | <span data-ttu-id="04497-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04497-131">Description</span></span>                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04497-132">Informazioni su VDS</span><span class="sxs-lookup"><span data-stu-id="04497-132">About VDS</span></span>](about-vds.md)<br/>         | <span data-ttu-id="04497-133">Descrive il modello a oggetti VDS, le strategie di configurazione dell'archiviazione e le notifiche VDS.</span><span class="sxs-lookup"><span data-stu-id="04497-133">Describes the VDS object model, storage-configuration strategies, and VDS notifications.</span></span><br/>    |
| [<span data-ttu-id="04497-134">Uso di VDS</span><span class="sxs-lookup"><span data-stu-id="04497-134">Using VDS</span></span>](using-vds.md)<br/>         | <span data-ttu-id="04497-135">Viene descritto come utilizzare VDS per eseguire query e configurare i dispositivi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="04497-135">Describes how to use VDS to query and configure storage devices.</span></span><br/>                            |
| [<span data-ttu-id="04497-136">Riferimento VDS</span><span class="sxs-lookup"><span data-stu-id="04497-136">VDS Reference</span></span>](vds-reference.md)<br/> | <span data-ttu-id="04497-137">Descrive le costanti VDS, i tipi di dati, le enumerazioni, le interfacce, le strutture e i codici di errore.</span><span class="sxs-lookup"><span data-stu-id="04497-137">Describes VDS constants, data types, enumerations, interfaces, structures, and error codes.</span></span><br/> |



 

 

