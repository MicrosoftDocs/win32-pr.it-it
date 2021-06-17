---
description: Informazioni sul ruolo del richiedente nei backup incrementali e differenziali, che richiedono una stretta collaborazione tra richiedenti e writer.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Ruolo richiedente nel backup di archivi complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84dfa1b0b1837bacc2488b6bd9e3ffdd51b92c0
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262183"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Ruolo richiedente nel backup di archivi complessi

Come per tutte le operazioni importanti in VSS, i backup [*incrementali*](vssgloss-i.md) e [*differenziali*](vssgloss-d.md) richiedono una stretta collaborazione tra richiedenti e writer.

## <a name="backup-type"></a>Tipo di backup

L'infrastruttura offre un supporto speciale per cinque tipi di backup. Sono descritte come segue:

-   Full (**VSS \_ BT \_ FULL**). Verrà eseguito il backup dei file indipendentemente dalla data dell'ultimo backup. La cronologia di backup di ogni file verrà aggiornata e questo tipo di backup può essere usato come base di un backup incrementale o differenziale. Se sono presenti file di log, è possibile che siano troncati in seguito a questo backup.

    Il ripristino di un backup completo richiede una sola immagine di backup.

-   Differenziale (**VSS \_ BT \_ DIFFERENTIAL**). L'API VSS viene usata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo devono essere copiati in un supporto di archiviazione. tutte le informazioni di backup intermedie vengono ignorate. Può includere interi file o intervalli specifici all'interno dei file. Un backup differenziale è associato a un backup completo e in genere non può essere ripristinato fino al ripristino del backup completo. Se sono presenti file di log, in genere non verranno troncati come risultato di questo backup.

    Il ripristino di un backup differenziale richiede l'immagine di backup originale e l'immagine di backup differenziale più recente effettuata dopo l'ultimo backup completo.

-   Incrementale (**VSS \_ BT \_ INCREMENTAL**). L'API VSS viene usata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo o incrementale devono essere copiati in un supporto di archiviazione. Può includere interi file o intervalli specifici all'interno dei file. Alcuni writer non consentono l'esecuzione di backup incrementali con backup differenziali. Se sono presenti file di log, è possibile che siano troncati in seguito a questo backup.

    Il ripristino di un backup incrementale richiede l'immagine di backup originale e tutte le immagini di backup incrementale effettuate dopo il backup iniziale.

