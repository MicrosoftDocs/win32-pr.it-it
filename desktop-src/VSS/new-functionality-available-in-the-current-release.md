---
description: 'La Windows Server 2003 del Servizio Copia Shadow del volume contiene le nuove funzionalità seguenti:'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Nuove funzionalità disponibili in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bc444a062fd2e1dae33af80feb88e1da52452064d8ed38c2db6fd5f7f3ae2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591392"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Nuove funzionalità disponibili in Windows Server 2003

La Windows Server 2003 del Servizio Copia Shadow del volume contiene le nuove funzionalità seguenti:

-   Supporto per [*la selezionabilità per il*](vssgloss-s.md) ripristino oltre a e su base uguale con la selezionabilità per il [*backup*](vssgloss-s.md) (in precedenza definita semplicemente selezionabilità). Per [altre informazioni, vedere Uso della selezionabilità e dei](working-with-selectability-and-logical-paths.md) percorsi logici.
-   Introduzione di un [*evento BackupShutdown*](vssgloss-b.md) che indica che un'applicazione di backup conforme a VSS (richiedente) è stata arrestata, indipendentemente dal fatto che il tentativo di backup sia stato completato correttamente o meno. Per [altre informazioni, vedere Gestione degli eventi BackupShutdown.](handling-backupshutdown-events.md)
-   Supporto per dipendenze esplicite del componente writer. Mezzo per descrivere e supportare le situazioni in cui un componente (e il set di componenti definito) gestito da un writer non può essere sottoposto a backup o ripristino indipendentemente dai componenti gestiti da altri writer. Per [altre informazioni, vedere Dipendenze tra componenti gestiti](dependencies-between-components-managed-by-different-writers.md) da writer diversi.
-   Supporto completo per [*le operazioni sui file*](vssgloss-p.md) parziali. Il backup e il ripristino di segmenti di file da parte di writer e richiedenti è ora completamente supportato. Per altre informazioni sulle operazioni sui file [parziali,](working-with-partial-files.md) vedere Uso di file parziali.
-   Introduzione dei [*file con differenze per*](vssgloss-d.md) supportare le operazioni di backup e ripristino incrementali. Per [altre informazioni, vedere Backup incrementali](incremental-and-differential-backups.md) e differenziali.
-   Introduzione degli schemi di backup come concetto che indica il livello di supporto del writer per i tipi di operazioni di backup. Per altre [**informazioni, vedere VSS \_ BACKUP \_ SCHEMA.**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema)
-   Supporto per la specifica del richiedente di nuove destinazioni di ripristino file ([*nuovi percorsi di destinazione*](vssgloss-n.md)) durante le operazioni di ripristino. Per [altre informazioni, vedere Uso di nuove destinazioni](working-with-new-targets-during-restore.md) durante il ripristino.
-   Supporto per il ripristino condizionale in fase di riavvio. Per altre informazioni, vedere VSS \_ RME \_ RESTORE AT REBOOT IF CANNOT REPLACE ( \_ \_ \_ \_ \_ [**VSE \_ RESTOREMETHOD \_ ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)).
-   Definizione di uno stato di ripristino e di un tipo di ripristino. Per [**altre informazioni, vedere VSS \_ RESTORE \_ TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) e [VSS Restore State](vss-restore-state.md) .
-   Supporto per le query writer sullo stato della copia shadow. Per altre informazioni, vedere [**CVssWriter::GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) e [**CVssWriter::GetSnapshotDeviceName.**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   Supporto per copie shadow trasportabili in Windows Server 2003, edizione Enterprise e Windows Server 2003, Datacenter Edition. Per altre informazioni, vedere [Importazione di volumi copiati shadow trasportabili](importing-transportable-shadow-copied-volumes.md).

 

 



