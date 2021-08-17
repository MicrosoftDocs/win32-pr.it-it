---
description: Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per terminare un'operazione di backup. Per altre informazioni, vedere Panoramica dell'elaborazione di un backup in VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Panoramica della terminazione del backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fd57822a62cf3fa39cee2b17d79ae2545afa07bd722d26cacda68cba3b6695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937969"
---
# <a name="overview-of-backup-termination"></a>Panoramica della terminazione del backup

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per terminare un'operazione di backup. Per altre informazioni, vedere [Panoramica dell'elaborazione di un backup in VSS.](overview-of-processing-a-backup-under-vss.md)



| Azione richiedente                                                                                                                                                                                                              | Evento                                                                 | Azione writer                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il richiedente termina la copia shadow rilasciando [**l'interfaccia IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o chiamando [**IVssBackupComponents::D eleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | Nessuno                                                                  | Nessuno                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) viene rilasciato chiamando [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | Il writer gestisce l'evento [**con CVssWriter::OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), che consente di pulire qualsiasi stato correlato al set di copie shadow. Se l'operazione di backup non è riuscita, ovvero non ha generato un evento [**BackupComplete,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) il writer potrebbe anche eseguire la gestione degli errori. Per [altre informazioni, vedere Gestione degli eventi BackupShutdown.](handling-backupshutdown-events.md) |



 

Poiché non è possibile riutilizzare un'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e il distruttore dell'interfaccia termina le copie shadow, in genere non è necessario chiamare [**IVssBackupComponents::D eleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). Questo metodo è progettato per essere usato in combinazione con la gestione degli errori e l'interruzione dei backup (vedere [Interruzione delle operazioni vss](aborting-vss-operations.md)).

 

 
