---
description: Oltre a eseguire un backup o un ripristino e a supervisionare le copie shadow, un richiedente deve gestire le informazioni sui componenti dei writer con cui interagisce.
ms.assetid: 641abfbe-fc72-4468-9ef6-69c452adb1b3
title: Uso dei componenti da parte del richiedente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3149800a3f8cb52afff044e593f6b01177b27054c64a2ee19c19cb570ed633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998081"
---
# <a name="use-of-components-by-the-requester"></a>Uso dei componenti da parte del richiedente

Oltre a eseguire un backup o un ripristino e a supervisionare le copie shadow, un richiedente deve gestire le informazioni sui componenti dei writer con cui interagisce. La selezionabilità dei componenti e il percorso logico vengono usati per includere o escludere dati da un backup e per decidere quali informazioni sui componenti sono incluse nel documento Componenti di backup.

## <a name="requester-component-selection-during-backup"></a>Selezione del componente richiedente durante il backup

Durante le operazioni di backup, un richiedente importa i dati del componente dei metadati del writer usando i metodi [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e [**IVssBackupComponents::GetWriterMetadata .Per**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) altre informazioni, vedere Panoramica dell'inizializzazione del [backup.](overview-of-backup-initialization.md)

Dopo aver esaminato le informazioni sul writer con l'interfaccia [**IVssExamineWriterMetadata,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) un richiedente decide quali writer ne esegue il backup e, in misura limitata, quale dei componenti di un writer specificato ne esegue il backup.

Quando si esegue il backup di un writer, un richiedente:

-   Deve [*includere in*](vssgloss-e.md) modo esplicito tutti i componenti non selezionabili di un writer per i componenti di backup senza selezionabili per i predecessori di backup usando [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per aggiungere il componente al documento Componenti di backup
-   Può includere in modo esplicito qualsiasi componente selezionabile di un writer per i componenti di backup [**usando IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per aggiungere il componente al documento Componenti di backup
-   Se un componente selezionabile per il backup definisce un [*set*](vssgloss-c.md)di componenti, l'inclusione esplicita include [*implicitamente*](vssgloss-i.md) tutti i membri del set di componenti, indipendentemente dal fatto che sia selezionabile per il backup o meno. Questi componenti non vengono aggiunti al documento Componenti di backup.

Nell'aggiunta di un componente selezionabile per il backup o di un componente non selezionabile per i componenti di backup senza selezionabile per i predecessori di backup nel documento dei componenti di backup, un richiedente specifica quanto segue:

-   Istanza del writer che gestisce il componente
-   Identificatore di classe del writer
-   Percorso [*logico del*](vssgloss-l.md) componente (che può essere **NULL)**
-   Nome del componente

Se un componente non corrisponde alla specifica, verrà restituito un errore.

Se tale componente esiste, VSS crea [**un'interfaccia IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per il componente nel documento Componenti di backup. Queste informazioni saranno accessibili e modificabili dal writer e dal richiedente. Per un componente selezionabile che definisce un [*set*](vssgloss-c.md)di componenti, descrive non solo le proprietà del componente, ma anche tutti i sottocomponenti in esso contenuti.

Le informazioni sui componenti aggiunti in modo implicito non sono disponibili nel documento Componenti di backup. Inoltre, nel documento Componenti di backup non sono disponibili informazioni sui file. Per ottenere queste informazioni, il richiedente dovrà esaminare i documenti dei metadati del writer (che saranno già stati letti) nel contesto dei componenti archiviati selezionati nel documento Componenti di backup.

## <a name="requester-component-selection-during-restore"></a>Selezione del componente richiedente durante il ripristino

Durante le operazioni di ripristino, un richiedente non deve importare le informazioni sui componenti dai writer attualmente attivi nel sistema tramite [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), perché lo stato dei processi attualmente in esecuzione non riflette necessariamente lo stato dei processi durante un backup.

Deve comunque generare un evento [*Identify*](vssgloss-i.md) tramite [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), sia per creare un evento *Identify* che per determinare quali writer sono attualmente presenti nel sistema e il relativo stato.

Il richiedente recupera il documento dei componenti di backup archiviato durante l'inizializzazione e i documenti dei metadati del writer archiviati (per altre informazioni, vedere [Panoramica](overview-of-restore-initialization.md) dell'inizializzazione del ripristino).

L'inclusione dei componenti durante il backup è in gran [](vssgloss-s.md) parte la stessa [](vssgloss-l.md)di quella per il ripristino, ad eccezione del fatto che è necessario considerare selezionabile per il ripristino insieme al percorso logico, non selezionabile per [*il backup*](vssgloss-s.md).

Esistono tuttavia alcune differenze:

-   Se un componente [](vssgloss-e.md) è già stato incluso in modo esplicito nel documento Componenti di backup durante il backup, se è incluso per il ripristino (in modo esplicito o implicito), viene usato [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) per aggiungerlo in modo esplicito al documento dei componenti di backup per il ripristino.
-   Se un componente è stato [*incluso in*](vssgloss-i.md) modo implicito nel backup e non è selezionabile per il ripristino senza selezionabile per i predecessori di ripristino, che nel caso del backup implica la necessità di inclusione esplicita, il componente non viene incluso in modo esplicito, ovvero non viene aggiunto al documento Componenti di backup usando [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore). Tale componente deve essere considerato selezionato in modo implicito per il ripristino.
-   Di questi componenti selezionati in modo implicito per il backup (indipendentemente dal fatto che tale componente sia selezionabile per il backup o meno), solo quelli selezionabili per il ripristino possono essere aggiunti al documento Componenti di backup usando [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent).
-   Selezionabile per i componenti di ripristino può definire un [*set di componenti*](vssgloss-c.md) per il ripristino, proprio come per i componenti di backup. Questo elemento selezionabile per il componente di ripristino definisce quindi questo set di componenti per l'operazione di ripristino.

Un writer senza componenti selezionati in modo esplicito per il ripristino prima della generazione di un evento [*PreRestore*](vssgloss-p.md) non riceverà eventi vss.

I richiedenti e i writer possono accedere alle informazioni sui componenti archiviati usando [**l'interfaccia IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) Tramite **l'interfaccia IVssComponent,** i writer possono modificare alcune delle impostazioni dei componenti inclusi in modo esplicito nel documento Componenti di backup per supportare un ripristino , ad esempio la destinazione [*di ripristino*](vssgloss-r.md). Se definisce un set di componenti, le modifiche del writer di un componente incluso in modo esplicito verranno propagate ai [*relativi sottocomponenti*](vssgloss-s.md). Inoltre, l'interfaccia fornisce un meccanismo per passare informazioni sull'esito positivo e negativo del ripristino tra writer e richiedente.

Come durante il backup, le informazioni nel documento Componenti di backup non sono sufficienti per implementare il ripristino. Anche in questo caso, i documenti dei metadati del writer dovranno fornire informazioni sui percorsi effettivi dei file da ripristinare e individuare i componenti non selezionabili che fanno parte del set di componenti selezionabili e quindi devono essere ripristinati.

Per [informazioni sui tipi di selezionabilità](working-with-selectability-and-logical-paths.md) e il relativo utilizzo, vedere Uso della selezionabilità e dei percorsi logici.

## <a name="use-of-writer-component-document-information-by-the-requester"></a>Uso delle informazioni sui documenti del componente writer da parte del richiedente

Ogni componente è identificato in modo univoco [*dall'ID*](vssgloss-w.md) classe writer del writer padre, dal nome e dal [*percorso logico.*](vssgloss-l.md)

Il richiedente può usare [**l'interfaccia IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) restituita dal metodo [**IVssBackupComponents::GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) per ottenere informazioni su ogni componente archiviato.

Il nome e il percorso logico del componente (tra gli altri elementi) sono disponibili tramite [**l'interfaccia IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) restituita da [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent).

> [!Note]  
> Durante la fase di ripristino, il richiedente deve chiamare [**IVssWriterComponentsExt::GetComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) o [**IVssWriterComponentsExt::GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) solo dopo la chiamata a [**IVssBackupComponents::P reRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) per consentire al writer di aggiornare il documento dei componenti di backup. Un esempio di tale aggiornamento è la modifica della destinazione di ripristino.

 

Le informazioni sul writer padre di ogni componente selezionabile archiviato sono disponibili tramite [**IVssWriterComponentsExt::GetWriterInfo**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getwriterinfo).

Con queste informazioni, è possibile eseguire query sui documenti dei metadati del writer e identificare il documento corrispondente. Quindi, usando il percorso logico [*,*](vssgloss-l.md)il richiedente può identificare i componenti non selezionabili dipendenti per ogni componente selezionabile, ovvero identificare tutti i membri del set di componenti del componente [*selezionabile.*](vssgloss-c.md)

Usando l'interfaccia [**IVssExamineWriterMetadata,**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) il richiedente dispone ora di informazioni complete sul componente, inclusa la specifica del percorso (dall'interfaccia [**IVssWMComponent),**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) per i componenti selezionabili e non selezionabili di cui deve eseguire il backup o il ripristino.

Questo è uno dei motivi per cui è fondamentale che un richiedente salvi sia lo stato del proprio documento dei componenti di backup che i documenti dei metadati del writer di cui è in esecuzione il backup.

Per [informazioni più dettagliate, vedere](working-with-selectability-and-logical-paths.md) Uso della selezionabilità e dei percorsi logici.

 

 
