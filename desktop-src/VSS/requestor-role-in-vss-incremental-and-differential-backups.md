---
description: "Per supportare un'operazione di backup incrementale o differenziale, un richiedente deve eseguire le operazioni seguenti:"
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: Ruolo del richiedente nei backup incrementali e differenziali VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 718a5a0b22d9cc1cfa31404b3a0ac71a3a07731f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310676"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>Ruolo del richiedente nei backup incrementali e differenziali VSS

Per supportare un'operazione di backup [*incrementale*](vssgloss-i.md) o [*differenziale*](vssgloss-d.md) , un richiedente deve eseguire le operazioni seguenti:

1.  Determinare il grado di supporto del writer disponibile (usando [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) per ottenere l'accesso alle informazioni nei documenti di metadati del writer), in particolare determinare quale schema di backup è supportato ([**\_ \_ schema di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)).
2.  Imposta uno stato di backup appropriato.
3.  Ottenere le specifiche a livello di file e di set di file per un backup incrementale o differenziale.
4.  Eseguire il backup.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Determinazione del richiedente di supporto e configurazione incrementale e differenziale

Un richiedente deve ottenere informazioni sul supporto del writer prima di selezionare i componenti da includere in un backup incrementale o differenziale o di impostare il proprio stato.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Determinazione del supporto del writer
</dt> <dd>

Un richiedente determina se un determinato writer supporta i backup incrementali o differenziali VSS recuperando la maschera dello schema di backup del writer usando il metodo [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema) .

La maschera dello schema di backup di un writer che supporta le tecniche incrementali o differenziali VSS conterrà i **valori \_ \_ differenziali** **VSS BS \_ \_ incrementale** o VSS BS o entrambi. I writer possono inoltre indicare restrizioni sulla loro partecipazione al flag di **\_ \_ \_ \_ differenziale incrementale esclusivo VSS BS** . Per ulteriori informazioni sugli schemi di backup, vedere lo [**\_ \_ schema di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) .

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Impostazione dello stato di backup del richiedente
</dt> <dd>

Un richiedente indica che un backup è un backup incrementale o differenziale impostando un tipo di backup **su \_ VSS \_ BT incrementale** o su **VSS \_ BT \_ differenziale** usando il metodo [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) prima di generare un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) .

Il metodo [**IVssBackupComponents:: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) viene usato anche per indicare se il richiedente fornisce il supporto per i [*file parziali*](vssgloss-p.md), usato di frequente per implementare determinate operazioni di backup e ripristino incrementali.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Recupero delle specifiche del writer per i backup incrementali e differenziali

