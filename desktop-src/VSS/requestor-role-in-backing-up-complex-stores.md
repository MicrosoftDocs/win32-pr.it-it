---
description: Come per tutte le operazioni importanti in VSS, i backup incrementali e differenziali richiedono una stretta collaborazione tra i richiedenti e i writer.
ms.assetid: 00391a49-8c81-4518-88a2-741ad5ee4ac3
title: Ruolo del richiedente nel backup di archivi complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 197351e76b6861ee9b9d1e0589ef028c911430ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049846"
---
# <a name="requester-role-in-backing-up-complex-stores"></a>Ruolo del richiedente nel backup di archivi complessi

Come per tutte le operazioni importanti in VSS, i backup [*incrementali*](vssgloss-i.md) e [*differenziali*](vssgloss-d.md) richiedono una stretta collaborazione tra i richiedenti e i writer.

## <a name="backup-type"></a>Tipo di backup

L'infrastruttura fornisce supporto speciale per cinque tipi di backup. Sono descritte come segue:

-   Completo (**VSS \_ BT \_ completo**). Verrà eseguito il backup dei file indipendentemente dalla data dell'ultimo backup. La cronologia di backup di ogni file verrà aggiornata e questo tipo di backup può essere utilizzato come base per un backup incrementale o differenziale. Se sono presenti file di log, è possibile che vengano troncati in seguito a questo backup.

    Il ripristino di un backup completo richiede una sola immagine di backup.

-   Differenziale (**VSS \_ BT \_ differenziale**). L'API VSS viene utilizzata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo vengano copiati in un supporto di archiviazione. tutte le informazioni sul backup intermedio verranno ignorate. Questo può includere interi file o intervalli specifici all'interno dei file. Un backup differenziale è associato a un backup completo e in genere non può essere ripristinato fino a quando non viene ripristinato il backup completo. Se sono presenti file di log, in genere non verranno troncati in seguito a questo backup.

    Il ripristino di un backup differenziale richiede l'immagine di backup originale e l'immagine di backup differenziale più recente eseguita dopo l'ultimo backup completo.

-   Incrementale (**VSS \_ BT \_ incrementale**). L'API VSS viene utilizzata per garantire che solo i file che sono stati modificati o aggiunti dopo l'ultimo backup completo o incrementale vengano copiati in un supporto di archiviazione. Questo può includere interi file o intervalli specifici all'interno dei file. Alcuni writer non consentono di combinare backup incrementali con backup differenziali. Se sono presenti file di log, è possibile che vengano troncati in seguito a questo backup.

    Il ripristino di un backup incrementale richiede l'immagine di backup originale e tutte le immagini di backup incrementali effettuate dal backup iniziale.

-   Backup del log **( \_ \_ log di VSS BT**). Verrà eseguito il backup solo dei file di log del writer, ovvero i file aggiunti a un componente con il metodo [**IVssCreateWriterMetadata:: AddDataBaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) e recuperato da una chiamata a [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile). Questo tipo di backup è specifico per VSS. I backup del log tendono a essere eseguiti con molta frequenza. In genere, il file di log verrà troncato in seguito a questo backup.
-   Backup di copia **( \_ \_ copia di VSS BT**). Analogamente al \_ \_ tipo di backup completo VSS BT, verrà eseguito il backup dei file indipendentemente dalla data dell'ultimo backup. Tuttavia, la cronologia di backup di ogni file non verrà aggiornata e questo tipo di backup non può essere utilizzato come base per un backup incrementale o differenziale. I file di log non devono mai essere troncati come risultato di un backup di copia.

<dl> <dt>

<span id="Partial_File_Support"></span><span id="partial_file_support"></span><span id="PARTIAL_FILE_SUPPORT"></span>Supporto file parziale
</dt> <dd>

Alcuni writer supportano il ripristino dei file tramite la sovrascrittura delle parti dei file gestiti. Un richiedente può essere progettato per trarre vantaggio da questo e, in caso affermativo, impostando le informazioni in [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate).

</dd> </dl>

