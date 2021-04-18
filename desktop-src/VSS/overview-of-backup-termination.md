---
description: Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per la terminazione di un'operazione di backup. Per ulteriori informazioni, vedere Cenni preliminari sull'elaborazione di un backup in VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Panoramica della terminazione del backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9268bd8fd4ec51be2ee7a891d4dffb3a5cb1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310690"
---
# <a name="overview-of-backup-termination"></a>Panoramica della terminazione del backup

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per la terminazione di un'operazione di backup. Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md).



| Azione del richiedente                                                                                                                                                                                                              | Evento                                                                 | Azione del writer                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il richiedente termina la copia shadow rilasciando l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o chiamando [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | nessuno                                                                  | nessuno                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) viene rilasciata chiamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | Il writer gestisce l'evento con [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), che consente di eseguire la pulizia di qualsiasi stato correlato al set di copie shadow. Se l'operazione di backup non è riuscita, ovvero non ha generato un evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , il writer potrebbe anche dover eseguire la gestione degli errori. Per ulteriori informazioni, vedere [gestione degli eventi BackupShutdown](handling-backupshutdown-events.md) . |



 

Poiché un'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) non può essere riutilizzata e il distruttore dell'interfaccia termina le copie shadow, non esiste in genere un motivo per chiamare [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). Questo metodo è progettato per essere utilizzato insieme alla gestione degli errori e all'interruzione dei backup (vedere [interruzione di operazioni VSS](aborting-vss-operations.md)).

 

 
