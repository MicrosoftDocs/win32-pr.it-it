---
description: Riepilogo delle modifiche all'API VSS in Windows Server 2003
ms.assetid: 35572fc6-9147-4726-ae7a-d78292683ba0
title: Riepilogo delle modifiche all'API VSS in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9154da0ac67dd7a599064ed3b5cf1dc7285b0fb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310662"
---
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a><span data-ttu-id="340b5-103">Riepilogo delle modifiche all'API VSS in Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="340b5-103">Summary of VSS API Changes in Windows Server 2003</span></span>

## <a name="changes-in-the-vss-service"></a><span data-ttu-id="340b5-104">Modifiche nel servizio VSS</span><span class="sxs-lookup"><span data-stu-id="340b5-104">Changes in the VSS Service</span></span>

<dl> <dt>

<span data-ttu-id="340b5-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Eventi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-105"><span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Events added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-106">*BackupShutdown*</span><span class="sxs-lookup"><span data-stu-id="340b5-106">*BackupShutdown*</span></span>](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a><span data-ttu-id="340b5-107">Modifiche alla funzionalità VSS</span><span class="sxs-lookup"><span data-stu-id="340b5-107">Changes in VSS Functionality</span></span>

<dl> <dt>

<span data-ttu-id="340b5-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Funzionalità aggiuntive:</span><span class="sxs-lookup"><span data-stu-id="340b5-108"><span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Additional functionality:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-109">*supporto file parziale*</span><span class="sxs-lookup"><span data-stu-id="340b5-109">*partial file support*</span></span>](vssgloss-p.md)

