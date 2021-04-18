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
# <a name="whats-new-in-vss-in-windows-vista"></a>Novità di VSS in Windows Vista

In Windows Vista sono state introdotte le seguenti modifiche apportate al Servizio Copia Shadow del volume.

Si noti che tutte le modifiche per Windows Vista si applicano anche a Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

## <a name="new-vss-interfaces"></a>Nuove interfacce VSS

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Nuove classi VSS

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Nuove enumerazioni VSS

[**\_tipo di rollforward VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Modifiche dell'enumerazione VSS esistenti

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ dello schema di backup**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

\_ \_ ripristino autorevole di VSS BS \_

\_stato del \_ \_ sistema indipendente VSS BS \_

\_ridenominazione \_ ripristino VSS BS \_

\_ \_ ripristino rollforward VSS \_ BS

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>Servizio Copia [**shadow \_ del volume Enumerazione \_ flag componenti**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

VSS \_ CF \_ non \_ stato del sistema \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumerazione [**\_ \_ \_ \_ attributi snapshot del volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

VSS \_ VolSnap \_ attr \_ nessun \_ recupero automatico

VSS \_ VolSnap \_ attr \_ non \_ transazionale

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Traccia e registrazione di eventi VSS

-   Il file di traccia VSS ora può trovarsi in qualsiasi volume locale. Nelle versioni di Windows precedenti a Windows Vista, non è stato possibile individuare il file di traccia VSS in un volume presente nel set di copie shadow.
-   Molte voci del registro eventi sono state riformulate in modo da renderle più chiare.
-   Tutte le voci del registro eventi VSS contengono ora informazioni sul contesto.

## <a name="vss-error-reporting"></a>Segnalazione errori VSS

-   È ora possibile recuperare le descrizioni di tutti i codici di errore VSS chiamando la funzione [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con il \_ messaggio Format \_ dal \_ flag HMODULE specificato nel parametro *dwFlags* .
-   I messaggi del codice di errore VSS sono contenuti in vsstrace.dll. È necessario specificare un handle per questo modulo nel parametro *lpSource* .

## <a name="excluding-files-from-shadow-copies"></a>Esclusione di file dalle copie shadow

Le applicazioni o i servizi possono utilizzare la chiave del registro di sistema FilesNotToSnapshot per specificare i file da eliminare dalle copie shadow appena create. Per altre informazioni, vedere [esclusione di file dalle copie shadow](excluding-files-from-shadow-copies.md).

## <a name="backup-and-restore-application-compatibility"></a>Compatibilità delle applicazioni di backup e ripristino

Gli sviluppatori di applicazioni di backup e ripristino devono essere a conoscenza di alcune nuove funzionalità di Windows Vista e Windows Server 2008. Per un elenco di controllo per la compatibilità delle applicazioni, vedere [compatibilità delle applicazioni per il backup e il ripristino](application-compatibility-for-backup-and-restore.md).

 

 
