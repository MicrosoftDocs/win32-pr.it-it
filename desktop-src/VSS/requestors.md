---
description: Un richiedente è qualsiasi applicazione che usa l'API VSS (in particolare l'interfaccia IVssBackupComponents) per richiedere ai servizi del Servizio Copia Shadow del volume di creare e gestire copie shadow e set di copie shadow di uno o più volumi.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Requesters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b676b8cd287365b257e3b6ee85a7e47a70f88ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227038"
---
# <a name="requesters"></a>Requesters

Un [*richiedente*](vssgloss-r.md) è qualsiasi applicazione che usa l'API VSS (in particolare l'interfaccia [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ) per richiedere ai servizi del servizio Copia Shadow del volume di creare e gestire copie shadow e set di copie shadow di uno o più volumi.

L'esempio più comune di un richiedente (e l'unico trattato in questa documentazione) è un'applicazione di backup/ripristino compatibile con VSS, che usa dati copiati in Shadow come origine stabile per le operazioni di backup.

Oltre ad avviare le copie shadow, le applicazioni di richiesta di backup/ripristino comunicano con i producer (writer) per raccogliere informazioni sul sistema e segnalare ai writer di preparare i dati per il backup.

## <a name="requester-state"></a>Stato del richiedente

Un richiedente mantiene le informazioni sullo stato in un oggetto di metadati basato su XML denominato documento componenti di backup. I metadati del richiedente sono necessari, ma non sufficienti per consentire a un richiedente di eseguire il backup e quindi ripristinare un file system. I motivi sono i seguenti:

-   Durante un'operazione di backup, solo un subset di tutti i componenti inclusi nel backup, non [*selezionabili per*](vssgloss-s.md) i componenti di backup senza selezionare per i predecessori di backup e selezionabili per i componenti di backup che sono stati [*inclusi in modo esplicito*](vssgloss-e.md) nel backup, hanno aggiunto le informazioni al documento componenti di backup del richiedente.
-   Le informazioni anche per i componenti aggiunti al documento componenti di backup sono incomplete: le specifiche di file e percorsi non sono incluse.
-   Durante le operazioni di ripristino, un componente [*incluso in modo implicito*](vssgloss-i.md) nel backup può essere [*selezionabile per il ripristino*](vssgloss-s.md) e pertanto può essere incluso in modo esplicito nel ripristino. Questa operazione richiede l'aggiornamento del documento dei componenti di backup del richiedente con le informazioni provenienti da copie archiviate del documento di metadati del writer del writer.

Per consentire la specifica completa di un'operazione di backup o ripristino, l'API VSS consente al richiedente di eseguire query sui metadati dei writer (durante i backup) o di esaminare i metadati del writer archiviati (durante i ripristini). Inoltre, un writer può modificare le informazioni sui componenti nel documento componenti di backup nel corso di un'operazione di backup o ripristino.

Utilizzando le informazioni sui componenti selezionati per il backup e il ripristino e le regole relative alla selezione dei componenti (per altre informazioni, vedere [configurazione dell'organizzazione dei componenti](definition-of-components-by-writers.md) e [utilizzo di percorsi di selezione e logici](working-with-selectability-and-logical-paths.md)), un richiedente può determinare i file di cui è necessario eseguire il backup o il ripristino del writer e individuare i file.

Come parte di un backup, è necessario archiviare sia i metadati del richiedente che del writer, in modo da poterli usare nel ripristino. Viceversa, le operazioni di ripristino richiedono il recupero dei vecchi componenti di backup e dei documenti di metadati del writer per ottenere istruzioni complete sul ripristino di file.

## <a name="requester-interprocess-communication"></a>Comunicazione interprocesso del richiedente

Il richiedente mantiene il controllo sulle operazioni di backup e ripristino di VSS generando eventi COM tramite varie chiamate nell'API del richiedente. Queste chiamate possono eseguire le operazioni seguenti:

-   Effettuare richieste dei provider, ad esempio [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) fa in modo che il provider crei una copia shadow del volume selezionato.
-   Attivare i writer per restituire informazioni, ad esempio [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) consente al richiedente di ottenere il documento di metadati del writer di ogni writer.
-   Richiedere ai writer di preparare o gestire varie fasi della copia shadow e delle operazioni di backup, ad esempio [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) segnala ai writer la configurazione per il blocco di i/O.

Un richiedente riceve informazioni dai writer tramite documenti di metadati del writer live o archiviati e tramite l'interfaccia [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) , che può essere aggiornata dal writer.

## <a name="life-cycle-of-a-requester-during-backup"></a>Ciclo di vita di un richiedente durante il backup

Di seguito è riportato un riepilogo del ciclo di vita del richiedente per il backup:

1.  Creare un'istanza e inizializzare le interfacce API VSS.
2.  Contattare i writer e recuperare le informazioni.
3.  Scegliere i dati di cui eseguire il backup.
4.  Richiedere una copia shadow del provider.
5.  Eseguire il backup dei dati.
6.  Rilasciare l'interfaccia e la copia shadow.

## <a name="life-cycle-of-a-requester-during-restore"></a>Ciclo di vita di un richiedente durante il ripristino

Il ciclo di vita del ripristino non richiede una copia shadow, ma richiede comunque la collaborazione del writer:

1.  Creare un'istanza delle interfacce API VSS.
2.  Inizializzare il richiedente per l'operazione di ripristino tramite il caricamento di un documento dei componenti di backup archiviati.
3.  Recuperare i metadati del writer archiviato e i documenti dei componenti di backup.
4.  Contattare i writer per inizializzare la collaborazione.
5.  Verificare la presenza di aggiornamenti del writer nel documento componenti di backup.
6.  Ripristinare i dati.

 

 



