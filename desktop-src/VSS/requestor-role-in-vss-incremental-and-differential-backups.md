---
description: "Per supportare un'operazione di backup incrementale o differenziale, un richiedente deve eseguire le operazioni seguenti:"
ms.assetid: a77700e3-8217-460e-bec9-1041d03eec41
title: Ruolo richiedente nei backup incrementali e differenziali di VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637d4bf97b97d484080c85a2345599a05e4bbd89f88a0c1786b5bda911a83331
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122006"
---
# <a name="requester-role-in-vss-incremental-and-differential-backups"></a>Ruolo richiedente nei backup incrementali e differenziali di VSS

Per supportare [*un'operazione di*](vssgloss-i.md) backup [*incrementale*](vssgloss-d.md) o differenziale, un richiedente deve eseguire le operazioni seguenti:

1.  Determinare il livello di supporto del writer disponibile (usando [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) per ottenere l'accesso alle informazioni nei documenti dei metadati del writer), in particolare determinare lo schema di backup supportato ([**VSS \_ BACKUP \_ SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)).
2.  Impostare uno stato di backup appropriato.
3.  Ottenere le specifiche a livello di file e set di file per un backup incrementale o differenziale.
4.  Eseguire il backup.

## <a name="requester-determination-of-incremental-and-differential-support-and-configuration"></a>Determinazione del supporto e della configurazione incrementali e differenziali del richiedente

Un richiedente deve ottenere informazioni sul supporto del writer prima di selezionare i componenti da includere in un backup incrementale o differenziale o impostare il proprio stato.

<dl> <dt>

<span id="Determining_Writer_Support"></span><span id="determining_writer_support"></span><span id="DETERMINING_WRITER_SUPPORT"></span>Determinazione del supporto del writer
</dt> <dd>

Un richiedente determina se un determinato writer supporta i backup incrementali o differenziali di VSS recuperando la maschera dello schema di backup del writer usando il metodo [**IVssExamineWriterMetadata::GetBackupSchema.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

La maschera dello schema di backup di un writer che supporta tecniche incrementali o differenziali di VSS conterrà **\_ VSS BS \_ INCREMENTAL** o **\_ VSS BS \_ DIFFERENTIAL** o entrambe. I writer possono anche indicare restrizioni sulla loro partecipazione con il flag **DIFFERENZIALE INCREMENTALE ESCLUSIVO DI \_ VSS \_ \_ \_ BS.** Per altre informazioni sugli schemi di backup, vedere [**VSS \_ BACKUP \_ SCHEMA.**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)

</dd> <dt>

<span id="Setting_Requester_Backup_State"></span><span id="setting_requester_backup_state"></span><span id="SETTING_REQUESTER_BACKUP_STATE"></span>Impostazione dello stato di backup del richiedente
</dt> <dd>

Un richiedente indica che un backup è un backup incrementale o differenziale impostando un tipo di backup su **VSS \_ BT \_ INCREMENTAL** o **VSS \_ BT \_ DIFFERENTIAL** usando il metodo [**IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) prima di generare un evento [**PrepareForBackup.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)

Il [**metodo IVssBackupComponents::SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) viene usato anche per indicare se il richiedente fornisce il supporto di [*file*](vssgloss-p.md)parziali, che viene spesso usato per implementare determinate operazioni di backup e ripristino incrementali.

</dd> </dl>

## <a name="getting-writer-specifications-for-incremental-and-differential-backups"></a>Recupero delle specifiche del writer per i backup incrementali e differenziali

Le informazioni sulla specifica di backup dei file a livello di set di file ([**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) contenute nel documento dei metadati del writer di ogni writer sono disponibili per l'esame dopo la corretta restituzione di [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

Tuttavia, un writer può aggiungere [*file con*](vssgloss-d.md) differenze o richiedere il supporto parziale [*dei file*](vssgloss-p.md) fino alla corretta gestione dell'evento [*PostSnapshot.*](vssgloss-p.md)

Le specifiche di supporto file e file parziali differenze possono eseguire l'override del tipo di backup della specifica di file, pertanto i richiedenti possono voler rinviare un'analisi completa di tutte le specifiche del writer sui backup incrementali e differenziali fino a dopo la restituzione corretta di [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).

<dl> <dt>

<span id="Getting_File_Backup_Specification_Information"></span><span id="getting_file_backup_specification_information"></span><span id="GETTING_FILE_BACKUP_SPECIFICATION_INFORMATION"></span>Recupero delle informazioni sulle specifiche di backup dei file
</dt> <dd>

Le informazioni sulla specifica di backup dei file a livello di set di file ([**VSS \_ FILE SPEC \_ BACKUP \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) sono contenute nel documento di metadati writer di ogni writer e possono essere esaminate immediatamente dopo il corretto ritorno di [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).

I richiedenti devono ottenere le maschere di specifica del backup dei file ([**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)) per ogni set di [](vssgloss-e.md) file di ognuno dei componenti di un writer da includere nel backup incrementale o differenziale, indipendentemente dal fatto che il componente sia stato incluso in modo esplicito o [*implicito.*](vssgloss-i.md)

Un richiedente può determinare quale documento di metadati del writer deve essere sottoposto a query usando [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). L'istanza dell'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituita da **IVssBackupComponents::GetWriterComponents** fornisce informazioni sul writer tramite il metodo [**IVssWriterComponentsExt::GetWriterInfo.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo)

Il richiedente ottiene informazioni sul componente tramite istanze [**dell'interfaccia IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) corrispondente a un componente incluso gestito da un writer specificato tramite [**IVssExamineWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent).

Le informazioni sui set di file gestiti dal componente corrispondente all'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) vengono ottenute tramite chiamate a [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent::GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)o [**IVssWMComponent::GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile) (in base alle esigenze).

Queste chiamate possono restituire istanze [**dell'interfaccia IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) per ogni set di file di un componente.

Il tipo di backup della specifica file di un set di file viene ottenuto chiamando [**IVssWMFiledesc::GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask).

</dd> <dt>

<span id="Getting_Partial_File_and_Differenced_File_Information"></span><span id="getting_partial_file_and_differenced_file_information"></span><span id="GETTING_PARTIAL_FILE_AND_DIFFERENCED_FILE_INFORMATION"></span>Recupero di file parziali e informazioni sui file con differenze
</dt> <dd>

Un richiedente ottiene informazioni parziali sul file e sui file con differenze tramite [**l'interfaccia IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Un richiedente può scorrere tutti i writer inclusi in un backup usando [**IVssBackupComponents::GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) e [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

L'istanza di un'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituita da [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) fornisce l'accesso a tutte [](vssgloss-e.md) le istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondenti ai componenti inclusi in modo esplicito di un determinato writer tramite i metodi [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) [**e IVssWriterComponentsExt::GetComponentCount.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount)

Un richiedente dovrà eseguire tutte le istanze di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per tutti i writer il cui schema supporta il backup incrementale o differenziale, ovvero i writer la cui maschera dello schema di backup, come restituito da [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), include **VSS \_ BS \_ INCREMENTAL** quando il tipo di backup è **VSS \_ BT \_ INCREMENTAL** o **VSS \_ BS \_ DIFFERENTIAL** quando il tipo di backup è **VSS \_ BS \_ DIFFERENTIAL.**

Le informazioni sul file parziale vengono ottenute chiamando [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) e [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) (vedere [Uso di file parziali).](working-with-partial-files.md)

Per i writer che supportano le operazioni di backup sulla base degli ultimi dati di modifica di un file (writer la cui maschera dello schema di backup, come restituito da [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), include **VSS \_ BS \_ LAST \_ MODIFY),** le informazioni sui file differenze vengono ottenute chiamando [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount) e [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile).

Si noti che i file con differenze possono essere nuovi file, ovvero file che non sono membri di alcun set di file attualmente in un documento di metadati del writer specificato.

I richiedenti non devono trovare i file inclusi sia per le operazioni di file parziali che come file con differenze. Se un richiedente rileva una situazione di questo tipo, deve restituire e registrare un errore del writer.

Un richiedente può comunque scegliere di procedere con il backup dei file del writer problematico, ma in tal caso deve farlo in base alla specifica presente nelle informazioni sui file con differenze.

</dd> </dl>

## <a name="implementing-incremental-or-differential-backups"></a>Implementazione di backup incrementali o differenziali

Prima di implementare un backup, i richiedenti devono avere informazioni sui writer che supportano un [*backup*](vssgloss-d.md) [*incrementale*](vssgloss-i.md) o differenziale, su tutte le operazioni di file parziali richieste, su tutti i file con differenze e sul tipo di backup delle specifiche di tutti gli altri file.

<dl> <dt>

<span id="Nonsupporting_Writers"></span><span id="nonsupporting_writers"></span><span id="NONSUPPORTING_WRITERS"></span>Writer non diupporting
</dt> <dd>

I writer il cui schema non supportano il backup incrementale o differenziale (writer la cui maschera dello schema di backup, come restituito da [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), include **VSS \_ BS \_ INCREMENTAL** quando il tipo di backup è **VSS \_ BT \_ INCREMENTAL** o non include **VSS \_ BS \_ DIFFERENTIAL** quando il tipo di backup è **VSS \_ BS \_ DIFFERENTIAL**) non può fornire alcun supporto diretto a un'operazione di backup incrementale o differenziale.

Ciò non significa necessariamente che i dati dei writer non saranno coinvolti in un'operazione di backup incrementale o differenziale. Tuttavia, la scelta di cosa fare è a discrezione del richiedente. Il richiedente può eseguire una delle operazioni seguenti:

-   Eseguire il backup di nessun file appartenente ai writer non di backup (indicarlo chiaramente all'utente)
-   Eseguire il backup di tutti i file di writer non di backup
-   Eseguire un backup incrementale usando file system dati e i log della cronologia del richiedente.

L'ultima alternativa deve essere usata con cautela e solo se il richiedente comprende se i writer interessati possono supportare il backup incrementale o differenziale e il ripristino dei dati indipendentemente dal meccanismo VSS.

</dd> <dt>

<span id="Supporting_Writers"></span><span id="supporting_writers"></span><span id="SUPPORTING_WRITERS"></span>Writer di supporto
</dt> <dd>

Un richiedente deve elaborare (nell'ordine) tutti i file con differenze di un [*writer,*](vssgloss-d.md)gestire eventuali richieste di [*file*](vssgloss-p.md) parziali e quindi eseguire il backup dei file rimanenti in base al tipo di backup della specifica di file ([**VSS FILE \_ SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

1.  **Backup dei file con differenze:**

    Per i writer che supportano le operazioni di backup sulla base dei dati dell'ultima modifica (writer la cui maschera dello schema di backup, come restituito da [**IVssExamineWriterMetadata::GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema), include **VSS \_ BS \_ LAST \_ MODIFY),** un richiedente usa il percorso, la specifica del file e le informazioni sul flag di ricorsione restituite da [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) per generare un elenco di file come candidati per il backup incrementale o il ripristino.

    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile) può anche restituire un'ora dell'ultima modifica (espressa come [**struttura FILETIME).**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

    Se l'ora dell'ultima modifica fornita dal writer è diversa da zero, il richiedente la usa come base (anziché file system informazioni o dati archiviati del richiedente) per determinare se il file deve essere incluso nel backup [*incrementale*](vssgloss-i.md) o [*differenziale.*](vssgloss-d.md)

    Ad esempio, se l'ora dell'ultima modifica di un file restituita dal writer era:

    -   Dopo l'ultimo backup completo, il file deve essere incluso nei backup incrementali e differenziali.
    -   Dopo l'ultimo backup completo, ma prima dell'ultimo backup incrementale, il file deve essere incluso nelle operazioni di backup incrementale, ma non nei backup differenziali.

    Se l'ora dell'ultima modifica fornita dal writer è zero, il richiedente deve usare le informazioni file system e i propri dati archiviati per determinare l'ora di modifica del file con differenze.

2.  **Uso di operazioni di file parziali:**

    Se un writer ha richiesto il backup di un file usando un'operazione di file parziale, il richiedente usa le informazioni di offset del file per salvare i segmenti di file indicati nei supporti di backup. Per altre informazioni sulle operazioni sui file [parziali,](working-with-partial-files.md) vedere Uso di file parziali.

    Come indicato in precedenza, un writer non deve designare un file sia come file con differenze che come partecipante a un'operazione di file parziale. Se un richiedente rileva una situazione di questo tipo, deve restituire e registrare un errore del writer.

    Un richiedente può comunque scegliere di procedere con il backup dei file del writer problematico, ma in tal caso deve farlo in base alla specifica presente nelle informazioni sui file con differenze.

3.  **Uso del tipo di backup della specifica file:**

    Dopo aver elaborato tutti i file con differenze e le operazioni di file parziali, il richiedente elabora ora tutti i file rimanenti nel set di backup in base al tipo di backup della specifica di file ([**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type)).

    Esistono tre valori "necessari per il backup" dell'enumerazione [**VSS \_ FILE SPEC BACKUP \_ \_ \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) che influiscono sui backup differenziali e incrementali:

    -   VSS \_ FSBT \_ ALL \_ BACKUP \_ REQUIRED
    -   BACKUP INCREMENTALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO
    -   BACKUP DIFFERENZIALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO

    Sono disponibili tre valori "copia shadow obbligatoria":

    -   VSS \_ FSBT \_ ALL \_ SNAPSHOT \_ REQUIRED
    -   SNAPSHOT INCREMENTALE DI VSS \_ FSBT \_ \_ \_ OBBLIGATORIO
    -   È NECESSARIO UNO SNAPSHOT DIFFERENZIALE DI VSS \_ FSBT \_ \_ \_

    I set di file contrassegnati con un tipo di backup di specifica file "copia shadow obbligatoria" indicano che un richiedente deve copiare i dati da una copia shadow durante l'esecuzione di operazioni di backup INCREMENTAL, DIFFERENZIALE o ALL (che include operazioni incrementali e differenziali).

    Il flag "backup obbligatorio", applicato alle operazioni di backup INCREMENTAL, DIFFERENZIALE o ALL, indica che il writer prevede la disponibilità di una copia della versione corrente del set di file dopo il ripristino di qualsiasi operazione di backup. In genere, ciò significa che se un set di file è contrassegnato con "backup obbligatorio", un richiedente copierà tutti i relativi membri nei supporti di backup durante un backup incrementale o differenziale, indipendentemente dall'ultima volta che si è verificato il backup o la modifica.

    Per impostazione predefinita, i set di file vengono aggiunti ai componenti con un tipo di backup della specifica di file DI VSS \_ FSBT \_ ALL BACKUP REQUIRED \_ \_ \| VSS \_ FSBT \_ ALL SNAPSHOT \_ \_ REQUIRED. Pertanto, a meno che un writer non imposta in modo esplicito il tipo di backup della specifica di file in caso contrario, i richiedenti dovranno copiare i file non gestiti da operazioni di file parziali o file con differenze designate nella maggior parte dei set di file in genere verranno copiati nella loro interezza nei supporti di backup.

</dd> <dt>

<span id="Backup_Stamps"></span><span id="backup_stamps"></span><span id="BACKUP_STAMPS"></span>Stamp di backup
</dt> <dd>

I writer che supportano i timestamp di backup (VSS BS TIMESTAMP) possono scegliere di generare informazioni sul timestamp di backup da usare per supportare le operazioni di backup e ripristino incrementali e \_ \_ differenziali future.

Il formato e le informazioni contenute nelle stringhe contenenti informazioni sul timbro di backup sono privati per il writer che le genera; il richiedente non sa come elaborare queste informazioni.

I writer di supporto archiviano il timbro di backup nel documento componenti di backup come stringa usando il [**metodo IVssComponent::SetBackupStamp.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)

Il ruolo del richiedente nella gestione delle informazioni sul timestamp di backup è (se esistente) per renderle disponibili al writer chiamando [**IVssBackupComponents::SetPreviousBackupStamp**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setpreviousbackupstamp) in una futura operazione di backup o ripristino.

</dd> </dl>

 

 
