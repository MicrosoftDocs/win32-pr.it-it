---
description: Riepilogo delle modifiche all'API vss in Windows Server 2003
ms.assetid: 35572fc6-9147-4726-ae7a-d78292683ba0
title: Riepilogo delle modifiche all'API vss in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a620a7498e5bc6af29e46e41f34c4cc96e04241db9d7618009d61493595945f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121564"
---
# <a name="summary-of-vss-api-changes-in-windows-server-2003"></a>Riepilogo delle modifiche all'API vss in Windows Server 2003

## <a name="changes-in-the-vss-service"></a>Modifiche al servizio VsS

<dl> <dt>

<span id="Events_added_"></span><span id="events_added_"></span><span id="EVENTS_ADDED_"></span>Eventi aggiunti:
</dt> <dd>

[*BackupShutdown*](vssgloss-b.md)

</dd> </dl>

## <a name="changes-in-vss-functionality"></a>Modifiche apportate alle funzionalità del Servizio Copia Studio

<dl> <dt>

<span id="Additional_functionality_"></span><span id="additional_functionality_"></span><span id="ADDITIONAL_FUNCTIONALITY_"></span>Funzionalità aggiuntive:
</dt> <dd>

[*supporto di file parziali*](vssgloss-p.md)

[*targeting diretto*](vssgloss-d.md)

</dd> </dl>

## <a name="new-vss-interfaces"></a>Nuove interfacce vss

