---
description: Panoramica della configurazione
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Panoramica della configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966612"
---
# <a name="configuration-overview"></a><span data-ttu-id="1d794-103">Panoramica della configurazione</span><span class="sxs-lookup"><span data-stu-id="1d794-103">Configuration Overview</span></span>

<span data-ttu-id="1d794-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1d794-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="1d794-105">Se non si ha familiarità con gli oggetti definiti da VDS, vedere il [modello a oggetti VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="1d794-105">If you are unfamiliar with the objects that are defined by VDS, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="1d794-106">La complessità della configurazione di un disco virtuale può variare da molto semplice a ottimizzata.</span><span class="sxs-lookup"><span data-stu-id="1d794-106">The configuration complexity of a virtual disk can range from very simple to finely tuned.</span></span> <span data-ttu-id="1d794-107">I dischi virtuali dell'organizzazione e della cura gratuita definiscono tre prospettive di configurazione tipiche.</span><span class="sxs-lookup"><span data-stu-id="1d794-107">No-care, free-from-care, and enterprise virtual disks define three typical configuration perspectives.</span></span> <span data-ttu-id="1d794-108">Ogni prospettiva presenta requisiti leggermente diversi:</span><span class="sxs-lookup"><span data-stu-id="1d794-108">Each perspective presents somewhat different requirements:</span></span>

-   <span data-ttu-id="1d794-109">I dischi virtuali senza assistenza sono configurati in modo leggero, forse solo per automatizzare il partizionamento e la formattazione dei nuovi dischi o per creare temporaneamente un volume con mirroring per la migrazione dei dati da un disco a un altro senza tempi di inattività.</span><span class="sxs-lookup"><span data-stu-id="1d794-109">No-care virtual disks are lightly configured, perhaps only to automate the partitioning and formatting of new disks, or to temporarily create a mirrored volume for migrating data from one disk to another without downtime.</span></span> <span data-ttu-id="1d794-110">Tali dischi sono utili per i computer notebook e altri sistemi con uno o pochi dischi.</span><span class="sxs-lookup"><span data-stu-id="1d794-110">Such disks are good for notebook computers and other systems with one or a few disks.</span></span>
-   <span data-ttu-id="1d794-111">I dischi virtuali free-from-Care forniscono archiviazione con configurazione automatica, correzione automatica e disponibilità. USA i volumi con striping e i LUN per ottenere prestazioni migliori. USA volumi e lun con mirroring per ottenere una migliore disponibilità; e usa i pacchetti per rendere le modalità di errore pulita e contenuta.</span><span class="sxs-lookup"><span data-stu-id="1d794-111">Free-from-care virtual disks provide storage that appears self-configuring, self-healing, and available; uses striped volumes and LUNs to achieve better performance; uses mirrored volumes and LUNs to achieve better availability; and uses packs to make the failure modes clean and contained.</span></span> <span data-ttu-id="1d794-112">Questo livello di configurazione è ideale quando si sostituiscono dischi di sistema vecchi, piccoli e lenti con nuovi dischi veloci e di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1d794-112">This configuration level is ideal when replacing old, small, slow system disks with new, large, fast disks is routine.</span></span> <span data-ttu-id="1d794-113">È ideale anche per il mirroring dei dati con la disattivazione a caldo automatica: un singolo mandrino di riserva può proteggere molti assi.</span><span class="sxs-lookup"><span data-stu-id="1d794-113">It is also ideal for mirroring data with automated hot sparing—a single spare spindle can protect many spindles.</span></span> <span data-ttu-id="1d794-114">Per informazioni dettagliate, vedere [Hot Spare](hot-sparing.md).</span><span class="sxs-lookup"><span data-stu-id="1d794-114">For details, see [Hot Sparing](hot-sparing.md).</span></span>

    <span data-ttu-id="1d794-115">I San con scalabilità ridotta dipendono dalla flessibilità e dall'automazione offerti da questo livello di configurazione, così come gli appliance di archiviazione collegata alla rete (NAS).</span><span class="sxs-lookup"><span data-stu-id="1d794-115">Small-scale SANs depend on the flexibility and automation that is offered by this configuration level, as do Network Attached Storage (NAS) appliances.</span></span> <span data-ttu-id="1d794-116">I dischi virtuali free-from-care semplificano l'attività di consolidamento dell'archiviazione dell'applicazione, ad esempio l'archiviazione per SQL e Exchange, senza consolidare i server.</span><span class="sxs-lookup"><span data-stu-id="1d794-116">Free-from-care virtual disks simplify the task of consolidating application storage—for example, the storage for SQL and Exchange—without consolidating the servers.</span></span>

