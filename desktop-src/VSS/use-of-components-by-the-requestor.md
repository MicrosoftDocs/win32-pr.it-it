---
description: Oltre a eseguire un backup o un ripristino e la supervisione delle copie shadow, un richiedente deve gestire le informazioni sui componenti dei writer con cui interagisce.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Uso dei componenti da parte del richiedente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83efdb9e80ac0331289c3b611978e66a58098de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526305"
---
# <a name="use-of-components-by-the-requester"></a>Uso dei componenti da parte del richiedente

Oltre a eseguire un backup o un ripristino e la supervisione delle copie shadow, un richiedente deve gestire le informazioni sui componenti dei writer con cui interagisce. La selezione dei componenti e il percorso logico vengono utilizzati per includere o escludere i dati da un backup e per decidere quali informazioni sui componenti sono incluse nel documento componenti di backup.

## <a name="requester-component-selection-during-backup"></a>Selezione componente del richiedente durante il backup

Durante le operazioni di backup, un richiedente importa i dati dei componenti dei metadati del writer usando i metodi [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) (vedere [Panoramica dell'inizializzazione del backup](overview-of-backup-initialization.md) per ulteriori informazioni).

Dopo aver esaminato le informazioni del writer con l'interfaccia [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , un richiedente decide i writer di cui verrà eseguito il backup e, in un extent limitato, i componenti di un determinato writer di cui verrà eseguito il backup.

Quando si esegue il backup di un writer, un richiedente:

-   Deve [*includere in modo esplicito*](vssgloss-e.md) tutti i non selezionabili di un writer per i componenti di backup senza selezionare per i predecessori di backup usando [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per aggiungere il componente al documento componenti di backup
-   Può includere in modo esplicito qualsiasi elemento selezionabile del writer per i componenti di backup usando [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per aggiungere il componente al documento dei componenti di backup
-   Se un componente selezionabile per il backup definisce un [*set di componenti*](vssgloss-c.md), l'inclusione esplicita include in [*modo implicito*](vssgloss-i.md) tutti i membri del set di componenti, indipendentemente dal fatto che sia selezionabile per il backup. Questi componenti non vengono aggiunti al documento componenti di backup.

Quando si aggiunge un componente selezionabile per il backup o non selezionabile per i componenti di backup senza selezionare per i predecessori del backup nel documento relativo ai componenti di backup, un richiedente specifica quanto segue:

-   Istanza del writer che gestisce il componente
-   Identificatore di classe del writer
-   [*Percorso logico*](vssgloss-l.md) del componente, che può essere **null**.
-   Nome del componente

Se un componente non corrisponde alla specifica, verrà restituito un errore.

Se è presente un componente di questo tipo, VSS crea un'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per il componente nel documento componenti di backup. Queste informazioni saranno accessibili e modificabili dal writer e dal richiedente. Per un componente selezionabile che definisce un [*set di componenti*](vssgloss-c.md), descrive non solo le proprietà del componente, ma anche tutti i sottocomponenti in essa contenuti.

Le informazioni sui componenti aggiunti in modo implicito non sono disponibili nel documento componenti di backup. Inoltre, nel documento componenti di backup non sono disponibili informazioni sul file. Per ottenere tali informazioni, il richiedente dovrà esaminare i documenti dei metadati del writer (che sono già stati letti) nel contesto dei componenti archiviati selezionati nel documento componenti di backup.

## <a name="requester-component-selection-during-restore"></a>Selezione componente del richiedente durante il ripristino

Durante le operazioni di ripristino, un richiedente non deve importare le informazioni sui componenti dagli autori attualmente attivi nel sistema tramite [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), perché lo stato dei processi attualmente in esecuzione non riflette necessariamente lo stato dei processi quando è stato eseguito un backup.

Deve comunque generare un [*evento di identificazione*](vssgloss-i.md) tramite [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), per creare un *evento di identificazione* e per determinare quali writer sono attualmente presenti nel sistema e il relativo stato.

Il richiedente Recupera il documento dei componenti di backup archiviati durante l'inizializzazione e i documenti dei metadati del writer archiviati. per ulteriori informazioni, vedere [Panoramica dell'inizializzazione del ripristino](overview-of-restore-initialization.md) .

L'inclusione di componenti durante il backup è sostanzialmente identica a quella per il ripristino, ad eccezione del fatto che è necessario considerare [*selezionabile per il ripristino*](vssgloss-s.md) insieme al [*percorso logico*](vssgloss-l.md), non [*selezionabile per il backup*](vssgloss-s.md).

Esistono, tuttavia, alcune differenze:

-   Se un componente è già stato [*incluso in modo esplicito*](vssgloss-e.md) nel documento componenti di backup durante il backup, se è incluso per il ripristino (in modo esplicito o implicito), [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) viene utilizzato per aggiungerlo in modo esplicito al documento componenti di backup per il ripristino.
-   Se un componente è stato [*incluso in modo implicito*](vssgloss-i.md) nel backup e non è selezionabile per il ripristino senza selezionare per i predecessori di ripristino, che nel caso di backup implica la necessità di inclusione esplicita, il componente non è incluso in modo esplicito (ovvero non viene aggiunto al documento dei componenti di backup usando [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore)). Tale componente deve essere considerato in modo implicito selezionato per il ripristino.
-   Dei componenti selezionati in modo implicito per il backup (indipendentemente dal fatto che il componente fosse selezionabile per il backup), è possibile aggiungere solo quelli selezionabili per il ripristino al documento componenti di backup usando [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).
-   Selezionabile per i componenti di ripristino può definire un [*set di componenti*](vssgloss-c.md) per il ripristino, come selezionabile per i componenti di backup. Questo componente selezionabile per il ripristino definisce quindi il set di componenti per l'operazione di ripristino.

Un writer senza componenti selezionato in modo esplicito per il ripristino prima della generazione di un evento di [*preripristino*](vssgloss-p.md) non riceverà alcun evento VSS.

I richiedenti e i writer possono accedere alle informazioni sui componenti archiviati usando l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . Tramite l'interfaccia **IVssComponent** , i writer possono modificare alcune impostazioni di quelle dei componenti inclusi in modo esplicito nel documento componenti di backup per supportare un ripristino, ad esempio la [*destinazione di ripristino*](vssgloss-r.md). Se definisce un set di componenti, le modifiche del writer di un componente incluso in modo esplicito vengono propagate ai relativi [*sottocomponenti*](vssgloss-s.md). Inoltre, l'interfaccia fornisce un meccanismo per passare le informazioni sull'esito positivo e negativo del ripristino tra writer e richiedente.

Come durante il backup, nel documento componenti di backup non sono disponibili informazioni sufficienti per implementare il ripristino. Anche in questo caso, i documenti di metadati del writer saranno necessari per fornire informazioni sui percorsi effettivi dei file da ripristinare e per individuare i componenti non selezionabili che fanno parte del set di componenti selezionabili e pertanto devono essere ripristinati.

Per informazioni sui tipi di selezione e sul relativo utilizzo, vedere [utilizzo dei percorsi di selezione e logica](working-with-selectability-and-logical-paths.md) .

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Uso delle informazioni del documento del componente writer da parte del richiedente

Ogni componente viene identificato in modo univoco dall' [*ID classe Writer*](vssgloss-w.md) del writer padre, dal nome e dal [*percorso logico*](vssgloss-l.md).

Il richiedente può usare l'interfaccia [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituita dal metodo [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) per ottenere informazioni su ogni componente archiviato.

Il nome del componente e il percorso logico (tra gli altri elementi) sono reperibili tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) restituita da [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent).

> [!Note]  
> Durante la fase di ripristino, il richiedente deve chiamare [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) o [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) solo dopo che è stata restituita la chiamata a [**IVssBackupComponents::P rerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , per consentire al writer di aggiornare il documento dei componenti di backup. Un esempio di tale aggiornamento consiste nel modificare la destinazione di ripristino.

 

È possibile trovare informazioni su ogni writer padre del componente selezionabile archiviato usando [**IVssWriterComponentsExt:: GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo).

Con queste informazioni, è possibile eseguire query sui documenti dei metadati del writer e identificare il documento corrispondente. Quindi, utilizzando il [*percorso logico*](vssgloss-l.md), il richiedente può identificare i componenti non selezionabili dipendenti per ogni componente selezionabile, ovvero identificare tutti i membri del [*set di componenti*](vssgloss-c.md)selezionabile del componente.

Usando l'interfaccia [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) , il richiedente dispone ora di informazioni complete sul componente, inclusa la specifica del percorso (dall'interfaccia [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) ), per i componenti selezionabili e non selezionabili di cui è necessario eseguire il backup o il ripristino.

Questo è un motivo per cui è essenziale per un richiedente salvare sia lo stato del documento dei propri componenti di backup che i documenti di metadati del writer dei writer di cui è in esecuzione il backup.

Per informazioni più dettagliate, vedere [utilizzo della selezione e dei percorsi logici](working-with-selectability-and-logical-paths.md) .

 

 
