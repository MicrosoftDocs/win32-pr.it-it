---
description: È possibile che un'applicazione di backup (richiedente) termini e non generi un evento BackupComplete.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Gestione degli eventi BackupShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e60a063a11f0a492407daed31ace4a62aec2a13fe824e110de272d58b84bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998251"
---
# <a name="handling-backupshutdown-events"></a>Gestione degli eventi BackupShutdown

È possibile che un'applicazione di backup (richiedente) termini e non generi un [*evento BackupComplete.*](vssgloss-b.md) L'applicazione di backup potrebbe bloccarsi o essere terminata (ad esempio dal Gestione attività) e non essere in grado di chiamare [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Pertanto, l'infrastruttura vss (anziché il richiedente) genera un evento [*BackupShutdown*](vssgloss-b.md) ogni volta che viene rilasciata un'istanza di [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) che partecipa a un backup, indipendentemente dal fatto che sia rilasciata dal richiedente o dal sistema.

Se un backup continua correttamente, un writer riceverà un evento BackupComplete seguito da un evento BackupShutdown.

Se l'operazione viene interrotta (il richiedente genera un evento [*Abort*](vssgloss-a.md) chiamando [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) o ha esito negativo improvvisamente, un writer può ricevere solo un evento BackupShutdown e potrebbe non ricevere altri eventi che eseguono operazioni di pulizia. Il writer deve determinare se un evento BackupShutdown segue una sequenza corretta di eventi o rappresenta un errore imprevisto delle operazioni di backup.

Il gestore dell'evento BackupShutdown, [**CVssWriter::OnBackupShutdown,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)riceve l'ID VSS (GUID) del set di copie shadow dell'operazione di backup da \_ arrestare. Il writer può usarlo per determinare quale operazione di backup viene arrestata, se ha archiviato l'ID del set di copie shadow durante la sequenza di backup (ad esempio, dall'interno di [**CVssWriter::OnFreeze,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)o [**CVssWriter::OnPostSnapshot)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)usando [**CVssWriter::GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid).

Tuttavia, un writer non deve chiamare [**CVssWriter::GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) dall'interno [**di CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown). Non è **inoltre possibile chiamare CVssWriter::GetCurrentSnapshotSetId** dopo il ritorno [**di CVssWriter::OnPostSnapshot.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

È possibile che il writer sia coinvolto in più operazioni di backup e se viene chiamato un evento BackupShutdown a causa di un arresto improvviso di un richiedente, l'ID VSS restituito potrebbe essere quello di un'altra operazione di backup a cui il writer stava \_ partecipando.

 

 



