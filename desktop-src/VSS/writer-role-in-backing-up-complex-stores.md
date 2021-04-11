---
description: Come per tutte le operazioni importanti in VSS, i backup incrementali e differenziali richiedono una stretta collaborazione tra i richiedenti e i writer.
ms.assetid: 3cf5dd1f-dc58-42bc-925f-fee7d34053c5
title: Ruolo di writer per il backup di archivi complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80864256b9a19c25a2f0dce0d0c929ed19fd7269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129267"
---
# <a name="writer-role-in-backing-up-complex-stores"></a>Ruolo di writer per il backup di archivi complessi

Come per tutte le operazioni importanti in VSS, i backup [*incrementali*](vssgloss-i.md) e [*differenziali*](vssgloss-d.md) richiedono una stretta collaborazione tra i richiedenti e i writer.

## <a name="backup-types"></a>Tipi di backup

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

I writer indicano il tipo di backup supportati chiamando [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) durante l'elaborazione dell'evento di [*Identificazione*](vssgloss-i.md) . Il parametro *dsSchemaMask* per il metodo **IVssCreateWriterMetadata:: SetBackupSchema** è una maschera di bit che indica i tipi di backup supportati. Tutti i writer devono supportare backup completi.

<dl> <dt>

<span id="VSS_BS_DIFFERENTIAL"></span><span id="vss_bs_differential"></span>**\_differenziale di VSS BS \_**
</dt> <dd>

Indica il supporto per i backup differenziali.

</dd> <dt>

<span id="VSS_BS_INCREMENTAL"></span><span id="vss_bs_incremental"></span>**\_ \_ incrementale BS VSS**
</dt> <dd>

Indica il supporto per i backup incrementali.

</dd> <dt>

<span id="VSS_BS_LOG"></span><span id="vss_bs_log"></span>**LOG di VSS \_ BS \_**
</dt> <dd>

Indica il supporto per i backup del log.

</dd> <dt>

<span id="VSS_BS_COPY"></span><span id="vss_bs_copy"></span>**copia di VSS \_ BS \_**
</dt> <dd>

Indica il supporto per i backup di copia.

</dd> <dt>

<span id="VSS_BS_EXCLUSIVE_INCREMENTAL_DIFFERENTIAL"></span><span id="vss_bs_exclusive_incremental_differential"></span>**\_ \_ \_ differenziale incrementale esclusivo VSS BS \_**
</dt> <dd>

Indica che un writer non supporta la combinazione di backup incrementali con backup differenziali.

</dd> </dl>

Il writer può determinare il tipo di backup da eseguire chiamando [**CVssWriter:: GetBackupType**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getbackuptype). Il primo punto in cui può essere eseguito è durante l'elaborazione dell'evento PrepareForBackup. **CVssWriter:: GetBackupType** restituirà un membro dell'enumerazione [**del \_ \_ tipo di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type) . Se il tipo di backup non è supportato dal writer, il writer deve trattare il backup come backup completo.

## <a name="backup-stamps"></a>Timbri di backup

I backup incrementali e differenziali sono sempre associati a un backup precedente. Esistono due modi per associare i backup. Per gli archivi dati semplici, il richiedente può tenere traccia della correlazione tra i backup. Tuttavia, per gli archivi dati più complessi, il writer dovrà mantenere il proprio timestamp con il backup; Questo timestamp può tenere traccia della posizione del log, delle informazioni sui checkpoint e così via. Un writer indica che sono necessari timestamp personalizzati impostando il bit del **\_ \_ timestamp** del servizio Copia Shadow del volume BS quando chiama [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema).

Un writer può archiviare un timestamp con ogni componente di cui viene eseguito il backup. Il writer archivia il timestamp chiamando [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)e passando una rappresentazione di stringa dell'indicatore per il parametro *wszBackupStamp* . In genere, un writer chiamerà questo metodo durante l'elaborazione dell'evento [*PostSnapshot*](vssgloss-p.md) . Tuttavia, per i backup che non coinvolgono una copia shadow, l'evento PostSnapshot non verrà inviato. In questo caso, è necessario chiamare **IVssComponent:: SetBackupStamp** durante l'elaborazione dell'evento [*PrepareForBackup*](vssgloss-p.md) .

Quando viene eseguito un backup incrementale o differenziale, il richiedente indicherà al writer l'indicatore di backup del backup precedente che funge da base per il backup. Il writer può accedere a questo indicatore di backup precedente durante l'elaborazione dell'evento PrepareForBackup o PostSnapshot, chiamando [**IVssComponent:: GetPreviousBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp). Il writer può utilizzare il timbro restituito per determinare gli elementi di cui deve essere eseguito il backup.

## <a name="backup-strategies"></a>Strategie di backup

### <a name="file-backup-files-strategies"></a>Strategie per i file di backup dei file

