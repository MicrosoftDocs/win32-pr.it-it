---
description: Esistono situazioni in cui i dati di un writer dipendono dai dati gestiti da un altro writer. In questi casi, è necessario eseguire il backup o il ripristino dei dati da entrambi i writer.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Dipendenze tra componenti gestiti da Writer diversi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba3be6a2c2f0a722c4c5f06ca95351e004e1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349271"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Dipendenze tra componenti gestiti da Writer diversi

Esistono situazioni in cui i dati di un writer dipendono dai dati gestiti da un altro writer. In questi casi, è necessario eseguire il backup o il ripristino dei dati da entrambi i writer.

VSS gestisce questo problema tramite la nozione di dipendenza esplicita del componente writer e l'interfaccia [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) .

Un writer aggiunge una o più dipendenze durante la creazione del documento di metadati del writer usando il metodo [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) . Il writer passa il metodo il nome e il percorso logico del componente dipendente (gestito), nonché il nome e il percorso logico e l' [*ID della classe Writer*](vssgloss-w.md) (il GUID che identifica la classe) del componente da cui dipende.

Una volta stabilita, questa dipendenza informa il richiedente che durante qualsiasi operazione di backup o ripristino sia il componente dipendente che le destinazioni delle relative dipendenze devono partecipare.

Un determinato componente può disporre di più dipendenze, per cui è necessario che l'insieme e tutte le relative destinazioni dipendenti partecipino al backup e al ripristino.

Il componente dipendente e/o le destinazioni delle relative dipendenze possono essere inclusi in [*modo esplicito*](vssgloss-e.md) o [*implicito*](vssgloss-i.md) in un'operazione di backup o ripristino.

Il meccanismo di dipendenza del componente writer esplicito non deve essere utilizzato per creare una dipendenza tra due componenti sullo stesso writer. Le regole di selezione possono fornire la stessa funzionalità in modo più efficiente senza rischiare dipendenze circolari.

Ad esempio, è possibile usare [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) per definire la dipendenza del componente writerData (con il percorso logico "") del writer writeback sul componente internetData (con un percorso logico "Connections") di un writer denominato InternetConnector con un ID classe Writer X. Sebbene sia possibile che più writer con lo stesso ID di classe si trovino simultaneamente nel sistema, è possibile evitare confusione perché la combinazione di percorso logico e nome del componente è univoca nel sistema in VSS.

Un writer aggiunge più dipendenze a un determinato componente semplicemente chiamando [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) ripetuto con componenti diversi di writer diversi. È possibile trovare il numero di altri componenti da cui dipende un determinato componente esaminando il membro **cDependencies** della struttura [**\_ COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) .

Un writer o un richiedente recupera le istanze dell'interfaccia [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) con [**IVssWMComponent:: getdependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). **IVssWMDependency** restituisce il nome del componente, il percorso logico e l'ID di classe del writer che gestisce il componente che rappresenta la destinazione della dipendenza.

Il meccanismo di dipendenza non prescrive alcun ordine di preferenza particolare tra il componente dipendente e le destinazioni delle relative dipendenze. Come indicato in precedenza, tutte le dipendenze indicano che ogni volta che viene eseguito il backup o il ripristino di un componente specifico, è necessario eseguire il backup o il ripristino anche del componente o dei componenti da cui dipende. L'esatta implementazione di dipendenza è a discrezione dell'applicazione di backup.

Nel caso precedente, ad esempio, il componente writerData (percorso logico "") dipende dal componente InternetConnector (percorso logico "Connections"). Un richiedente è libero di interpretare questo problema in uno dei modi seguenti:

-   Se il componente dipendente, writerData, è selezionato (in modo implicito o esplicito) per il backup o il ripristino, il richiedente deve selezionare (in modo implicito o esplicito) la destinazione della relativa dipendenza, internetData
-   Se la destinazione della relativa dipendenza, internetData, non è selezionata per il backup, non è necessario selezionare il componente dipendente, writerData.

Tuttavia, durante lo sviluppo del supporto per le dipendenze, gli sviluppatori del richiedente devono tenere presente che non esiste alcun modo in cui un writer può determinare se uno dei suoi componenti è la destinazione di una dipendenza.

