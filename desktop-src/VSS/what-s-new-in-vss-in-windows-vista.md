---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Novità di VSS in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307134"
---
# <a name="whats-new-in-vss-in-windows-vista"></a><span data-ttu-id="6c164-103">Novità di VSS in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c164-103">What's New in VSS in Windows Vista</span></span>

<span data-ttu-id="6c164-104">In Windows Vista sono state introdotte le seguenti modifiche apportate al Servizio Copia Shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="6c164-104">Windows Vista introduces the following changes to the Volume Shadow Copy Service.</span></span>

<span data-ttu-id="6c164-105">Si noti che tutte le modifiche per Windows Vista si applicano anche a Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6c164-105">Note that all changes for Windows Vista also apply to Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="6c164-106">Nuove interfacce VSS</span><span class="sxs-lookup"><span data-stu-id="6c164-106">New VSS Interfaces</span></span>

[<span data-ttu-id="6c164-107">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="6c164-107">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[<span data-ttu-id="6c164-108">**IVssComponentEx**</span><span class="sxs-lookup"><span data-stu-id="6c164-108">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[<span data-ttu-id="6c164-109">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="6c164-109">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[<span data-ttu-id="6c164-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="6c164-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[<span data-ttu-id="6c164-111">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="6c164-111">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a><span data-ttu-id="6c164-112">Nuove classi VSS</span><span class="sxs-lookup"><span data-stu-id="6c164-112">New VSS Classes</span></span>

[<span data-ttu-id="6c164-113">**CVssWriterEx**</span><span class="sxs-lookup"><span data-stu-id="6c164-113">**CVssWriterEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a><span data-ttu-id="6c164-114">Nuove enumerazioni VSS</span><span class="sxs-lookup"><span data-stu-id="6c164-114">New VSS Enumerations</span></span>

[<span data-ttu-id="6c164-115">**\_tipo di rollforward VSS \_**</span><span class="sxs-lookup"><span data-stu-id="6c164-115">**VSS\_ROLLFORWARD\_TYPE**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="6c164-116">Modifiche dell'enumerazione VSS esistenti</span><span class="sxs-lookup"><span data-stu-id="6c164-116">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="6c164-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ dello schema di backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="6c164-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="6c164-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="6c164-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="6c164-119">\_ \_ ripristino autorevole di VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="6c164-119">VSS\_BS\_AUTHORITATIVE\_RESTORE</span></span>

<span data-ttu-id="6c164-120">\_stato del \_ \_ sistema indipendente VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="6c164-120">VSS\_BS\_INDEPENDENT\_SYSTEM\_STATE</span></span>

<span data-ttu-id="6c164-121">\_ridenominazione \_ ripristino VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="6c164-121">VSS\_BS\_RESTORE\_RENAME</span></span>

<span data-ttu-id="6c164-122">\_ \_ ripristino rollforward VSS \_ BS</span><span class="sxs-lookup"><span data-stu-id="6c164-122">VSS\_BS\_ROLLFORWARD\_RESTORE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="6c164-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ flag componenti**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span><span class="sxs-lookup"><span data-stu-id="6c164-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="6c164-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="6c164-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="6c164-125">VSS \_ CF \_ non \_ stato del sistema \_</span><span class="sxs-lookup"><span data-stu-id="6c164-125">VSS\_CF\_NOT\_SYSTEM\_STATE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="6c164-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumerazione [**\_ \_ \_ \_ attributi snapshot del volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="6c164-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="6c164-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="6c164-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="6c164-128">VSS \_ VolSnap \_ attr \_ nessun \_ recupero automatico</span><span class="sxs-lookup"><span data-stu-id="6c164-128">VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY</span></span>

<span data-ttu-id="6c164-129">VSS \_ VolSnap \_ attr \_ non \_ transazionale</span><span class="sxs-lookup"><span data-stu-id="6c164-129">VSS\_VOLSNAP\_ATTR\_NOT\_TRANSACTED</span></span>

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="6c164-130">Traccia e registrazione di eventi VSS</span><span class="sxs-lookup"><span data-stu-id="6c164-130">VSS Event Tracing and Logging</span></span>

-   <span data-ttu-id="6c164-131">Il file di traccia VSS ora può trovarsi in qualsiasi volume locale.</span><span class="sxs-lookup"><span data-stu-id="6c164-131">The VSS trace file can now be located on any local volume.</span></span> <span data-ttu-id="6c164-132">Nelle versioni di Windows precedenti a Windows Vista, non è stato possibile individuare il file di traccia VSS in un volume presente nel set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="6c164-132">On versions of Windows prior to Windows Vista, the VSS trace file could not be located on a volume that was in the shadow copy set.</span></span>
-   <span data-ttu-id="6c164-133">Molte voci del registro eventi sono state riformulate in modo da renderle più chiare.</span><span class="sxs-lookup"><span data-stu-id="6c164-133">Many event log entries have been reworded to make them clearer.</span></span>
-   <span data-ttu-id="6c164-134">Tutte le voci del registro eventi VSS contengono ora informazioni sul contesto.</span><span class="sxs-lookup"><span data-stu-id="6c164-134">All VSS event log entries now contain context information.</span></span>

## <a name="vss-error-reporting"></a><span data-ttu-id="6c164-135">Segnalazione errori VSS</span><span class="sxs-lookup"><span data-stu-id="6c164-135">VSS Error Reporting</span></span>

-   <span data-ttu-id="6c164-136">È ora possibile recuperare le descrizioni di tutti i codici di errore VSS chiamando la funzione [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con il \_ messaggio Format \_ dal \_ flag HMODULE specificato nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6c164-136">Descriptions of all VSS error codes can now be retrieved by calling the [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_HMODULE flag specified in the *dwFlags* parameter.</span></span>
-   <span data-ttu-id="6c164-137">I messaggi del codice di errore VSS sono contenuti in vsstrace.dll.</span><span class="sxs-lookup"><span data-stu-id="6c164-137">The VSS error code messages are contained in vsstrace.dll.</span></span> <span data-ttu-id="6c164-138">È necessario specificare un handle per questo modulo nel parametro *lpSource* .</span><span class="sxs-lookup"><span data-stu-id="6c164-138">A handle to this module must be specified in the *lpSource* parameter.</span></span>

## <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="6c164-139">Esclusione di file dalle copie shadow</span><span class="sxs-lookup"><span data-stu-id="6c164-139">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="6c164-140">Le applicazioni o i servizi possono utilizzare la chiave del registro di sistema FilesNotToSnapshot per specificare i file da eliminare dalle copie shadow appena create.</span><span class="sxs-lookup"><span data-stu-id="6c164-140">Applications or services can use the FilesNotToSnapshot registry key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="6c164-141">Per altre informazioni, vedere [esclusione di file dalle copie shadow](excluding-files-from-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="6c164-141">For more information, see [Excluding Files from Shadow Copies](excluding-files-from-shadow-copies.md).</span></span>

## <a name="backup-and-restore-application-compatibility"></a><span data-ttu-id="6c164-142">Compatibilità delle applicazioni di backup e ripristino</span><span class="sxs-lookup"><span data-stu-id="6c164-142">Backup and Restore Application Compatibility</span></span>

<span data-ttu-id="6c164-143">Gli sviluppatori di applicazioni di backup e ripristino devono essere a conoscenza di alcune nuove funzionalità di Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6c164-143">Developers of backup and restore applications need to be aware of certain new features in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6c164-144">Per un elenco di controllo per la compatibilità delle applicazioni, vedere [compatibilità delle applicazioni per il backup e il ripristino](application-compatibility-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="6c164-144">For an application compatibility checklist, see [Application Compatibility for Backup and Restore](application-compatibility-for-backup-and-restore.md).</span></span>

 

 
