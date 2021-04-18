---
description: "Dopo la chiamata a IVssBackupComponents:: GatherWriterMetadata, un richiedente usa l'istanza dell'interfaccia IVssAsync restituita da questa chiamata per determinare quando tutti i writer del sistema hanno terminato la costruzione dei documenti di metadati del writer."
ms.assetid: 04658d50-04f0-4189-8b88-ff152f1bf482
title: Panoramica della fase di individuazione del backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d2a2d05220ecf3e25c77c18cc62b07726964f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310683"
---
# <a name="overview-of-the-backup-discovery-phase"></a>Panoramica della fase di individuazione del backup

Dopo la chiamata a [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), un richiedente usa l'istanza dell'interfaccia [**IVssAsync**](/windows/desktop/api/Vss/nn-vss-ivssasync) restituita da questa chiamata per determinare quando tutti i writer del sistema hanno terminato la costruzione dei documenti di metadati del writer. Per ulteriori informazioni, vedere [Cenni preliminari sull'elaborazione di un backup in VSS](overview-of-processing-a-backup-under-vss.md).

A questo punto, il richiedente può iniziare una fase di individuazione, esaminando i metadati per determinare quali applicazioni sono in esecuzione e quali volumi devono essere copiati come copie shadow per ottenere un backup completo. Nella tabella seguente viene illustrata la sequenza di azioni ed eventi necessari per la fase di individuazione del backup.



| Azione del richiedente                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Evento | Azione del writer                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|-----------------------------------------------------------------------------------|
| Recuperare i documenti dei metadati del writer (vedere [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata), [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)).                                                                                                                                                                                                                                                                                                                                                 | nessuno  | Durante questo periodo, è possibile che i writer continuino con le normali operazioni. |
| Usare l'elenco dei componenti e i relativi [*set di file*](vssgloss-f.md), nonché i file esclusi, per ottenere un elenco di volumi e file inclusi nel backup (vedere [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)).                                                                                                                                                                                                                                                                      | nessuno  | nessuno                                                                              |
| Scegliere i componenti nel documento di metadati del writer del writer di cui eseguire il backup. Chiamare [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per ogni componente per aggiungerlo al documento componenti di backup. (Vedere [utilizzo della selezione per il backup](working-with-selectability-for-backup.md) e [utilizzo del documento componenti di backup](working-with-the-backup-components-document.md)).                                                                                                                      | nessuno  | nessuno                                                                              |
| Inizializzare il set di copie shadow, il contesto e verificare la presenza di volumi supportati (vedere [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset), [**IVssBackupComponents:: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported)).                                                                                                                                                                                                                                                                                   | nessuno  | nessuno                                                                              |
| Se si esegue un backup non componente, aggiungere i volumi di destinazione desiderati dal documento di metadati del writer al set di copie shadow chiamando [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) per ogni volume. In caso contrario, per i componenti nel documento di metadati del writer che sono già stati aggiunti al documento dei componenti di backup (chiamando [**addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), il richiedente deve anche chiamare **IVssBackupComponents:: AddToSnapshotSet** per ogni volume interessato. | nessuno  | nessuno                                                                              |



 

## <a name="writer-actions-during-the-discovery-phase"></a>Azioni del writer durante la fase di individuazione

Poiché la fase di individuazione di un backup è costituita principalmente da un richiedente che elabora le informazioni recuperate dai documenti dei metadati del writer, esistono pochi requisiti per un writer.

In teoria, un writer potrebbe continuare a funzionare normalmente a questo punto. Tuttavia, potrebbe essere auspicabile che i writer comincino a prepararsi per le operazioni di copia shadow e backup in arrivo.

## <a name="requester-actions-during-the-discovery-phase"></a>Azioni del richiedente durante la fase di individuazione

Un richiedente usa gli oggetti [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) ottenuti tramite [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) per eseguire l'iterazione su tutti i metadati dei writer e selezionare i writer i cui dati intende eseguire il backup.

A questo punto, il richiedente dovrà generare un elenco iniziale dei candidati di backup di ogni writer eseguendo l'iterazione sui componenti del writer usando [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent). In questo modo viene fornito il richiedente con oggetti [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) , da cui è possibile ottenere le specifiche per i file di cui eseguire il backup mediante [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile), [**IVssWMComponent:: GetDatabaseFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabasefile)e [**IVssWMComponent:: GetDatabaseLogFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdatabaselogfile).

Poiché l'oggetto [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) può usare caratteri jolly per contenere informazioni sul percorso del file, potrebbe essere necessario usare funzioni quali [**FindFirstFile**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/win32/api/fileapi/nf-fileapi-findfirstfileexa)e [**FindNextFile**](/windows/win32/api/fileapi/nf-fileapi-findnextfilea).

Fino a quando la copia shadow non è stata completata, è ancora possibile che i writer aggiungano o rimuovano i file dal disco nel corso normale del lavoro, pertanto non è necessario generare l'elenco effettivo dei file di cui eseguire il backup in questo momento.

Al contrario, l'elenco iniziale di file e volumi di cui eseguire il backup si trova in questa fase eseguendo le operazioni seguenti:

1.  L'analisi di tutti i componenti selezionabili per il backup e non selezionabili nel documento di metadati del writer di ogni writer (tramite [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) e nell'organizzazione dei [*set di componenti*](vssgloss-c.md) usa il [*percorso logico*](vssgloss-l.md) (vedere [utilizzo della selezione e dei percorsi logici](working-with-selectability-and-logical-paths.md))
2.  [*Inclusione esplicita*](vssgloss-e.md) di tutti i componenti richiesti (non selezionabili per i componenti di backup senza selezionare per i predecessori di backup) nel documento componenti di backup con [ **IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)
3.  La scelta di includere in modo esplicito facoltativamente facoltativo per i componenti di backup che non definiscono un set di componenti (usando [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent))
4.  Se si selezionano i [*set di componenti*](vssgloss-c.md) per la partecipazione a un backup, è necessario aggiungere esplicitamente la definizione selezionabile per il componente di backup (usando [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)), che [*include implicitamente*](vssgloss-i.md) i [*sottocomponenti*](vssgloss-s.md)del set di componenti.
5.  Utilizzando le informazioni sui [*set di file*](vssgloss-f.md) nel documento dei metadati writer e nelle funzioni di gestione del volume dei writer selezionati, un richiedente determina i percorsi dei file di cui eseguire il backup e i volumi che devono essere replicati.

Si noti che solo i componenti inclusi in modo esplicito (usando [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent)) nel backup e nel documento componenti di backup disporranno di istanze dell'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) aggiunte a tale documento. Queste istanze verranno utilizzate per esaminare e modificare le impostazioni del componente per i componenti inclusi in modo esplicito e per i relativi sottocomponenti inclusi in modo implicito (vedere [selezione e utilizzo delle proprietà del componente](selectability-and-working-with-component-properties.md)).

Se un writer include i componenti di un writer, deve aggiungere tutti i componenti necessari. Tuttavia, un richiedente è anche libero di ignorare completamente tutti i set di componenti di un writer. Se nessuno dei componenti di un writer è selezionato in modo esplicito, il writer non è selezionato e VSS impedisce a tale writer di partecipare al resto dell'operazione di backup.

Il richiedente avvia il set di copie shadow che conterrà i volumi selezionati chiamando [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset).

Se il volume può partecipare a una copia shadow, che può essere controllata con [**IVssBackupComponents:: IsVolumeSupported**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-isvolumesupported), il richiedente può aggiungere tale volume al set di copie shadow usando [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).

Sebbene non sia in genere utile, un richiedente può anche scegliere quale [*provider*](vssgloss-p.md) manterrà la copia shadow per un volume specifico. vedere [selezione dei provider](selecting-providers.md) per i dettagli.

È necessario prestare particolare attenzione alla gestione di un volume contenente cartelle montate o reparse point. Una cartella montata o un punto di analisi può essere visualizzato in una copia shadow ed è possibile eseguirne il backup. Tuttavia, non è possibile attraversare una cartella montata o un punto di analisi nel volume copiato Shadow (vedere [uso di cartelle montate e reparse point](working-with-reparse-and-mount-points.md)).

A questo punto del backup, il documento componenti di backup viene inizializzato e compilato. Nelle operazioni future, i writer e i richiedenti possono usare l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per comunicare tra loro.

Ai writer viene concesso l'accesso all'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) per la gestione degli eventi [*PrepareForBackup*](vssgloss-p.md), [*PostSnapshot*](vssgloss-p.md)e [*BackupComplete*](vssgloss-b.md) .

 

 
