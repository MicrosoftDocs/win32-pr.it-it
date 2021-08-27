---
description: I richiedenti hanno la responsabilità principale del ciclo di vita di un documento dei componenti di backup.
ms.assetid: 287b7b9a-ac04-4a74-83c1-2cdd4a571ac1
title: Ciclo di vita dei documenti dei componenti di backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4804625f979e0d5621d96a2230c1419354d0dbeb4c368312dbd3943e0ac0c4bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124531"
---
# <a name="backup-components-document-life-cycle"></a>Ciclo di vita dei documenti dei componenti di backup

I richiedenti hanno la responsabilità principale del ciclo di vita di un documento dei componenti di backup.

Questo controllo viene esercitato da un'istanza dell'oggetto [**interfaccia IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) restituito da [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents).

Un richiedente deve inizializzare un documento dei componenti di backup prima di un backup o di un ripristino chiamando [**IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) o [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore). Il richiedente può inizializzare il documento come vuoto oppure caricare una copia archiviata in precedenza del documento.

Per le operazioni di backup, un documento dei componenti di backup viene in genere inizializzato come vuoto. I dati verranno compilati con la collaborazione dei writer del sistema nel corso dell'elaborazione del backup.

Per le operazioni di ripristino, un documento dei componenti di backup viene in genere inizializzato da un documento archiviato generato durante il backup iniziale. In questo modo il ripristino (in combinazione con l'esame dei documenti dei metadati del writer archiviati) consente di determinare i dati di cui è stato eseguito inizialmente il backup e la modalità di ripristino.

Il backup di [*copie shadow trasportabili*](vssgloss-t.md) è un'eccezione a questa regola. In questo caso, una copia shadow potrebbe essere stata spostata da un sistema (in cui è stata creata insieme al documento dei componenti di backup iniziale) a un altro tramite la riassegnazione dell'unità logica di un dispositivo di archiviazione condiviso. Per eseguire il backup in queste circostanze, un richiedente carica lo stato di backup archiviato e procede da dove il sistema iniziale è stato lasciato. Per altre informazioni, vedere [Importazione di volumi copiati shadow trasportabili.](importing-transportable-shadow-copied-volumes.md)

Nel corso dell'elaborazione di un backup, il richiedente decide quali componenti copiare effettivamente in base ai [](vssgloss-l.md)componenti contrassegnati come selezionabili per [*il backup,*](vssgloss-s.md)i percorsi logici del componente e la propria logica interna.

Alcuni componenti verranno inclusi in modo [*esplicito nell'operazione*](vssgloss-e.md) di backup. Le informazioni sul componente verranno aggiunte al documento Componenti di backup. Altri verranno [*inclusi in modo implicito*](vssgloss-i.md) nel backup. Le informazioni sui componenti aggiunti non verranno aggiunte al documento Componenti di backup.

Tutti i componenti non selezionabili di un writer per i componenti di backup senza un predecessore selezionabile nel percorso logico e quelli selezionabili per i componenti di backup selezionati dal richiedente verranno aggiunti in modo esplicito.

I componenti non selezionabili e selezionabili per i componenti di backup possono essere aggiunti in modo implicito se hanno un predecessore selezionabile nel percorso logico, incluso in modo esplicito nel backup. Questi componenti ([*sottocomponenti*](vssgloss-s.md)) sono membri di [*set di componenti*](vssgloss-s.md) definiti dal predecessore selezionabile.

Quando si gestisce le operazioni [](vssgloss-s.md) di ripristino, il richiedente usa la selezionabilità per il ripristino anziché la selezionabilità per il backup insieme alle informazioni sul percorso logico e alla propria logica interna per decidere quali file ripristinare.

Se un componente aggiunto in modo implicito al backup deve ora essere aggiunto in modo esplicito al ripristino, il richiedente aggiornerà il documento dei componenti di backup con le informazioni del componente.

Le informazioni sui componenti archiviati sono disponibili sia per i richiedenti che per i writer tramite istanze [**dell'interfaccia IVssComponent.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent)

È tramite [**le interfacce IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) che i writer possono eseguire query e (fino alla fine degli eventi [**PostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) e [**PostRestore)**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) modificare le informazioni nel documento Componenti di backup.

Quando vengono chiamati [**CVssWriter::OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup), [**CVssWriter::OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore), [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot), [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete)o [**CVssWriter::OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore) , un writer riceve un'istanza di [**un'interfaccia IVssWriterComponents.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents)

Si noti che al momento della generazione dell'evento [**BackupComplete,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) il documento dei componenti di backup viene reso di sola lettura e pertanto [**CVssWriter::OnBackupComplete**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupcomplete) non può usare l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per modificarlo.

[**Dall'interfaccia IVSSWriterComponents,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswritercomponents) il writer può recuperare istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) che gli consentiranno di accedere a tutti i componenti aggiunti in modo esplicito al documento Componenti di backup e di modificarne lo stato. Per altre informazioni, vedere [Panoramica dell'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md) e [Panoramica dell'elaborazione di un ripristino in VSS.](overview-of-processing-a-restore-under-vss.md)

I documenti dei componenti di backup vengono rimossi dalla memoria quando viene rilasciata l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) e devono essere archiviati usando [**IVssBackupComponents::SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml)oppure tutte le informazioni andranno perse.

Inoltre, quando un [**documento IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) viene rilasciato correttamente, viene generato un evento [**BackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown) e vengono eliminate [*le copie shadow*](vssgloss-a.md) con rilascio automatico.

 

 



