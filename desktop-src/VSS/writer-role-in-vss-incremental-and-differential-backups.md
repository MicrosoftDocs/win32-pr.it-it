---
description: 'La partecipazione di un writer ai backup incrementali e differenziali avviene in genere durante la gestione di eventi di identificazione (CVssWriter:: onidentifi), PrepareForBackup (CVssWriter: OnPrepareBackup) e PostSnapshot (CVssWriter: OnPostSnapshot).'
ms.assetid: 85c4e003-b531-4283-83aa-dd5cc53f35b1
title: Ruolo writer nei backup incrementali e differenziali VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2cda57d907bed4572f0c0f71f9ee829bee18299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526256"
---
# <a name="writer-role-in-vss-incremental-and-differential-backups"></a>Ruolo writer nei backup incrementali e differenziali VSS

La partecipazione di un writer ai backup incrementali e differenziali avviene in genere durante la gestione di eventi di [*Identificazione*](vssgloss-i.md) ([**CVssWriter:: onidentifi**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify)), [*PrepareForBackup*](vssgloss-p.md) ([**CVssWriter: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup)) e *PostSnapshot* ([**CVssWriter: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)). Il modo in cui un writer partecipa viene definito in base a come supporta timbri di backup e ora dell'Ultima modifica e se il richiedente che esegue il backup supporta [*operazioni parziali su file*](vssgloss-p.md).

## <a name="handling-identify-events-during-incremental-and-differential-backups"></a>Gestione degli eventi di identificazione durante i backup incrementali e differenziali

Durante la gestione dell'evento di identificazione, i writer stabiliscono l'architettura di base per l'operazione di backup incrementale e differenziale tramite lo schema di backup ([**\_ \_ schema di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)) e le maschere del tipo di backup delle specifiche file ([**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type))

Un writer indica le operazioni supportate nel documento di metadati del writer creando una maschera di bit dei [**valori \_ \_ dello schema di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) e passandola al metodo [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) . Con questo, un writer può indicare se supporta quanto segue:

-   Backup incrementali (**VSS \_ BS \_ incrementale**)
-   Backup differenziali (**\_ \_ differenziale VSS BS**)
-   Non è possibile combinare i backup incrementali e differenziali (**VSS \_ BS \_ Exclusive \_ unincrement \_**)
-   Backup incrementali e differenziali con timbri di backup (con **\_ \_ timestamp di VSS BS**)
-   Backup incrementali e differenziali sulla base delle informazioni sull'Ultima modifica di un file (**\_ \_ Ultima \_ modifica di VSS BS**)

I writer utilizzano la maschera del tipo di backup specifica file per fornire informazioni a livello di set di file ai richiedenti su come includere i file in un backup incrementale o differenziale.

Un writer può impostare la maschera del tipo di backup delle specifiche file di un set di file quando aggiunge il set di file a un componente creando una maschera di bit dei valori del [**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) e passandolo a [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup).

Sono disponibili tre valori "backup obbligatorio" dell'enumerazione [**del \_ \_ tipo di \_ backup \_ delle specifiche del file VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che interessano i backup differenziali e incrementali:

-   **VSS \_ FSBT \_ tutti i \_ backup \_ necessari**
-   **è \_ \_ necessario il backup incrementale FSBT VSS \_ \_**
-   **è \_ \_ necessario il \_ backup DIFFERENZIAle FSBT VSS \_**

Sono disponibili tre valori "copia shadow obbligatoria":

-   **VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari**
-   **\_ \_ snapshot incrementale FSBT \_ VSS \_ obbligatorio**
-   **\_ \_ snapshot differenziale FSBT VSS \_ \_ obbligatorio**

I set di file contrassegnati con un tipo di backup della specifica del file "copia shadow obbligatoria" indicano se un richiedente deve copiare i dati da una copia shadow durante l'esecuzione di operazioni di backup INCREMENTAli, DIFFERENZIAli o tutte (che includono operazioni sia incrementali che differenziali).

Il flag "backup obbligatorio", applicato a operazioni INCREMENTAli, DIFFERENZIAli o di backup, indica che il writer prevede una copia della versione corrente del set di file in modo che sia disponibile dopo il ripristino di qualsiasi operazione di backup. In genere, ciò significa che se un set di file è contrassegnato con "backup obbligatorio", tutti i relativi membri verranno copiati nei supporti di backup durante un backup incrementale o differenziale, indipendentemente dal momento in cui si è verificata l'ultima modifica o backup.

Per impostazione predefinita, i set di file vengono aggiunti ai componenti con un tipo di backup della specifica del file **VSS \_ FSBT \_ tutti i \_ backup \_ necessari** \| **VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari**. Pertanto, a meno che uno sviluppatore di writer non decida di non utilizzare l'impostazione predefinita (scegliendo un altro tipo di backup di specifica file, usando operazioni di file parziali o usando file differenziati), i file nella maggior parte dei set di file verranno in genere copiati interamente nei supporti di backup.

