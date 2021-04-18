---
description: Un oggetto pool di archiviazione modella un pool di archiviazione in un sottosistema di archiviazione.
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: Oggetto pool di archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318592"
---
# <a name="storage-pool-object"></a><span data-ttu-id="16dd5-103">Oggetto pool di archiviazione</span><span class="sxs-lookup"><span data-stu-id="16dd5-103">Storage Pool Object</span></span>

<span data-ttu-id="16dd5-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="16dd5-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="16dd5-105">Un oggetto pool di archiviazione modella un pool di archiviazione in un sottosistema di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="16dd5-105">A storage pool object models a storage pool in a storage subsystem.</span></span>

<span data-ttu-id="16dd5-106">Un pool di archiviazione contiene extent di unità da una o più unità gestite dallo stesso provider hardware.</span><span class="sxs-lookup"><span data-stu-id="16dd5-106">A storage pool contains drive extents from one or more drives that are managed by the same hardware provider.</span></span>

<span data-ttu-id="16dd5-107">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="16dd5-107">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="16dd5-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="16dd5-108">Type</span></span>                                              | <span data-ttu-id="16dd5-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="16dd5-109">Element</span></span>                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16dd5-110">Interfacce sempre esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="16dd5-110">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="16dd5-111">**IVdsStoragePool**</span><span class="sxs-lookup"><span data-stu-id="16dd5-111">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| <span data-ttu-id="16dd5-112">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="16dd5-112">Associated enumerations</span></span>                           | <span data-ttu-id="16dd5-113">[**VDS \_ \_Tipo di RAID**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**\_ \_ \_ stato del pool di archiviazione VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)e [**\_ \_ \_ tipo di pool di archiviazione VDS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span><span class="sxs-lookup"><span data-stu-id="16dd5-113">[**VDS\_RAID\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type), [**VDS\_STORAGE\_POOL\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status), and [**VDS\_STORAGE\_POOL\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type).</span></span>                                                                                                                                  |
| <span data-ttu-id="16dd5-114">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="16dd5-114">Associated structures</span></span>                             | <span data-ttu-id="16dd5-115">[**VDS \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**\_ \_ attributi del pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**\_ \_ \_ attributi personalizzati del pool VDS**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**\_ \_ \_ \_ extent dell'unità del pool di archiviazione VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)e la [**\_ \_ \_ prop del pool di archiviazione VDS**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span><span class="sxs-lookup"><span data-stu-id="16dd5-115">[**VDS\_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2), [**VDS\_POOL\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes), [**VDS\_POOL\_CUSTOM\_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes), [**VDS\_STORAGE\_POOL\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent), and [**VDS\_STORAGE\_POOL\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop).</span></span> |



 

 

 
