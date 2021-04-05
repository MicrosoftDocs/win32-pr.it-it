---
description: A volte è consigliabile creare una copia shadow in un sistema, ma usare la copia shadow in un secondo sistema.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importazione di volumi di copie shadow trasportabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d259fbc047d088ee1f7064804a3ee98fe48da1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131279"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importazione di volumi di copie shadow trasportabili

A volte è consigliabile creare una copia shadow in un sistema, ma usare la copia shadow in un secondo sistema.

Si consideri il caso in cui i dati di cui eseguire il backup vengono in genere gestiti da un determinato sistema (*systemOne*) durante le normali operazioni e che questi dati vengono archiviati fisicamente in un array di archiviazione o in un dispositivo.

Per ridurre al minimo eventuali problemi di *systemOne* (poiché le operazioni di backup possono richiedere un utilizzo intensivo delle risorse), è consigliabile eseguire il backup mediante *systemTwo*, un server di backup, che ha accesso allo stesso array di archiviazione di *systemOne*.

Per garantire una copia shadow corretta, cooperando con i writer in *systemOne* e mantenendo lo stato appropriato per le attività in corso, la copia shadow deve essere eseguita da *systemOne*.

Pertanto, *systemOne* deve creare una [*copia shadow trasportabile*](vssgloss-t.md), che verrà quindi importata da *systemTwo* .

**Windows server 2003, Standard Edition, Windows server 2003, Web Edition e Windows XP:** I set di copie shadow trasportabili non sono supportati. Tutte le edizioni di Windows Server 2003 con Service Pack 1 (SP1) supportano set di copie shadow trasportabili.

Un esempio tipico di importazione di una copia shadow trasportabile può procedere nel modo seguente:

1.  Inizialmente, l'unità logica (LUN) fornita dall'array di archiviazione viene montata come volume in *systemOne* (ad esempio, F:).
2.  Un richiedente in esecuzione su *systemOne* crea un'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e procede come se fosse preparato per un backup. Per ulteriori informazioni, vedere [Panoramica dell'inizializzazione del backup](overview-of-backup-initialization.md), [Panoramica della fase di individuazione dei backup](overview-of-the-backup-discovery-phase.md)e [Panoramica delle attività di pre-backup](overview-of-pre-backup-tasks.md) .
3.  Il richiedente in *systemOne* modifica il contesto di copia shadow usato in genere per l'operazione di backup locale (**\_ backup dell' \_ app \_ VSS CTX**) per indicare che verrà creata una copia shadow trasportabile (**VSS \_ VolSnap \_ attr \_ Transportable**). L'attributo trasportabile può essere aggiunto anche ad altri contesti di copia shadow.
4.  Con un contesto di copia shadow **di \_ VSS CTX \_ app \_ backup** \| **VSS \_ VolSnap \_ attr \_ Transportable**, il richiedente in *systemOne* crea una copia shadow chiamando [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset).
5.  *SystemOne* utilizza [**IVssBackupComponents:: saveasxml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) per salvare lo stato corrente del documento dei componenti di backup e [**IVssExamineWriterMetadata:: saveasxml**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) per salvare i documenti di metadati del writer del writer. Le stringhe XML che contengono questi documenti vengono quindi rese disponibili a un richiedente in esecuzione in *systemTwo*.

    Il richiedente trasferisce il documento componenti di backup in *systemTwo*.

    Si noti che il richiedente in *systemOne* non rilascia la propria istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) in questa fase se lo scopo della copia shadow è per il backup. L'interfaccia deve rimanere aperta fino a quando *systemTwo* non completa correttamente le operazioni di backup. Solo a questo punto il richiedente emette un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) poiché alcuni writer troncano i log ed eseguono altre operazioni dopo un backup riuscito. Se l'obiettivo della copia shadow è data mining o altri scopi, l'interfaccia può essere chiusa in questo passaggio.

6.  Il richiedente in *systemTwo* chiama quindi [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) per ottenere l'accesso alla copia shadow creata dal richiedente in *systemOne*.
    > [!Note]  
    > Il richiedente è responsabile della serializzazione dell'operazione di copia shadow di importazione. Se inoltre la chiamata a [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) ha esito negativo, il servizio Copia Shadow del volume non esegue la pulizia dei lun. Il richiedente deve avviare la pulizia dei lun.

     

7.  Il richiedente in *systemTwo* procede con il backup del materiale copia shadow esattamente come se eseguisse il backup di una copia shadow creata da se stessa. vedere [Panoramica del backup effettivo dei file](overview-of-actual-backup-of-files.md).

    Il richiedente in *systemTwo* Ottiene l' [*oggetto dispositivo*](vssgloss-d.md) della copia shadow usando [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) sulla copia shadow importata e lo aggiunge all'inizio dei percorsi file originali ottenuti dai metadati per accedere ai file di cui eseguire il backup.

8.  Dopo aver utilizzato la copia shadow, il richiedente in *systemTwo* deve eliminare la copia shadow. Come per le copie shadow non trasportabili, se il contesto della copia shadow indica le copie shadow della versione automatica (ad esempio, il **\_ \_ backup VSS CTX**), il rilascio di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) in *systemTwo* provocherà l'eliminazione della copia shadow da parte del servizio VSS. In caso contrario, se il contesto indica una copia shadow permanente (ad esempio, il **\_ \_ \_ rollback dell'app VSS CTX**), il richiedente in *systemTwo* deve eliminare in modo esplicito la copia shadow.

    Il richiedente in *systemTwo* segnala al richiedente in *systemOne* che è terminato con il backup della copia shadow trasportabile.

9.  Dopo che il richiedente in *systemOne* ha ricevuto la notifica che il richiedente in *systemTwo* ha completato il backup della copia shadow trasportabile, invia una notifica ai writer del sistema generando un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) con una chiamata a **IVssBackupComponents:: BackupComplete**. A questo punto, il richiedente in *systemOne* è libero di rilasciare l'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

**Copie shadow trasportabili in un cluster:** Le copie shadow trasportabili devono essere importate dall'esterno del cluster, purché il volume originale sia montato all'interno del cluster. Per informazioni sull'implementazione di un ripristino rapido in un cluster, vedere [ripristino rapido con volumi copiati shadow trasportabili](fast-recovery-using-transportable-shadow-copied-volumes.md).

 

 



