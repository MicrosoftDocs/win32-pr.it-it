---
description: Rienumerazione e aggiornamento
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Rienumerazione e aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313247"
---
# <a name="reenumerating-and-refreshing"></a><span data-ttu-id="01a63-103">Rienumerazione e aggiornamento</span><span class="sxs-lookup"><span data-stu-id="01a63-103">Reenumerating and Refreshing</span></span>

<span data-ttu-id="01a63-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="01a63-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="01a63-105">L'operazione di rienumerazione individua dispositivi appena connessi e appena disconnessi.</span><span class="sxs-lookup"><span data-stu-id="01a63-105">The reenumeration operation discovers newly connected and newly disconnected devices.</span></span> <span data-ttu-id="01a63-106">L'operazione di aggiornamento aggiorna le informazioni di configurazione dei dispositivi esistenti.</span><span class="sxs-lookup"><span data-stu-id="01a63-106">The refresh operation updates the configuration information of existing devices.</span></span>

<span data-ttu-id="01a63-107">**Per rienumerare gli oggetti provider software**</span><span class="sxs-lookup"><span data-stu-id="01a63-107">**To reenumerate software provider objects**</span></span>

-   <span data-ttu-id="01a63-108">Chiamare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="01a63-108">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method.</span></span> <span data-ttu-id="01a63-109">Questo metodo individua tutti i dischi e le unità CD-ROM appena connesse e disconnesse e garantisce che tutti i dischi dispongano del proprietario appropriato.</span><span class="sxs-lookup"><span data-stu-id="01a63-109">This method discovers all newly connected and disconnected disks and CD-ROM drives, and ensures that all disks have the proper owner.</span></span> <span data-ttu-id="01a63-110">VDS possiede dischi RAW o dischi con errori; il provider Basic possiede i dischi di base; e il provider dinamico possiede dischi dinamici.</span><span class="sxs-lookup"><span data-stu-id="01a63-110">VDS owns raw disks or disks with failures; the basic provider owns basic disks; and the dynamic provider owns dynamic disks.</span></span> <span data-ttu-id="01a63-111">Questa operazione può implicare l'analisi dei bus di sottosistema interni e l'attesa di timeout.</span><span class="sxs-lookup"><span data-stu-id="01a63-111">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="01a63-112">**Per rienumerare e aggiornare gli oggetti provider software**</span><span class="sxs-lookup"><span data-stu-id="01a63-112">**To reenumerate and refresh software provider objects**</span></span>

-   <span data-ttu-id="01a63-113">Chiamare il metodo [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) , quindi chiamare il metodo [**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) .</span><span class="sxs-lookup"><span data-stu-id="01a63-113">Call the [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) method and then call the [**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) method.</span></span> <span data-ttu-id="01a63-114">Oltre a individuare i dischi appena connessi e disconnessi e le unità CD-ROM, questa combinazione di metodi Aggiorna tutte le informazioni su disco, volume e Plex nella cache VDS per i dischi che non sono stati connessi o disconnessi di recente.</span><span class="sxs-lookup"><span data-stu-id="01a63-114">In addition to discovering newly connected and disconnected disks and CD-ROM drives, this combination of methods updates all disk, volume, and plex information in the VDS cache for disks that have not been recently connected or disconnected.</span></span> <span data-ttu-id="01a63-115">Chiamare solo **Refresh** per aggiornare le informazioni sulle proprietà degli oggetti esistenti nella cache.</span><span class="sxs-lookup"><span data-stu-id="01a63-115">Call **Refresh** alone to refresh the property information of existing objects in the cache.</span></span> <span data-ttu-id="01a63-116">Questa operazione può implicare l'analisi dei bus di sottosistema interni e l'attesa di timeout.</span><span class="sxs-lookup"><span data-stu-id="01a63-116">This operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span> <span data-ttu-id="01a63-117">Si noti che VDS aggiorna automaticamente la cache ogni volta che viene apportata una modifica che attiva una notifica.</span><span class="sxs-lookup"><span data-stu-id="01a63-117">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="01a63-118">Inoltre, la chiamata di **Refresh** in risposta a una notifica VDS potrebbe causare l'invio di un ciclo infinito di notifiche.</span><span class="sxs-lookup"><span data-stu-id="01a63-118">Also, calling **Refresh** in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="01a63-119">Per questi motivi, è consigliabile chiamare **Refresh** solo quando sembra che la cache non venga aggiornata correttamente.</span><span class="sxs-lookup"><span data-stu-id="01a63-119">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

