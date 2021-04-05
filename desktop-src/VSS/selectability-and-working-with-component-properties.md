---
description: Per lavorare con i componenti selezionati in modo implicito è necessario l'accesso ai documenti dei metadati del documento e del writer dei componenti di backup.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Selezione e utilizzo delle proprietà dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d06683bafb02802d84f152f1ceb662eb7491f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131258"
---
# <a name="selectability-and-working-with-component-properties"></a>Selezione e utilizzo delle proprietà dei componenti

Per lavorare con i componenti selezionati in modo implicito è necessario l'accesso ai documenti dei metadati del documento e del writer dei componenti di backup.

per due motivi:

-   I dati del componente archiviati nel documento dei componenti di backup (rappresentato dall'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) ) non dispongono dell'accesso alle informazioni sui set di file dei componenti, ovvero specifica file, percorso e flag di ricorsione. Vedere [utilizzo del documento componenti di backup](working-with-the-backup-components-document.md).
-   Solo i componenti [*inclusi in modo esplicito*](vssgloss-e.md) nel documento componenti di backup durante il backup hanno le informazioni archiviate direttamente nel documento componenti di backup. I richiedenti e i writer devono utilizzare le informazioni disponibili tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , in combinazione con le informazioni sul [*percorso logico*](vssgloss-l.md) e i documenti dei metadati del writer per ottenere informazioni su e impostare le proprietà dei componenti [*inclusi in modo implicito*](vssgloss-i.md) .

Il caso "writeback" descritto in [percorsi logici di componenti](logical-pathing-of-components.md) può essere utilizzato per illustrare la selezione per il backup.



| Nome componente | Percorso logico            | Selezionabile per il backup | Selezionabile per il ripristino | Incluso in modo esplicito |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| Eseguibili  | ""                      | N                     | N                      | S                   |
| "ConfigFiles"  | Eseguibili           | N                     | N                      | S                   |
| LicenseInfo  | ""                      | S                     | N                      | S                   |
| "Security"     | ""                      | S                     | N                      | S                   |
| UserInfo     | "Security"              | N                     | N                      | N                   |
| Certificati | "Security"              | N                     | N                      | N                   |
| "writerData"   | ""                      | S                     | S                      | S                   |
| Set1         | "writerData"            | N                     | S                      | N                   |
| Jan          | "writerData \\ set1"      | N                     | N                      | N                   |
| Dec          | "writerData \\ set1"      | N                     | N                      | N                   |
| Set2         | "writerData"            | N                     | S                      | N                   |
| Jan          | "writerData \\ set2"      | N                     | N                      | N                   |
| Dec          | "writerData \\ set2"      | N                     | N                      | N                   |
| Query        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| Utilizzo        | "writerData"            | S                     | S                      | N                   |
| Jan          | " \\ utilizzo writerData"     | N                     | N                      | N                   |
| Dec          | " \\ utilizzo writerData"     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Componenti inclusi in modo implicito nel set di backup

Durante l'esame del documento di metadati del writer del writer (vedere [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) durante il backup, un richiedente deve archiviare un elenco di tutti i componenti, i [*percorsi logici*](vssgloss-l.md)e le informazioni sui set di file.

Il set di file e le informazioni sui file esclusi saranno necessari per determinare un elenco di file per qualsiasi componente incluso (in modo esplicito o implicito).

Per i componenti non selezionabili per i componenti di backup senza selezione per i predecessori di backup e selezionabili per i componenti di backup che non definiscono un [*set*](vssgloss-c.md)di componenti, saranno necessarie solo le informazioni sui file impostati e esclusi per identificare tutti i candidati del componente per il backup, in quanto questi componenti non definiscono sottocomponenti.

Per i componenti selezionabili inclusi in modo esplicito per i componenti di backup che definiscono un set di componenti, le informazioni sui file vengono impostate ed escluse sia per il componente di definizione che per tutti i [*sottocomponenti*](vssgloss-s.md) da utilizzare per selezionare i file per il backup.

Ciò significa che i set di backup per i componenti "Executables", "ConfigFiles" e "LicenseInfo" possono essere trovati solo esaminando i metadati del writer solo per questi componenti usando le istanze dell'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .

Tuttavia, se writerData è incluso in modo esplicito nel backup, è necessario esaminarne l'istanza dell'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) e quelli per "set1", "Jan" (con percorso logico "writerData \\ set1"), "Dec" (con percorso logico "writerData \\ set1"), "set2", "Jan" (con percorso logico "writerData \\ set2"), "Dec" (con percorso logico "writerData \\ set2"), "query", "Usage", "Jan" (con percorso logico "WriterData \\ Usage") e "Dec" (con percorso logico "writerData \\ Usage").

A tale scopo, è necessario che un richiedente identifichi innanzitutto che il componente "writerData" (percorso logico "") è selezionabile. Dovrà quindi eseguire l'analisi di tutti gli altri componenti gestiti dal writer per determinare se il primo elemento nel percorso logico è "writerData". I componenti che contengono "writerData" come membri iniziali del percorso logico sono identificati come sottocomponenti di "writerData" e sono selezionati in modo implicito quando vengono selezionati in modo esplicito.

In realtà, è necessario eseguire un'analisi simile per determinare che nessun componente ha "LicenseInfo" come membro principale del percorso logico e che quindi "LicenseInfo" non ha sottocomponenti.

