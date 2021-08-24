---
description: A volte è consigliabile creare una copia shadow in un sistema, ma usare la copia shadow in un secondo sistema.
ms.assetid: 4ec63917-03c0-434e-892e-3d9d4c47740e
title: Importazione di volumi copiati shadow trasportabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73cee5d491cde59767a321094f0a7de2f34da97b29c6ed02e5cc490643b4dcd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510261"
---
# <a name="importing-transportable-shadow-copied-volumes"></a>Importazione di volumi copiati shadow trasportabili

A volte è consigliabile creare una copia shadow in un sistema, ma usare la copia shadow in un secondo sistema.

Si consideri il caso in cui i dati di cui eseguire il backup vengono in genere gestiti da un determinato sistema (*systemOne*) durante le normali operazioni e che questi dati vengono archiviati fisicamente in un array di archiviazione o in un'appliance.

Per ridurre al minimo eventuali interruzioni di *systemOne* (poiché le operazioni di backup possono essere a elevato utilizzo di risorse), è consigliabile eseguire il backup usando *systemTwo*, un server di backup, che ha accesso allo stesso array di archiviazione di *systemOne*.

Per garantire una copia shadow appropriata, cooperando con i writer in *systemOne* e mantenendo lo stato in modo appropriato per le attività in corso, la copia shadow deve essere eseguita *da systemOne*.

Di conseguenza, *systemOne* deve creare una [*copia shadow trasportabile,*](vssgloss-t.md)che verrà quindi importata da *systemTwo.*

**Windows Server 2003, edizione Standard, Windows Server 2003, Web Edition e Windows XP:** I set di copie shadow trasportabili non sono supportati. Tutte le edizioni di Windows Server 2003 con Service Pack 1 (SP1) supportano set di copie shadow trasportabili.

Un esempio tipico di importazione di una copia shadow trasportabile può procedere nel modo seguente:

1.  Inizialmente, l'unità logica (LUN) fornita dall'array di archiviazione viene montata come volume in *systemOne* (ad esempio, F:).
2.  Un richiedente in esecuzione in *systemOne* crea un'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e procede come se si preparava per un backup. Per altre informazioni, vedere Panoramica [dell'inizializzazione](overview-of-backup-initialization.md)del backup, Panoramica della fase di individuazione del [backup](overview-of-the-backup-discovery-phase.md)e Panoramica delle [attività di pre-backup.](overview-of-pre-backup-tasks.md)
3.  Il richiedente in *systemOne* modifica il contesto della copia shadow usato in genere per l'operazione di backup locale (**VSS \_ CTX \_ APP \_ BACKUP**) per indicare che verrà creata una copia shadow trasportabile (**VSS \_ VOLSNAP \_ ATTR \_ TRANSPORTABLE).** L'attributo trasportabile può essere aggiunto anche ad altri contesti di copia shadow.
4.  Con un contesto di copia shadow di **VSS \_ CTX \_ APP \_ BACKUP** VSS VOLSNAP ATTR TRANSPORTABLE, il richiedente che si trova in systemOne crea una copia shadow chiamando \| [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). **\_ \_ \_** 
5.  *SystemOne* usa [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) per salvare lo stato corrente del documento Componenti di backup e [**IVssExamineWriterMetadata::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) per salvare i documenti dei metadati del writer di ogni writer. Le stringhe XML che contengono questi documenti vengono quindi rese disponibili per un richiedente in esecuzione in *systemTwo*.

    Il richiedente trasferisce il documento Dei componenti di backup *a systemTwo.*

    Si noti che il richiedente in *systemOne* non rilascia l'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) a questo punto se lo scopo della copia shadow è il backup. L'interfaccia deve rimanere aperta fino a *quando systemTwo non* completa correttamente le operazioni di backup. Solo in questo caso il richiedente emettere un [**evento BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) perché alcuni writer troncano i log ed esereranno altre operazioni dopo un backup riuscito. Se l'obiettivo della copia shadow data mining o altri scopi, l'interfaccia può essere chiusa in questo passaggio.

6.  Il richiedente in *systemTwo* chiama [**quindi IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) per ottenere l'accesso alla copia shadow creata dal richiedente in *systemOne*.
    > [!Note]  
    > Il richiedente è responsabile della serializzazione dell'operazione di importazione della copia shadow. Inoltre, se la chiamata a [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) ha esito negativo, vss non pulirà i lun di propria proprietà. Il richiedente deve avviare la pulizia dei LUN.

     

7.  Il richiedente in *systemTwo* procede con il backup del materiale copiato shadow esattamente come se fosse il backup di una copia shadow creata da sola (vedere Panoramica del backup effettivo dei [file](overview-of-actual-backup-of-files.md)).

    Il richiedente in *systemTwo* ottiene l'oggetto dispositivo della copia shadow usando [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) nella copia shadow importata e lo aggiunge all'inizio dei percorsi di file originali ottenuti dai metadati per accedere ai file di cui eseguire il backup. [](vssgloss-d.md)

8.  Dopo aver utilizzato la copia shadow, il richiedente in *systemTwo* deve eliminare la copia shadow. Come per le copie shadow non trasportabili, se il contesto della copia shadow indica copie shadow di rilascio automatico (ad esempio, **VSS \_ CTX \_ BACKUP),** il rilascio di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) in *systemTwo* causerà l'eliminazione della copia shadow da parte del servizio VSS. In caso contrario, se il contesto indica una copia shadow permanente (ad **esempio, VSS \_ CTX \_ APP \_ ROLLBACK),** il richiedente in *systemTwo* deve eliminare in modo esplicito la copia shadow.

    Il richiedente in *systemTwo* segnala quindi al richiedente in *systemOne* che è stato completato il backup della copia shadow trasportabile.

9.  Dopo che il richiedente in *systemOne* ha ricevuto la notifica che il richiedente in *systemTwo* ha completato il backup della copia shadow trasportabile, invia una notifica ai writer nel sistema generando un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) con una chiamata a **IVssBackupComponents::BackupComplete**. A questo punto, il richiedente in *systemOne* è libero di rilasciare la propria istanza di [**IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

**Copie shadow trasportabili in un cluster:** Le copie shadow trasportabili devono essere importate dall'esterno del cluster, purché il volume originale sia montato all'interno del cluster. Per informazioni sull'implementazione di un ripristino rapido in un cluster, vedere Ripristino rapido [tramite volumi copiati shadow trasportabili](fast-recovery-using-transportable-shadow-copied-volumes.md).

 

 



