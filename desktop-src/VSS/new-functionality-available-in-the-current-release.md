---
description: 'La versione di Windows Server 2003 della Servizio Copia Shadow del volume contiene le seguenti nuove funzionalità:'
ms.assetid: 3dcfcc01-3e3c-43e9-a933-5c72f331da9a
title: Nuove funzionalità disponibili in Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5782ef6b24f208f69e50cdb992e12ba3212c47f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131275"
---
# <a name="new-functionality-available-in-windows-server-2003"></a>Nuove funzionalità disponibili in Windows Server 2003

La versione di Windows Server 2003 della Servizio Copia Shadow del volume contiene le seguenti nuove funzionalità:

-   Supporto per la [*selezione per il ripristino*](vssgloss-s.md) , oltre a e su base uguale con la [*selezione per il backup*](vssgloss-s.md) (in precedenza appena definita selezione). Per ulteriori informazioni, vedere [utilizzo della selezione e dei percorsi logici](working-with-selectability-and-logical-paths.md) .
-   Introduzione di un evento [*BackupShutdown*](vssgloss-b.md) che indica che un'applicazione di backup compatibile con VSS (richiedente) è stata arrestata, se il tentativo di backup è stato completato correttamente o meno. Per ulteriori informazioni, vedere [gestione degli eventi BackupShutdown](handling-backupshutdown-events.md) .
-   Supporto per le dipendenze del componente writer esplicito. Un modo per descrivere e supportare le situazioni in cui un componente (e il set di componenti che definisce) gestito da un writer non può essere eseguito il backup o il ripristino indipendentemente dai componenti gestiti da altri writer. Per ulteriori informazioni, vedere [dipendenze tra i componenti gestiti da diversi writer](dependencies-between-components-managed-by-different-writers.md) .
-   Supporto completo per le operazioni di [*file parziali*](vssgloss-p.md) . Il backup e il ripristino di segmenti di file in base a writer e richiedenti sono ora completamente supportati. Per ulteriori informazioni sulle operazioni di file parziali, vedere [utilizzo dei file parziali](working-with-partial-files.md) .
-   Introduzione di [*file differenziati*](vssgloss-d.md) per supportare operazioni di backup e ripristino incrementali. Per ulteriori informazioni, vedere [backup incrementali e differenziali](incremental-and-differential-backups.md) .
-   Introduzione degli schemi di backup come concetto che indica il livello di supporto del writer per i tipi di operazioni di backup. Per ulteriori informazioni, vedere [**\_ \_ schema di backup VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) .
-   Supporto per la specifica del richiedente di nuove destinazioni di ripristino di file ([*nuovi percorsi di destinazione*](vssgloss-n.md)) durante le operazioni di ripristino. Per ulteriori informazioni, vedere [utilizzo di nuove destinazioni durante il ripristino](working-with-new-targets-during-restore.md) .
-   Supporto per il ripristino condizionale al momento del riavvio. \_ \_ \_ Per ulteriori informazioni, vedere il ripristino di VSS RME al \_ riavvio \_ se \_ non è in grado \_ di sostituire ([**VSE \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)).
-   Definizione di uno stato di ripristino e di un tipo di ripristino. Per ulteriori informazioni, vedere [**\_ \_ tipo di ripristino VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) e [Stato ripristino VSS](vss-restore-state.md) .
-   Supporto per le query del writer sullo stato della copia shadow. Per ulteriori informazioni, vedere [**CVssWriter:: GetContext**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcontext) e [**CVssWriter:: GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename) .
-   Supporto per le copie shadow trasportabili in Windows Server 2003, Enterprise Edition e Windows Server 2003, Datacenter Edition. Per ulteriori informazioni, vedere [importazione di volumi di copie shadow trasportabili](importing-transportable-shadow-copied-volumes.md).

 

 



