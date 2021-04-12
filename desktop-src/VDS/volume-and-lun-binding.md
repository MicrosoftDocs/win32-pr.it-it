---
description: Binding di volumi e LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Binding di volumi e LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234412"
---
# <a name="volume-and-lun-binding"></a><span data-ttu-id="70c08-103">Binding di volumi e LUN</span><span class="sxs-lookup"><span data-stu-id="70c08-103">Volume and LUN Binding</span></span>

<span data-ttu-id="70c08-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="70c08-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="70c08-105">Il binding è la creazione di volumi o lun.</span><span class="sxs-lookup"><span data-stu-id="70c08-105">Binding is the creation of volumes or LUNs.</span></span> <span data-ttu-id="70c08-106">I volumi sono costituiti da extent del disco e lun sono costituiti da extent di unità.</span><span class="sxs-lookup"><span data-stu-id="70c08-106">Volumes consist of disk extents and LUNs consist of drive extents.</span></span> <span data-ttu-id="70c08-107">L'associazione seleziona per un set di mapping a risorse fisiche e si verifica all'interno di un sottosistema, all'interno di un pacchetto o in entrambi.</span><span class="sxs-lookup"><span data-stu-id="70c08-107">Binding selects for a set of mappings to physical resources and occurs within a subsystem, within a pack, or both.</span></span> <span data-ttu-id="70c08-108">Tutti i programmi del provider supportano l'associazione parzialmente diretta a un modello in cui il chiamante specifica solo gli attributi di binding di particolare interesse e consente al provider di scegliere il resto.</span><span class="sxs-lookup"><span data-stu-id="70c08-108">All provider programs support partially directed binding a model in which the caller specifies only those binding attributes of particular interest, and allows the provider to choose the rest.</span></span> <span data-ttu-id="70c08-109">Le operazioni in VDS per l'associazione di volumi e lun sono simili, ma non identiche.</span><span class="sxs-lookup"><span data-stu-id="70c08-109">The operations in VDS for binding volumes and LUNs are similar but not identical.</span></span> <span data-ttu-id="70c08-110">I provider hardware possono ad esempio offrire opzioni di associazione aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="70c08-110">For example, hardware providers can offer additional binding options.</span></span>

<span data-ttu-id="70c08-111">VDS supporta i cinque tipi di binding di volumi e LUN seguenti per le configurazioni parzialmente dirette.</span><span class="sxs-lookup"><span data-stu-id="70c08-111">VDS supports the following five volume and LUN binding types for partially directed configurations.</span></span> <span data-ttu-id="70c08-112">I provider di hardware possono e supportano molte altre associazioni.</span><span class="sxs-lookup"><span data-stu-id="70c08-112">(Hardware providers can and do support many other bindings.)</span></span>



| <span data-ttu-id="70c08-113">Termine</span><span class="sxs-lookup"><span data-stu-id="70c08-113">Term</span></span>                                                                                                                                             | <span data-ttu-id="70c08-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70c08-114">Description</span></span>                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c08-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Semplice</span><span class="sxs-lookup"><span data-stu-id="70c08-115"><span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple</span></span><br/>                                                     | <span data-ttu-id="70c08-116">Mapping lineare con un solo extent contiguo.</span><span class="sxs-lookup"><span data-stu-id="70c08-116">Linear mapping with one and only one contiguous extent.</span></span><br/>                             |
| <span data-ttu-id="70c08-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Con spanning</span><span class="sxs-lookup"><span data-stu-id="70c08-117"><span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Spanned</span></span><br/>                                                 | <span data-ttu-id="70c08-118">Mapping lineare con più extent non contigui tra più dischi o unità.</span><span class="sxs-lookup"><span data-stu-id="70c08-118">Linear mapping with multiple noncontiguous extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="70c08-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Strisce</span><span class="sxs-lookup"><span data-stu-id="70c08-119"><span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Striped</span></span><br/>                                                 | <span data-ttu-id="70c08-120">Mapping che interleave gli extent del volume contiguo tra più dischi o unità.</span><span class="sxs-lookup"><span data-stu-id="70c08-120">Mapping that interleaves contiguous volume extents across multiple disks or drives.</span></span><br/> |
| <span data-ttu-id="70c08-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Specchio</span><span class="sxs-lookup"><span data-stu-id="70c08-121"><span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Mirrored</span></span><br/>                                             | <span data-ttu-id="70c08-122">Mapping che gestisce due o più copie di dati identiche.</span><span class="sxs-lookup"><span data-stu-id="70c08-122">Mapping that maintains two or more identical data copies.</span></span><br/>                           |
| <span data-ttu-id="70c08-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Con striping con parità</span><span class="sxs-lookup"><span data-stu-id="70c08-123"><span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Striped with parity</span></span><br/> | <span data-ttu-id="70c08-124">Mapping che distribuisce le informazioni di controllo della parità tra più dischi o unità.</span><span class="sxs-lookup"><span data-stu-id="70c08-124">Mapping that distributes parity check information across multiple disks or drives.</span></span><br/>  |



 

