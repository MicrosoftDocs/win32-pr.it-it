---
description: "Gli eventi di interruzione possono essere generati durante un'operazione di backup in uno dei casi seguenti:"
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Interruzione di operazioni vss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120ef8fb16c23d77a24526aad0fd62e56c1888a76dc2de884140094c6591cd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998271"
---
# <a name="aborting-vss-operations"></a>Interruzione di operazioni vss

[*Gli*](vssgloss-a.md) eventi di interruzione possono essere generati durante un'operazione di backup in uno dei casi seguenti:

-   Un richiedente genera in modo [*esplicito un evento Abort*](vssgloss-a.md) chiamando [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   I gestori eventi [*Freeze*](vssgloss-f.md) e [*Thaw*](vssgloss-t.md) di un writer ([**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) e [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) restituiscono **false** o non possono essere completati nell'intervallo di tempo specificato in [**CVssWriter::Initialize.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize)
-   Si è verificato un errore del provider o del Servizio Copia Shadow del volume durante la creazione di una copia shadow dopo [*l'evento PrepareForSnapshot.*](vssgloss-p.md)

Le interrompi non sono supportate per le operazioni di ripristino.

## <a name="requester-handling-and-creation-of-abort-events"></a>Gestione e creazione di eventi di interruzione da parte del richiedente

Un'istanza [**dell'interfaccia IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) può essere usata per un solo backup, pertanto se si verifica un errore durante l'elaborazione di un backup è in genere consigliabile rilasciare l'istanza corrente e ricominciare.

Un richiedente deve segnalare in modo esplicito che sta interrompendo un'operazione di backup (usando [**IVssBackupComponents::AbortBackup)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)solo dopo l'effettiva preparazione per un backup, che coinvolge writer o la creazione di una copia shadow.

Ciò significa che ogni volta che un richiedente deve arrestare un'operazione di backup dopo la generazione di un evento [*PrepareForBackup*](vssgloss-p.md) chiamando [**IVssBackupComponents::P repareForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)deve chiamare [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e attendere la restituzione prima di rilasciare l'istanza [**di IVSSBackupComponents corrente.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

Ad esempio, se un writer ha sospeso un'operazione di backup, un richiedente deve usare [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) per notificare a tutti gli altri writer che l'operazione di backup non verrà completata.

Prima di chiamare [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)o se la chiamata a **PrepareForBackup** non riesce, un richiedente può rilasciare l'istanza corrente dell'interfaccia [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) senza dover generare un evento Abort.

Ad esempio, se l'istanza corrente di [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) viene usata solo per ottenere informazioni chiamando [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e generando un evento [*Identify,*](vssgloss-i.md) una volta restituite le informazioni, l'istanza di **IVSSBackupComponents** può essere semplicemente rilasciata.

Un richiedente genera una serie di eventi ([*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*Thaw*](vssgloss-t.md)e [*PostSnapshot*](vssgloss-p.md)) quando chiama [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Durante la gestione degli eventi Freeze e Thaw, un writer può avere esito negativo e generare un evento Abort in modo proprio. La mancata gestione degli eventi PrepareForSnapshot e PostSnapshot non genera un evento Abort.

Non è sempre possibile che un richiedente sappia se è stato generato un evento Abort quando [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) indica un errore. Pertanto, un richiedente che deve terminare un'operazione di backup perché lo stato di **IVssBackupComponents::D oSnapshotSet** indica che un problema deve comunque chiamare [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Se un richiedente ha chiamato [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), non è necessario chiamare [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) prima di rilasciare un'istanza di [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

## <a name="writer-handling-and-creation-of-abort-events"></a>Gestione del writer e creazione di eventi di interruzione

Come indicato in precedenza, un writer può ricevere un evento Abort da un richiedente oppure il provider può attivarne uno. Inoltre, un writer può ricevere più eventi Abort in determinate circostanze. Gli sviluppatori di writer devono scrivere codice per qualsiasi implementazione di [**CVssWriter::OnAbort.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort)

Nella gestione di un evento Abort, un writer deve tentare di ripristinare qualsiasi processo gestito allo stato di esecuzione normale, nonché di eseguire la gestione e la registrazione degli errori.

Questo può significare che un'implementazione di [**CVssWriter::OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) potrebbe dover eseguire molte, se non tutte, delle stesse attività del gestore eventi Thaw ([**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) e del gestore eventi PostSnapshot ([**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) e questi gestori possono essere chiamati dall'interno di **CVssWriter::OnAbort**.

 

 