## <a name="declaring-remote-dependencies"></a>Dichiarazione delle dipendenze Remote

Un'applicazione distribuita è un'applicazione che può essere configurata per l'utilizzo di uno o più computer alla volta. In genere l'applicazione viene eseguita in uno o più computer del server applicazioni e comunica con (ma può essere effettivamente eseguita o meno) uno o più computer server di database. Questa configurazione viene a volte definita distribuzione multisistema. Spesso la stessa applicazione può essere configurata anche per l'esecuzione in un singolo computer che esegue sia un server applicazioni che un server di database. Una configurazione di questo tipo è detta distribuzione a singolo sistema. In entrambe le configurazioni, il server applicazioni e il server di database dispongono ognuno dei propri writer VSS indipendenti.

In una distribuzione multisistema, se un componente gestito dal writer dell'applicazione dipende da un componente remoto gestito dal writer del server di database, questo viene definito dipendenza remota. Una distribuzione a singolo sistema, al contrario, ha solo dipendenze locali.

Come esempio di una distribuzione multisistema, si consideri un server applicazioni che utilizza un server di database SQL Server come archivio dati. I dati specifici dell'applicazione, che includono le web part, i file di contenuto Web e la metabase IIS, si trovano in uno o più computer, detti server Web front-end. L'archivio dati SQL effettivo, che include il database di configurazione e più database di contenuto, risiede in uno o più computer, detti server di database back-end. Ogni server Web front-end contiene lo stesso contenuto e la stessa configurazione specifici dell'applicazione. Ogni server di database back-end può ospitare qualsiasi database di contenuto o il database di configurazione. Il software applicativo viene eseguito solo nei server Web front-end, non nei server di database. In questa configurazione, la VSS writer dell'applicazione ha dipendenze remote dai componenti gestiti dal writer SQL.

