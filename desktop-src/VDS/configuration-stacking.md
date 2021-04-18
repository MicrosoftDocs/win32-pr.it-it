---
description: Stack di configurazione
ms.assetid: 1f0f75d6-3553-4ee1-8ee6-bd617da4a109
title: Stack di configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b50b90629556b5ed00db712b49fe8fa4e48ea8cc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566510"
---
# <a name="configuration-stacking"></a><span data-ttu-id="6d139-103">Stack di configurazione</span><span class="sxs-lookup"><span data-stu-id="6d139-103">Configuration Stacking</span></span>

<span data-ttu-id="6d139-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d139-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="6d139-105">Lo stacking prevede la concatenazione di un set di mapping dei blocchi logici.</span><span class="sxs-lookup"><span data-stu-id="6d139-105">Stacking involves the concatenating of a set of logical block mappings.</span></span> <span data-ttu-id="6d139-106">È possibile impilare più lun dallo stesso sottosistema in un LUN.</span><span class="sxs-lookup"><span data-stu-id="6d139-106">You can stack multiple LUNs from the same subsystem under one LUN.</span></span> <span data-ttu-id="6d139-107">È possibile impilare un LUN insieme ai volumi dello stesso pacchetto in un volume.</span><span class="sxs-lookup"><span data-stu-id="6d139-107">You can stack a LUN together with volumes from the same pack under one volume.</span></span> <span data-ttu-id="6d139-108">Inoltre, è possibile sovrapporre più LUN esposti da sottosistemi eterogenei in un volume.</span><span class="sxs-lookup"><span data-stu-id="6d139-108">Further, you can stack multiple LUNs that are surfaced by heterogeneous subsystems under one volume.</span></span>

<span data-ttu-id="6d139-109">Come illustrato nella figura seguente, la creazione di un volume non comporta la modifica dell'associazione esistente di un LUN che contribuisce.</span><span class="sxs-lookup"><span data-stu-id="6d139-109">As the following illustration shows, the creating of a volume does not change the existing binding of a contributing LUN.</span></span> <span data-ttu-id="6d139-110">Analogamente, l'annullamento dell'associazione di un volume non associa un LUN di contributo.</span><span class="sxs-lookup"><span data-stu-id="6d139-110">Similarly, the unbinding of a volume does not unbind a contributing LUN.</span></span> <span data-ttu-id="6d139-111">Nella figura è illustrata la configurazione RAID 0 1 (0 + 1).</span><span class="sxs-lookup"><span data-stu-id="6d139-111">The illustration depicts the RAID 0 1 (0+1) configuration.</span></span> <span data-ttu-id="6d139-112">Questa configurazione ben nota combina lo striping (RAID 0) e il mirroring (RAID 1), che abbina l'accesso rapido ai dati di RAID 0 con l'affidabilità di RAID 1.</span><span class="sxs-lookup"><span data-stu-id="6d139-112">This well-known configuration combines striping (RAID 0) and mirroring (RAID 1), which pairs the fast data access of RAID 0 with the reliability of RAID 1.</span></span>

![Diagramma che mostra una configurazione RAID 0 1 (0 + 1).](images/vdsstacklunvolzeroplusone.png)

<span data-ttu-id="6d139-114">I LUN che contribuiscono possono avere tipi di binding diversi.</span><span class="sxs-lookup"><span data-stu-id="6d139-114">Contributing LUNs can have different binding types.</span></span> <span data-ttu-id="6d139-115">Molte configurazioni sono possibili con VDS, ma sono molto improbabili, come la figura successiva.</span><span class="sxs-lookup"><span data-stu-id="6d139-115">Many configurations are possible with VDS but are highly unlikely, such as the next illustration.</span></span> <span data-ttu-id="6d139-116">In questo esempio un volume Plex è un LUN con striping e l'altro è un LUN con mirroring a tre vie.</span><span class="sxs-lookup"><span data-stu-id="6d139-116">In this example, one volume plex is a striped LUN and the other is a three-way mirrored LUN.</span></span>

![Diagramma che mostra una configurazione VDS in cui un plex del volume è un LUN con striping e l'altro è un LUN con mirroring a tre vie.](images/vdsstacklunvol.png)

<span data-ttu-id="6d139-118">Sebbene non pratico, in questo esempio viene illustrato un aspetto importante dello stacking.</span><span class="sxs-lookup"><span data-stu-id="6d139-118">Although impractical, this example illustrates an important aspect of stacking.</span></span> <span data-ttu-id="6d139-119">Poiché lo stacking concatena i plex, VDS aggiunge i tre Plex di LUN ai due plex del volume per un totale di cinque Plex.</span><span class="sxs-lookup"><span data-stu-id="6d139-119">Because stacking concatenates plexes, VDS adds the three LUN plexes to the two volume plexes for a total of five plexes.</span></span>

 

 