Il richiedente specifica il tipo di backup eseguito tramite il parametro *BackupType* di [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate). Writer diversi supporteranno tipi diversi di backup. Dopo la chiamata di [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) , il richiedente può determinare i tipi di backup supportati da un determinato writer chiamando [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Il valore restituito è una maschera di bit che indica il supporto per diversi tipi di backup. Servizio Copia **shadow \_ del volume Il \_ differenziale BS** indica il supporto per i backup differenziali, il servizio Copia Shadow del volume **\_ \_ incrementale** per i backup incrementali, il **\_ \_ log VSS BS** per i backup del log e la **\_ \_ copia VSS BS** per i backup di copia. tutti i writer devono supportare backup completi. Se un writer non supporta la combinazione di backup incrementali con backup differenziali, verrà aggiunto anche il flag di **\_ \_ \_ \_ differenziale incrementale esclusivo VSS BS** . Se il richiedente esegue un backup incrementale o differenziale e un determinato writer non supporta tale tipo di backup, è necessario eseguire un backup completo su tale writer.

## <a name="backup-stamps"></a>Timbri di backup

I backup incrementali e differenziali sono sempre associati a un backup precedente. Esistono due modi per associare i backup. Per gli archivi dati semplici, il richiedente può tenere traccia della correlazione tra i backup. Tuttavia, per gli archivi dati più complessi, il writer dovrà mantenere il proprio timestamp con il backup; Questo timestamp può tenere traccia della posizione del log, delle informazioni sui checkpoint e così via. Il richiedente può determinare se un determinato writer deve archiviare il proprio timestamp controllando il bit del **\_ \_ timestamp di VSS BS** nel valore restituito da [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

I writer in cui viene archiviato un timestamp in un backup aggiungeranno il timestamp durante l'elaborazione di [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o durante l'elaborazione di [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Il richiedente può ottenere questo timestamp chiamando [**IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp). Quando si esegue un backup incrementale o differenziale, il richiedente deve associare il backup corrente a un backup precedente. Questa operazione viene eseguita ottenendo il timestamp dal backup precedente di un componente specifico e passandolo alla funzione [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) ; Questa operazione deve essere eseguita per ogni componente di cui è stato eseguito il backup nel backup precedente.

## <a name="backing-up-files"></a>Backup di file

### <a name="backing-up-files-reported-by-writer"></a>Backup dei file segnalati dal writer

Ogni specifica di file aggiunta da un writer ai relativi metadati durante la fase GatherWriterMetadata contiene una maschera del tipo di backup che specifica quando eseguire il backup del file. Il richiedente determina l'elemento della maschera chiamando [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask). I valori in questa maschera vengono utilizzati per determinare per quali tipi di backup deve essere eseguito il backup della specifica del file. La maschera può contenere uno o più dei seguenti valori di bit:

<dl> <dt>

<span id="VSS_FSBT_FULL_BACKUP_REQUIRED"></span><span id="vss_fsbt_full_backup_required"></span>**\_ \_ backup completo VSS \_ FSBT \_ obbligatorio**
</dt> <dd>

Obbligatorio per i backup completi.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_differential_backup_required"></span>**è \_ \_ necessario il \_ backup DIFFERENZIAle FSBT VSS \_**
</dt> <dd>

Obbligatorio per i backup differenziali.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_BACKUP_REQUIRED"></span><span id="vss_fsbt_incremental_backup_required"></span>**è \_ \_ necessario il backup incrementale FSBT VSS \_ \_**
</dt> <dd>

Obbligatorio per i backup incrementali.

</dd> <dt>

<span id="VSS_FSBT_LOG_BACKUP_REQUIRED"></span><span id="vss_fsbt_log_backup_required"></span>**\_backup del \_ log FSBT VSS \_ \_ obbligatorio**
</dt> <dd>

Obbligatorio per i backup del log.

</dd> <dt>

<span id="VSS_FSBT_ALL_BACKUP_REQUIRED"></span><span id="vss_fsbt_all_backup_required"></span>**VSS \_ FSBT \_ tutti i \_ backup \_ necessari**
</dt> <dd>

Obbligatorio per tutti i tipi di backup; si tratta dell'impostazione predefinita.

</dd> </dl>

Questa specifica esegue l'override della specifica di selettività del componente. Si consideri, ad esempio, un componente i cui file sono tutti contrassegnati con il **\_ backup del log VSS FSBT \_ \_ \_ richiesto** , ma non con il **\_ \_ backup completo VSS FSBT \_ \_ obbligatorio**. Si supponga che il componente non sia selezionabile per il backup (*bSelectable* è false quando [**IVssCreateWriterMetadata:: AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent) è stato chiamato). Nel caso di un backup del log, significa che è necessario eseguire sempre il backup di tutti i file di questo componente. Tuttavia, nel caso di un backup completo, non è necessario eseguire il backup di nessuno dei file, nonostante il fatto che la selettività del componente ne implichi il backup.

### <a name="backup-by-last-modify-time"></a>Ora dell'Ultima modifica del backup

Le informazioni sulle specifiche del file specificate nella fase [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) non forniscono informazioni sul richiedente relative a quanto è stato modificato dall'ultimo backup. Un metodo per un writer per indicare le modifiche al richiedente consiste nell'usare il meccanismo di file differenziato. Un writer può specificare che è necessario eseguire il backup di determinati file di un componente solo se sono stati modificati da un determinato periodo di tempo; il writer può specificare questi file in [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un richiedente può determinare questi file chiamando [**IVssComponent:: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Se la specifica del file corrisponde a un set in **IVssBackupComponents:: GatherWriterMetadata** (attualmente valido in base al tipo di backup mask), le informazioni sul file differenziato eseguono l'override delle informazioni precedenti. in altre termini, viene eseguito il backup dei file corrispondenti alla specifica del file solo se sono stati modificati dopo l'ora specificata. L'ora dell'Ultima modifica viene comunicata utilizzando una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Se il valore di questa struttura è pari a zero, significa che è necessario determinare l'ora dell'Ultima modifica in base al record del richiedente dell'ora dell'ultimo backup.

### <a name="partial-file-backup"></a>Backup parziale dei file

Un altro modo affinché un writer indichi modifiche al richiedente consiste nell'usare il meccanismo di file parziale. Un writer può specificare intervalli di byte nei file di componente di cui è necessario eseguire il backup; il writer può specificare questi intervalli di file in [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o in [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Un richiedente può determinare questi file chiamando [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). **IVssComponent:: GetPartialFile** restituirà un percorso e un nome di file che punta al file e una stringa di intervalli che indica gli elementi di cui è necessario eseguire il backup nel file. Come per i file differenziati, se il percorso e il nome del file corrispondono a una specifica del file impostata dal writer in [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), le informazioni sul file parziale eseguono l'override dell'impostazione precedente. La stringa degli intervalli può avere due formati: può specificare direttamente gli intervalli o specificare un file contenente le informazioni sugli intervalli. Se si specificano gli intervalli direttamente, la sintassi è un elenco delimitato da virgole nel formato offset1: length1, offset2: length2, dove ogni offset e lunghezza è un Unsigned Integer a 64 bit. Se si specifica un file degli intervalli, la stringa degli intervalli deve essere impostata su file = *filename*, dove *filename* è il percorso completo del file degli intervalli. Il file degli intervalli è un file binario formattato come un elenco di interi senza segno a 64 bit. Il primo valore integer indica il numero di intervalli rappresentati nel file. Ogni coppia di numeri interi successiva rappresenta l'offset e la lunghezza di un intervallo. Il richiedente deve prestare attenzione al backup e al ripristino del file degli intervalli.

### <a name="file-specification-rules"></a>Regole specifiche file

Le specifiche dei file aggiunte tramite il file differenziato e i meccanismi di file parziale modificheranno le specifiche del file impostate in [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) o aggiungono file completamente nuovi. Se si modificano le specifiche dei file impostate in **IVssBackupComponents:: GatherWriterMetadata** usando il meccanismo di file parziale, un richiedente può prevedere che la specifica del file corrisponda esattamente a una delle specifiche del file impostate nel componente in **IVssBackupComponents:: GatherWriterMetadata**. La specifica del file non si sovrappone parzialmente a un'altra specifica di file e non corrisponderà ad alcuna specifica di file in alcun altro componente di tale writer. Le specifiche dei file aggiunte utilizzando il meccanismo di file parziale possono, tuttavia, sovrapporsi parzialmente a un'altra specifica di file. Quando è true, la specifica del file differenziato o del file parziale sostituisce il set di specifiche in **IVssBackupComponents:: GatherWriterMetadata**. Le specifiche di file generali possono avere un valore di percorso alternativo (restituito da [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation)) che indica una posizione alternativa da cui ottenere il file in fase di backup. Se le specifiche del file impostate tramite i meccanismi di file differenziati o parziali corrispondono a una specifica di file esistente con un percorso alternativo, i dati devono essere prelevati da questo percorso alternativo. Se le specifiche del file impostate tramite i meccanismi di file differenziato o di file parziale non corrispondono ad alcuna specifica esistente per il componente, è ora necessario aggiungere questi intervalli di file al backup. Il richiedente può prevedere che solo i file nei volumi che sono già stati inclusi nel set di copie shadow verranno aggiunti usando uno di questi meccanismi.

### <a name="backup-without-a-shadow-copy"></a>Backup senza copia shadow

Potrebbe non essere necessario eseguire il backup di alcuni tipi di file da un volume di copia shadow. Questo, ad esempio, sarà spesso vero per i file di log del database. Poiché i file di log aumentano in modo progressivo e un writer può specificare esattamente le parti del file di cui eseguire il backup usando file parziali, è spesso possibile eseguire il backup della disconnessione dal volume originale. Come ottimizzazione, un writer può contrassegnare i file che richiedono copie shadow per diversi tipi di backup usando la maschera del tipo di backup. Il valore restituito da [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) può contenere uno o più dei seguenti valori di bit:

<dl> <dt>

<span id="VSS_FSBT_FULL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_full_snapshot_required"></span>**\_ \_ snapshot completo VSS \_ FSBT \_ necessario**
</dt> <dd>

Copia shadow necessaria per i backup completi.

</dd> <dt>

<span id="VSS_FSBT_DIFFERENTIAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_differential_snapshot_required"></span>**\_ \_ snapshot differenziale FSBT VSS \_ \_ obbligatorio**
</dt> <dd>

Copia shadow necessaria per i backup differenziali.

</dd> <dt>

<span id="VSS_FSBT_INCREMENTAL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_incremental_snapshot_required"></span>**\_ \_ snapshot incrementale FSBT \_ VSS \_ obbligatorio**
</dt> <dd>

Copia shadow necessaria per i backup incrementali.

</dd> <dt>

<span id="VSS_FSBT_LOG_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_log_snapshot_required"></span>**\_snapshot del \_ log FSBT VSS \_ \_ obbligatorio**
</dt> <dd>

Copia shadow necessaria per i backup del log.

</dd> <dt>

<span id="VSS_FSBT_ALL_SNAPSHOT_REQUIRED"></span><span id="vss_fsbt_all_snapshot_required"></span>**VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari**
</dt> <dd>

Copia shadow necessaria per tutti i tipi di backup; si tratta dell'impostazione predefinita.

</dd> </dl>

Se un volume specifico contiene solo componenti che non richiedono una copia shadow per questo backup, il richiedente può ignorare il passaggio della creazione di una copia shadow per questo volume. Tutti i dati di questo volume possono essere copiati nel supporto di backup direttamente dal volume originale.

## <a name="restoring-files"></a>Ripristino di file

### <a name="sequential-restores"></a>Ripristini sequenziali

Al termine dell'esecuzione di un'operazione di ripristino, il richiedente invia l'evento PostRestore a tutti i writer. In genere, i writer gestiscono questo evento eseguendo il ripristino o altre operazioni di post-ripristino. Il ripristino dei backup incrementali, tuttavia, si verifica in genere come una sequenza di operazioni di ripristino, una per ogni backup incrementale. Il richiedente deve informare il writer che tale ripristino è in corso per impedire che il ripristino o altre operazioni indesiderate vengano eseguite fino al completamento del ripristino. Questa operazione viene eseguita chiamando [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores). Questo metodo viene chiamato per componente e indica al writer che sono in arrivo più ripristini per quel componente. Per il ripristino finale nella sequenza, il flag di ripristini aggiuntivi deve essere impostato su false (valore predefinito), che indica che si tratta dell'ultimo ripristino nella sequenza per quel componente.

### <a name="new-targets"></a>Nuove destinazioni

Se supportato dal writer, il richiedente può ripristinare i file di dati in un percorso diverso da quello originale in fase di backup. Il richiedente può verificare la presenza di questo supporto chiamando [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Il **\_ writer BS \_ VSS \_ supporta \_ \_** la creazione di un nuovo bit di destinazione se il writer supporta questo comportamento. Il richiedente informa il writer del nuovo percorso chiamando [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget) per ogni specifica di file rilocata. Il richiedente può inoltre decidere di ripristinare un file di intervalli specifico in un percorso diverso. Il richiedente informa il writer di questa modifica chiamando [**IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

### <a name="directed-targets"></a>Destinazioni dirette

Per gli scenari di ripristino complessi, un writer potrebbe voler eseguire il mapping degli intervalli di un file di cui è stato eseguito il backup in intervalli diversi dello stesso file o di un file diverso. Questa operazione può essere eseguita usando il meccanismo di destinazione diretto. Il richiedente può determinare dopo la fase [**IVssBackupComponents::P Rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) che questo meccanismo viene usato per un componente chiamando [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) e controllando la presenza di un ritorno di **VSS \_ RT \_ diretto**. È possibile che il richiedente ottenga tutti i ripristini reindirizzati chiamando [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget). **IVssComponent:: GetDirectedTarget** restituirà il percorso completo di un file di origine nel backup e il percorso completo di un file di destinazione in cui verrà ripristinato. Restituisce anche un elenco di intervalli per ognuno di questi file. Il richiedente è quindi responsabile del ripristino degli intervalli specificati nel file di origine agli intervalli mappati nel file di destinazione. Il formato della stringa degli intervalli è identico a quello di [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile).

-   [Ruolo writer nei backup incrementali e differenziali VSS](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Ruolo del richiedente nei backup incrementali e differenziali VSS](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 
