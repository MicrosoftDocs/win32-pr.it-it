---
description: Nella tabella seguente vengono descritti i quattro tipi di componenti che possono essere coinvolti in un'operazione di backup.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Uso della selezionabilità per il backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82081bb9cef51572afc2a8b5c08cf845ee22736dd8fdc20edf60fa0082ce8c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118842315"
---
# <a name="working-with-selectability-for-backup"></a>Uso della selezionabilità per il backup

Nella tabella seguente vengono descritti i quattro tipi di componenti che possono essere coinvolti in un'operazione di backup.



| Tipo di componente                                                                                                                                                                                                               | Descrizione                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componenti non selezionabili per il backup<br/>             | Nessun predecessore selezionabile per il backup nei percorsi logici.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componenti selezionabili per il backup<br/>                         | Nessun predecessore selezionabile per il backup nei percorsi logici.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Sottocomponenti non selezionabili per il backup<br/> | Componenti non selezionabili per il backup con predecessori selectable-for-backup nel percorso.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Sottocomponenti selezionabili per il backup<br/>             | Componenti selezionabili per il backup con predecessori selectable-for-backup nel percorso.<br/>    |



 

Inoltre, qualsiasi componente selezionabile per il backup, indipendentemente dal fatto che abbia predecessori selezionabili per il backup, definisce un [*set*](vssgloss-c.md) di componenti se altri componenti lo hanno come predecessore nei percorsi logici.

Le regole che regolano la selezione dei componenti per il backup possono essere riepilogate nel modo seguente:

-   Quando un componente senza un predecessore selectable-for-backup nel percorso logico, indipendentemente dal fatto che sia selezionabile per il [](vssgloss-e.md)backup o non selezionabile per il backup, viene incluso in un backup, deve essere incluso in modo esplicito. Ciò significa che i metadati per questi componenti vengono aggiunti al documento Dei componenti di backup.

    I richiedenti aggiungono questi componenti in modo [**esplicito usando il metodo IVssBackupComponents::AddComponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)

-   I sottocomponenti non selezionabili per il backup vengono sempre [*inclusi in modo implicito*](vssgloss-i.md) nel backup. Ciò significa che i metadati per questi componenti non fanno parte del documento Componenti di backup.
-   I sottocomponenti selectable-for-backup vengono inclusi in modo implicito se tale predecessore è incluso in modo esplicito nel backup. In questo caso, i metadati per questi componenti non vengono aggiunti al documento Dei componenti di backup. Se un sottocomponente di backup selezionabile in modo implicito definisce un set di componenti, vengono selezionati in modo implicito anche i membri di tale set di componenti.
-   I sottocomponenti selectable-for-backup il cui predecessore selectable-for-backup non è incluso in modo esplicito nel backup possono comunque essere inclusi in modo esplicito dal richiedente usando il metodo [**IVssBackupComponents::AddComponent.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) I metadati per il componente verranno quindi aggiunti al documento Dei componenti di backup. Inoltre, se un sottocomponente selectable-for-backup definisce un set di componenti, i membri di tale set di componenti vengono inclusi in modo implicito nel backup.

Il caso "MyWriter" illustrato in [Percorso](logical-pathing-of-components.md) logico dei componenti può essere usato come esempio per illustrare la selezionabilità per il backup.



| Nome componente | Percorso logico            | Selezionabile per il backup |
|----------------|-------------------------|-----------------------|
| "Eseguibili"  | ""                      | N                     |
| "ConfigFiles"  | "Eseguibili"           | N                     |
| "LicenseInfo"  | ""                      | S                     |
| "Security"     | ""                      | S                     |
| "UserInfo"     | "Security"              | N                     |
| "Certificati" | "Security"              | N                     |
| "writerData"   | ""                      | S                     |
| "Set1"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set1"      | N                     |
| "Dec"          | "writerData \\ Set1"      | N                     |
| "Set2"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set2"      | N                     |
| "Dec"          | "writerData \\ Set2"      | N                     |
| "Query"        | "writerData \\ QueryLogs" | N                     |
| "Utilizzo"        | "writerData"            | S                     |
| "Jan"          | "writerData \\ Usage"     | N                     |
| "Dec"          | "writerData \\ Usage"     | N                     |



 

Ogni volta che viene eseguito il backup di "MyWriter", l'inclusione esplicita del componente "Executables" tramite il metodo [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) includerà in modo implicito il componente "ConfigFiles".

Il componente "LicenseInfo" è un componente autonomo selezionabile per il backup. Può essere selezionato usando il metodo [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) a discrezione del richiedente, ma la selezione non selezionerà altri componenti.

Il componente selectable-for-backup "Security" definisce un semplice set di componenti contenente due sottocomponenti non selezionabili per il backup, "UserInfo" e "Certificates". Se "Security" è incluso in modo esplicito per il backup, anche "UserInfo" e "Certificates" vengono sempre inclusi in modo implicito. Non è possibile includere i sottocomponenti "UserInfo" o "Certificates" in un'operazione di backup a meno che non sia incluso "Security".

Se il componente "writerData" è selezionato, i componenti non selezionabili per il backup "Set1", "Set2" e "Query" e il componente selezionabile per il backup "Usage" vengono selezionati in modo implicito. Ognuno di questi componenti include sottocomponenti selezionati in modo implicito per il backup. Nessuno dei relativi metadati verrà aggiunto al documento Dei componenti di backup.

Se il componente "writerData" non è selezionato, i componenti non selezionabili per il backup "Set1", "Set2" e "Query" non sono inclusi per il backup.

Tuttavia, i richiedenti possono scegliere di includere in modo esplicito il componente selezionabile per il componente di backup "Usage". I metadati per questo componente verranno aggiunti al documento Dei componenti di backup. I sottocomponenti "Jan" e "Dec" di "Usage" verranno aggiunti in modo implicito al backup, ma le relative informazioni non verranno aggiunte al documento Dei componenti di backup.

L'inclusione esplicita di un componente per il backup creerà [**un'istanza di IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente nel documento dei componenti di backup.

Un richiedente recupererà informazioni sui componenti inclusi in modo esplicito dal documento dei componenti di backup esaminando tali writer (usando [**IVssBackupComponents::GetWriterComponents)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)inclusi nel documento e recuperando gli oggetti [**IVssComponent archiviati.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

Poiché né le informazioni sul set di file (specifica di file, percorso e flag di ricorsione) dei componenti presenti nel documento dei componenti di backup, né le informazioni sui componenti aggiunti in modo implicito saranno presenti, i richiedenti doranno eseguire query sui documenti dei metadati del writer per ottenere informazioni complete su tutti i componenti inclusi nel documento dei componenti di backup.

 

 




