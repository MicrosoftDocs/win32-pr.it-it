---
description: Dopo aver eseguito le azioni descritte in Panoramica dell'inizializzazione del ripristino e della panoramica della preparazione per il ripristino, il richiedente ha informazioni sufficienti per iniziare a ripristinare i file.
ms.assetid: 15df39fa-1eb1-4e96-9e26-14470f391de4
title: Panoramica del ripristino dei file effettivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6527a10d0880b1e599377abb797449816019ab89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310692"
---
# <a name="overview-of-actual-file-restoration"></a>Panoramica del ripristino dei file effettivi

Dopo aver eseguito le azioni descritte in [Panoramica dell'inizializzazione del ripristino](overview-of-restore-initialization.md) e [della panoramica della preparazione per il ripristino](overview-of-preparing-for-restore.md), il richiedente ha informazioni sufficienti per iniziare a ripristinare i file. Il ripristino dei file non implica interazioni del writer o la generazione di eventi. Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md).

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per ripristinare i file.



| Azione del richiedente                                                                                                                                                                                                                                                                                                          | Evento | Azione del writer |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|---------------|
| Genera un elenco di set di ripristino per i file nei supporti di backup.                                                                                                                                                                                                                                                                 | nessuno  | nessuno          |
| Gestire le [*destinazioni dirette*](vssgloss-d.md) o il ripristino [*parziale di file*](vssgloss-p.md) (vedere [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget), [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile)). | nessuno  | nessuno          |
| Se necessario, ignorare tutti i percorsi di ripristino specificati e ripristinare un nuovo percorso specificato in una precedente chiamata a [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).                                                                                                                       | nessuno  | nessuno          |
| Se il ripristino è incrementale e sono necessari ulteriori ripristini, indicare (vedere [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores) e [backup incrementali e differenziali](incremental-and-differential-backups.md)).                                                     | nessuno  | nessuno          |
| Per sapere se un writer ha modificato il contenuto del documento dei componenti di backup, chiamare [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents). Ad esempio, il writer potrebbe aver modificato la destinazione di ripristino.                                                                 | nessuno  | nessuno          |



 

## <a name="requester-actions-during-restoring-files"></a>Azioni del richiedente durante il ripristino dei file

Per la maggior parte dei file nel supporto di backup, il richiedente deve determinare i percorsi originali e le nuove posizioni o i mapping del percorso alternativo che vi si applicano. (Vedere [generazione di un set di ripristino](generating-a-restore-set.md) per una descrizione delle procedure consigliate per determinare quali file ripristinare e dove ripristinarli.)

Inoltre, alcuni file potrebbero avere [*destinazioni dirette*](vssgloss-d.md) o supportare il ripristino di [*file parziali*](vssgloss-p.md) . Il numero di tali file può essere trovato chiamando [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) e [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount)e le informazioni sulle istruzioni di ripristino dettagliate sono reperibili chiamando [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) e [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). I file parziali e diretti possono far parte di componenti aggiunti in modo implicito o esplicito al backup originale. per ulteriori informazioni, vedere [utilizzo della selezione per il ripristino e i sottocomponenti](working-with-selectability-for-restore-and-subcomponents.md) .

L'esito positivo o negativo di un ripristino è indicato in base a un componente, usando [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus). La necessità di ulteriori operazioni di ripristino (in caso di ripristini incrementali o differenziali) viene anche indicata in base a un componente, usando [**IVssBackupComponents:: SetAdditionalRestores**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setadditionalrestores).

In generale, il servizio Copia Shadow del volume non specifica un meccanismo per il recupero di dati da un supporto di archiviazione, una scelta di supporto di archiviazione o come determinare i file da ripristinare laddove.

Tuttavia, per determinati writer, il ripristino dei file può comportare l'utilizzo di un'interfaccia e una procedura personalizzate documentate. I writer di sistema Windows, che attualmente richiedono tale supporto, sono documentati in [casi di utilizzo VSS speciali](special-vss-usage-cases.md).

In generale, è consigliabile che i file di ogni componente di ogni [*istanza di writer*](vssgloss-w.md) vengano elaborati come unità. A questo scopo è necessario:

-   Associazione di ogni file da ripristinare con il componente che lo ha gestito. Questa operazione richiede l'utilizzo di documenti di metadati del writer.
-   Recupero delle informazioni corrette sulla destinazione di ripristino. Questa operazione richiede informazioni dal documento componenti di backup.

 

 



