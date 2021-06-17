---
description: Informazioni sul ruolo di writer nei backup incrementali e differenziali, che richiedono una stretta collaborazione tra richiedenti e writer.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Ruolo writer nel backup di archivi complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30e34952cc4a2184d2f9abcc43283d24f64bdcc3
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262153"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Ruolo writer nel backup di archivi complessi

Come per tutte le operazioni importanti in VSS, i [*backup*](vssgloss-d.md) [*incrementali*](vssgloss-i.md) e differenziali richiedono una stretta collaborazione tra richiedenti e writer.

## <a name="backup-types"></a>Tipi di backup

L'infrastruttura offre un supporto speciale per cinque tipi di backup. Sono descritte come segue:

-   Completo **(VSS \_ BT \_ FULL).** Verrà eseguito il backup dei file indipendentemente dalla data dell'ultimo backup. La cronologia di backup di ogni file verrà aggiornata e questo tipo di backup può essere utilizzato come base per un backup incrementale o differenziale. Se sono presenti file di log, è possibile che siano troncati in seguito a questo backup.

    Il ripristino di un backup completo richiede una sola immagine di backup.

-   Differenziale (**VSS \_ BT \_ DIFFERENTIAL**). L'API vss viene usata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo devono essere copiati in un supporto di archiviazione; tutte le informazioni di backup intermedie vengono ignorate. Può trattarsi di interi file o intervalli specifici all'interno dei file. Un backup differenziale è associato a un backup completo e in genere non può essere ripristinato fino a quando non viene ripristinato il backup completo. Se sono presenti file di log, in genere non verranno troncati come risultato di questo backup.

    Il ripristino di un backup differenziale richiede l'immagine di backup originale e l'immagine di backup differenziale più recente dall'ultimo backup completo.

-   Incrementale (**VSS \_ BT \_ INCREMENTAL**). L'API vss viene usata per garantire che solo i file modificati o aggiunti dopo l'ultimo backup completo o incrementale devono essere copiati in un supporto di archiviazione. Può trattarsi di interi file o intervalli specifici all'interno dei file. Alcuni writer non consentono l'esecuzione di backup incrementali con backup differenziali. Se sono presenti file di log, è possibile che siano troncati in seguito a questo backup.

    Il ripristino di un backup incrementale richiede l'immagine di backup originale e tutte le immagini di backup incrementale effettuate dopo il backup iniziale.