Spesso è necessario eseguire il backup di alcuni file segnalati nei metadati del writer solo quando si eseguono determinati tipi di backup. È possibile che alcuni file siano necessari solo quando si esegue un backup completo. Per eseguire un backup incrementale o differenziale è possibile che siano necessari altri file. VSS fornisce un metodo affinché i writer indichino queste informazioni al richiedente. Quando si aggiungono file ai componenti usando [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), il parametro *dwBackupTypeMask* indica per quali tipi di backup è necessario eseguire il backup di questi file. La maschera può contenere uno o più dei valori seguenti:

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

Un metodo per un writer per indicare quali file sono stati modificati consiste nell'usare il meccanismo di file differenziato. Un writer può specificare che è necessario eseguire il backup di determinati file di un componente solo se sono stati modificati da un determinato periodo di tempo. Il writer chiama [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) con una specifica del file e l'ora dell'Ultima modifica. **IVssComponent:: AddDifferencedFilesByLastModifyTime** viene in genere chiamato durante l'elaborazione dell'evento PostSnapshot, sebbene possa essere chiamato durante l'elaborazione dell'evento PrepareForBackup. Il richiedente deve quindi eseguire il backup di tutti i file che corrispondono alla specifica del file che sono stati modificati dall'ora specificata. Se il writer utilizza il meccanismo del timbro di backup, l'ora dell'Ultima modifica verrà determinata in base all'indicatore di backup precedente nel documento di backup. Il writer può anche passare zero per l'ora dell'Ultima modifica, che indica che il richiedente è responsabile della determinazione dell'ora dell'ultimo backup e dei file modificati da quel momento.

### <a name="partial-file-backup"></a>Backup parziale dei file

Un altro modo affinché un writer indichi modifiche al richiedente consiste nell'usare il meccanismo di file parziale. Un writer può specificare intervalli di byte nei file di componente di cui è necessario eseguire il backup; il writer può specificare questi intervalli di file durante l'elaborazione dell'evento PostSnapshot o PrepareForBackup. Il writer chiama [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) per aggiungere specifiche di file parziali al backup. Una specifica del file parziale è costituita da un percorso e un nome file con informazioni sugli intervalli nel file di cui è necessario eseguire il backup.

### <a name="file-specification-rules"></a>Regole specifiche file

È possibile usare [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) o [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) per modificare le specifiche del file specificate durante l'evento di identificazione o per aggiungere file completamente nuovi alla specifica. Se il writer sta modificando il set di informazioni durante l'evento di identificazione usando **IVssComponent:: AddDifferencedFilesByLastModifyTime**, la specifica del file deve corrispondere esattamente a una delle specifiche del file nel componente corrente. La specifica del file non deve sovrapporsi parzialmente ai file nel componente corrente e non deve corrispondere ai file in altri componenti. I file specificati con **IVssComponent:: AddPartialFile** possono, tuttavia, sovrapporsi parzialmente a un'altra specifica di file. Le informazioni impostate da **IVssComponent:: AddDifferencedFilesByLastModifyTime** o **IVssComponent:: AddPartialFile** eseguono l'override delle informazioni impostate in precedenza tramite l'interfaccia [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) in risposta all'evento di identificazione.

