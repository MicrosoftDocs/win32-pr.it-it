---
description: "Gli eventi Abort possono essere generati durante un'operazione di backup nei casi seguenti:"
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Interruzione delle operazioni VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e4b82ba4227dfeb02e3da91c9bc1e77f10f492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313236"
---
# <a name="aborting-vss-operations"></a>Interruzione delle operazioni VSS

Gli eventi [*Abort*](vssgloss-a.md) possono essere generati durante un'operazione di backup nei casi seguenti:

-   Un richiedente genera in modo esplicito un [*evento Abort*](vssgloss-a.md) chiamando [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   I gestori eventi [*Freeze*](vssgloss-f.md) e [*scongela*](vssgloss-t.md) del writer ([**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) e [**CVssWriter:: onscongelate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) restituiscono **false** oppure non possono essere completati nell'intervallo di tempo specificato in [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize).
-   Si è verificato un errore del provider o VSS durante la creazione di una copia shadow dopo l'evento [*PrepareForSnapshot*](vssgloss-p.md) .

Le interruzioni non sono supportate per le operazioni di ripristino.

## <a name="requester-handling-and-creation-of-abort-events"></a>Gestione e creazione di eventi di interruzione del richiedente

Un'istanza dell'interfaccia [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) può essere utilizzata solo per un backup, pertanto se si verifica un errore durante l'elaborazione di un backup, è in genere consigliabile rilasciare l'istanza corrente e ricominciare.

Un richiedente deve segnalare in modo esplicito che sta interrompendo un'operazione di backup (usando [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) solo dopo la preparazione effettiva di un backup, che interessa i writer o che è stata eseguita la creazione di una copia shadow.

In realtà, ciò significa che ogni volta che un richiedente deve arrestare un'operazione di backup dopo la generazione di un evento [*PrepareForBackup*](vssgloss-p.md) chiamando [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), deve chiamare [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e attendere la restituzione prima di rilasciare l'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) corrente.

Se, ad esempio, un writer ha bloccato un'operazione di backup, un richiedente deve utilizzare [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) per notificare a tutti gli altri writer che l'operazione di backup non verrà completata.

Prima di chiamare [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)o se la chiamata a **PrepareForBackup** ha esito negativo, un richiedente può rilasciare l'istanza corrente dell'interfaccia [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) senza dover generare un evento Abort.

Se, ad esempio, l'istanza corrente di [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) viene utilizzata semplicemente per ottenere informazioni chiamando [**IVSSBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e generando un evento di [*Identificazione*](vssgloss-i.md) , una volta restituite le informazioni, l'istanza di **IVSSBackupComponents** può semplicemente essere rilasciata.

Un richiedente genera una serie di eventi ([*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*scongelate*](vssgloss-t.md)e [*postsnapshot*](vssgloss-p.md)) quando chiama [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Quando si gestiscono gli eventi di blocco e sblocco, un writer potrebbe non riuscire e generare un evento Abort autonomamente. La mancata gestione degli eventi PrepareForSnapshot e PostSnapshot non genera un evento Abort.

Non è sempre possibile che un richiedente sappia se è stato generato un evento Abort quando [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) indica un errore. Pertanto, un richiedente che deve terminare un'operazione di backup perché lo stato di **IVssBackupComponents::D osnapshotset** indica che un problema deve comunque chiamare [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Se un richiedente ha chiamato [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), non è necessario chiamare [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) prima di rilasciare un'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

## <a name="writer-handling-and-creation-of-abort-events"></a>Gestione e creazione di eventi di interruzione del writer

Come indicato in precedenza, un writer può ricevere un evento Abort da un richiedente oppure il provider può attivarne uno. Inoltre, un writer può ricevere più eventi Abort in determinate circostanze. Gli sviluppatori di Writer devono codificare qualsiasi implementazione di [**CVssWriter:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) tenendo presente questo aspetto.

Durante la gestione di un evento Abort, un writer deve tentare di ripristinare il processo gestito con lo stato di esecuzione normale, oltre a eseguire la gestione e la registrazione degli errori.

Questo può significare che un'implementazione di [**CVssWriter:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) potrebbe dover eseguire molte, se non tutte, le stesse attività del gestore eventi di disgelo ([**CVssWriter:: onscongelate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) e del gestore eventi PostSnapshot ([**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) e questi gestori possono essere chiamati dall'interno di **CVssWriter:: OnAbort**.

 

 