Le informazioni sulle specifiche del backup dei file a livello di set di file ([**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) contenute nel documento di metadati del writer di ogni writer sono disponibili per l'esame dopo la restituzione corretta di [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Tuttavia, un writer può aggiungere [*file differenziati*](vssgloss-d.md) o richiedere il [*supporto di file parziali*](vssgloss-p.md) fino alla corretta gestione dell'evento [*PostSnapshot*](vssgloss-p.md) .

La specifica del supporto file differenziato e file parziale può eseguire l'override del tipo di backup delle specifiche file, quindi i richiedenti possono rinviare un'analisi completa di tutte le specifiche del writer sui backup incrementali e differenziali fino a quando non viene restituito il risultato corretto di [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Recupero delle informazioni sulle specifiche del backup di file
</dt> <dd>

Le informazioni sulle specifiche del backup dei file a livello di set di file ([**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) sono contenute nel documento di metadati del writer di ogni writer e possono essere esaminate immediatamente dopo la restituzione corretta di [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

I richiedenti devono ottenere le maschere delle specifiche del backup dei file ([**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) per ogni set di file di ogni componente di un writer da includere nel backup incrementale o differenziale, indipendentemente dal fatto che il componente sia incluso in [*modo esplicito*](vssgloss-e.md) o [*implicito*](vssgloss-i.md) .

Un richiedente può determinare quale documento di metadati del writer di writer deve eseguire una query usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). L'istanza dell'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituita da **IVssBackupComponents:: GetWriterComponents** fornisce informazioni sul writer tramite il metodo [**IVssWriterComponentsExt:: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo) .

Il richiedente ottiene informazioni sul componente tramite istanze dell'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) che corrispondono a un componente incluso gestito da un writer specificato tramite [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

Le informazioni sui set di file gestiti dal componente corrispondente all'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) vengono ottenute dalle chiamate a [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)o [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (a seconda dei casi).

Queste chiamate possono restituire istanze dell'interfaccia [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) per ognuno dei set di file di un componente.

Il tipo di backup delle specifiche file di un set di file viene ottenuto chiamando [**IVssWMFiledesc:: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask).

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Recupero delle informazioni sul file parziale e sul file differenziato
</dt> <dd>

Un richiedente ottiene le informazioni sul file parziale e sul file differenziato tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Un richiedente può scorrere tutti i writer inclusi in un backup usando [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L'istanza di un'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituita da [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) fornisce l'accesso a tutte le istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) che corrispondono ai componenti [*inclusi in modo esplicito*](vssgloss-e.md) di un writer specificato tramite i metodi [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) e [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) .

Un richiedente deve esaminare tutte le istanze di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per tutti i writer il cui schema supporta il backup incrementale o differenziale, ovvero i writer la cui maschera di backup schema, restituita da [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), include il servizio **VSS \_ BS \_ incrementale** quando il tipo di backup è il backup **\_ \_ incrementale** di VSS, oppure il valore **\_ \_ differenziale BS BS** quando il tipo di backup è un backup **\_ \_ differenzia**

Le informazioni parziali sul file vengono ottenute chiamando [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (vedere [uso di file parziali](working-with-partial-files.md)).

Per i writer che supportano le operazioni di backup in base ai dati dell'Ultima modifica di un file (i writer la cui maschera di backup schema, come restituito da [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), includono **\_ \_ l'ultima \_ modifica di VSS BS**), le informazioni sul file differenziato vengono ottenute chiamando [**IVssComponent:: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile).

Si noti che i file differenziati possono essere nuovi file, ovvero file che non sono membri di alcun set di file attualmente nel documento di metadati del writer di un determinato writer.

I richiedenti non devono trovare i file inclusi sia per le operazioni parziali dei file che come file differenziati. Se un richiedente incontra tale circostanza, deve restituire e registrare un errore del writer.

Un richiedente può comunque scegliere di continuare a eseguire il backup dei file del writer problematico, ma in tal caso deve eseguire questa operazione in base alla specifica rilevata nelle informazioni sul file differenziato.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Implementazione di backup incrementali o differenziali

Prima di implementare un backup, i richiedenti devono avere informazioni sui writer che supportano un backup [*incrementale*](vssgloss-i.md) o [*differenziale*](vssgloss-d.md) , tutte le operazioni di file parziali richieste, tutti i file differenziati e il tipo di backup delle specifiche file di tutti gli altri file.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Writer non supportati
</dt> <dd>

Writer il cui schema non supporta il backup incrementale o differenziale (i writer la cui maschera di backup schema, come restituito da [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), includono il servizio **VSS \_ BS \_ incrementale** quando il tipo di backup è di tipo **VSS \_ BT \_** incrementale o non include il backup **\_ \_ differenziale di VSS BS** quando il tipo di backup è un backup **\_ \_ differenziale** del servizio Copia Shadow del volume)

Ciò non significa necessariamente che i dati dei writer non saranno interessati da un'operazione di backup incrementale o differenziale. Tuttavia, la scelta delle operazioni da eseguire è a discrezione del richiedente. Il richiedente può eseguire una delle operazioni seguenti:

-   Esegui il backup dei file appartenenti ai writer non supportati (indica chiaramente questo problema all'utente)
-   Eseguire il backup di tutti i file di writer non supportati
-   Eseguire un backup incrementale usando i dati file system e i log della cronologia del richiedente.

L'ultima alternativa deve essere utilizzata con grande attenzione e solo se il richiedente riconosce se i writer interessati possono supportare il backup incrementale o differenziale e il ripristino dei dati indipendentemente dal meccanismo VSS.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Writer di supporto
</dt> <dd>

Un richiedente deve elaborare (in ordine) tutti i [*file differenziati*](vssgloss-d.md)di un writer, quindi gestire eventuali richieste di [*file parziali*](vssgloss-p.md) e quindi eseguire il backup dei file rimanenti in base al tipo di backup delle specifiche file (tipo di backup delle [**specifiche del \_ file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

1.  **Backup di file differenziati:**

    Per i writer che supportano le operazioni di backup sulla base dei dati dell'Ultima modifica (i writer la cui maschera di backup schema, come restituito da [**IVssExamineWriterMetadata:: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), includono l' **\_ \_ Ultima \_ modifica di VSS BS**), un richiedente usa il percorso, la specifica del file e le informazioni sui flag di ricorsione restituiti da [**IVssComponent:**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)

    [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) può inoltre restituire un'ora dell'Ultima modifica (espressa come struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) ).

    Se l'ora dell'Ultima modifica fornita dal writer è diversa da zero, il richiedente lo utilizzerà come base (anziché file system informazioni o i dati archiviati del richiedente) per determinare se il file deve essere incluso nel backup [*incrementale*](vssgloss-i.md) o [*differenziale*](vssgloss-d.md) .

    Ad esempio, se l'ora dell'Ultima modifica di un file restituita dal writer è:

    -   Dopo l'ultimo backup completo, il file deve essere incluso nei backup incrementali e differenziali.
    -   Dopo l'ultimo backup completo, ma prima dell'ultimo backup incrementale, il file deve essere incluso nelle operazioni di backup incrementale, ma non nei backup differenziali.

    Se l'ora dell'Ultima modifica fornita dal writer è zero, il richiedente deve utilizzare file system informazioni e i relativi dati archiviati per determinare l'ora di modifica del file differenziato.

2.  **Utilizzo di operazioni di file parziali:**

    Se un writer ha richiesto il backup di un file usando un'operazione di file parziale, il richiedente usa le informazioni di offset del file per salvare i segmenti di file indicati nei supporti di backup. Per ulteriori informazioni sulle operazioni di file parziali, vedere [utilizzo dei file parziali](working-with-partial-files.md) .

    Come indicato in precedenza, un writer non deve designare un file come un file differenziato e come partecipante a un'operazione di file parziale. Se un richiedente incontra tale circostanza, deve restituire e registrare un errore del writer.

    Un richiedente può comunque scegliere di continuare a eseguire il backup dei file del writer problematico, ma in tal caso deve eseguire questa operazione in base alla specifica rilevata nelle informazioni sul file differenziato.

3.  **Utilizzo del tipo di backup delle specifiche file:**

    Dopo aver elaborato tutti i file differenziati e le operazioni parziali sui file, il richiedente elabora tutti i file rimanenti nel set di backup in base al tipo di backup delle specifiche file ([**tipo di backup delle \_ specifiche del file \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Sono disponibili tre valori "backup obbligatorio" dell'enumerazione [**del \_ \_ tipo di \_ backup \_ delle specifiche del file VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che interessano i backup differenziali e incrementali:

    -   VSS \_ FSBT \_ tutti i \_ backup \_ necessari
    -   è \_ \_ necessario il backup incrementale FSBT VSS \_ \_
    -   è \_ \_ necessario il \_ backup DIFFERENZIAle FSBT VSS \_

    Sono disponibili tre valori "copia shadow obbligatoria":

    -   VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari
    -   \_ \_ snapshot incrementale FSBT \_ VSS \_ obbligatorio
    -   \_ \_ snapshot differenziale FSBT VSS \_ \_ obbligatorio

    I set di file contrassegnati con un tipo di backup della specifica del file "copia shadow obbligatoria" indicano che un richiedente deve copiare i dati da una copia shadow durante l'esecuzione di operazioni di backup INCREMENTAli, DIFFERENZIAli o tutte (che includono operazioni sia incrementali che differenziali).

    Il flag "backup obbligatorio", applicato a operazioni INCREMENTAli, DIFFERENZIAli o di backup, indica che il writer prevede una copia della versione corrente del set di file in modo che sia disponibile dopo il ripristino di qualsiasi operazione di backup. In genere, ciò significa che se un set di file è contrassegnato con "backup obbligatorio", un richiedente copia tutti i membri sui supporti di backup durante un backup incrementale o differenziale, indipendentemente dal momento in cui si è verificata l'ultima modifica o backup.

    Per impostazione predefinita, i set di file vengono aggiunti ai componenti con un tipo di backup della specifica del file VSS \_ FSBT \_ tutti i \_ backup \_ necessari \| VSS \_ FSBT \_ tutti gli \_ snapshot \_ necessari. Pertanto, a meno che un writer non imposti in modo esplicito il tipo di backup per la specifica del file in caso contrario, i richiedenti dovranno copiare i file non gestiti dalle operazioni parziali dei file o i file differenziati specificati nella maggior parte dei set di file verranno in genere copiati integralmente nei supporti di backup.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Timbri di backup
</dt> <dd>

I writer che supportano i timbri di backup (timestamp del VSS \_ BS \_ ) possono scegliere di generare informazioni sugli Stamp di backup da utilizzare per supportare le successive operazioni di backup e ripristino differenziale.

Il formato e le informazioni contenute nelle stringhe contenenti informazioni sugli Stamp di backup sono privati per il writer che li genera; il richiedente non è in grado di elaborare queste informazioni.

I writer di supporto archiviano l'indicatore di backup nel documento componenti di backup come stringa usando il metodo [**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) .

Il ruolo del richiedente nella gestione delle informazioni sugli indicatori di backup è (se esistente) per renderlo disponibile al writer chiamando [**IVssBackupComponents:: SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) in un'operazione di backup o ripristino futura.

</dd> </dl>

 

 