-   <span data-ttu-id="1d794-117">I dischi virtuali aziendali contengono configurazioni aziendali molto grandi o complesse con requisiti aggiuntivi specifici del sito o dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d794-117">Enterprise virtual disks contain very large or complex enterprise configurations with additional site-specific or application-specific requirements.</span></span> <span data-ttu-id="1d794-118">Gli amministratori ottimizzano il sottosistema di archiviazione per una singola applicazione che può essere eseguita solo raramente, ad esempio un processo di creazione di report batch mensile in un sistema di transazione per l'esecuzione di ordini.</span><span class="sxs-lookup"><span data-stu-id="1d794-118">Administrators tune the storage subsystem for a single application that might run only infrequently, such as a monthly batch reporting job on an order-taking transaction system.</span></span> <span data-ttu-id="1d794-119">È necessario che i dischi virtuali aziendali siano ridimensionati, mostrino l'attività in tempo reale del sottosistema di archiviazione e soddisfino i requisiti degli amministratori pratici.</span><span class="sxs-lookup"><span data-stu-id="1d794-119">Enterprise virtual disks must scale, show the real-time activity of the storage subsystem, and satisfy the requirements of hands-on administrators.</span></span>

<span data-ttu-id="1d794-120">Per altre informazioni sui mirror, sulle strisce e sulle altre opzioni di configurazione in VDS, vedere [binding di volumi e lun](volume-and-lun-binding.md).</span><span class="sxs-lookup"><span data-stu-id="1d794-120">For additional information about mirrors, stripes, and the other configuration options in VDS, see [Volume and LUN Binding](volume-and-lun-binding.md).</span></span> <span data-ttu-id="1d794-121">Una tecnica di configurazione avanzata, denominata stacking, consente di combinare le configurazioni associate a volumi e lun esistenti.</span><span class="sxs-lookup"><span data-stu-id="1d794-121">An advanced configuration technique, called stacking, enables you to combine the configurations that are associated with existing volumes and LUNs.</span></span> <span data-ttu-id="1d794-122">Per informazioni dettagliate, vedere [stack di configurazione](configuration-stacking.md).</span><span class="sxs-lookup"><span data-stu-id="1d794-122">For details, see [Configuration Stacking](configuration-stacking.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d794-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d794-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d794-124">Servizio dischi virtuali</span><span class="sxs-lookup"><span data-stu-id="1d794-124">Virtual Disk Service</span></span>](virtual-disk-service-portal.md)
</dt> <dt>

[<span data-ttu-id="1d794-125">Modello a oggetti VDS</span><span class="sxs-lookup"><span data-stu-id="1d794-125">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="1d794-126">Hot Spare</span><span class="sxs-lookup"><span data-stu-id="1d794-126">Hot Sparing</span></span>](hot-sparing.md)
</dt> <dt>

[<span data-ttu-id="1d794-127">Binding di volumi e LUN</span><span class="sxs-lookup"><span data-stu-id="1d794-127">Volume and LUN Binding</span></span>](volume-and-lun-binding.md)
</dt> <dt>

[<span data-ttu-id="1d794-128">Stack di configurazione</span><span class="sxs-lookup"><span data-stu-id="1d794-128">Configuration Stacking</span></span>](configuration-stacking.md)
</dt> </dl>

 

 