A causa della complessità di questo meccanismo nel servizio Copia Shadow del volume, molti writer del richiedente possono rivelarsi utili per creare strutture personalizzate per archiviare le informazioni sui componenti e sui set di backup sia per i componenti esplicitamente che per quelli aggiunti in modo implicito.

## <a name="properties-of-implicitly-included-components"></a>Proprietà dei componenti inclusi in modo implicito

Durante le operazioni di ripristino e backup, le istanze delle interfacce [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) e [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) vengono utilizzate sia per recuperare informazioni sui componenti, sia per impostare o modificare le proprietà del componente. Tuttavia, solo i componenti inclusi in modo esplicito avranno istanze dell'interfaccia **IVssComponent** o saranno accessibili all'interfaccia **IVssBackupComponents** .

Alcune proprietà sono a livello di set di componenti nell'ambito. Queste proprietà includono quanto segue:

-   Stato di backup e ripristino: <dl>

[**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent:: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Opzioni di backup e ripristino: <dl>

[**IVssBackupComponents:: SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent:: GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents:: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent:: GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Messaggi di errore: <dl>

[**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent:: SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent:: SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Destinazioni di ripristino: <dl>

[**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Timbri di backup: <dl>

[**IVssComponent:: SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**IVssComponent:: GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Metadati aggiuntivi: <dl>

[**IVssComponent:: SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**IVssComponent:: GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**IVssComponent:: SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Pertanto, si utilizza l'istanza dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) del membro di definizione di un set di componenti o si utilizza il nome, il tipo e il percorso logico del membro di definizione con un metodo [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) per impostare o recuperare le proprietà per tutti i membri del set di componenti.

Per questo motivo, i set di componenti vengono considerati come unità. Un backup di un set di componenti, ad esempio, ha esito positivo solo se il backup di tutti i set di file di tutti i relativi componenti ha esito positivo.

Nell'esempio precedente, si supponga che un file nel componente "Jan" (con percorso logico "writerData \\ set2") sia un membro del set di componenti definito da "writerData". Se non è stato possibile eseguire il backup di uno dei file "gen", un richiedente utilizzerebbe le informazioni "writerData" (il nome "writerData", il percorso "" e il tipo di componente) come argomenti quando si imposta [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) con **false** per indicare l'errore del set di componenti.

Analogamente, lo stato restituito da [**IVssComponent:: GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) per l'istanza "writerData" dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) si applica non solo a "writerData" ma anche a tutti i relativi sottocomponenti.

Se, inoltre, un writer sceglie di modificare la destinazione di ripristino utilizzando [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) dell'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)"writerData", la destinazione di ripristino verrà modificata per tutti i set di file di tutti i sottocomponenti "writerData".

Le proprietà seguenti si applicano non a livello di componente, ma a specifici file o set di file:

-   Mapping percorsi alternativi: <dl>

[**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent:: GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   File differenziati: <dl>

[**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent:: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent:: GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   File parziali: <dl>

[**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Destinazioni dirette: <dl>

[**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Nuove destinazioni: <dl>

[**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Quando un richiedente accede a queste funzionalità per un sottocomponente usando l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , USA le informazioni sul componente per il componente di definizione del set di componenti, ma le informazioni sui file o sui file impostati per il sottocomponente.

Analogamente, se la proprietà è accessibile tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , viene utilizzata l'istanza corrispondente al sottocomponente che lo definisce, ma gli argomenti del file o del set di file vengono ricavati dal sottocomponente.

Si supponga, ad esempio, che il sottocomponente "Jan" (con percorso logico "writerData \\ set2") abbia un file impostato con il percorso "c: \\ Fred", una specifica di file " \* . dat" e un flag ricorsivo di **true** potrebbe dover essere ripristinato in un percorso alternativo.

In tal caso, un richiedente chiamerà [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping), usando le informazioni di "writerData" (tipo di componente, il nome del componente "writeData" e il percorso logico "") insieme alle informazioni sul set di file di "Jan" (percorso "c: \\ Fred", specifica del file " \* . dat" e ricorsione uguale a **true**).

Si noti che in questo caso le informazioni sui set di file devono corrispondere esattamente alle informazioni del set di file usate da [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) per aggiungere file a Jan.

Analogamente, se un writer volesse aggiungere una destinazione diretta a un file con il percorso "c: \\ Ethel" e il nome "Lucy. dat" gestito da "Jan" (con percorso logico "writerData \\ set2"), userà l'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente a "writerData", ma le informazioni sul file di "Jan".

## <a name="implicitly-included-components-in-the-restore-set"></a>Componenti inclusi in modo implicito nel set di ripristino

I componenti inclusi in modo implicito in un backup possono essere inclusi in modo esplicito in un ripristino se possono essere selezionati per il ripristino. Come indicato in [utilizzo della selezione per il ripristino e i sottocomponenti](working-with-selectability-for-restore-and-subcomponents.md), tali componenti vengono aggiunti al documento componenti di backup usando il metodo [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) .

Tuttavia, non viene creata una nuova istanza dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , né il componente è direttamente accessibile tramite l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

Al contrario, un componente incluso in modo esplicito per il ripristino, ma incluso in modo implicito per il backup, deve essere accessibile tramite un'istanza dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) che corrisponde al componente che definisce il set di componenti di cui è membro al momento del backup.

Ad esempio, per includere in modo esplicito per il ripristino "set1", un sottocomponente del componente selezionabile per il backup "writerData", è possibile ottenere informazioni su di esso chiamando il metodo [**IVssComponent:: GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) dell'istanza "writerData" dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

 

 