-   Backup del log (**VSS \_ BT \_ LOG**). Verrà eseguito il backup solo dei file di log di un writer (file aggiunti a un componente con il metodo [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperati da una chiamata a [**IVssWMComponent::GetDatabaseLogFile).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) Questo tipo di backup è specifico di VSS. I backup del log tendono a essere evasi con una frequenza piuttosto frequente. In genere, il file di log verrà troncato in seguito a questo backup.
-   Copiare il backup (**VSS \_ BT \_ COPY**). Analogamente al tipo di backup FULL di VSS BT, verrà eseguito il backup dei file \_ \_ indipendentemente dalla data dell'ultimo backup. Tuttavia, la cronologia di backup di ogni file non verrà aggiornata e questo tipo di backup non può essere utilizzato come base di un backup incrementale o differenziale. I file di log non devono mai essere troncati in seguito a un backup di copia.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Supporto di file parziali
</dt> <dd>

Alcuni writer supportano il ripristino dei file tramite la sovrascrittura di parti dei file gestiti. Un richiedente può essere progettato per sfruttare questo vantaggio e, in tal caso, lo indica impostando le informazioni in [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

I writer indicano il tipo di backup supportato chiamando [**IVssCreateWriterMetadata::SetBackupSchema durante**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) l'elaborazione [*dell'evento Identify.*](vssgloss-i.md) Il *parametro dsSchemaMask* per il metodo **IVssCreateWriterMetadata::SetBackupSchema** è una maschera di bit che indica i tipi di backup supportati. Tutti i writer devono supportare backup completi.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**DIFFERENZIALE \_ VSS BS \_**
</dt> <dd>

Indica il supporto per i backup differenziali.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**VSS \_ BS \_ INCREMENTAL**
</dt> <dd>

Indica il supporto per i backup incrementali.

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**LOG DI VSS \_ BS \_**
</dt> <dd>

Indica il supporto per i backup del log.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**COPIA DI VSS \_ BS \_**
</dt> <dd>

Indica il supporto per i backup di copia.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**DIFFERENZIALE \_ INCREMENTALE ESCLUSIVO VSS BS \_ \_ \_**
</dt> <dd>

Indica che un writer non supporta la combinazione di backup incrementali con backup differenziali.

</dd> </dl>

Il writer può determinare il tipo di backup eseguito chiamando [**CVssWriter::GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype). Il punto meno recente in cui questa operazione può essere eseguita è durante l'elaborazione dell'evento PrepareForBackup. **CVssWriter::GetBackupType** restituirà un membro [**dell'enumerazione \_ VSS BACKUP \_ TYPE.**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) Se il tipo di backup non è supportato dal writer, il writer deve considerare il backup come backup completo.

## <a name="backup-stamps"></a>Stamp di backup

I backup incrementali e differenziali sono sempre associati a un backup precedente. Esistono due modi per collegare i backup. Per gli archivi dati semplici, il richiedente può tenere traccia della correlazione tra i backup. Tuttavia, per gli archivi dati più complessi, il writer dovrà mantenere il proprio timestamp con il backup. questo timestamp può tenere traccia della posizione del log, delle informazioni sui checkpoint e così via. Un writer indica che è necessario un timestamp personalizzato impostando il bit **\_ \_ TIMESTAMPED di VSS BS** quando chiama [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema).

Un writer può archiviare un timestamp con ogni componente di cui viene eseguito il backup. Il writer archivia il timestamp chiamando [**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)e passando una rappresentazione di stringa del timestamp per *il parametro wszBackupStamp.* In genere, un writer chiamerà questo metodo durante l'elaborazione [*dell'evento PostSnapshot.*](vssgloss-p.md) Tuttavia, per i backup che non coinvolgono una copia shadow, l'evento PostSnapshot non verrà inviato. In questo caso, **è necessario chiamare IVssComponent::SetBackupStamp** durante l'elaborazione dell'evento [*PrepareForBackup.*](vssgloss-p.md)

Quando viene eseguito un backup incrementale o differenziale, il richiedente indicherà al writer il timestamp di backup del backup precedente che funge da base per questo backup. Il writer può accedere a questo stamp di backup precedente durante l'elaborazione dell'evento PrepareForBackup o PostSnapshot chiamando [**IVssComponent::GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Il writer può usare lo stamp restituito per determinare gli elementi di cui eseguire il backup.

## <a name="backup-strategies"></a>Strategie di backup

### <a name="file-backup-files-strategies"></a>Strategie per i file di backup dei file

Spesso, alcuni file segnalati nei metadati del writer devono essere sottoposti a backup solo quando si eseguono determinati tipi di backup. Alcuni file possono essere necessari solo quando si esegue un backup completo. Altri file possono essere necessari solo quando si esegue un backup incrementale o differenziale. VsS fornisce un metodo per i writer per indicare queste informazioni al richiedente. Quando si aggiungono file ai componenti usando [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), il *parametro dwBackupTypeMask* indica per quali tipi di backup è necessario eseguire il backup di questi file. La maschera può contenere uno o più dei valori seguenti:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**BACKUP COMPLETO \_ DI VSS FSBT \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup completi.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**BACKUP \_ DIFFERENZIALE DI VSS FSBT \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup differenziali.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**BACKUP \_ INCREMENTALE DI VSS FSBT \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup incrementali.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**BACKUP DEL LOG FSBT VSS \_ \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup del log.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED**
</dt> <dd>

Obbligatorio per tutti i tipi di backup. si tratta dell'impostazione predefinita.

</dd> </dl>

Questa specifica sostituisce la specifica di selettività del componente. Si consideri ad esempio un componente i cui file sono tutti contrassegnati con **VSS \_ FSBT \_ LOG BACKUP \_ \_ REQUIRED** ma non con **VSS \_ FSBT \_ FULL BACKUP \_ \_ REQUIRED**. Si supponga che questo componente non sia selezionabile per il backup (*bSelectable* era false quando è stato chiamato [**IVssCreateWriterMetadata::AddComponent).**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) Nel caso di un backup del log, è necessario eseguire sempre il backup di tutti i file in questo componente. Tuttavia, nel caso di un backup completo, non è necessario eseguire il backup di nessuno dei file, anche se la selettività del componente implica che deve essere eseguito il backup.

### <a name="backup-by-last-modify-time"></a>Backup in base all'ora dell'ultima modifica

Un modo per un writer per indicare quali file sono stati modificati consiste nell'usare il meccanismo dei file differenze. Un writer può specificare che deve essere eseguito il backup di determinati file in un componente solo se sono stati modificati da un determinato momento. Il writer chiama [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) con una specifica di file e un'ora dell'ultima modifica. **IVssComponent::AddDifferencedFilesByLastModifyTime** viene in genere chiamato durante l'elaborazione dell'evento PostSnapshot, anche se può essere chiamato durante l'elaborazione dell'evento PrepareForBackup. Il richiedente deve quindi eseguire il backup di tutti i file corrispondenti alla specifica di file che sono stati modificati dopo l'ora specificata. Se il writer usa il meccanismo di stamp di backup, l'ora dell'ultima modifica verrà determinata in base al timestamp di backup precedente nel documento di backup. Il writer può anche passare zero per l'ora dell'ultima modifica, a indicare che il richiedente è responsabile della determinazione dell'ora dell'ultimo backup e dei file modificati da quel momento.

### <a name="partial-file-backup"></a>Backup parziale di file

Un altro modo per un writer per indicare le modifiche al richiedente è l'uso del meccanismo di file parziale. Un writer può specificare intervalli di byte all'interno dei file dei componenti di cui è necessario eseguire il backup. Il writer può specificare questi intervalli di file durante l'elaborazione dell'evento PostSnapshot o PrepareForBackup. Il writer chiama [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) per aggiungere specifiche di file parziali al backup. Una specifica di file parziale è costituita da un percorso e un nome file insieme a informazioni sugli intervalli nel file di cui eseguire il backup.

### <a name="file-specification-rules"></a>Regole di specifica dei file

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) o [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) possono essere entrambi usati per modificare le specifiche di file fornite durante l'evento Identify o per aggiungere file completamente nuovi alla specifica. Se il writer modifica le informazioni impostate durante l'evento Identify usando **IVssComponent::AddDifferencedFilesByLastModifyTime,** la specifica del file deve corrispondere esattamente a una delle specifiche di file nel componente corrente. La specifica del file non deve sovrapporsi parzialmente ai file nel componente corrente e non deve corrispondere ai file in altri componenti. I file specificati **usando IVssComponent::AddPartialFile** possono tuttavia sovrapporsi parzialmente a un'altra specifica di file. Le informazioni impostate da **IVssComponent::AddDifferencedFilesByLastModifyTime** o **IVssComponent::AddPartialFile** sostituiscono le informazioni impostate in precedenza usando l'interfaccia [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) in risposta all'evento Identify.

Le specifiche di file generali possono avere un valore di posizione alternativa (impostato dal parametro *wszAlternateLocation* di [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) che indica un percorso alternativo da cui ottenere il file in fase di backup. Se la specifica del file impostata tramite i meccanismi differenced-file o partial-file corrisponde a una specifica di file esistente con un percorso alternativo, l'applicazione di backup o ottiene i dati da questo percorso alternativo.

Se la specifica del file impostata in [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) o in [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) non corrisponde ai file e nel componente di cui viene eseguito il backup, tutti i file corrispondenti vengono ora aggiunti al backup. È necessario fare attenzione che durante questa operazione il writer aseonda solo i file esistenti in un volume che è già in fase di copia shadow. In caso contrario, il richiedente potrebbe non riuscire a eseguire il backup di questi file. Se queste funzioni vengono chiamate durante l'elaborazione dell'evento PostSnapshot, è possibile determinarlo usando il [**metodo CVssWriter::IsPathAffected.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) Se viene chiamato durante la gestione dell'evento PrepareForBackup, il writer deve effettuare questa determinazione usando un altro metodo.

### <a name="backup-without-a-shadow-copy"></a>Backup senza copia shadow

Potrebbe non essere necessario eseguire il backup di alcuni tipi di file da un volume di copia shadow. Ad esempio, questo vale spesso per i file di log del database. Poiché le dimensioni dei file di log aumentano in modo monotona e un writer può specificare esattamente le parti del file di cui eseguire il backup usando file parziali, è spesso possibile eseguire il backup della disconnessione dal volume originale. Come ottimizzazione, un writer può contrassegnare i file che richiedono copie shadow per tipi di backup diversi usando i flag impostati nel parametro *dwBackupTypeMask* di [**IVssCreateWriterMetadata::AddDatabaseFiles,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup). I flag supportati includono:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**VSS \_ FSBT \_ FULL \_ SNAPSHOT \_ REQUIRED**
</dt> <dd>

Copia shadow necessaria per i backup completi.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**VSS \_ FSBT \_ DIFFERENTIAL \_ SNAPSHOT \_ REQUIRED**
</dt> <dd>

Copia shadow necessaria per i backup differenziali.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**VSS \_ FSBT \_ INCREMENTAL \_ SNAPSHOT \_ REQUIRED**
</dt> <dd>

Copia shadow necessaria per i backup incrementali.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**VSS \_ FSBT \_ LOG \_ SNAPSHOT \_ REQUIRED**
</dt> <dd>

Copia shadow necessaria per i backup del log.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED**
</dt> <dd>

Copia shadow necessaria per tutti i tipi di backup. si tratta dell'impostazione predefinita.

</dd> </dl>

Se un volume specifico contiene solo componenti che non richiedono una copia shadow per questo backup, il richiedente può ignorare il passaggio di creazione di una copia shadow per questo volume. Tutti i dati in questo volume possono essere copiati nel supporto di backup direttamente dal volume originale.

## <a name="backup-cleanup"></a>Pulizia dei backup

Se il writer deve eseguire il troncamento del log o un'altra pulizia post-backup, la posizione corretta per eseguire questa operazione è durante l'elaborazione [*dell'evento BackupComplete.*](vssgloss-b.md) [*L'evento BackupShutdown*](vssgloss-b.md) verrà inviato dopo BackupComplete, quindi è possibile eseguire alcune operazioni di pulizia anche nel gestore dell'evento BackupShutdown.

L'evento BackupShutdown viene sempre inviato dopo la chiusura di un backup. Se il richiedente termina in modo anomalo durante l'esecuzione di un backup, BackupShutdown verrà inviato immediatamente, senza prima inviare BackupComplete. Se il writer deve eseguire la pulizia di uno stato, questa operazione può essere eseguita qui. Tuttavia, il troncamento del log non dovrebbe verificarsi in questo evento perché il backup non è stato necessariamente completato.

## <a name="restore-strategies"></a>Strategie di ripristino

Le attività di base dei writer al momento del ripristino sono la verifica che il ripristino possa avvenire nella gestione dell'evento PreRestore e che il ripristino si sia verificato nella gestione dell'evento PostRestore. Gli archivi più complessi eseguiranno anche un processo di ripristino nel gestore PostRestore. Se il ripristino fa parte di un ripristino incrementale o differenziale, il writer in genere vorrà ritardare il processo di ripristino fino al completamento di tutti i ripristini incrementali o differenziali. [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) indicherà se si tratta del ripristino finale di questo componente o se saranno disponibili altri ripristini. Se **IVssComponent::GetAdditionalRestores** restituisce **true,** il writer non deve eseguire la procedura di ripristino su tale componente.

## <a name="new-targets"></a>Nuove destinazioni

Se supportato dal writer, il richiedente può ripristinare i file di dati in un percorso diverso da quello dell'ora di backup originale. Un writer indica il supporto per questa modalità di ripristino impostando il bit **\_ VSS BS \_ WRITER \_ SUPPORTS \_ NEW \_ TARGET** nel parametro *dsSchemaMask* quando si chiama [**IVssCreateWriterMetadata::SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema). Un writer ottiene i nuovi percorsi per i file dei componenti in fase di ripristino chiamando [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent::GetNewTarget.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

## <a name="directed-targets"></a>Destinazioni indirizzate

Per scenari di ripristino complessi, un writer potrebbe voler eseguire il mapping di intervalli di un file di cui è stato eseguito il backup in intervalli diversi dello stesso file o in un file diverso. Questa operazione può essere eseguita usando il meccanismo di destinazione diretta. A tale scopo, un writer deve prima indicare che ciò si verifica chiamando [**IVssComponent::SetRestoreTarget,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)passando **VSS \_ RT \_ DIRECTED** per il parametro *di* destinazione. Quindi, per ogni mapping, il writer chiama [**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget). Questo metodo accetta un percorso completo di un file di origine nel backup e un percorso completo di un file di destinazione in cui verrà ripristinato . Accetta anche un elenco di intervalli per ognuno di questi file. Il writer chiama queste funzioni durante la gestione dell'evento PreRestore e il richiedente è quindi responsabile del ripristino degli intervalli specificati nel file di origine negli intervalli mappati nel file di destinazione. Il formato della stringa degli intervalli è lo stesso di [ **IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Metadati del writer privato

È spesso utile per un writer mantenere metadati privati con un backup per eseguire correttamente un ripristino incrementale o differenziale. Un writer può chiamare [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) durante la gestione di PrepareForBackup o PostSnapshot per archiviare i metadati. Il writer può accedere a questi metadati durante PreRestore o PostRestore chiamando [**IVssComponent::GetBackupMetadata.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) I metadati possono anche essere archiviati con la specifica di file parziale usando il *parametro wszMetadata* di [**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile); È possibile accedere a questi metadati *tramite il parametro pbstrMetadata* di [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Il writer può anche passare metadati a se stesso [**tra CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) e [**CVssWriter::OnPostRestore.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) In **CVssWriter::OnPreRestore** i metadati vengono impostati chiamando [**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata). In **CVssWriter::OnPostRestore** i metadati vengono recuperati chiamando [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata).

-   [Ruolo writer nei backup incrementali e differenziali vss](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Ruolo richiedente nei backup incrementali e differenziali vss](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



