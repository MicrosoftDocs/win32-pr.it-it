---
description: Dopo un ripristino, i writer controllano lo stato dell'operazione in modo che possano usare i dati ripristinati e gestire gli errori.
ms.assetid: f9def67a-c4ea-4014-929f-51fbd10d770a
title: Panoramica della pulizia e della terminazione del ripristino
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8ad0b7d40f3c0e5322810f96bb120f28effe4ec3f0d4e278af924962713b2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122033"
---
# <a name="overview-of-restore-clean-up-and-termination"></a>Panoramica della pulizia e della terminazione del ripristino

Dopo un ripristino, i writer controllano lo stato dell'operazione in modo che possano usare i dati ripristinati e gestire gli errori. Il richiedente deve attendere il completamento di questa attività. Per altre informazioni, vedere [Panoramica dell'elaborazione di un ripristino in VSS.](overview-of-processing-a-restore-under-vss.md)

La tabella seguente illustra la sequenza di azioni ed eventi necessari dopo l'esecuzione di un'operazione di ripristino.



| Azione richiedente                                                                                                                                                                                                                                                                                                                                                              | Event                                                           | Azione writer                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il richiedente indica la fine del ripristino (vedere [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)).                                                                                                                                                                                                                                           | [*PostRestore*](vssgloss-p.md) | Il writer esegue la pulizia post-ripristino e gestisce gli errori di ripristino e i file ripristinati in percorsi non standard (vedere [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore), [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)). |
| Il richiedente attende i writer per gestire [**l'evento PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) con [**IVssAsync.**](/windows/desktop/api/Vss/nn-vss-ivssasync) Deve anche verificare lo stato del writer (vedere [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus)). | Nessuno                                                            | Nessuno                                                                                                                                                                                                                                               |
| Il richiedente rilascia [**l'interfaccia IVssBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)                                                                                                                                                                                                                                                                                    | Nessuno                                                            | Nessuno                                                                                                                                                                                                                                               |



 

## <a name="requester-actions-during-cleanup-and-termination"></a>Azioni del richiedente durante la pulizia e la chiusura

A questo punto, un richiedente indica la fine delle attività di ripristino dei file generando un evento [*PostRestore*](vssgloss-p.md) chiamando [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Le azioni del richiedente sono limitate all'attesa sui writer, che potrebbe dover eseguire alcune operazioni di pulizia finale e gestire gli errori di ripristino, e al rilascio dell'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) dopo che tutti i writer sono tornati dalla gestione [*dell'evento PostRestore.*](vssgloss-p.md)

## <a name="writer-actions-during-cleanup-and-termination"></a>Azioni writer durante la pulizia e la terminazione

[*L'evento PostRestore*](vssgloss-p.md) viene gestito dal metodo virtuale [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore). L'implementazione predefinita restituisce **semplicemente true** senza eseguire alcuna azione. Se un writer deve esercitare un maggiore controllo sulla situazione post-ripristino, può eseguire l'override di questo metodo.

Oltre a qualsiasi pulizia normale ,ad esempio la rimozione di file temporanei, che un writer potrebbe eseguire in [**CVssWriter::OnPostRestore,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)può gestire l'esito positivo o negativo delle operazioni di ripristino.

Il modo in cui gestisce gli errori di ripristino, i file ripristinati in un percorso alternativo e la necessità di ripristini futuri sono completamente a discrezione del writer. Le azioni tipiche possono includere il confronto di file in percorsi alternativi o nuovi con i file attualmente in uso, l'unione di dati da più file o l'avvio di nuove sessioni connesse ai nuovi file di dati. VSS offre i meccanismi seguenti per supportare questa funzionalità in base al componente:

-   L'esito positivo o negativo del ripristino di qualsiasi componente è disponibile con [**IVssComponent::GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus).
-   L'uso di mapping di percorsi alternativi nel ripristino dei file verrà indicato da [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).
-   Per determinare se un ripristino è incrementale e richiederà ulteriori ripristini, chiamare [**IVssComponent::GetAdditionalRestores**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getadditionalrestores). I writer che necessitano di un ripristino completo dei dati non devono essere riavviati fino a quando questo metodo non restituisce false.
-   I writer possono determinare se il richiedente ha bisogno di ripristinare i file in un percorso non specificato in precedenza usando [**IVssComponent::GetNewTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtargetcount) e [**IVssComponent::GetNewTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)

Per altre informazioni sul ripristino dei file in percorsi non predefiniti, vedere Percorsi di [backup e ripristino non predefiniti.](non-default-backup-and-restore-locations.md)

Come per qualsiasi [](working-with-selectability-for-restore-and-subcomponents.md) metodo [**IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) le informazioni restituite [](vssgloss-e.md) da una determinata istanza [](vssgloss-i.md) si applicano ai componenti inclusi in modo esplicito per il backup e a qualsiasi componente implicitamente incluso per i sottocomponenti di backup, inclusi i sottocomponenti inclusi in modo esplicito per il ripristino dal richiedente [**usando IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) (Uso della selezionabilità per il ripristino e dei sottocomponenti per informazioni dettagliate).

Poiché i writer richiederanno l'accesso al documento Componenti di backup, è importante che il richiedente non rilasci [**l'interfaccia IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) fino al termine dell'elaborazione dei writer.

 

 



