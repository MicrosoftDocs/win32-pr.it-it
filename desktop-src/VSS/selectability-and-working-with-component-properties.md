---
description: L'uso di componenti selezionati in modo implicito richiede l'accesso ai documenti di metadati del documento e del writer dei componenti di backup.
ms.assetid: ede51931-be50-4286-818b-0e6122247bdd
title: Selezionabilità e uso delle proprietà dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735481d4bd0d7fdaa4102026b74ca78be947afbab24858d88d9210dd7bd4e6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751653"
---
# <a name="selectability-and-working-with-component-properties"></a>Selezionabilità e uso delle proprietà dei componenti

L'uso di componenti selezionati in modo implicito richiede l'accesso ai documenti di metadati del documento e del writer dei componenti di backup.

per due motivi:

-   I dati dei componenti archiviati nel documento dei componenti di backup (rappresentati dall'interfaccia [**IVssComponent)**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) non hanno accesso alle informazioni sul set di file dei componenti, ovvero la specifica del file, il percorso e il flag di ricorsione. Vedere [Working with the Backup Components Document](working-with-the-backup-components-document.md).)
-   Solo i componenti inclusi [*in modo esplicito nel*](vssgloss-e.md) documento dei componenti di backup durante il backup hanno le informazioni direttamente archiviate nel documento dei componenti di backup. I richiedenti e i writer devono usare le informazioni disponibili [](vssgloss-l.md) tramite l'interfaccia [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) insieme alle informazioni sul percorso logico e ai documenti dei metadati del writer per ottenere informazioni sui componenti inclusi in modo [*implicito*](vssgloss-i.md) e impostarne le proprietà.

Il caso "MyWriter" illustrato in [Percorso logico](logical-pathing-of-components.md) dei componenti può essere usato per illustrare la selezionabilità per il backup.



| Nome componente | Percorso logico            | Selezionabile per il backup | Selezionabile per il ripristino | Incluso in modo esplicito |
|----------------|-------------------------|-----------------------|------------------------|---------------------|
| "Eseguibili"  | ""                      | N                     | N                      | S                   |
| "ConfigFiles"  | "Eseguibili"           | N                     | N                      | S                   |
| "LicenseInfo"  | ""                      | S                     | N                      | S                   |
| "Security"     | ""                      | S                     | N                      | S                   |
| "UserInfo"     | "Security"              | N                     | N                      | N                   |
| "Certificati" | "Security"              | N                     | N                      | N                   |
| "writerData"   | ""                      | S                     | S                      | S                   |
| "Set1"         | "writerData"            | N                     | S                      | N                   |
| "Jan"          | "writerData \\ Set1"      | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Set1"      | N                     | N                      | N                   |
| "Set2"         | "writerData"            | N                     | S                      | N                   |
| "Jan"          | "writerData \\ Set2"      | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Set2"      | N                     | N                      | N                   |
| "Query"        | "writerData \\ QueryLogs" | N                     | N                      | N                   |
| "Utilizzo"        | "writerData"            | S                     | S                      | N                   |
| "Jan"          | "writerData \\ Usage"     | N                     | N                      | N                   |
| "Dec"          | "writerData \\ Usage"     | N                     | N                      | N                   |



 

## <a name="implicitly-included-components-in-the-backup-set"></a>Componenti inclusi in modo implicito nel set di backup

Durante l'analisi del documento di metadati del writer (vedere [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)) durante il backup, un richiedente deve archiviare un elenco di tutti i componenti, i relativi percorsi logici e le relative informazioni sul set di file. [](vssgloss-l.md)

Le informazioni sul set di file e sui file esclusi saranno necessarie per determinare un elenco di file per qualsiasi componente incluso (in modo esplicito o implicito).

Per i componenti non selezionabili per i componenti di backup senza selezionabili per i predecessori di backup e selezionabili per i componenti di backup che non definiscono un set di componenti , saranno necessarie solo le informazioni sul [*set*](vssgloss-c.md)di file e sul file escluso per identificare tutti i candidati del componente per il backup, perché questi componenti non definiscono sottocomponenti.

Per includere in modo esplicito i componenti di backup che definiscono un set di componenti, il file imposta ed esclude le informazioni sui file sia per il componente di definizione che per tutti i [*sottocomponenti*](vssgloss-s.md) deve essere usato per selezionare i file per il backup.

Ciò significa che i set di backup per i componenti "Executables", "ConfigFiles" e "LicenseInfo" possono essere trovati solo esaminando i metadati del writer solo per questi componenti usando le relative istanze [**dell'interfaccia IVssWMComponent.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent)

Tuttavia, se writerData è incluso in modo esplicito nel backup, è necessario esaminare la relativa istanza [**dell'interfaccia IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) e quelle per "Set1", "Jan" (con percorso logico "writerData \\ Set1"), "Dec" (con percorso logico "writerData \\ Set1"), "Set2", "Jan" (con percorso logico "writerData \\ Set2"), "Dec" (con percorso logico "writerData \\ Set2"), "Query", "Usage", "Jan" (con percorso logico "writerData Usage") e "Dec" (con percorso logico \\ "writerData \\ Usage").

A tale scopo, un richiedente dovrà prima identificare che il componente "writerData" (percorso logico "") è selezionabile. Sarà quindi necessario analizzare tutti gli altri componenti gestiti dal writer per determinare se il primo elemento nel percorso logico è "writerData". I componenti che hanno "writerData" come membri iniziali del percorso logico vengono identificati come sottocomponenti di "writerData" e vengono selezionati in modo implicito quando viene selezionato in modo esplicito.

Sarà infatti necessario eseguire un'analisi simile per determinare che nessun componente ha "LicenseInfo" come membro iniziale del percorso logico e quindi che "LicenseInfo" non ha sottocomponenti.

A causa della complessità di questo meccanismo in VSS, molti writer richiedenti possono risultare utili per creare strutture proprie per l'archiviazione delle informazioni sui componenti e sui set di backup per i componenti aggiunti in modo esplicito e implicito.

## <a name="properties-of-implicitly-included-components"></a>Proprietà dei componenti inclusi in modo implicito

Durante le operazioni di ripristino e backup, le istanze delle interfacce [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) e [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) vengono usate sia per recuperare informazioni sui componenti che per impostare o modificare le proprietà dei componenti. Tuttavia, solo i componenti inclusi in modo esplicito avranno istanze **dell'interfaccia IVssComponent** o saranno accessibili all'interfaccia **IVssBackupComponents.**

Alcune proprietà hanno un ambito a livello di set di componenti. Queste proprietà includono quanto segue:

-   Stato di backup e ripristino: <dl>

[**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)  
    [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded)  
    [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus)  
    [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus)  
    </dl>
-   Opzioni di backup e ripristino: <dl>

[**IVssBackupComponents::SetBackupOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupoptions)  
    [**IVssComponent::GetBackupOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupoptions)  
    [**IVssBackupComponents::SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions)  
    [**IVssComponent::GetRestoreOptions**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoreoptions)  
    </dl>
-   Messaggi di errore: <dl>

[**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    [**IVssComponent::SetPostRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setpostrestorefailuremsg)  
    [**IVssComponent::SetPreRestoreFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setprerestorefailuremsg)  
    </dl>
-   Destinazioni di ripristino: <dl>

[**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget)  
    [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget)  
    </dl>
-   Indicatori di backup: <dl>

[**IVssComponent::SetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp)  
    [**IVssComponent::GetBackupStamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupstamp)  
    </dl>
-   Metadati aggiuntivi: <dl>

[**IVssComponent::SetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoremetadata)  
    [**IVssComponent::GetRestoreMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoremetadata)  
    [**IVssComponent::SetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupmetadata)  
    [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata)  
    </dl>

Si usa quindi l'istanza dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) del membro di definizione di un set di componenti oppure il nome, il tipo e il percorso logico del membro di definizione con un metodo [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) per impostare o recuperare le proprietà per tutti i membri del set di componenti.

Per questo motivo, i set di componenti vengono considerati come unità. Ad esempio, un backup di un set di componenti ha esito positivo solo se il backup di tutti i set di file di tutti i relativi componenti ha esito positivo.

Nell'esempio precedente si supponga che un file nel componente "Jan" (con percorso logico "writerData Set2") sia un membro del set di componenti definito \\ da "writerData". Se non è stato possibile eseguire il backup di uno dei file di "Jan", un richiedente userebbe le informazioni di "writerData" (il nome "writerData", il percorso "" e il relativo tipo di componente) come argomenti durante l'impostazione di [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) con **false** per indicare l'errore del set di componenti.

Analogamente, lo stato restituito da [**IVssComponent::GetBackupSucceeded**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupsucceeded) per l'istanza di "writerData" [**dell'interfaccia IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) si applica non solo a "writerData", ma anche a tutti i relativi sottocomponenti.

Inoltre, se un writer sceglie di modificare la destinazione di ripristino usando [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) dell'istanza di "writerData" di [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)la destinazione di ripristino viene cambiata per tutti i set di file di tutti i sottocomponenti di "writerData".

Le proprietà seguenti non si applicano a livello di componente, ma a determinati file o set di file:

-   Mapping di percorsi alternativi: <dl>

[**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)  
    [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping)  
    [**IVssComponent::GetAlternateLocationMappingCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmappingcount)  
    </dl>
-   File differenze: <dl>

[**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime)  
    [**IVssComponent::GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile)  
    [**IVssComponent::GetDifferencedFilesCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfilescount)  
    </dl>
-   File parziali: <dl>

[**IVssComponent::AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile)  
    [**IVssComponent::GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)  
    [**IVssComponent::GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)  
    </dl>
-   Destinazioni indirizzate: <dl>

[**IVssComponent::AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget)  
    [**IVssComponent::GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget)  
    [**IVssComponent::GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount)  
    </dl>
-   Nuove destinazioni: <dl>

[**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)  
    [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)  
    [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount)  
    </dl>

Quando un richiedente accede a queste funzionalità per un sottocomponente usando [**l'interfaccia IVssBackupComponents,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) usa le informazioni sul componente per il componente di definizione del set di componenti, ma le informazioni sul file o sul set di file per il sottocomponente.

Analogamente, se la proprietà è accessibile tramite l'interfaccia [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) viene usata l'istanza corrispondente al sottocomponente di definizione, ma gli argomenti del file o del set di file vengono presi dal sottocomponente.

Si supponga, ad esempio, che il sottocomponente "Jan" (con percorso logico "writerData Set2") abbia un set di file con un percorso \\ "c: fred", una specifica \\ di file \* ".dat"  e un flag ricorsivo true che potrebbe dover essere ripristinato in un percorso alternativo.

In questo caso, un richiedente chiamerebbe [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping)usando le informazioni di "writerData" (tipo di componente, nome del componente "writeData" e percorso logico "") insieme alle informazioni sul set di file di "Jan" (percorso "c:fu", \\ specifica del file " .dat" e ricorsione uguale a \* **true).**

Si noti che in questo caso le informazioni sul set di file devono corrispondere esattamente alle informazioni sul set di file usate da [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)o [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) per aggiungere file a Jan.

Analogamente, se un writer vuole aggiungere una destinazione diretta a un file con il percorso "c: ethel" e il nome \\ "writer.dat" gestito da "Jan" (con percorso logico "writerData \\ Set2"), userebbe l'istanza [**di IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente a "writerData", ma le informazioni sul file di "Jan".

## <a name="implicitly-included-components-in-the-restore-set"></a>Componenti inclusi in modo implicito nel set di ripristino

I componenti inclusi implicitamente in un backup possono essere inclusi in modo esplicito in un ripristino se sono selezionabili per il ripristino. Come illustrato in [Working with Selectability for Restore and Subcomponents](working-with-selectability-for-restore-and-subcomponents.md)(Uso della selezionabilità per il ripristino e i sottocomponenti), tali componenti vengono aggiunti al documento dei componenti di backup usando il metodo [**IVssBackupComponents::AddRestoreSubcomponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent)

Tuttavia, non viene creata una nuova istanza [**dell'interfaccia IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) né il componente è direttamente accessibile tramite l'interfaccia [**IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

È invece necessario accedere a un componente incluso in modo esplicito per il ripristino, ma in modo implicito per il backup, tramite un'istanza [**dell'interfaccia IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente al componente che ha definito il set di componenti di cui era membro al momento del backup.

Ad esempio, per includere in modo esplicito per il ripristino "Set1", un sottocomponente del componente selezionabile per il componente di backup "writerData", è necessario ottenere informazioni chiamando il metodo [**IVssComponent::GetRestoreSubcomponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoresubcomponent) dell'istanza di "writerData" [**dell'interfaccia IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

 

 