<span data-ttu-id="70c08-125">VDS costruisce con mirroring, con striping e con striping con binding di parità da più di un membro.</span><span class="sxs-lookup"><span data-stu-id="70c08-125">VDS constructs mirrored, striped, and striped with parity bindings from more than one member.</span></span> <span data-ttu-id="70c08-126">Ad esempio, un mirroring a due vie ha due membri.</span><span class="sxs-lookup"><span data-stu-id="70c08-126">For example, a two-way mirror has two members.</span></span> <span data-ttu-id="70c08-127">Ogni membro può occupare extent in più dischi o unità.</span><span class="sxs-lookup"><span data-stu-id="70c08-127">Each member can occupy extents on more than one disk or drive.</span></span> <span data-ttu-id="70c08-128">VDS concatena gli extent per formare il membro, quindi associa il volume o il LUN sui membri.</span><span class="sxs-lookup"><span data-stu-id="70c08-128">VDS concatenates the extents to form the member and then binds the volume or LUN on the members.</span></span> <span data-ttu-id="70c08-129">Un provider può supportare tutti i tipi di binding o qualsiasi subset.</span><span class="sxs-lookup"><span data-stu-id="70c08-129">A provider can support all binding types, or any subset.</span></span> <span data-ttu-id="70c08-130">Nel modello a oggetti VDS ogni membro di un mirror è un oggetto indipendente denominato Plex.</span><span class="sxs-lookup"><span data-stu-id="70c08-130">In the VDS object model, each member of a mirror is an independent object called a plex.</span></span>

