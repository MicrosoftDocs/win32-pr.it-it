---
description: In alcune situazioni i dati di un writer dipendono dai dati gestiti da un altro writer. In questi casi, è consigliabile eseguire il backup o il ripristino dei dati da entrambi i writer.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Dipendenze tra componenti gestiti da writer diversi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d50e88e13899951802b2ec3aa0bd9e651c16928b9f57409329035a28cfa1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122156"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Dipendenze tra componenti gestiti da writer diversi

In alcune situazioni i dati di un writer dipendono dai dati gestiti da un altro writer. In questi casi, è consigliabile eseguire il backup o il ripristino dei dati da entrambi i writer.

VSS gestisce questo problema tramite la nozione di dipendenza esplicita writer-componente e [**l'interfaccia IVssWMDependency.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

Un writer aggiunge una o più dipendenze durante la creazione del documento di metadati del writer usando il [**metodo IVssCreateWriterMetadata::AddComponentDependency.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) Il writer passa al metodo il nome e il percorso logico del componente dipendente (che gestisce), nonché il nome e il percorso logico e [*l'ID*](vssgloss-w.md) classe del writer (IL GUID che identifica la classe) del componente da cui dipende.

Una volta stabilita, questa dipendenza informa il richiedente che durante qualsiasi operazione di backup o ripristino sia il componente dipendente che le destinazioni delle relative dipendenze devono partecipare.

Un determinato componente può avere più dipendenze, il che richiede che il componente e tutte le destinazioni dipendenti partecipino insieme al backup e al ripristino.

Il componente dipendente e/o le destinazione delle relative dipendenze possono essere inclusi in modo esplicito o [*implicito*](vssgloss-i.md) in operazioni di backup o ripristino. [](vssgloss-e.md)

Il meccanismo di dipendenza del componente writer esplicito non deve essere usato per creare una dipendenza tra due componenti nello stesso writer. Le regole di selezione possono fornire la stessa funzionalità in modo più efficiente senza il rischio di dipendenze circolari.

Ad esempio, è possibile usare [**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) per definire la dipendenza del componente writerData (con percorso logico "") del writer MyWriter nel componente internetData (con un percorso logico "Connections") di un writer denominato InternetConnector con id di classe X del writer. Anche se è possibile che più writer con lo stesso ID di classe siano presenti contemporaneamente nel sistema, la confusione verrà evitata perché la combinazione di percorso logico e nome del componente è univoca nel sistema in VSS.

Un writer aggiunge più dipendenze a un determinato componente semplicemente chiamando [**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) ripetuto con componenti diversi di writer diversi. È possibile trovare il numero di altri componenti da cui dipende un determinato componente esaminando il membro **cDependencies** della [**struttura \_ COMPONENTINFO di VSS.**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)

Un writer o un richiedente recupera le istanze [**dell'interfaccia IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) [**con IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). **IVssWMDependency** restituisce il nome del componente, il percorso logico e l'ID classe del writer che gestisce il componente che è la destinazione della dipendenza.

Il meccanismo di dipendenza non prescrive alcun ordine di preferenza particolare tra il componente dipendente e le destinazioni delle relative dipendenze. Come indicato in precedenza, tutte le dipendenze indicano che ogni volta che viene eseguito il backup o il ripristino di un determinato componente, è necessario eseguire il backup o il ripristino anche del componente o dei componenti da cui dipende. L'implementazione esatta della dipendenza è a discrezione dell'applicazione di backup.

Nel caso precedente, ad esempio, il componente writerData (percorso logico "") dipende dal componente InternetConnector (percorso logico "Connessioni"). Un richiedente può interpretarlo in uno dei modi seguenti:

-   Se il componente dipendente, writerData, è selezionato (in modo implicito o esplicito) per il backup o il ripristino, il richiedente deve selezionare (in modo implicito o esplicito) la destinazione della dipendenza, internetData
-   Se la destinazione della dipendenza, internetData, non è selezionata per il backup, il componente dipendente, writerData, non deve essere selezionato.

Tuttavia, quando si sviluppa il supporto per le dipendenze, gli sviluppatori richiedenti devono tenere presente che un writer non può determinare in alcun modo se uno dei relativi componenti è la destinazione di una dipendenza.

## <a name="declaring-remote-dependencies"></a>Dichiarazione di dipendenze remote

Un'applicazione distribuita è un'applicazione che può essere configurata per l'utilizzo di uno o più computer alla volta. In genere l'applicazione viene eseguita in uno o più computer server applicazioni e comunica con uno o più computer server di database. Questa configurazione viene talvolta definita distribuzione multi-sistema. Spesso la stessa applicazione può anche essere configurata per l'esecuzione in un singolo computer che esegue sia un server applicazioni che un server di database. Tale configurazione è detta distribuzione a sistema singolo. In entrambe le configurazioni, il server applicazioni e il server di database hanno ognuno i propri VSS writer indipendenti.

In una distribuzione multi-sistema, se un componente gestito dal writer dell'applicazione dipende da un componente remoto gestito dal writer del server di database, si tratta di una dipendenza remota. Al contrario, una distribuzione a sistema singolo ha solo dipendenze locali.

Come esempio di distribuzione multi-sistema, si consideri un server applicazioni che usa un server di database SQL Server come archivio dati. I dati specifici dell'applicazione, che includono le web part, i file di contenuto Web e la metabase IIS, si trovano in uno o più computer, denominati server Web front-end. L'SQL dati, che include il database config e più database del contenuto, risiede in uno o più computer, denominati server di database back-end. Ogni server Web front-end contiene lo stesso contenuto e la stessa configurazione specifici dell'applicazione. Ogni server di database back-end può ospitare uno dei database del contenuto o del database di configurazione. Il software applicativo viene eseguito solo nei server Web front-end, non nei server di database. In questa configurazione, il VSS writer dell'applicazione ha dipendenze remote dai componenti gestiti dal writer SQL.

Un writer può dichiarare una dipendenza remota chiamando il metodo [**AddComponentDependency,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) anteponendo " RemoteComputerName ", dove RemoteComputerName è il nome del computer in cui si trova il componente remoto, al percorso logico nel \\ \\  \\ *parametro wszOnLogicalPath.*  Il valore di *RemoteComputerName* può essere un indirizzo IP o un nome di computer restituito dalla [**funzione GetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)

**Windows Server 2003:** Un writer non può dichiarare dipendenze remote fino Windows Server 2003 con Service Pack 1 (SP1).

Per identificare una dipendenza, un richiedente chiama i metodi [**GetWriterId,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid) [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)e [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) dell'interfaccia [**IVssWMDependency.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) Il richiedente deve esaminare il nome del componente **restituito da GetComponentName** nel *parametro pbstrComponentName.* Se il nome del componente inizia con " ", il richiedente deve presupporre che specifichi una dipendenza remota e che il primo componente che segue " " sia il RemoteComputerName specificato quando il writer ha chiamato \\ \\ \\ \\ [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency).  Se il nome del componente non inizia con " ", il richiedente deve presupporre \\ \\ che specifichi una dipendenza locale.

Se è presente una dipendenza remota, il richiedente deve eseguire il backup del componente remoto quando esegue il backup del componente locale. Per eseguire il backup del componente remoto, il richiedente deve disporre di un agente nel computer remoto e avviare il backup nel computer remoto.

## <a name="structuring-remote-dependencies"></a>Strutturazione delle dipendenze remote

È importante comprendere che una dipendenza non è un componente di e di se stessa. Un componente è necessario per contenere la dipendenza.

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

Nell'esempio 1, le dipendenze sono mantenute dal componente A. Poiché è possibile selezionare solo i componenti, non i singoli file, strutturando le dipendenze del componente A in questo modo è necessario eseguire sempre il backup e il ripristino dell'intero componente, sia dei file che delle dipendenze. Non è possibile eseguire il backup o il ripristino singolarmente.

Nell'esempio 2, i componenti separati (Componenti A e B) contengono ognuna delle dipendenze. In questo caso, i due componenti possono essere selezionati in modo indipendente e quindi sottoposti a backup e ripristino in modo indipendente. Strutturare le dipendenze in questo modo offre a un'applicazione distribuita una maggiore flessibilità nella gestione delle dipendenze remote.

## <a name="supporting-remote-dependencies"></a>Supporto delle dipendenze remote

Un richiedente può fornire supporto completo o parziale per le dipendenze remote.

Per fornire supporto completo, il richiedente deve eseguire le operazioni seguenti in fase di backup e ripristino.

In fase di backup, il richiedente deve avviare il backup nel computer front-end (locale), determinare le dipendenze esistenti ed eseguire lo spooling di processi di backup aggiuntivi per acquisire i database back-end. Il richiedente deve attendere il completamento dei processi di backup back-end nel computer remoto prima di chiamare i metodi [**IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**IVssBackupComponents::BackupComplete.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Se il richiedente attende il completamento del backup dei componenti back-end prima di chiamare **BackupComplete,** durante il backup verrà generato un backup più facilmente recuperabile per un writer che implementa miglioramenti aggiuntivi, ad esempio il blocco della topologia. La procedura seguente descrive le operazioni che il richiedente deve eseguire:

1.  Nel computer locale il richiedente chiama i metodi [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)e [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
2.  Dopo il completamento della copia shadow locale, ma prima del completamento del backup, il richiedente esegue lo spooling di processi di backup aggiuntivi inviando una richiesta al relativo agente nel computer remoto.
3.  Nel computer remoto, l'agente del richiedente esegue la sequenza di backup con spooling chiamando [**InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)e [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).
4.  Quando l'agente del richiedente ha completato i processi di spooling nel computer remoto, il richiedente completa la sequenza di backup chiamando [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

In fase di ripristino, il richiedente deve avviare il ripristino che interessa il computer front-end (locale), selezionare i componenti e le relative dipendenze da ripristinare e quindi inviare l'evento [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) chiamando il metodo **IVssBackupComponents::P reRestore.** Il richiedente deve quindi eseguire lo spooling dei processi di ripristino back-end nel computer remoto e chiamare il metodo [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) al termine dei ripristini back-end. Questo requisito offre al writer front-end un maggiore controllo sull'esperienza di ripristino e un'esperienza utente di amministratore migliore in generale. Poiché i backup in ognuno dei sistemi non vengono eseguiti nello stesso momento, il writer front-end dovrà eseguire alcune operazioni di pulizia dei dati back-end. Nell'applicazione di esempio illustrata nella sezione precedente "Dichiarazione delle dipendenze remote", il writer deve avviare un nuovo mapping o reindicizzazione del sito dopo il completamento di un ripristino di uno dei database back-end. A tale scopo, il writer deve ricevere eventi nel server front-end. La procedura seguente descrive le operazioni che il richiedente deve eseguire:

1.  Nel computer locale il richiedente chiama [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (o [**IVssBackupComponentsEx::SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) e [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).
2.  Al termine della fase [**prerestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ma prima dell'inizio della fase [**PostRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) il richiedente esegue lo spooling di processi di ripristino aggiuntivi inviando una richiesta al relativo agente nel computer remoto.
3.  Nel computer remoto, l'agente del richiedente esegue i processi di ripristino con spooling chiamando [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore), [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (o [**SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) e [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).
4.  Quando l'agente del richiedente ha completato i processi di spooling nel computer remoto, il richiedente completa la sequenza di ripristino chiamando [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) e [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Per fornire supporto parziale per le dipendenze remote, il richiedente deve seguire le dipendenze remote e includerle come parte del backup, ma l'ordinamento degli eventi nei sistemi front-end e back-end come descritto in dettaglio nelle due procedure precedenti non sarebbe necessario. Per un richiedente che implementa solo il supporto parziale, il richiedente deve fare riferimento alla documentazione di backup/ripristino dell'applicazione writer per comprendere quali scenari possono essere supportati.

 

 
