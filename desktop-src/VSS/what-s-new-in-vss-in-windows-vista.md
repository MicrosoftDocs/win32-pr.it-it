---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Novità di VSS in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9e0780b092b2bed0235ba62377da9a4f7f0b53bded9e3f7feb5d412f5ab982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751143"
---
# <a name="whats-new-in-vss-in-windows-vista"></a>Novità di VSS in Windows Vista

Windows Vista introduce le modifiche seguenti al Servizio Copia Shadow del volume.

Si noti che tutte le modifiche Windows Vista si applicano anche a Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).

## <a name="new-vss-interfaces"></a>Nuove interfacce vss

[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[**IVssComponentEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[**IVssCreateWriterMetadataEx**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[**IVssDifferentialSoftwareSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[**IVssExamineWriterMetadataEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a>Nuove classi VSS

[**CVssWriterEx**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a>Nuove enumerazioni VSS

[**TIPO \_ ROLLFORWARD VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a>Modifiche all'enumerazione VSS esistente

<dl> <dt>

<span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VsS \_ Enumerazione BACKUP \_ SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

RIPRISTINO \_ AUTOREVOLE DI VSS BS \_ \_

STATO DEL SISTEMA \_ INDIPENDENTE DA VSS BS \_ \_ \_

RIDENOMINAZIONE \_ DI VSS BS \_ RESTORE \_

RIPRISTINO \_ \_ ROLLFORWARD DI VSS BS \_

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VsS \_ Enumerazione COMPONENT \_ FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

VSS \_ CF \_ NOT \_ SYSTEM \_ STATE

</dd> </dl> </dd> </dl>

<dl> <dt>

<span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_ Enumerazione VSS \_ VOLUME SNAPSHOT \_ \_ ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)
</dt> <dd>

<dl> <dt>

<span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valori aggiunti:
</dt> <dd>

VSS \_ VOLSNAP \_ ATTR \_ NO \_ AUTORECOVERY

VSS \_ VOLSNAP \_ ATTR \_ NOT \_ TRANSACTED

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>Traccia e registrazione di eventi vss

-   Il file di traccia VSS può ora trovarsi in qualsiasi volume locale. Nelle versioni di Windows precedenti a Windows Vista, non è stato possibile trovare il file di traccia VSS in un volume che si trova nel set di copie shadow.
-   Molte voci del registro eventi sono state riformulate per renderle più chiare.
-   Tutte le voci del registro eventi vss contengono ora informazioni di contesto.

## <a name="vss-error-reporting"></a>Segnalazione errori VSS

-   È ora possibile recuperare le descrizioni di tutti i codici di errore vss chiamando la funzione [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con il flag FORMAT MESSAGE FROM HMODULE specificato \_ nel parametro \_ \_ *dwFlags.*
-   I messaggi di codice di errore vss sono contenuti in vsstrace.dll. È necessario specificare un handle per questo modulo nel *parametro lpSource.*

## <a name="excluding-files-from-shadow-copies"></a>Esclusione di file da copie shadow

Le applicazioni o i servizi possono usare la chiave del Registro di sistema FilesNotToSnapshot per specificare i file da eliminare dalle nuove copie shadow create. Per altre informazioni, vedere [Esclusione di file da copie shadow.](excluding-files-from-shadow-copies.md)

## <a name="backup-and-restore-application-compatibility"></a>Compatibilità delle applicazioni di backup e ripristino

Gli sviluppatori di applicazioni di backup e ripristino devono essere a conoscenza di alcune nuove funzionalità di Windows Vista e Windows Server 2008. Per un elenco di controllo per la compatibilità delle applicazioni, vedere [Compatibilità delle applicazioni per il backup e il ripristino.](application-compatibility-for-backup-and-restore.md)

 

 
