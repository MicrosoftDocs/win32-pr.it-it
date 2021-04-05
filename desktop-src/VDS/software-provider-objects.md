---
description: Oggetti provider di software
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: Oggetti provider di software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16f81cd975c892760d1851720e65584453e7745
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "103885895"
---
# <a name="software-provider-objects"></a><span data-ttu-id="e2314-103">Oggetti provider di software</span><span class="sxs-lookup"><span data-stu-id="e2314-103">Software Provider Objects</span></span>

<span data-ttu-id="e2314-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e2314-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e2314-105">Gli oggetti del provider di software modellano i dispositivi fisici, ad esempio dischi IDE e CD-ROM, ed elementi virtuali come pacchetti, volumi e Plex del volume.</span><span class="sxs-lookup"><span data-stu-id="e2314-105">Software provider objects model physical devices, such as IDE disks and CD-ROMs, and virtual elements like packs, volumes, and volume plexes.</span></span> <span data-ttu-id="e2314-106">Nella figura seguente viene illustrata la relazione tra l'oggetto provider e il set di oggetti provider software, nonché la relazione tra i vari oggetti provider di software.</span><span class="sxs-lookup"><span data-stu-id="e2314-106">The following illustration shows the relationship between the provider object and the set of software provider objects, as well as the relationship between the various software provider objects themselves.</span></span>

![Diagramma che mostra la relazione tra gli oggetti ' provider ' e provider software, ad esempio ' Pack ' è volume '.](images/vdsswobjects.png)

<span data-ttu-id="e2314-108">Un oggetto provider può contenere zero o più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="e2314-108">A provider object can contain zero or more packs.</span></span> <span data-ttu-id="e2314-109">Un oggetto Pack può contenere zero o più dischi e volumi.</span><span class="sxs-lookup"><span data-stu-id="e2314-109">A pack object can contain zero or more disks and volumes.</span></span> <span data-ttu-id="e2314-110">Un volume è costituito da almeno un plex del volume e ogni volume Plex può essere mappato a uno o più dischi, a seconda del tipo di Plex.</span><span class="sxs-lookup"><span data-stu-id="e2314-110">A volume comprises of at least one volume plex and each volume plex can map to one or more disks, depending on the plex type.</span></span> <span data-ttu-id="e2314-111">VDS gestisce i dischi non allocati direttamente, senza un contenitore Pack.</span><span class="sxs-lookup"><span data-stu-id="e2314-111">VDS manages unallocated disks directly, without a pack container.</span></span> <span data-ttu-id="e2314-112">Gli argomenti rimanenti di questa sezione descrivono gli oggetti Pack, disk, volume e Plex del volume.</span><span class="sxs-lookup"><span data-stu-id="e2314-112">The remaining topics of this section describe the pack, disk, volume, and volume plex objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2314-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2314-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2314-114">Modello a oggetti VDS</span><span class="sxs-lookup"><span data-stu-id="e2314-114">VDS Object Model</span></span>](vds-object-model.md)
</dt> </dl>

 

 