-   Backup del log (**VSS \_ BT \_ LOG**). Verrà eseguito il backup solo dei file di log di un writer (file aggiunti a un componente con il metodo [**IVssCreateWriterMetadata::AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperati da una chiamata a [**IVssWMComponent::GetDatabaseLogFile).**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) Questo tipo di backup è specifico di VSS. I backup del log tendono a essere esersi con una frequenza piuttosto frequente. In genere, il file di log verrà troncato in seguito a questo backup.
-   Copiare il backup (**VSS \_ BT \_ COPY**). Analogamente al tipo di backup FULL di VSS BT, verrà eseguito il backup dei file \_ \_ indipendentemente dalla data dell'ultimo backup. Tuttavia, la cronologia di backup di ogni file non verrà aggiornata e questo tipo di backup non può essere usato come base di un backup incrementale o differenziale. I file di log non devono mai essere troncati in seguito a un backup di copia.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Supporto di file parziali
</dt> <dd>

Alcuni writer supportano il ripristino dei file tramite la sovrascrittura di parti dei file gestiti. Un richiedente può essere progettato per sfruttare questo vantaggio e, in tal caso, lo indica impostando le informazioni in [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

Il richiedente specifica il tipo di backup eseguito tramite il parametro *backupType* di [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Writer diversi supporteranno tipi diversi di backup. Dopo aver chiamato [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) il richiedente può determinare i tipi di backup supportati da un determinato writer chiamando [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Il valore restituito è una maschera di bit che indica il supporto per tipi di backup diversi. **VSS \_ BS \_ DIFFERENTIAL** indica il supporto per i backup differenziali, **VSS \_ BS \_ INCREMENTAL** per i backup incrementali, **VSS \_ BS \_ LOG** per i backup del log e **VSS \_ BS \_ COPY** per i backup di copia. Tutti i writer devono supportare i backup completi. Se un writer non supporta la combinazione di backup incrementali con backup differenziali, verrà aggiunto anche il flag **\_ \_ \_ \_ DIFFERENZIALE INCREMENTALE** ESCLUSIVO DI VSS BS. Se il richiedente esegue un backup incrementale o differenziale e un writer specificato non supporta tale tipo di backup, è necessario eseguire un backup completo su tale writer.

## <a name="backup-stamps"></a>Stamp di backup

I backup incrementali e differenziali sono sempre associati a un backup precedente. Esistono due modi per collegare i backup. Per gli archivi dati semplici, il richiedente può tenere traccia della correlazione tra i backup. Tuttavia, per archivi dati più complessi, il writer dovrà mantenere il proprio timestamp con il backup. questo timestamp può tenere traccia della posizione del log, delle informazioni sul checkpoint e così via. Il richiedente può determinare se un determinato writer deve archiviare il proprio timestamp controllando il bit **\_ \_ TIMESTAMPED di VSS BS** nel valore restituito da [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

I writer che archiviano un timestamp in un backup aggiungeranno il timestamp durante l'elaborazione [**di IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o durante l'elaborazione [**di IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Il richiedente può ottenere questo timestamp chiamando [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp). Quando si esegue un backup incrementale o differenziale, il richiedente deve collegare il backup corrente a un backup precedente. Questa operazione viene eseguita ottenendo il timestamp dal backup precedente di un componente specifico e passandolo alla funzione [**IVssBackupComponents::SetPreviousBackupStamp.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) questa operazione deve essere eseguita per ogni componente di cui è stato eseguito il backup nel backup precedente.

## <a name="backing-up-files"></a>Backup di file

### <a name="backing-up-files-reported-by-writer"></a>Backup dei file segnalati dal writer

Ogni specifica di file aggiunta da un writer ai metadati durante la fase GatherWriterMetadata contiene una maschera del tipo di backup che specifica quando eseguire il backup del file. Il richiedente determina che cos'è questa maschera chiamando [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask). I valori in questa maschera vengono usati per determinare per quali tipi di backup deve essere eseguito il backup della specifica di file. La maschera può contenere uno o più dei valori di bit seguenti:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**BACKUP COMPLETO DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup completi.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**BACKUP DIFFERENZIALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup differenziali.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**BACKUP INCREMENTALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup incrementali.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**BACKUP DEL LOG FSBT DI VSS \_ \_ \_ \_ OBBLIGATORIO**
</dt> <dd>

Obbligatorio per i backup del log.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED**
</dt> <dd>

Obbligatorio per tutti i tipi di backup. si tratta dell'impostazione predefinita.

</dd> </dl>

Questa specifica esegue l'override della specifica di selettività del componente. Si consideri ad esempio un componente i cui file sono tutti contrassegnati con **VSS \_ FSBT \_ LOG BACKUP \_ \_ REQUIRED** ma non con **VSS \_ FSBT \_ FULL BACKUP \_ \_ REQUIRED**. Si supponga che questo componente non sia selezionabile per il backup (*bSelectable* era false quando è stato chiamato [**IVssCreateWriterMetadata::AddComponent).**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) Nel caso di un backup del log, ciò significa che è sempre necessario eseguire il backup di tutti i file in questo componente. Tuttavia, nel caso di un backup completo, non è necessario eseguire il backup di nessuno dei file, anche se la selettività del componente implica che deve essere eseguito il backup.

### <a name="backup-by-last-modify-time"></a>Backup in base all'ora dell'ultima modifica

Le informazioni sulla specifica del file specificate nella fase [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) non forniscono al richiedente informazioni sugli elementi modificati dopo l'ultimo backup. Un modo per indicare le modifiche al richiedente da parte di un writer consiste nell'usare il meccanismo di file differenze. Un writer può specificare che è necessario eseguire il backup di determinati file in un componente solo se sono stati modificati da un determinato periodo di tempo. il writer può specificare questi file in [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o in [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un richiedente può determinare questi file chiamando [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Se la specifica del file corrisponde a un set in **IVssBackupComponents::GatherWriterMetadata** (attualmente valido in base alla maschera del tipo di backup), le informazioni sui file con differenze eseguono l'override delle informazioni precedenti. in altri, i file corrispondenti a tale specifica di file vengono ora sottoposti a backup solo se sono stati modificati dopo l'ora specificata. L'ora dell'ultima modifica viene comunicata usando una [**struttura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) Se il valore di questa struttura è zero, significa che l'ora dell'ultima modifica deve essere determinata in base al record del richiedente dell'ora dell'ultimo backup.

### <a name="partial-file-backup"></a>Backup parziale di file

Un altro modo per indicare le modifiche al richiedente da parte di un writer è l'uso del meccanismo di file parziale. Un writer può specificare intervalli di byte all'interno dei file del componente di cui è necessario eseguire il backup; Il writer può specificare questi intervalli di file in [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o in [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un richiedente può determinare questi file chiamando [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). **IVssComponent::GetPartialFile** restituirà un percorso e un nome file che punta al file e una stringa di intervalli che indica gli elementi di cui eseguire il backup nel file. Come per i file con differenze, se il percorso e il nome del file corrispondono a una specifica di file impostata dal writer in [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), le informazioni sul file parziale eseguono l'override dell'impostazione precedente. La stringa ranges può avere due formati: può specificare direttamente gli intervalli oppure può specificare un file contenente informazioni sugli intervalli. Se si specificano direttamente gli intervalli, la sintassi è un elenco delimitato da virgole nel formato offset1:length1, offset2:length2, dove ogni offset e lunghezza è un intero senza segno a 64 bit. Se si specifica un file di intervalli, la stringa degli intervalli deve essere impostata su File= *nomefile*, dove *nomefile* è il percorso completo del file di intervalli. Il file di intervalli stesso è un file binario formattato come elenco di interi senza segno a 64 bit. Il primo numero intero indica il numero di intervalli rappresentati nel file. Ogni coppia successiva di interi rappresenta l'offset e la lunghezza di un intervallo. Il richiedente deve eseguire anche il backup e il ripristino di questo file di intervalli.

### <a name="file-specification-rules"></a>Regole di specifica dei file

Le specifiche di file aggiunte tramite i meccanismi differenced-file e partial-file modificheranno le specifiche di file impostate in [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) o aggiungeranno file completamente nuovi. Se si modificano le specifiche dei file impostate in **IVssBackupComponents::GatherWriterMetadata** usando il meccanismo di file parziale, un richiedente può aspettarsi che la specifica del file corrisponda esattamente a una delle specifiche di file impostate nel componente in **IVssBackupComponents::GatherWriterMetadata**. La specifica del file non si sovrapporrà parzialmente a un'altra specifica di file e non corrisponderà ad alcuna specifica di file in altri componenti del writer. Le specifiche di file aggiunte usando il meccanismo del file parziale possono tuttavia sovrapporsi parzialmente a un'altra specifica di file. In questo caso, la specifica differenced-file o partial-file sostituisce la specifica impostata in **IVssBackupComponents::GatherWriterMetadata**. Le specifiche di file generali possono avere un valore di posizione alternativa (restituito da [**IVssWMFiledesc::GetAlternateLocation)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)che indica una posizione alternativa da cui ottenere il file in fase di backup. Se le specifiche di file impostate tramite i meccanismi di file differenze o parziali corrispondono a una specifica di file esistente con un percorso alternativo, i dati devono essere prelevati da questo percorso alternativo. Se le specifiche di file impostate tramite i meccanismi differenced-file o partial-file non corrispondono ad alcuna specifica esistente per il componente, questi intervalli di file dovrebbero ora essere aggiunti al backup. Il richiedente può prevedere che solo i file nei volumi già inclusi nel set di copie shadow verranno aggiunti usando uno di questi meccanismi.

### <a name="backup-without-a-shadow-copy"></a>Backup senza copia shadow

Potrebbe non essere necessario eseguire il backup di alcuni tipi di file da un volume di copia shadow. Ad esempio, questo vale spesso per i file di log del database. Poiché le dimensioni dei file di log aumentano in modo monotona e un writer può specificare esattamente le parti del file di cui eseguire il backup usando file parziali, è spesso possibile eseguire il backup della disconnessione dal volume originale. Come ottimizzazione, un writer può contrassegnare i file che richiedono copie shadow per tipi di backup diversi usando la maschera del tipo di backup. Il valore restituito [**da IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) può contenere uno o più dei valori di bit seguenti:

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

## <a name="restoring-files"></a>Ripristino di file

### <a name="sequential-restores"></a>Ripristini sequenziali

Dopo che il richiedente ha eseguito un'operazione di ripristino, invia l'evento PostRestore a tutti i writer. In genere, i writer gestiscono questo evento eseguendo il ripristino o altre operazioni successive al ripristino. Il ripristino dei backup incrementali, tuttavia, avviene in genere come sequenza di operazioni di ripristino, una per ogni backup incrementale. Il richiedente deve informare il writer che tale ripristino è in corso per impedire il ripristino o altre operazioni indesiderate fino al completamento del ripristino. Questa operazione viene eseguita chiamando [**IVssBackupComponents::SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores). Questo metodo viene chiamato per ogni componente e indica al writer che sono in arrivo altri ripristini per tale componente. Per il ripristino finale nella sequenza, il flag additional-restores deve essere impostato su false (valore predefinito), che indica che si tratta dell'ultimo ripristino nella sequenza per tale componente.

### <a name="new-targets"></a>Nuove destinazioni

Se supportato dal writer, il richiedente può ripristinare i file di dati in un percorso diverso da quello dell'ora di backup originale. Il richiedente può verificare questo supporto chiamando [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Il bit **VSS \_ BS \_ WRITER \_ SUPPORTS \_ NEW \_ TARGET** verrà impostato se il writer supporta questo comportamento. Il richiedente informa il writer del nuovo percorso chiamando [**IVssBackupComponents::AddNewTarget per**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) ogni specifica di file rilocato. Il richiedente può anche decidere di ripristinare un file di intervalli specifico in un percorso diverso. Il richiedente informa il writer di questa modifica chiamando [**IVssBackupComponents::SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

### <a name="directed-targets"></a>Destinazioni dirette

Per scenari di ripristino complessi, un writer potrebbe voler eseguire il mapping di intervalli di un file di cui è stato eseguito il backup in intervalli diversi dello stesso file o in un file diverso. Questa operazione può essere eseguita usando il meccanismo di destinazione diretto. Il richiedente può determinare dopo la fase [**IVssBackupComponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) che questo meccanismo viene usato per un componente chiamando [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) e controllando la restituzione di **VSS \_ RT \_ DIRECTED.** Il richiedente può ottenere tutti questi ripristini reindirizzati chiamando [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget). **IVssComponent::GetDirectedTarget** restituirà un percorso completo di un file di origine nel backup e un percorso completo di un file di destinazione in cui verrà ripristinato. Restituisce anche un elenco di intervalli per ognuno di questi file. Il richiedente è quindi responsabile del ripristino degli intervalli specificati nel file di origine negli intervalli mappati nel file di destinazione. Il formato della stringa degli intervalli è lo stesso di [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).

-   [Ruolo writer nei backup incrementali e differenziali vss](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Ruolo richiedente nei backup incrementali e differenziali vss](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