<span data-ttu-id="70c08-131">Anche in questo caso i tipi di volume e LUN sono simili, ma non esatti.</span><span class="sxs-lookup"><span data-stu-id="70c08-131">Again, volume and LUN types are similar, but not exact.</span></span> <span data-ttu-id="70c08-132">Per una descrizione dei tipi di volume, vedere l' [oggetto volume](volume-object.md); per i tipi LUN, vedere l' [oggetto lun](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="70c08-132">For a description of volume types, see the [Volume Object](volume-object.md); for LUN types, see the [LUN Object](lun-object.md).</span></span> <span data-ttu-id="70c08-133">I tipi di binding non sono a tolleranza d'errore o a tolleranza di errore.</span><span class="sxs-lookup"><span data-stu-id="70c08-133">Binding types are either non-fault tolerant or fault tolerant.</span></span>

### <a name="non-fault-tolerant-binding"></a><span data-ttu-id="70c08-134">Associazione non a tolleranza di errore</span><span class="sxs-lookup"><span data-stu-id="70c08-134">Non-Fault Tolerant Binding</span></span>

<span data-ttu-id="70c08-135">I volumi e i LUN non a tolleranza di errore non offrono il ripristino di emergenza.</span><span class="sxs-lookup"><span data-stu-id="70c08-135">Non-fault tolerant volumes and LUNs do not offer disaster recovery.</span></span> <span data-ttu-id="70c08-136">Se uno degli assi che contribuiscono a un volume non a tolleranza di errore o a un LUN ha esito negativo, l'intero volume o LUN ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="70c08-136">If one of the spindles that contributes to a non-fault tolerant volume or LUN fails, the entire volume or LUN fails.</span></span> <span data-ttu-id="70c08-137">In Exchange il rischio per i dati, i volumi non a tolleranza di errore e i LUN offrono prestazioni di input/output generalmente superiori a quelle dei volumi e dei LUN a tolleranza di errore.</span><span class="sxs-lookup"><span data-stu-id="70c08-137">In exchange for the risk to data, non-fault tolerant volumes and LUNs offer input/output performance that is generally superior to that of fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="70c08-138">VDS supporta i tre tipi non a tolleranza di errore seguenti: semplice, con spanning e con striping.</span><span class="sxs-lookup"><span data-stu-id="70c08-138">VDS supports the following three non-fault tolerant types: simple, spanned, and striped.</span></span>

<span data-ttu-id="70c08-139">Semplice</span><span class="sxs-lookup"><span data-stu-id="70c08-139">Simple</span></span>

![Diagramma che mostra un tipo semplice a tolleranza non di errore con 2 pacchetti e 2 sottosistemi.](images/vdssimplelunvol.png)

<span data-ttu-id="70c08-141">Spanned</span><span class="sxs-lookup"><span data-stu-id="70c08-141">Spanned</span></span>

![Diagramma che mostra un tipo non a tolleranza di errore con spanning con 1 pacchetto e 1 sottosistema.](images/vdsspanlunvol.png)

<span data-ttu-id="70c08-143">Strisce</span><span class="sxs-lookup"><span data-stu-id="70c08-143">Striped</span></span>

![Diagramma che mostra un tipo a tolleranza non di errore con striping con 1 pacchetto e 1 sottosistema.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a><span data-ttu-id="70c08-145">Associazione a tolleranza di errore</span><span class="sxs-lookup"><span data-stu-id="70c08-145">Fault Tolerant Binding</span></span>

<span data-ttu-id="70c08-146">I seguenti volumi di errore e lun offrono il ripristino di emergenza.</span><span class="sxs-lookup"><span data-stu-id="70c08-146">The following fault tolerant volumes and LUNs offer disaster recovery.</span></span> <span data-ttu-id="70c08-147">Se uno degli assi che contribuiscono a un volume a tolleranza di errore o a un LUN ha esito negativo, è possibile recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="70c08-147">If one of the spindles that contributes to a fault tolerant volume or LUN fails, the data can be recovered.</span></span> <span data-ttu-id="70c08-148">In Exchange per la sicurezza dei dati, le prestazioni di input/output di volumi a tolleranza di errore e lun sono generalmente inferiori a quelle dei volumi e dei LUN non a tolleranza di errore.</span><span class="sxs-lookup"><span data-stu-id="70c08-148">In exchange for data security, the input/output performance of fault tolerant volumes and LUNs is generally inferior to that of non-fault tolerant volumes and LUNs.</span></span> <span data-ttu-id="70c08-149">VDS supporta due tipi di tolleranza di errore: con mirroring e con striping con parità.</span><span class="sxs-lookup"><span data-stu-id="70c08-149">VDS supports two fault tolerant types: mirrored and striped with parity.</span></span>

<span data-ttu-id="70c08-150">Con mirroring (mirroring a tre vie)</span><span class="sxs-lookup"><span data-stu-id="70c08-150">Mirrored (three-way mirror)</span></span>

![Diagramma che mostra un tipo a tolleranza di errore con mirroring (mirroring a 3 vie).](images/vdsmirrorlunvol.png)

<span data-ttu-id="70c08-152">Con striping con parità</span><span class="sxs-lookup"><span data-stu-id="70c08-152">Striped with parity</span></span>

![Diagramma che mostra un tipo a tolleranza di errore con striping con parità.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a><span data-ttu-id="70c08-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70c08-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70c08-155">Panoramica della configurazione</span><span class="sxs-lookup"><span data-stu-id="70c08-155">Configuration Overview</span></span>](configuration.md)
</dt> <dt>

[<span data-ttu-id="70c08-156">Oggetto volume</span><span class="sxs-lookup"><span data-stu-id="70c08-156">Volume Object</span></span>](volume-object.md)
</dt> <dt>

[<span data-ttu-id="70c08-157">LUN (oggetto)</span><span class="sxs-lookup"><span data-stu-id="70c08-157">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

