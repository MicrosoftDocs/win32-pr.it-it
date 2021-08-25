---
description: Un richiedente è qualsiasi applicazione che usa l'API vss (in particolare l'interfaccia IVssBackupComponents) per richiedere i servizi del Servizio Copia Shadow del volume per creare e gestire copie shadow e set di copie shadow di uno o più volumi.
ms.assetid: e49920d0-5b66-4aa1-b3ca-641629df5f8a
title: Requesters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e7fa7b1718b0da278dabb164fbffee43c939cd688c150e202bfafc4731a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866381"
---
# <a name="requesters"></a>Requesters

Un [](vssgloss-r.md) richiedente è qualsiasi applicazione che usa l'API vss (in particolare l'interfaccia [**IVssBackupComponents)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) per richiedere i servizi del Servizio Copia Shadow del volume per creare e gestire copie shadow e set di copie shadow di uno o più volumi.

L'esempio più tipico di un richiedente (e l'unico descritto in questa documentazione) è un'applicazione di backup/ripristino in grado di riconoscere VSS, che usa i dati copiati shadow come origine stabile per le operazioni di backup.

Oltre all'avvio delle copie shadow, le applicazioni richiedenti di backup/ripristino comunicano con i data producer (writer) per raccogliere informazioni sul sistema e segnalare ai writer di preparare i dati per il backup.

## <a name="requester-state"></a>Stato del richiedente

Un richiedente mantiene le informazioni sullo stato in un oggetto metadati basato su XML denominato Documento dei componenti di backup. I metadati del richiedente sono necessari, ma non sufficienti per consentire a un richiedente di eseguire il backup e quindi ripristinare un file system. I motivi sono i seguenti:

-   Durante un'operazione di backup, solo un subset di tutti i componenti coinvolti nel backup, non selezionabili per i componenti di [*backup*](vssgloss-s.md) senza selezionabili per i predecessori di backup e selezionabili per i componenti di backup inclusi [*in*](vssgloss-e.md) modo esplicito nel backup, hanno aggiunto le informazioni al documento Dei componenti di backup del richiedente.
-   Le informazioni anche per i componenti aggiunti al documento Componenti di backup sono incomplete. Le specifiche di file e percorso non sono incluse.
-   Durante le operazioni di ripristino, un componente [](vssgloss-s.md) [*incluso in*](vssgloss-i.md) modo implicito nel backup può essere selezionabile per il ripristino e pertanto può essere incluso in modo esplicito nel ripristino. Ciò richiederà l'aggiornamento del documento dei componenti di backup del richiedente con le informazioni provenienti da copie archiviate del documento di metadati writer di un writer.

Per consentire la specifica completa di un'operazione di backup o ripristino, l'API vss consente al richiedente di eseguire query sui metadati dei writer (durante i backup) o di esaminare i metadati del writer archiviato (durante i ripristini). Inoltre, un writer può modificare le informazioni sui componenti nel documento Componenti di backup nel corso di un'operazione di backup o ripristino.

Usando le informazioni sui componenti selezionati per il backup e il ripristino e [](definition-of-components-by-writers.md) le regole relative alla selezione dei componenti (per altre informazioni, vedere Configurazione dell'organizzazione dei componenti e Uso della selezionabilità e dei percorsi logici), [](working-with-selectability-and-logical-paths.md)un richiedente può determinare i file di cui è necessario eseguire il backup o il ripristino e dove può trovare tali file.

Come parte di un backup, i metadati del richiedente e del writer devono essere archiviati in modo che possano essere usati nel ripristino. Al contrario, le operazioni di ripristino richiedono il recupero dei vecchi componenti di backup e dei documenti dei metadati del writer per ottenere istruzioni complete sul ripristino dei file.

## <a name="requester-interprocess-communication"></a>Comunicazione interprocesso richiedente

Il richiedente mantiene il controllo sulle operazioni di backup e ripristino di VSS generando eventi COM tramite varie chiamate nell'API richiedente. Queste chiamate possono eseguire le operazioni seguenti:

-   Effettuare richieste dei provider, ad esempio [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) fa sì che il provider crei una copia shadow del volume selezionato.
-   Attivare i writer per restituire informazioni, ad esempio [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) consente al richiedente di ottenere il documento di metadati del writer di ogni writer.
-   Richiedere ai writer di preparare o gestire varie fasi delle operazioni di copia shadow e backup, ad esempio [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) segnala ai writer di impostare per il blocco di I/O.

Un richiedente riceve informazioni dai writer tramite documenti di metadati del writer live o archiviati e tramite l'uso [**dell'interfaccia IVssComponent,**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) che il writer può aggiornare.

## <a name="life-cycle-of-a-requester-during-backup"></a>Ciclo di vita di un richiedente durante il backup

Di seguito è riportato un riepilogo del ciclo di vita del richiedente per il backup:

1.  Creare un'istanza e inizializzare le interfacce API vss.
2.  Contattare gli autori e recuperarne le informazioni.
3.  Scegliere i dati di cui eseguire il backup.
4.  Richiedere una copia shadow del provider.
5.  Eseguire il backup dei dati.
6.  Rilasciare l'interfaccia e la copia shadow.

## <a name="life-cycle-of-a-requester-during-restore"></a>Ciclo di vita di un richiedente durante il ripristino

Il ciclo di vita di ripristino non richiede una copia shadow, ma richiede comunque la collaborazione tra writer:

1.  Creare un'istanza delle interfacce API di VSS.
2.  Inizializzare il richiedente per l'operazione di ripristino caricando un documento dei componenti di backup archiviato.
3.  Recuperare i metadati del writer archiviati e i documenti dei componenti di backup.
4.  Contattare i writer per inizializzare la collaborazione.
5.  Verificare la presenza di aggiornamenti del writer nel documento Componenti di backup.
6.  Ripristinare i dati.

 

 



