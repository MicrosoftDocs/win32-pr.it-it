---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Novità di VSS in Windows Server 2008 e Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129278"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="b0c60-103">Novità di VSS in Windows Server 2008 e Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="b0c60-103">What's New in VSS in Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="b0c60-104">Windows Server 2008 e Windows Vista con Service Pack 1 (SP1) introducono le seguenti modifiche al Servizio Copia Shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="b0c60-104">Windows Server 2008 and Windows Vista with Service Pack 1 (SP1) introduce the following changes to the Volume Shadow Copy Service.</span></span>

> [!Note]  
> <span data-ttu-id="b0c60-105">Tutte le modifiche per Windows Vista si applicano a Windows Server 2008 e Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="b0c60-105">All changes for Windows Vista apply to Windows Server 2008 and Windows Vista with SP1.</span></span> <span data-ttu-id="b0c60-106">Per informazioni dettagliate su tali modifiche, vedere Novità di [VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="b0c60-106">For details on those changes, see [What's New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span></span>

 

-   [<span data-ttu-id="b0c60-107">Nuove interfacce VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-107">New VSS Interfaces</span></span>](#new-vss-interfaces)
-   [<span data-ttu-id="b0c60-108">Nuove enumerazioni VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-108">New VSS Enumerations</span></span>](#new-vss-enumerations)
-   [<span data-ttu-id="b0c60-109">Nuove strutture VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-109">New VSS Structures</span></span>](#new-vss-structures)
-   [<span data-ttu-id="b0c60-110">Modifiche dell'enumerazione VSS esistenti</span><span class="sxs-lookup"><span data-stu-id="b0c60-110">Existing VSS Enumeration Modifications</span></span>](#existing-vss-enumeration-modifications)
-   [<span data-ttu-id="b0c60-111">Modifiche all'interfaccia VSS esistente</span><span class="sxs-lookup"><span data-stu-id="b0c60-111">Existing VSS Interface Modifications</span></span>](#existing-vss-interface-modifications)
-   [<span data-ttu-id="b0c60-112">Nuovi writer VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-112">New VSS Writers</span></span>](#new-vss-writers)

## <a name="new-vss-interfaces"></a><span data-ttu-id="b0c60-113">Nuove interfacce VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-113">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="b0c60-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="b0c60-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[<span data-ttu-id="b0c60-115">**IVssHardwareSnapshotProviderEx**</span><span class="sxs-lookup"><span data-stu-id="b0c60-115">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="b0c60-116">Nuove enumerazioni VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-116">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="b0c60-117">**\_\_Opzioni hardware \_ VSS**</span><span class="sxs-lookup"><span data-stu-id="b0c60-117">**\_VSS\_HARDWARE\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[<span data-ttu-id="b0c60-118">**\_errore di protezione VSS \_**</span><span class="sxs-lookup"><span data-stu-id="b0c60-118">**VSS\_PROTECTION\_FAULT**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[<span data-ttu-id="b0c60-119">**\_livello di protezione VSS \_**</span><span class="sxs-lookup"><span data-stu-id="b0c60-119">**VSS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a><span data-ttu-id="b0c60-120">Nuove strutture VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-120">New VSS Structures</span></span>

<dl>

[<span data-ttu-id="b0c60-121">**\_informazioni sulla \_ protezione del volume VSS \_**</span><span class="sxs-lookup"><span data-stu-id="b0c60-121">**VSS\_VOLUME\_PROTECTION\_INFO**</span></span>](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="b0c60-122">Modifiche dell'enumerazione VSS esistenti</span><span class="sxs-lookup"><span data-stu-id="b0c60-122">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="b0c60-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ dello schema di backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="b0c60-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="b0c60-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valore aggiunto:</span><span class="sxs-lookup"><span data-stu-id="b0c60-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Added value:</span></span>
</dt> <dd>

<span data-ttu-id="b0c60-125">VSS \_ BS \_ writer \_ supporta \_ i \_ ripristini paralleli</span><span class="sxs-lookup"><span data-stu-id="b0c60-125">VSS\_BS\_WRITER\_SUPPORTS\_PARALLEL\_RESTORES</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="b0c60-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumerazione [**\_ \_ \_ \_ attributi snapshot del volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="b0c60-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="b0c60-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="b0c60-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="b0c60-128">\_ \_ \_ snapshot posticipato VolSnap attr di VSS \_</span><span class="sxs-lookup"><span data-stu-id="b0c60-128">VSS\_VOLSNAP\_ATTR\_DELAYED\_POSTSNAPSHOT</span></span>

<span data-ttu-id="b0c60-129">VSS \_ VolSnap \_ attr \_ TXF \_ Recovery</span><span class="sxs-lookup"><span data-stu-id="b0c60-129">VSS\_VOLSNAP\_ATTR\_TXF\_RECOVERY</span></span>

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="b0c60-130">Modifiche all'interfaccia VSS esistente</span><span class="sxs-lookup"><span data-stu-id="b0c60-130">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="b0c60-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interfaccia [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)</span><span class="sxs-lookup"><span data-stu-id="b0c60-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="b0c60-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Metodo aggiunto:</span><span class="sxs-lookup"><span data-stu-id="b0c60-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Added method:</span></span>
</dt> <dd>

[<span data-ttu-id="b0c60-133">**BreakSnapshotSetEx**</span><span class="sxs-lookup"><span data-stu-id="b0c60-133">**BreakSnapshotSetEx**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a><span data-ttu-id="b0c60-134">Nuovi writer VSS</span><span class="sxs-lookup"><span data-stu-id="b0c60-134">New VSS Writers</span></span>

<span data-ttu-id="b0c60-135">In Windows Server 2008 e Windows Vista con SP1 sono stati introdotti i writer VSS seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0c60-135">Windows Server 2008 and Windows Vista with SP1 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="b0c60-136">Writer di configurazione IIS</span><span class="sxs-lookup"><span data-stu-id="b0c60-136">IIS Configuration Writer</span></span>
-   <span data-ttu-id="b0c60-137">Writer metabase IIS</span><span class="sxs-lookup"><span data-stu-id="b0c60-137">IIS Metabase Writer</span></span>
-   <span data-ttu-id="b0c60-138">Writer VSS server dei criteri di servizio</span><span class="sxs-lookup"><span data-stu-id="b0c60-138">NPS VSS Writer</span></span>
-   <span data-ttu-id="b0c60-139">Writer VSS del gateway Servizi Desktop remoto (Servizi terminal)</span><span class="sxs-lookup"><span data-stu-id="b0c60-139">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>
-   <span data-ttu-id="b0c60-140">Writer VSS di gestione licenze Servizi Desktop remoto (Servizi terminal)</span><span class="sxs-lookup"><span data-stu-id="b0c60-140">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="b0c60-141">Questi writer sono documentati in [writer VSS in-box](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="b0c60-141">These writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 



