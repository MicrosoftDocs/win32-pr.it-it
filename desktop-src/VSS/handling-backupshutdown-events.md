---
description: È possibile che un'applicazione di backup (richiedente) termini e non generi un evento BackupComplete.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Gestione degli eventi BackupShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939e8e64ca9ee463b0b8331e607f8068c3325d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310710"
---
# <a name="handling-backupshutdown-events"></a>Gestione degli eventi BackupShutdown

È possibile che un'applicazione di backup (richiedente) termini e non generi un evento [*BackupComplete*](vssgloss-b.md) . L'applicazione di backup potrebbe arrestarsi in modo anomalo o essere terminata (ad esempio dal gestore attività) e non essere in grado di chiamare [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Pertanto, l'infrastruttura VSS (anziché il richiedente) genera un evento [*BackupShutdown*](vssgloss-b.md) ogni volta che viene rilasciata un'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) che partecipa a un backup, indipendentemente dal fatto che venga rilasciata dal richiedente o dal sistema.

Se un backup procede correttamente, un writer riceverà un evento BackupComplete seguito da un evento BackupShutdown.

Se l'operazione viene interrotta (il richiedente genera un [*evento Abort*](vssgloss-a.md) chiamando [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) o ha esito negativo improvvisamente, un writer può ricevere solo un evento BackupShutdown e potrebbe non ricevere altri eventi che eseguono operazioni di pulizia. Spetta a un writer determinare se un evento BackupShutdown segue una sequenza di eventi corretta o rappresenta un errore imprevisto delle operazioni di backup.

Il gestore eventi BackupShutdown, [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), riceve l' \_ ID VSS (Guid) del set di copie shadow dell'operazione di backup che viene arrestata. Il writer può utilizzare questo oggetto per determinare quale operazione di backup verrà arrestata, se l'ID del set di copie shadow è stato archiviato durante la relativa sequenza di backup (ad esempio, dall'interno di [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), [**CVssWriter:: onscongelate**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)o [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) tramite [**CVssWriter:: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid).

Un writer, tuttavia, non deve chiamare [**CVssWriter:: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) dall'interno di [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown). Inoltre, **CVssWriter:: GetCurrentSnapshotSetId** non può essere chiamato dopo la restituzione di [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) .

È possibile che il writer sia coinvolto in più operazioni di backup e, se viene chiamato un evento BackupShutdown a causa di un arresto improvviso di un richiedente, l' \_ ID VSS restituito potrebbe essere quello di un'altra operazione di backup a cui il writer parteciperà.

 

 