Un writer può dichiarare una dipendenza remota chiamando il metodo [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) , anteponendo " \\ \\ *NomeComputerRemoto* \\ ", dove *NomeComputerRemoto* è il nome del computer in cui risiede il componente remoto, al percorso logico nel parametro *wszOnLogicalPath* . Il valore di *NomeComputerRemoto* può essere un indirizzo IP o un nome di computer restituito dalla funzione [**presunto GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

**Windows Server 2003:** Un writer non può dichiarare le dipendenze remote fino a Windows Server 2003 con Service Pack 1 (SP1).

Per identificare una dipendenza, un richiedente chiama i metodi [**GetWriterId**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)e [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) dell'interfaccia [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) . Il richiedente deve esaminare il nome del componente restituito da **GetComponentName** nel parametro *pbstrComponentName* . Se il nome del componente inizia con " \\ \\ ", il richiedente deve presupporre che specifichi una dipendenza remota e che il primo componente che segue " \\ \\ " è il *NomeComputerRemoto* specificato quando il writer ha chiamato [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency). Se il nome del componente non inizia con " \\ \\ ", il richiedente deve presupporre che specifichi una dipendenza locale.

Se è presente una dipendenza remota, il richiedente deve eseguire il backup del componente remoto quando esegue il backup del componente locale. Per eseguire il backup del componente remoto, il richiedente deve disporre di un agente nel computer remoto e deve avviare il backup nel computer remoto.

## <a name="structuring-remote-dependencies"></a>Strutturazione delle dipendenze Remote

È importante comprendere che una dipendenza non è un componente di e di se stessa. Un componente è necessario per mantenere la dipendenza.

Negli esempi seguenti vengono illustrati due modi per strutturare un set di dipendenze.

``` syntax
Example 1:
    Writer 1
        Component A
            File A
            File B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")

Example 2:
    Writer 2
        Component A
            File A
            File B
        Component B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")
```

Nell'esempio 1, le dipendenze sono detenute dal componente A. Poiché è possibile selezionare solo i componenti, non singoli file, strutturare le dipendenze del componente A in questo modo, è necessario che l'intero componente, sia i file che le dipendenze, debbano essere sempre sottoposti a backup e ripristino insieme. Non è possibile eseguirne il backup o il ripristino singolarmente.

Nell'esempio 2, i componenti separati (i componenti A e B) contengono tutte le dipendenze. In questo caso, è possibile selezionare i due componenti in modo indipendente e quindi eseguire il backup e il ripristino in modo indipendente. Strutturare le dipendenze in questo modo fornisce a un'applicazione distribuita maggiore flessibilità nella gestione delle dipendenze remote.

## <a name="supporting-remote-dependencies"></a>Supporto delle dipendenze Remote

Un richiedente può fornire supporto completo o parziale per le dipendenze remote.

Per fornire supporto completo, il richiedente deve eseguire le operazioni seguenti in fase di backup e ripristino.

Al momento del backup, il richiedente deve avviare il backup nel computer front-end (locale), determinare le dipendenze esistenti e quindi eseguire lo spooling di processi di backup aggiuntivi per acquisire i database back-end. Il richiedente deve attendere il completamento dei processi di backup back-end nel computer remoto prima di chiamare i metodi [**IVssBackupComponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) . Se il richiedente resta in attesa fino al completamento del backup dei componenti back-end prima di chiamare **BackupComplete**, in questo modo verrà generato un backup recuperabile più facilmente per un writer che implementa ulteriori miglioramenti, ad esempio il blocco della topologia, durante il backup. La procedura seguente descrive le operazioni che il richiedente deve eseguire:

1.  Sul computer locale, il richiedente chiama i metodi [**IVssBackupComponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::P Repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)e [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .
2.  Al termine della copia shadow locale, ma prima del completamento del backup, il richiedente spoolerà i processi di backup aggiuntivi inviando una richiesta all'agente nel computer remoto.
3.  Nel computer remoto, l'agente del richiedente esegue la sequenza di backup con spooling chiamando [**InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)e [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).
4.  Quando l'agente del richiedente ha completato i processi di spooling nel computer remoto, il richiedente completa la sequenza di backup chiamando [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Al momento del ripristino, il richiedente deve avviare il ripristino che interessa il computer front-end (locale), selezionare i componenti e le relative dipendenze da ripristinare e quindi inviare l'evento di [**Preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) chiamando il metodo **IVssBackupComponents::P rerestore** . Il richiedente deve quindi eseguire lo spooling dei processi di ripristino back-end nel computer remoto e chiamare il metodo [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) quando i ripristini back-end sono completi. Questo requisito offre al writer front-end maggiore controllo sull'esperienza di ripristino e una migliore esperienza utente dell'amministratore in generale. Poiché i backup in ogni sistema non si verificano nello stesso momento, il writer front-end dovrà eseguire alcune operazioni di pulizia dei dati back-end. Nell'applicazione di esempio illustrata in precedenza "dichiarazione delle dipendenze remote", il writer deve avviare un nuovo mapping del sito o reindicizzare dopo il completamento di un ripristino di uno dei database back-end. A tale scopo, il writer deve ricevere eventi nel server front-end. La procedura seguente descrive le operazioni che il richiedente deve eseguire:

1.  Nel computer locale, il richiedente chiama [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (o [**IVssBackupComponentsEx:: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) e [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).
2.  Al termine della fase di [**preripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , ma prima dell'inizio della fase di post- [**ripristino**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , il richiedente spoolà ulteriori processi di ripristino inviando una richiesta all'agente nel computer remoto.
3.  Nel computer remoto, l'agente del richiedente esegue i processi di ripristino con spooling chiamando [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore), [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (o [**SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) e [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).
4.  Quando l'agente del richiedente ha completato i processi di spooling nel computer remoto, il richiedente completa la sequenza di ripristino chiamando [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) e [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Per fornire supporto parziale per le dipendenze remote, il richiedente deve seguire le dipendenze remote e includerle come parte del backup, ma l'ordine degli eventi nei sistemi front-end e back-end, come descritto nelle due procedure precedenti, non è necessario. Per un richiedente che implementa solo il supporto parziale, il richiedente deve fare riferimento alla documentazione di backup/ripristino dell'applicazione Writer per comprendere quali scenari è possibile supportare.

 

 