[**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

## <a name="existing-vss-interface-modifications"></a>Modifiche all'interfaccia vss esistente

<dl> <dt>

<span id="IVssAsync_interface"></span><span id="ivssasync_interface"></span><span id="IVSSASYNC_INTERFACE"></span>[**Interfaccia IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync)
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Metodi modificati:
</dt> <dd>

[**IVssAsync::Wait**](/windows/desktop/api/Vss/nf-vss-ivssasync-wait)

</dd> </dl> </dd> <dt>

<span id="IVssBackupComponents_interface"></span><span id="ivssbackupcomponents_interface"></span><span id="IVSSBACKUPCOMPONENTS_INTERFACE"></span>[**Interfaccia IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:
</dt> <dd>

[**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)

[**IVssBackupComponents::QueryRevertStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-queryrevertstatus)

[**IVssBackupComponents::RevertToSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-reverttosnapshot)

[**IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath)

[**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate)

</dd> </dl> </dd> <dt>

<span id="IVssCreateWriterMetadata_interface"></span><span id="ivsscreatewritermetadata_interface"></span><span id="IVSSCREATEWRITERMETADATA_INTERFACE"></span>[**Interfaccia IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:
</dt> <dd>

[**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency)

[**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema)

</dd> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Metodi modificati:
</dt> <dd>

[**IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)

[**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)

[**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

[**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)

</dd> </dl> </dd> <dt>

<span id="IVssExamineWriterMetadata_interface"></span><span id="ivssexaminewritermetadata_interface"></span><span id="IVSSEXAMINEWRITERMETADATA_INTERFACE"></span>[**Interfaccia IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:
</dt> <dd>

[**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

</dd> </dl> </dd> <dt>

<span id="IVssComponent_interface"></span><span id="ivsscomponent_interface"></span><span id="IVSSCOMPONENT_INTERFACE"></span>[**Interfaccia IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)
</dt> <dd>

<dl> <dt>

<span id="Methods_removed_"></span><span id="methods_removed_"></span><span id="METHODS_REMOVED_"></span>Metodi rimossi:
</dt> <dd>

**IVssComponent::AddNewTarget**

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:
</dt> <dd>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)

[**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

[**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)

</dd> <dt>

<span id="Methods_no_longer_reserved_"></span><span id="methods_no_longer_reserved_"></span><span id="METHODS_NO_LONGER_RESERVED_"></span>Metodi non più riservati:
</dt> <dd>

[**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)

[**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)

</dd> </dl> </dd> <dt>

<span id="IVssWMComponent_interface"></span><span id="ivsswmcomponent_interface"></span><span id="IVSSWMCOMPONENT_INTERFACE"></span>[**Interfaccia IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:
</dt> <dd>

[**IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency)

</dd> </dl> </dd> <dt>

<span id="IVssWMFiledesc_interface"></span><span id="ivsswmfiledesc_interface"></span><span id="IVSSWMFILEDESC_INTERFACE"></span>[**Interfaccia IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)
</dt> <dd>

<dl> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:
</dt> <dd>

[**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask)

</dd> </dl> </dd> </dl>

## <a name="existing-vss-class-modifications"></a>Modifiche alle classi VSS esistenti

<dl> <dt>

<span id="CVssWriter_class"></span><span id="cvsswriter_class"></span><span id="CVSSWRITER_CLASS"></span>[**Classe CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter)
</dt> <dd>

<dl> <dt>

<span id="Methods_modified_"></span><span id="methods_modified_"></span><span id="METHODS_MODIFIED_"></span>Metodi modificati:
</dt> <dd>

[**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)

</dd> <dt>

<span id="Methods_added_"></span><span id="methods_added_"></span><span id="METHODS_ADDED_"></span>Metodi aggiunti:
</dt> <dd>

[**CVssWriter::GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext)

[**CVssWriter::GetRestoreType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getrestoretype)

[**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)

[**CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)

</dd> </dl> </dd> </dl>

## <a name="new-vss-enumerations"></a>Nuove enumerazioni VSS

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA"></span><span id="vss_backup_schema"></span>[**SCHEMA DI \_ BACKUP VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd></dd> <dt>

<span id="VSS_COMPONENT_FLAGS"></span><span id="vss_component_flags"></span>[**FLAG DEI \_ COMPONENTI VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd></dd> <dt>

<span id="VSS_FILE_SPEC_BACKUP_TYPE"></span><span id="vss_file_spec_backup_type"></span>[**TIPO DI \_ BACKUP DELLE SPECIFICHE FILE \_ VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)
</dt> <dd></dd> <dt>

<span id="VSS_RESTORE_TYPE"></span><span id="vss_restore_type"></span>[**TIPO DI RIPRISTINO \_ VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_restore_type)
</dt> <dd></dd> </dl>

## <a name="existing-vss-enumeration-modifications"></a>Modifiche all'enumerazione VSS esistente

<dl> <dt>

<span id="VSS_BACKUP_TYPE_enumeration"></span><span id="vss_backup_type_enumeration"></span><span id="VSS_BACKUP_TYPE_ENUMERATION"></span>[**VsS \_ Enumerazione BACKUP \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_backup_type)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

COPIA DI VSS \_ BT \_

</dd> </dl> </dd> <dt>

<span id="VSS_RESTORE_TARGET_enumeration"></span><span id="vss_restore_target_enumeration"></span><span id="VSS_RESTORE_TARGET_ENUMERATION"></span>[**VsS \_ Enumerazione RESTORE \_ TARGET**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restore_target)
</dt> <dd>

<dl> <dt>

<span id="Removed_values_"></span><span id="removed_values_"></span><span id="REMOVED_VALUES_"></span>Valori rimossi:
</dt> <dd>

VSS \_ RT \_ NEW

</dd> </dl> </dd> <dt>

<span id="VSS_RESTOREMETHOD_ENUM_enumeration"></span><span id="vss_restoremethod_enum_enumeration"></span><span id="VSS_RESTOREMETHOD_ENUM_ENUMERATION"></span>[**VsS \_ Enumerazione RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

RIPRISTINO DI \_ VSS RME \_ AL \_ \_ RIAVVIO \_ SE NON È \_ POSSIBILE \_ SOSTITUIRE

</dd> </dl> </dd> <dt>

<span id="VSS_SNAPSHOT_STATE_enumeration"></span><span id="vss_snapshot_state_enumeration"></span><span id="VSS_SNAPSHOT_STATE_ENUMERATION"></span>[**VsS \_ Enumerazione SNAPSHOT \_ STATE**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_state)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

\_POSTCOMMIT ELABORAZIONE VSS SS \_ \_

\_ \_ PREFINALCOMMIT ELABORAZIONE VSS SS \_

VSS \_ SS \_ PREFINALCOMMITTED

VSS \_ SS \_ PROCESSING \_ POSTFINALCOMMIT (POSTFINALCOMMIT ELABORAZIONE VSS SS)

</dd> </dl> </dd> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ Enumerazione VSS \_ VOLUME SNAPSHOT \_ \_ ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ AUTORECOVER

</dd> <dt>

<span id="Reserved_values_now_support_"></span><span id="reserved_values_now_support_"></span><span id="RESERVED_VALUES_NOW_SUPPORT_"></span>I valori riservati ora supportano:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ HARDWARE \_ ASSISTED

VSS \_ VOLSNAP \_ ATTR \_ IMPORTATO

ATTR \_ VSS \_ VOLSNAP ESPOSTO IN \_ \_ LOCALE

ATTR \_ VSS \_ VOLSNAP ESPOSTO IN \_ \_ REMOTO

</dd> </dl> </dd> <dt>

<span id="VSS_WRITER_STATE_enumeration"></span><span id="vss_writer_state_enumeration"></span><span id="VSS_WRITER_STATE_ENUMERATION"></span>[**VsS \_ Enumerazione WRITER \_ STATE**](/windows/desktop/api/Vss/ne-vss-vss_writer_state)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

VSS \_ WS FAILED AT BACKUPSHUTDOWN (VSS WS \_ NON RIUSCITO IN \_ \_ BACKUPSHUTDOWN)

</dd> </dl> </dd> </dl>

## <a name="changes-to-vss-structures"></a>Modifiche alle strutture vss

<dl> <dt>

<span id="VSS_COMPONENTINFO_structure"></span><span id="vss_componentinfo_structure"></span><span id="VSS_COMPONENTINFO_STRUCTURE"></span>[**VsS \_ Struttura COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)
</dt> <dd>

<dl> <dt>

<span id="Added_members_"></span><span id="added_members_"></span><span id="ADDED_MEMBERS_"></span>Membri aggiunti:
</dt> <dd>

**bSelectableForRestore**

**dwComponentFlags**

**Dipendenze di c**

</dd> </dl> </dd> </dl>

 

 