Le specifiche di file generali possono avere un valore di percorso alternativo (impostato dal parametro *wszAlternateLocation* di [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) che indica un percorso alternativo da cui ottenere il file in fase di backup. Se la specifica del file impostata tramite i meccanismi del file differenziato o del file parziale corrisponde a una specifica del file esistente con un percorso alternativo, l'applicazione di backup otterrà i dati da questo percorso alternativo.

Se il set di specifiche di file in [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) o [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile) non corrisponde a e ai file nel componente di cui viene eseguito il backup, tutti i file corrispondenti verranno aggiunti al backup. È necessario prestare attenzione che il writer aggiunga solo i file presenti in un volume di cui è già stata eseguita la copia shadow. in caso contrario, il richiedente potrebbe non riuscire a eseguire il backup di questi file. Se queste funzioni vengono chiamate durante l'elaborazione dell'evento PostSnapshot, questo può essere determinato tramite il metodo [**CVssWriter:: IsPathAffected**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispathaffected) . Se chiamato durante la gestione dell'evento PrepareForBackup, il writer deve effettuare questa determinazione usando un altro metodo.

### <a name="backup-without-a-shadow-copy"></a>Backup senza copia shadow

Potrebbe non essere necessario eseguire il backup di alcuni tipi di file da un volume di copia shadow. Questo, ad esempio, sarà spesso vero per i file di log del database. Poiché i file di log aumentano in modo progressivo e un writer può specificare esattamente le parti del file di cui eseguire il backup usando file parziali, è spesso possibile eseguire il backup della disconnessione dal volume originale. Come ottimizzazione, un writer può contrassegnare i file che richiedono copie shadow per diversi tipi di backup usando i flag impostati nel parametro *dwBackupTypeMask* di [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup). I flag supportati sono i seguenti:

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

## <a name="backup-cleanup"></a>Pulitura backup

Se il writer deve eseguire un troncamento del log o un'altra pulitura successiva al backup, il posto appropriato è durante l'elaborazione dell'evento [*BackupComplete*](vssgloss-b.md) . L'evento [*BackupShutdown*](vssgloss-b.md) verrà inviato un po' di tempo dopo BackupComplete, quindi alcune operazioni di pulizia possono essere eseguite anche nel gestore dell'evento BackupShutdown.

L'evento BackupShutdown viene sempre inviato dopo la terminazione di un backup. Se il richiedente termina in modo anomalo durante l'esecuzione di un backup, BackupShutdown verrà inviato immediatamente, senza prima inviare BackupComplete. Se il writer deve eseguire la pulizia di qualsiasi stato, è possibile eseguire questa operazione. il troncamento del log non dovrebbe tuttavia verificarsi in questo evento perché il backup non è stato necessariamente completato.

## <a name="restore-strategies"></a>Strategie di ripristino

Le attività di base dei writer in fase di ripristino sono la verifica che il ripristino possa verificarsi durante la gestione dell'evento di preripristino e che il ripristino si sia verificato durante la gestione dell'evento PostRestore. Gli archivi più complessi eseguiranno anche un processo di ripristino nel gestore PostRestore. Se il ripristino fa parte di un ripristino incrementale o differenziale, il writer desidera in genere ritardare il processo di ripristino fino a quando non vengono completati tutti i ripristini incrementali o differenziali. [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores) indicherà se si tratta del ripristino finale di questo componente o se sono presenti più ripristini da passare. Se **IVssComponent:: GetAdditionalRestores** restituisce **true**, il writer non deve eseguire la relativa procedura di recupero su tale componente.

## <a name="new-targets"></a>Nuove destinazioni

Se supportato dal writer, il richiedente può ripristinare i file di dati in un percorso diverso da quello originale in fase di backup. Un writer indica il supporto per questa modalità di ripristino impostando il writer del servizio Copia Shadow del volume, supporta il nuovo bit di **\_ \_ \_ \_ \_ destinazione** nel parametro *DsSchemaMask* durante la chiamata a [**IVssCreateWriterMetadata:: SetBackupSchema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema). Un writer ottiene i nuovi percorsi per i file dei componenti in fase di ripristino chiamando [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget).

## <a name="directed-targets"></a>Destinazioni dirette

Per gli scenari di ripristino complessi, un writer potrebbe voler eseguire il mapping degli intervalli di un file di cui è stato eseguito il backup in intervalli diversi dello stesso file o di un file diverso. A tale scopo, è possibile usare il meccanismo di destinazione diretto. A tale scopo, un writer deve prima indicare che questa situazione si verifica chiamando [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget), passando in **VSS \_ RT \_ indirizzato** per il parametro di *destinazione* . Quindi, per ogni mapping, il writer chiama [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget). Questo metodo accetta il percorso completo di un file di origine nel backup e il percorso completo di un file di destinazione in cui verrà ripristinato. Accetta inoltre un elenco di intervalli per ognuno di questi file. Il writer chiama queste funzioni durante la gestione dell'evento di preripristino e il richiedente è quindi responsabile del ripristino degli intervalli specificati nel file di origine agli intervalli mappati nel file di destinazione. Il formato della stringa degli intervalli è identico a quello di [ **IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)

## <a name="private-writer-metadata"></a>Metadati del writer privato

Spesso è utile per un writer mantenere i metadati privati con un backup per eseguire correttamente un ripristino incrementale o differenziale. Un writer può chiamare [**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata) durante la gestione di PrepareForBackup o PostSnapshot per archiviare i metadati. È possibile accedere a questi metadati dal writer durante il preripristino o dopo il ripristino chiamando [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata). I metadati possono anche essere archiviati con una specifica del file parziale usando il parametro *wszMetadata* di [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile); è possibile accedere a questi metadati tramite il parametro *pbstrMetadata* di [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Il writer può anche passare i metadati a se stesso tra [**CVssWriter:: OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore) e [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). In **CVssWriter:: OnPreRestore** i metadati vengono impostati chiamando [**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata). In **CVssWriter:: OnPostRestore** i metadati vengono recuperati chiamando [**IVssComponent:: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata).

-   [Ruolo writer nei backup incrementali e differenziali VSS](writer-role-in-vss-incremental-and-differential-backups.md)
-   [Ruolo del richiedente nei backup incrementali e differenziali VSS](requestor-role-in-vss-incremental-and-differential-backups.md)

 

 