A questo punto, il documento di metadati del writer del writer è completamente popolato con la maggior parte delle informazioni che un richiedente dovrà avviare un backup differenziale o incrementale. La specifica di aggiunta di informazioni a livello di file o set di file per supportare il backup verrà gestita durante l'evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

## <a name="handling-prepareforbackup-events-during-incremental-and-differential-backups"></a>Gestione degli eventi PrepareForBackup durante i backup incrementali e differenziali

Prima che il richiedente proceda con l'operazione di backup effettiva, i writer possono modificare la specifica di un backup [*incrementale*](vssgloss-i.md) o [*differenziale*](vssgloss-d.md) modificando il documento relativo ai componenti di backup del richiedente tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Poiché i writer utilizzano l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , in genere eseguono tali preparazioni durante la gestione dell'evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

In [**CVssWriter: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), i writer possono specificare in modo più preciso la modalità di valutazione di alcuni file per il backup, specificare quali meccanismi devono essere usati per eseguirne il backup ed eventualmente impostare timbri di backup.

<dl> <dt>

<span id="Partial_Files"></span><span id="partial_files"></span><span id="PARTIAL_FILES"></span>File parziali
</dt> <dd>

Se un richiedente li supporta, un writer può scegliere di disporre di un backup incrementale o differenziale implementato usando operazioni parziali su file. (I writer possono determinare se un richiedente supporta operazioni parziali sui file chiamando [**CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled)).

I writer utilizzano [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) per indicare le parti dei file selezionati di cui eseguire il backup durante l'operazione incrementale o differenziale. I richiedenti devono rispettare questa specifica e devono sempre eseguire il backup delle sezioni specificate dei file. Per ulteriori informazioni sulle operazioni di file parziali, vedere [utilizzo dei file parziali](working-with-partial-files.md) .

Se si usa [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile), un writer può aggiungere un file al backup che non è stato aggiunto in precedenza a uno dei relativi set di componenti (per [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) come file parziale. Tutti i nuovi file aggiunti al backup in questo modo devono trovarsi in un volume che è già stato replicato per questo backup.

Se un file è incluso in operazioni di file parziali, sostituisce qualsiasi tipo di backup delle specifiche di file, che viene ignorato.

</dd> <dt>

<span id="Differenced_Files"></span><span id="differenced_files"></span><span id="DIFFERENCED_FILES"></span>File differenziati
</dt> <dd>

I writer che supportano un ultimo schema di backup modificato (**\_ \_ schema** del servizio Copia Shadow del volume) possono aggiungere [*file*](vssgloss-d.md) differenziati a un backup incrementale o differenziale.

Quando si specifica un file differenziato, un writer USA [**IVssComponent:: AddDifferencedFileByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) e specifica un percorso, un nome di file e un flag ricorsivo. tali elementi, tuttavia, non devono corrispondere a un set di file incluso in alcun componente.

Un writer può infatti aggiungere un file non aggiunto in precedenza a uno dei relativi set di componenti (da [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) al backup come file differenziato. Tutti i nuovi file aggiunti al backup in questo modo devono trovarsi in un volume che è già stato replicato per questo backup.

In genere, un writer specifica anche l'ora dell'Ultima modifica quando si aggiunge un file differenziato, in base al meccanismo di cronologia del writer. L'ora dell'Ultima modifica, se specificata, deve essere sempre utilizzata dai richiedenti per determinare se un file deve essere incluso in un backup incrementale o differenziale.

Un writer può scegliere di non specificare l'ora dell'Ultima modifica quando si aggiunge un file differenziato a un set di backup incrementale o differenziale. In tal caso, i richiedenti possono usare i propri meccanismi, ad esempio i log dei backup precedenti o informazioni file system, per determinare se il file differenziato deve essere incluso in un backup incrementale o differenziale.

Il tipo di backup specifica file di qualsiasi file differenziato viene ignorato.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Timbri di backup
</dt> <dd>

I writer che supportano i timbri di backup (**\_ \_ timestamp del VSS BS**) hanno un proprio formato privato per archiviare le informazioni relative al momento in cui si è verificato l'ultimo backup. Queste informazioni vengono generate dal writer durante il backup.

Il timbro di backup viene archiviato nel documento componenti di backup sotto forma di stringa tramite il metodo [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) . Il timbro di backup si applica a tutti i set di file nel componente (o set di componenti) corrispondente all'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Se un richiedente ha accesso all'indicatore di backup di un backup precedente, sarà reso disponibile al writer chiamando [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp).

Un writer può quindi esaminare questo timestamp usando [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp).

Si noti che il richiedente archivia solo e restituisce la stringa contenente l'indicatore di backup. Non è in grado di conoscere il formato della stringa o come utilizzarlo; solo il writer ha tali informazioni.

Un writer può scegliere di aggiornare l'indicatore di backup corrente usando [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) dopo che è stato chiamato [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp), in modo da registrare nel proprio formato la data dell'operazione di backup incrementale o differenziale corrente.

</dd> </dl>

 

 



