---
description: Nella tabella seguente vengono descritti i quattro tipi di componenti che possono essere necessari per un'operazione di backup.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Utilizzo della selezione per il backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4bd20bd0c9139f8ed1c9f56cc8f499f1b6aaf14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485012"
---
# <a name="working-with-selectability-for-backup"></a>Utilizzo della selezione per il backup

Nella tabella seguente vengono descritti i quattro tipi di componenti che possono essere necessari per un'operazione di backup.



| Tipo di componente                                                                                                                                                                                                               | Descrizione                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componenti non selezionabili per il backup<br/>             | Nessun predecessore selezionabile per il backup nei percorsi logici.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Componenti selezionabili per il backup<br/>                         | Nessun predecessore selezionabile per il backup nei percorsi logici.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Sottocomponenti non selezionabili per il backup<br/> | Componenti non selezionabili per il backup con i predecessori selezionabili per il backup nel percorso.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Sottocomponenti selezionabili-per-backup<br/>             | Componenti selezionabili per il backup con i predecessori selezionabili per il backup nel percorso.<br/>    |



 

Inoltre, qualsiasi componente selezionabile per il backup, indipendentemente dal fatto che contenga o meno i predecessori per il backup selezionabili, definisce un set di [*componenti*](vssgloss-c.md) se altri componenti lo hanno come predecessore nei percorsi logici.

Le regole che regolano la selezione dei componenti per il backup possono essere riepilogate come segue:

-   Quando un componente senza un predecessore selezionabile per il backup nel relativo percorso logico, ovvero se il componente è selezionabile per il backup o non selezionabile per il backup, è incluso in un backup, deve essere incluso in [*modo esplicito*](vssgloss-e.md). Ciò significa che i metadati per questi componenti vengono aggiunti al documento componenti di backup.

    I richiedenti aggiungono in modo esplicito questi componenti usando il metodo [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) .

-   I sottocomponenti non selezionabili per il backup vengono sempre [*inclusi in modo implicito*](vssgloss-i.md) nel backup. Ciò significa che i metadati per questi componenti non fanno parte del documento componenti di backup.
-   I sottocomponenti selezionabili per il backup vengono inclusi in modo implicito se tale predecessore è incluso in modo esplicito nel backup. In questo caso, i metadati per questi componenti non vengono aggiunti al documento componenti di backup. Se un sottocomponente selezionabile in modo implicito per il backup definisce un set di componenti, anche i membri del set di componenti vengono selezionati in modo implicito.
-   I sottocomponenti selezionabili per il backup il cui predecessore selezionabile per il backup non sono inclusi in modo esplicito nel backup possono comunque essere inclusi in modo esplicito dal richiedente usando il metodo [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) . I metadati per il componente verranno quindi aggiunti al documento componenti di backup. Se, inoltre, un sottocomponente selezionabile per il backup definisce un set di componenti, i membri del set di componenti vengono inclusi implicitamente nel backup.

Il caso "writeback" descritto in [percorsi logici di componenti](logical-pathing-of-components.md) può essere utilizzato come esempio per illustrare la selezione per il backup.



| Nome componente | Percorso logico            | Selezionabile per il backup |
|----------------|-------------------------|-----------------------|
| Eseguibili  | ""                      | N                     |
| "ConfigFiles"  | Eseguibili           | N                     |
| LicenseInfo  | ""                      | S                     |
| "Security"     | ""                      | S                     |
| UserInfo     | "Security"              | N                     |
| Certificati | "Security"              | N                     |
| "writerData"   | ""                      | S                     |
| Set1         | "writerData"            | N                     |
| Jan          | "writerData \\ set1"      | N                     |
| Dec          | "writerData \\ set1"      | N                     |
| Set2         | "writerData"            | N                     |
| Jan          | "writerData \\ set2"      | N                     |
| Dec          | "writerData \\ set2"      | N                     |
| Query        | "writerData \\ QueryLogs" | N                     |
| Utilizzo        | "writerData"            | S                     |
| Jan          | " \\ utilizzo writerData"     | N                     |
| Dec          | " \\ utilizzo writerData"     | N                     |



 

Ogni volta che viene eseguito il backup di "writeback", includendo in modo esplicito il componente "Executables" con il metodo [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , verrà incluso in modo implicito il componente "ConfigFiles".

Il componente "LicenseInfo" è un componente autonomo selezionabile per il backup. È possibile selezionarlo utilizzando il metodo [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) a discrezione del richiedente, ma la selezione non seleziona altri componenti.

Il componente selezionabile per il backup "sicurezza" definisce un set di componenti semplice contenente due sottocomponenti non selezionabili per il backup, "UserInfo" e "Certificates". Se per il backup viene inclusa in modo esplicito "Security", anche "UserInfo" e "Certificates" vengono sempre inclusi in modo implicito. Non è possibile includere i sottocomponenti "UserInfo" o "Certificates" in un'operazione di backup, a meno che non sia incluso "Security".

Se il componente "writerData" è selezionato, i componenti non selezionabili per il backup "set1", "set2" e "query", nonché il componente selezionabile per il backup "Usage", vengono selezionati in modo implicito. Ognuno di questi componenti include sottocomponenti che vengono selezionati in modo implicito per il backup. Nessuno dei relativi metadati verrà aggiunto al documento componenti di backup.

Se il componente "writerData" non è selezionato, i componenti non selezionabili per il backup "set1", "set2" e "query" non sono inclusi per il backup.

Tuttavia, i richiedenti possono scegliere di includere in modo esplicito il selezionabile per il componente di backup "Usage". I metadati per questo componente verranno aggiunti al documento componenti di backup. I sottocomponenti "Usage" "gen" e "Dec" verranno aggiunti in modo implicito al backup, ma non avranno le informazioni aggiunte al documento componenti di backup.

L'inclusione esplicita di un componente per il backup creerà un'istanza di [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) corrispondente nel documento componenti di backup.

Un richiedente recupererà le informazioni sui componenti inclusi in modo esplicito dal documento relativo ai componenti di backup esaminando i writer (usando [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)) inclusi nel documento e recuperando gli oggetti [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) archiviati.

Poiché non sono presenti le informazioni sui set di file (specifica file, percorso e flag di ricorsione) dei componenti presenti nel documento componenti di backup, né informazioni sui componenti aggiunti in modo implicito, i richiedenti dovranno eseguire query nei documenti di metadati del writer per ottenere informazioni complete su tutti i componenti inclusi nel documento componenti di backup.

 

 




