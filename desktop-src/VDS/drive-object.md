---
description: Oggetto unità
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: Oggetto unità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df8501c79f9381dba80a1fe0276014dccdf7a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231681"
---
# <a name="drive-object"></a><span data-ttu-id="6435e-103">Oggetto unità</span><span class="sxs-lookup"><span data-stu-id="6435e-103">Drive Object</span></span>

<span data-ttu-id="6435e-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6435e-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="6435e-105">Un oggetto unità modella un'unità disco fisica che è contenuta all'interno di un sottosistema.</span><span class="sxs-lookup"><span data-stu-id="6435e-105">A drive object models a physical disk drive that is contained within a subsystem.</span></span> <span data-ttu-id="6435e-106">Ogni unità si connette a un bus, occupa uno slot e contiene un set di extent di unità.</span><span class="sxs-lookup"><span data-stu-id="6435e-106">Each drive connects to a bus, occupies a slot, and contains a set of drive extents.</span></span> <span data-ttu-id="6435e-107">Ogni unità può contribuire a un numero qualsiasi di lun.</span><span class="sxs-lookup"><span data-stu-id="6435e-107">Each drive can contribute extents to any number of LUNs.</span></span> <span data-ttu-id="6435e-108">Un'unità può anche essere designata come riserva a caldo.</span><span class="sxs-lookup"><span data-stu-id="6435e-108">A drive can also be designated as a hot spare.</span></span>

<span data-ttu-id="6435e-109">Usare il metodo [**IVdsSubSystem:: QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) per determinare le unità contenute in un sottosistema specifico.</span><span class="sxs-lookup"><span data-stu-id="6435e-109">Use the [**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) method to determine the drives that are contained by a specific subsystem.</span></span> <span data-ttu-id="6435e-110">I chiamanti possono ottenere un puntatore a un'unità specifica selezionando l'oggetto unità desiderato dall'enumerazione restituita dal metodo **QueryDrives** oppure richiamando il metodo [**IVdsSubSystem:: getdrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) e passando il bus e il numero di slot desiderati.</span><span class="sxs-lookup"><span data-stu-id="6435e-110">Callers can get a pointer to a specific drive by selecting the desired drive object from the enumeration that is returned by the **QueryDrives** method, or by invoking the [**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) method and passing in the desired bus and slot number.</span></span> <span data-ttu-id="6435e-111">Con un oggetto unità è possibile impostare lo stato dell'unità e la query per le proprietà dell'unità, gli extent di unità associati e il sottosistema che contiene l'unità.</span><span class="sxs-lookup"><span data-stu-id="6435e-111">With a drive object, you can set the drive status and query for drive properties, associated drive extents, and the subsystem containing the drive.</span></span>

<span data-ttu-id="6435e-112">Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto unità includono lo stato dell'unità, l'integrità e i flag. dimensioni in byte; e un bus e un numero di slot.</span><span class="sxs-lookup"><span data-stu-id="6435e-112">In addition to an object identifier, a name, and a serial number, drive object properties include the drive status, health, and flags; the size in bytes; and a bus and slot number.</span></span>

<span data-ttu-id="6435e-113">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="6435e-113">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="6435e-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="6435e-114">Type</span></span>                                              | <span data-ttu-id="6435e-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="6435e-115">Element</span></span>                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6435e-116">Interfacce sempre esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="6435e-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="6435e-117">**IVdsDrive**</span><span class="sxs-lookup"><span data-stu-id="6435e-117">**IVdsDrive**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| <span data-ttu-id="6435e-118">Interfacce che possono essere esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="6435e-118">Interfaces that may be exposed by this object</span></span>     | [<span data-ttu-id="6435e-119">**IVdsMaintenance**</span><span class="sxs-lookup"><span data-stu-id="6435e-119">**IVdsMaintenance**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| <span data-ttu-id="6435e-120">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="6435e-120">Associated enumerations</span></span>                           | <span data-ttu-id="6435e-121">[**VDS \_ \_Flag unità**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**\_ \_ stato unità VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)e [**\_ \_ extent unità VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span><span class="sxs-lookup"><span data-stu-id="6435e-121">[**VDS\_DRIVE\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag), [**VDS\_DRIVE\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status), and [**VDS\_DRIVE\_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent).</span></span> |
| <span data-ttu-id="6435e-122">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="6435e-122">Associated structures</span></span>                             | <span data-ttu-id="6435e-123">[**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) [**\_ \_ Notifica**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)dell'unità prop e VDS.</span><span class="sxs-lookup"><span data-stu-id="6435e-123">[**VDS\_DRIVE\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) and [**VDS\_DRIVE\_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6435e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6435e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6435e-125">Oggetti provider hardware</span><span class="sxs-lookup"><span data-stu-id="6435e-125">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="6435e-126">**IVdsSubSystem::QueryDrives**</span><span class="sxs-lookup"><span data-stu-id="6435e-126">**IVdsSubSystem::QueryDrives**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[<span data-ttu-id="6435e-127">**IVdsSubSystem:: getdrive**</span><span class="sxs-lookup"><span data-stu-id="6435e-127">**IVdsSubSystem::GetDrive**</span></span>](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
