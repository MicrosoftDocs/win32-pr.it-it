---
description: La partecipazione di un writer ai backup incrementali e differenziali avviene in genere durante la gestione degli eventi Identify (CVssWriter::OnIdentify), PrepareForBackup (CVssWriter:OnPrepareBackup) e PostSnapshot (CVssWriter:OnPostSnapshot).
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Ruolo writer nei backup incrementali e differenziali di VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3c84245c21a47ba5535eccdfcbf10e988cf72b30ea99ee92086a9ca8f65647
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863871"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Ruolo writer nei backup incrementali e differenziali di VSS

La partecipazione di un writer ai backup incrementali e differenziali avviene in genere durante la gestione degli eventi [*Identify*](vssgloss-i.md) ([**CVssWriter::OnIdentify),**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter:OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) e *PostSnapshot* ([**CVssWriter:OnPostSnapshot).**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) La modalità di partecipazione di un writer è data dal fatto che supporti i timestamp di backup e l'ora dell'ultima modifica e dal fatto che il richiedente che esegue il backup supporti operazioni [*di file parziali.*](vssgloss-p.md)

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Gestione degli eventi di identificazione durante i backup incrementali e differenziali

Durante la gestione dell'evento Identify, i writer stabiliscono l'architettura di base per l'operazione di backup incrementale e differenziale tramite le maschere dello schema di backup ([**VSS \_ BACKUP \_ SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) e del tipo di backup della specifica file ([**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE).**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)

Un writer indica le operazioni supportate nel documento di metadati del writer creando una maschera di bit dei valori [**DELLO \_ \_ SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) DI BACKUP di VSS e passandola al metodo [**IVssCreateWriterMetadata::SetBackupSchema.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) In questo modo, un writer può indicare se supporta quanto segue:

-   Backup incrementali (**VSS \_ BS \_ INCREMENTAL**)
-   Backup differenziali (**VSS \_ BS \_ DIFFERENTIAL**)
-   I backup incrementali e differenziali non possono essere misti (**\_ VSS BS \_ EXCLUSIVE INCREMENTAL \_ \_ DIFFERENTIAL**)
-   Backup incrementali e differenziali con indicatori di backup (**\_ VSS BS \_ TIMESTAMPED**)
-   Backup incrementali e differenziali in base alle informazioni sull'ultima modifica di un file (**\_ VSS BS \_ LAST \_ MODIFY**)

I writer usano la maschera del tipo di backup della specifica di file per fornire informazioni a livello di set di file ai richiedenti su come includere file in un backup incrementale o differenziale.

Un writer può impostare la maschera del tipo di backup della specifica file di un set di file quando aggiunge il set di file a un componente creando una maschera di bit dei valori [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) e passandola a [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup).

Esistono tre valori "necessari per il backup" dell'enumerazione [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che influiscono sui backup differenziali e incrementali:

-   **VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED**
-   **BACKUP INCREMENTALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO**
-   **BACKUP DIFFERENZIALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO**

Sono disponibili tre valori "copia shadow obbligatoria":

-   **VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED**
-   **SNAPSHOT INCREMENTALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO**
-   **È NECESSARIO UNO SNAPSHOT DIFFERENZIALE DI VSS \_ FSBT \_ \_ \_**

I set di file contrassegnati con un tipo di backup di specifica file "copia shadow obbligatoria" indicano se un richiedente deve copiare i dati da una copia shadow durante l'esecuzione di operazioni di backup INCREMENTAL, DIFFERENZIALE o ALL (che include operazioni incrementali e differenziali).

Il flag "backup obbligatorio", applicato alle operazioni di backup INCREMENTAL, DIFFERENZIALE o ALL, indica che il writer prevede la disponibilità di una copia della versione corrente del set di file dopo il ripristino di qualsiasi operazione di backup. In genere, ciò significa che se un set di file è contrassegnato con "backup obbligatorio", tutti i relativi membri verranno copiati nei supporti di backup durante un backup incrementale o differenziale, indipendentemente dall'ultima volta che si è verificato il backup o la modifica.

Per impostazione predefinita, i set di file vengono aggiunti ai componenti con un tipo di backup della specifica di file **DI VSS \_ FSBT \_ ALL BACKUP \_ \_ REQUIRED** \| **VSS \_ FSBT \_ ALL SNAPSHOT \_ \_ REQUIRED**. Pertanto, a meno che uno sviluppatore di writer non decida di non usare l'impostazione predefinita (scegliendo un altro tipo di backup della specifica di file, usando operazioni di file parziali o usando file con differenze), i file nella maggior parte dei set di file verranno in genere copiati nella loro interezza nei supporti di backup.