<span data-ttu-id="01a63-120">**Per rienumerare i sottosistemi hardware**</span><span class="sxs-lookup"><span data-stu-id="01a63-120">**To reenumerate hardware subsystems**</span></span>

-   <span data-ttu-id="01a63-121">Chiamare il metodo [**IVdsHwProvider:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) .</span><span class="sxs-lookup"><span data-stu-id="01a63-121">Call the [**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) method.</span></span> <span data-ttu-id="01a63-122">A seconda del provider, questa operazione può implicare l'invio di pacchetti di rete e l'attesa di timeout, la ripetizione dell'analisi dei bus SCSI e l'attesa di timeout e così via.</span><span class="sxs-lookup"><span data-stu-id="01a63-122">Depending on the provider, this operation can involve sending network packets and waiting for time-outs, rescanning SCSI buses and waiting for time-outs, and so on.</span></span>

<span data-ttu-id="01a63-123">**Per rienumerare gli oggetti del sottosistema hardware**</span><span class="sxs-lookup"><span data-stu-id="01a63-123">**To reenumerate hardware subsystem objects**</span></span>

-   <span data-ttu-id="01a63-124">Chiamare il metodo [**IVdsSubSystem:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) per eseguire l'inventario degli oggetti (in genere unità) nel sottosistema.</span><span class="sxs-lookup"><span data-stu-id="01a63-124">Call the [**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) method to inventory the objects (typically drives) in the subsystem.</span></span> <span data-ttu-id="01a63-125">A seconda del sottosistema, questa operazione può comportare l'analisi di bus di sottosistema interni e l'attesa di timeout.</span><span class="sxs-lookup"><span data-stu-id="01a63-125">Depending on the subsystem, this operation can involve scanning internal subsystem buses and waiting for time-outs.</span></span>

<span data-ttu-id="01a63-126">**Per aggiornare sottosistemi hardware e oggetti sottosistema**</span><span class="sxs-lookup"><span data-stu-id="01a63-126">**To refresh hardware subsystems and subsystem objects**</span></span>

-   <span data-ttu-id="01a63-127">Chiamare il metodo [**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) per aggiornare la cache VDS delle informazioni sui sottosistemi esistenti gestiti dai provider hardware VDS.</span><span class="sxs-lookup"><span data-stu-id="01a63-127">Call the [**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) method to refresh the VDS cache of information about existing subsystems that are managed by VDS hardware providers.</span></span> <span data-ttu-id="01a63-128">Si noti che VDS aggiorna automaticamente la cache ogni volta che viene apportata una modifica che attiva una notifica.</span><span class="sxs-lookup"><span data-stu-id="01a63-128">Note that VDS updates the cache automatically whenever a change occurs that triggers a notification.</span></span> <span data-ttu-id="01a63-129">Inoltre, la chiamata di [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in risposta a una notifica VDS potrebbe causare l'invio di un ciclo infinito di notifiche.</span><span class="sxs-lookup"><span data-stu-id="01a63-129">Also, calling [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) in response to a VDS notification could cause an endless loop of notifications to be sent.</span></span> <span data-ttu-id="01a63-130">Per questi motivi, è consigliabile chiamare **Refresh** solo quando sembra che la cache non venga aggiornata correttamente.</span><span class="sxs-lookup"><span data-stu-id="01a63-130">For these reasons, **Refresh** should be called only when it appears that the cache is not being updated properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01a63-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01a63-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a63-132">Uso di VDS</span><span class="sxs-lookup"><span data-stu-id="01a63-132">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="01a63-133">**IVdsService:: Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="01a63-133">**IVdsService::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[<span data-ttu-id="01a63-134">**IVdsService:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="01a63-134">**IVdsService::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[<span data-ttu-id="01a63-135">**IVdsHwProvider:: Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="01a63-135">**IVdsHwProvider::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[<span data-ttu-id="01a63-136">**IVdsSubSystem:: Reenumerate**</span><span class="sxs-lookup"><span data-stu-id="01a63-136">**IVdsSubSystem::Reenumerate**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[<span data-ttu-id="01a63-137">**IVdsHwProvider:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="01a63-137">**IVdsHwProvider::Refresh**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