[<span data-ttu-id="340b5-110">*destinazione diretta*</span><span class="sxs-lookup"><span data-stu-id="340b5-110">*directed targeting*</span></span>](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a><span data-ttu-id="340b5-111">Nuove interfacce VSS</span><span class="sxs-lookup"><span data-stu-id="340b5-111">New VSS Interfaces</span></span>

[<span data-ttu-id="340b5-112">**IVssWMDependency**</span><span class="sxs-lookup"><span data-stu-id="340b5-112">**IVssWMDependency**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="340b5-113">Modifiche all'interfaccia VSS esistente</span><span class="sxs-lookup"><span data-stu-id="340b5-113">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="340b5-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>Interfaccia [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)</span><span class="sxs-lookup"><span data-stu-id="340b5-114"><span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Metodi modificati:</span><span class="sxs-lookup"><span data-stu-id="340b5-115"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-116">**IVssAsync:: wait**</span><span class="sxs-lookup"><span data-stu-id="340b5-116">**IVssAsync::Wait**</span></span>](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>Interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)</span><span class="sxs-lookup"><span data-stu-id="340b5-117"><span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-118"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-119">**IVssBackupComponents:: AddNewTarget**</span><span class="sxs-lookup"><span data-stu-id="340b5-119">**IVssBackupComponents::AddNewTarget**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[<span data-ttu-id="340b5-120">**IVssBackupComponents:: QueryRevertStatus**</span><span class="sxs-lookup"><span data-stu-id="340b5-120">**IVssBackupComponents::QueryRevertStatus**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[<span data-ttu-id="340b5-121">**IVssBackupComponents:: RevertToSnapshot**</span><span class="sxs-lookup"><span data-stu-id="340b5-121">**IVssBackupComponents::RevertToSnapshot**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[<span data-ttu-id="340b5-122">**IVssBackupComponents:: SetRangesFilePath**</span><span class="sxs-lookup"><span data-stu-id="340b5-122">**IVssBackupComponents::SetRangesFilePath**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[<span data-ttu-id="340b5-123">**IVssBackupComponents:: SetRestoreState**</span><span class="sxs-lookup"><span data-stu-id="340b5-123">**IVssBackupComponents::SetRestoreState**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>Interfaccia [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)</span><span class="sxs-lookup"><span data-stu-id="340b5-124"><span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-125"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-126">**IVssCreateWriterMetadata:: AddComponentDependency**</span><span class="sxs-lookup"><span data-stu-id="340b5-126">**IVssCreateWriterMetadata::AddComponentDependency**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[<span data-ttu-id="340b5-127">**IVssCreateWriterMetadata:: SetBackupSchema**</span><span class="sxs-lookup"><span data-stu-id="340b5-127">**IVssCreateWriterMetadata::SetBackupSchema**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span data-ttu-id="340b5-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Metodi modificati:</span><span class="sxs-lookup"><span data-stu-id="340b5-128"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-129">**IVssCreateWriterMetadata:: AddComponent**</span><span class="sxs-lookup"><span data-stu-id="340b5-129">**IVssCreateWriterMetadata::AddComponent**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[<span data-ttu-id="340b5-130">**IVssCreateWriterMetadata:: AddDatabaseFiles**</span><span class="sxs-lookup"><span data-stu-id="340b5-130">**IVssCreateWriterMetadata::AddDatabaseFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[<span data-ttu-id="340b5-131">**IVssCreateWriterMetadata:: AddDatabaseLogFiles**</span><span class="sxs-lookup"><span data-stu-id="340b5-131">**IVssCreateWriterMetadata::AddDatabaseLogFiles**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[<span data-ttu-id="340b5-132">**IVssCreateWriterMetadata:: AddFilesToFileGroup**</span><span class="sxs-lookup"><span data-stu-id="340b5-132">**IVssCreateWriterMetadata::AddFilesToFileGroup**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>Interfaccia [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)</span><span class="sxs-lookup"><span data-stu-id="340b5-133"><span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-134"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-135">**IVssExamineWriterMetadata::GetBackupSchema**</span><span class="sxs-lookup"><span data-stu-id="340b5-135">**IVssExamineWriterMetadata::GetBackupSchema**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>Interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)</span><span class="sxs-lookup"><span data-stu-id="340b5-136"><span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Metodi rimossi:</span><span class="sxs-lookup"><span data-stu-id="340b5-137"><span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Methods removed:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-138">**IVssComponent:: AddNewTarget**</span><span class="sxs-lookup"><span data-stu-id="340b5-138">**IVssComponent::AddNewTarget**</span></span>

</dd> <dt>

<span data-ttu-id="340b5-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-139"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-140">**IVssComponent:: AddDifferencedFilesByLastModifyTime**</span><span class="sxs-lookup"><span data-stu-id="340b5-140">**IVssComponent::AddDifferencedFilesByLastModifyTime**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[<span data-ttu-id="340b5-141">**IVssComponent:: GetDifferencedFile**</span><span class="sxs-lookup"><span data-stu-id="340b5-141">**IVssComponent::GetDifferencedFile**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[<span data-ttu-id="340b5-142">**IVssComponent:: GetDifferencedFilesCount**</span><span class="sxs-lookup"><span data-stu-id="340b5-142">**IVssComponent::GetDifferencedFilesCount**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span data-ttu-id="340b5-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>I metodi non sono più riservati:</span><span class="sxs-lookup"><span data-stu-id="340b5-143"><span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Methods no longer reserved:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-144">**IVssComponent:: AddDirectedTarget**</span><span class="sxs-lookup"><span data-stu-id="340b5-144">**IVssComponent::AddDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[<span data-ttu-id="340b5-145">**IVssComponent:: GetDirectedTarget**</span><span class="sxs-lookup"><span data-stu-id="340b5-145">**IVssComponent::GetDirectedTarget**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>Interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)</span><span class="sxs-lookup"><span data-stu-id="340b5-146"><span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-147"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-148">**IVssWMComponent:: getdependency**</span><span class="sxs-lookup"><span data-stu-id="340b5-148">**IVssWMComponent::GetDependency**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>Interfaccia [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)</span><span class="sxs-lookup"><span data-stu-id="340b5-149"><span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-150"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-151">**IVssWMFiledesc::GetBackupTypeMask**</span><span class="sxs-lookup"><span data-stu-id="340b5-151">**IVssWMFiledesc::GetBackupTypeMask**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a><span data-ttu-id="340b5-152">Modifiche alle classi VSS esistenti</span><span class="sxs-lookup"><span data-stu-id="340b5-152">Existing VSS Class Modifications</span></span>

<dl> <dt>

<span data-ttu-id="340b5-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>Classe [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)</span><span class="sxs-lookup"><span data-stu-id="340b5-153"><span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) class</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Metodi modificati:</span><span class="sxs-lookup"><span data-stu-id="340b5-154"><span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Methods modified:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-155">**CVssWriter:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="340b5-155">**CVssWriter::Initialize**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span data-ttu-id="340b5-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-156"><span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Methods added:</span></span>
</dt> <dd>

[<span data-ttu-id="340b5-157">**CVssWriter:: GetContext**</span><span class="sxs-lookup"><span data-stu-id="340b5-157">**CVssWriter::GetContext**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[<span data-ttu-id="340b5-158">**CVssWriter:: GetRestoreType**</span><span class="sxs-lookup"><span data-stu-id="340b5-158">**CVssWriter::GetRestoreType**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[<span data-ttu-id="340b5-159">**CVssWriter:: GetSnapshotDeviceName**</span><span class="sxs-lookup"><span data-stu-id="340b5-159">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[<span data-ttu-id="340b5-160">**CVssWriter:: OnBackupShutdown**</span><span class="sxs-lookup"><span data-stu-id="340b5-160">**CVssWriter::OnBackupShutdown**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="340b5-161">Nuove enumerazioni VSS</span><span class="sxs-lookup"><span data-stu-id="340b5-161">New VSS Enumerations</span></span>

<dl> <dt>

<span data-ttu-id="340b5-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**\_schema di backup VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span><span class="sxs-lookup"><span data-stu-id="340b5-162"><span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="340b5-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**\_flag componente \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span><span class="sxs-lookup"><span data-stu-id="340b5-163"><span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="340b5-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**\_tipo di \_ backup delle specifiche del file VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span><span class="sxs-lookup"><span data-stu-id="340b5-164"><span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="340b5-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**\_tipo di ripristino VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span><span class="sxs-lookup"><span data-stu-id="340b5-165"><span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)</span></span>
<span data-ttu-id="340b5-166"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="340b5-166"></dt> <dd></dd> </dl></span></span>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="340b5-167">Modifiche dell'enumerazione VSS esistenti</span><span class="sxs-lookup"><span data-stu-id="340b5-167">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="340b5-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione del \_ tipo di backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)</span><span class="sxs-lookup"><span data-stu-id="340b5-168"><span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VSS\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-169"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-170">copia di VSS \_ BT \_</span><span class="sxs-lookup"><span data-stu-id="340b5-170">VSS\_BT\_COPY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ destinazione ripristino**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)</span><span class="sxs-lookup"><span data-stu-id="340b5-171"><span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VSS\_RESTORE\_TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Valori rimossi:</span><span class="sxs-lookup"><span data-stu-id="340b5-172"><span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Removed values:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-173">\_nuovo VSS RT \_</span><span class="sxs-lookup"><span data-stu-id="340b5-173">VSS\_RT\_NEW</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)</span><span class="sxs-lookup"><span data-stu-id="340b5-174"><span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-175"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-176">\_ripristino RME \_ VSS \_ al \_ riavvio \_ se \_ non è possibile \_ sostituire</span><span class="sxs-lookup"><span data-stu-id="340b5-176">VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ dello stato dello snapshot**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)</span><span class="sxs-lookup"><span data-stu-id="340b5-177"><span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VSS\_SNAPSHOT\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-178"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-179">\_postcommit \_ elaborazione VSS SS \_</span><span class="sxs-lookup"><span data-stu-id="340b5-179">VSS\_SS\_PROCESSING\_POSTCOMMIT</span></span>

<span data-ttu-id="340b5-180">\_ \_ PREFINALCOMMIT elaborazione VSS \_ SS</span><span class="sxs-lookup"><span data-stu-id="340b5-180">VSS\_SS\_PROCESSING\_PREFINALCOMMIT</span></span>

<span data-ttu-id="340b5-181">VSS \_ SS \_ PREFINALCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="340b5-181">VSS\_SS\_PREFINALCOMMITTED</span></span>

<span data-ttu-id="340b5-182">\_ \_ POSTFINALCOMMIT elaborazione VSS \_ SS</span><span class="sxs-lookup"><span data-stu-id="340b5-182">VSS\_SS\_PROCESSING\_POSTFINALCOMMIT</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumerazione [**\_ \_ \_ \_ attributi snapshot del volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="340b5-183"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-184"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-185">VSS \_ VolSnap \_ attr \_ autocover</span><span class="sxs-lookup"><span data-stu-id="340b5-185">VSS\_VOLSNAP\_ATTR\_AUTORECOVER</span></span>

</dd> <dt>

<span data-ttu-id="340b5-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>I valori riservati supportano ora:</span><span class="sxs-lookup"><span data-stu-id="340b5-186"><span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>Reserved values now support:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-187">VSS \_ VolSnap \_ attr \_ hardware \_ assistito</span><span class="sxs-lookup"><span data-stu-id="340b5-187">VSS\_VOLSNAP\_ATTR\_HARDWARE\_ASSISTED</span></span>

<span data-ttu-id="340b5-188">\_VolSnap di \_ VSS \_ importati</span><span class="sxs-lookup"><span data-stu-id="340b5-188">VSS\_VOLSNAP\_ATTR\_IMPORTED</span></span>

<span data-ttu-id="340b5-189">VSS \_ VolSnap \_ attr \_ esposto \_ localmente</span><span class="sxs-lookup"><span data-stu-id="340b5-189">VSS\_VOLSNAP\_ATTR\_EXPOSED\_LOCALLY</span></span>

<span data-ttu-id="340b5-190">VSS \_ VolSnap \_ attr \_ esposto in \_ remoto</span><span class="sxs-lookup"><span data-stu-id="340b5-190">VSS\_VOLSNAP\_ATTR\_EXPOSED\_REMOTELY</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="340b5-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ stato writer**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)</span><span class="sxs-lookup"><span data-stu-id="340b5-191"><span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VSS\_WRITER\_STATE**](/windows/desktop/api/Vss/ne-vss-vss_writer_state) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-192"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-193">VSS \_ WS \_ non riuscito \_ alle \_ BACKUPSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="340b5-193">VSS\_WS\_FAILED\_AT\_BACKUPSHUTDOWN</span></span>

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a><span data-ttu-id="340b5-194">Modifiche alle strutture VSS</span><span class="sxs-lookup"><span data-stu-id="340b5-194">Changes to VSS Structures</span></span>

<dl> <dt>

<span data-ttu-id="340b5-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>Servizio Copia [**shadow \_ del volume Struttura COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)</span><span class="sxs-lookup"><span data-stu-id="340b5-195"><span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="340b5-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Membri aggiunti:</span><span class="sxs-lookup"><span data-stu-id="340b5-196"><span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Added members:</span></span>
</dt> <dd>

<span data-ttu-id="340b5-197">**bSelectableForRestore**</span><span class="sxs-lookup"><span data-stu-id="340b5-197">**bSelectableForRestore**</span></span>

<span data-ttu-id="340b5-198">**dwComponentFlags**</span><span class="sxs-lookup"><span data-stu-id="340b5-198">**dwComponentFlags**</span></span>

<span data-ttu-id="340b5-199">**cDependencies**</span><span class="sxs-lookup"><span data-stu-id="340b5-199">**cDependencies**</span></span>

</dd> </dl> </dd> </dl>

 

 