A questo punto, il documento dei metadati del writer è completamente popolato con la maggior parte delle informazioni necessarie a un richiedente per avviare un backup differenziale o incrementale. L'aggiunta di informazioni sul set di file o sul livello di file per supportare il backup verrà gestita durante [**l'evento PrepareForBackup.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Gestione degli eventi PrepareForBackup durante i backup incrementali e differenziali

Prima che il richiedente proceda con l'operazione di backup effettiva, i writer possono modificare la specifica di un backup [*incrementale*](vssgloss-i.md) o [*differenziale*](vssgloss-d.md) modificando il documento dei componenti di backup del richiedente tramite l'interfaccia [**IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Poiché i writer usano [**l'interfaccia IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) in genere eseguono queste preparazioni durante la gestione [**dell'evento PrepareForBackup.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)

In [**CVssWriter:OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)i writer possono specificare in modo più preciso come valutare alcuni file per il backup, specificare i meccanismi da usare per il backup ed eventualmente impostare i timestamp di backup.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>File parziali
</dt> <dd>

Se un richiedente li supporta, un writer può scegliere di avere un backup incrementale o differenziale implementato tramite operazioni di file parziali. I writer possono determinare se un richiedente supporta operazioni di file parziali chiamando [**CVssWriter::IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled).

I writer usano [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) per indicare le parti dei file selezionati di cui eseguire il backup durante l'operazione incrementale o differenziale. I richiedenti devono rispettare questa specifica e devono sempre eseguire il backup delle sezioni specificate dei file. Per altre informazioni sulle operazioni sui file [parziali,](working-with-partial-files.md) vedere Uso di file parziali.

Usando [**IVssComponent::AddPartialFile,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)un writer può aggiungere un file al backup non aggiunto in precedenza a uno dei relativi set di componenti (da [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)come file parziale. Tutti i nuovi file aggiunti al backup in questo modo devono essere in un volume già copiato shadow per questo backup.

Se un file è coinvolto in operazioni di file parziali, questo sostituisce qualsiasi tipo di backup della specifica di file, che viene ignorato.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>File con differenze
</dt> <dd>

I writer che supportano un ultimo schema di backup modificato (**VSS \_ BS \_ SCHEMA**) possono aggiungere file con differenze [*a*](vssgloss-d.md) un backup incrementale o differenziale.

Quando si specifica un file con differenze, un writer usa [**IVssComponent::AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) e specifica un percorso, un nome file e un flag ricorsivo, ma non devono corrispondere a un set di file incluso in alcun componente.

Un writer può infatti aggiungere un file non aggiunto in precedenza a uno dei relativi set di componenti (da [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)al backup come file con differenze. Tutti i nuovi file aggiunti al backup in questo modo devono essere in un volume già copiato shadow per questo backup.

In genere, un writer specifica anche l'ora dell'ultima modifica quando si aggiunge un file con differenze, in base al meccanismo di cronologia del writer. L'ora dell'ultima modifica, se specificata, deve essere sempre usata dai richiedenti per determinare se un file deve essere incluso in un backup incrementale o differenziale.

Un writer può scegliere di non specificare un'ora dell'ultima modifica quando si aggiunge un file con differenze a un set di backup incrementale o differenziale. In questo caso, i richiedenti possono usare i propri meccanismi, ad esempio i log dei backup precedenti o le informazioni file system, per determinare se il file con differenze deve essere incluso in un backup incrementale o differenziale.

Il tipo di backup della specifica file di qualsiasi file con differenze viene ignorato.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Stamp di backup
</dt> <dd>

I writer che supportano gli indicatori di backup (**VSS \_ BS \_ TIMESTAMP**) hanno un proprio formato privato per l'archiviazione delle informazioni sull'ultimo backup. Queste informazioni vengono generate dal writer durante il backup.

Il timbro di backup viene archiviato nel documento Componenti di backup come stringa dal [**metodo IVssComponent::SetBackupStamp.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) Il timestamp di backup si applica a tutti i set di file nel componente (o nel set di componenti) corrispondente all'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Se un richiedente ha accesso al timestamp di backup di un backup precedente, lo ha reso disponibile al writer chiamando [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp).

Un writer può quindi esaminare questo timestamp usando [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).

Si noti che il richiedente archivia e restituisce semplicemente la stringa contenente il timbro di backup. Non sa nulla sul formato della stringa o su come usarlo. solo il writer ha queste informazioni.

Un writer può scegliere di aggiornare il timbro di backup corrente usando [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) dopo aver chiamato [**IVssComponent::GetPreviousBackupStamp,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)registrando così nel proprio formato la data dell'operazione di backup incrementale o differenziale corrente.

</dd> </dl>

 

 



