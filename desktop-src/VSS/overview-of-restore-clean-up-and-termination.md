---
description: In seguito a un ripristino, i writer controllano lo stato dell'operazione in modo che possano utilizzare i dati ripristinati e gestire gli errori.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Panoramica della pulizia e della chiusura del ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 391e029cdb109589b42240b5482f6aba2ff43555
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049848"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Panoramica della pulizia e della chiusura del ripristino

In seguito a un ripristino, i writer controllano lo stato dell'operazione in modo che possano utilizzare i dati ripristinati e gestire gli errori. Il richiedente deve attendere il completamento di questa attività. Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un ripristino in VSS](overview-of-processing-a-restore-under-vss.md).

Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari dopo che è stata eseguita un'operazione di ripristino.



| Azione del richiedente                                                                                                                                                                                                                                                                                                                                                              | Evento                                                           | Azione del writer                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il richiedente indica la fine del ripristino (vedere [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*PostRestore*](vssgloss-p.md) | Il writer esegue la pulizia post-ripristino e gestisce gli errori di ripristino e i file ripristinati in posizioni non standard (vedere [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| Il richiedente attende che i writer gestiscano l'evento [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) con [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync). Deve inoltre verificare lo stato del writer (vedere [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | nessuno                                                            | nessuno                                                                                                                                                                                                                                               |
| Il richiedente rilascia l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .                                                                                                                                                                                                                                                                                    | nessuno                                                            | nessuno                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Azioni del richiedente durante la pulizia e la terminazione

A questo punto, un richiedente indica la fine delle attività di ripristino del file generando un evento [*PostRestore*](vssgloss-p.md) chiamando [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Le azioni del richiedente sono limitate all'attesa dei writer, che potrebbe dover eseguire una pulizia finale e gestire gli errori di ripristino e rilasciare l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) dopo che tutti i writer hanno restituito la gestione dell'evento [*PostRestore*](vssgloss-p.md) .

## <a name="writer-actions-during-cleanup-and-termination"></a>Azioni del writer durante la pulizia e la terminazione

L'evento [*PostRestore*](vssgloss-p.md) viene gestito dal metodo virtuale [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). L'implementazione predefinita restituisce semplicemente **true** senza eseguire alcuna azione. Se un writer deve esercitare un maggiore controllo sulla situazione di post-ripristino, può eseguire l'override di questo metodo.

Oltre a qualsiasi pulizia normale, ad esempio la rimozione di file temporanei, che un writer può eseguire in [**CVssWriter:: OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), può gestire l'esito positivo o negativo delle operazioni di ripristino.

Il modo in cui gestisce gli errori di ripristino, i file ripristinati in un percorso alternativo e la necessità di ripristini futuri sono completamente a discrezione del writer. Le azioni tipiche possono includere il confronto di file in posizioni alternative o nuove con i file attualmente in uso, l'Unione di dati da più file o l'avvio di nuove sessioni connesse ai nuovi file di dati. VSS fornisce i meccanismi seguenti per supportare questa operazione in base a componenti:

-   L'esito positivo o negativo del ripristino di un componente può essere trovato con [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   L'uso di mapping di percorsi alternativi nel ripristino dei file verrà indicato da [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Per determinare se un ripristino è incrementale, è necessario eseguire ulteriori ripristini chiamando [**IVssComponent:: GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores). I writer che necessitano di un ripristino completo dei dati non devono essere riavviati finché il metodo non restituisce false.
-   I writer possono determinare se il richiedente deve ripristinare i file in un percorso precedentemente non specificato usando [**IVssComponent:: GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent:: GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

Per ulteriori informazioni sul ripristino dei file in percorsi non predefiniti, vedere [percorsi di backup e ripristino non predefiniti](non-default-backup-and-restore-locations.md).

Come per qualsiasi metodo [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , le informazioni restituite da una determinata istanza si applicano a tali componenti [*inclusi in modo esplicito*](vssgloss-e.md) per il backup e a tutti i sottocomponenti inclusi in modo [*implicito*](vssgloss-i.md) per il backup, inclusi quelli inclusi in modo esplicito per il ripristino da parte del richiedente tramite [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) . per informazioni dettagliate, vedere [utilizzo della selezione per il ripristino e i sottocomponenti](working-with-selectability-for-restore-and-subcomponents.md)

Poiché i writer dovranno accedere al documento dei componenti di backup, è importante che il richiedente non rilasci l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) fino a quando i writer non hanno terminato l'elaborazione.

 

 



