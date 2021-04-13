---
description: Durante l'elaborazione di un backup, un richiedente e una coordinata di writer per fornire un'immagine di sistema stabile dalla quale eseguire il backup dei dati (il volume copiato Shadow), raggruppare i file in base all'utilizzo e archiviare le informazioni sui dati salvati.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Cenni preliminari sull'elaborazione di un backup in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a11aeab87b503241acefdd15a153c9e417e537
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345021"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Cenni preliminari sull'elaborazione di un backup in VSS

Durante l'elaborazione di un backup, un richiedente e una coordinata di writer per fornire un'immagine di sistema stabile dalla quale eseguire il backup dei dati (il volume copiato Shadow), raggruppare i file in base all'utilizzo e archiviare le informazioni sui dati salvati. Questa operazione deve essere eseguita durante la creazione di un'interruzione minima del flusso di lavoro normale del writer.

Un richiedente esegue una query di writer per i relativi metadati, elabora questi dati, invia una notifica ai writer prima dell'inizio della copia shadow e delle operazioni di backup e quindi notifica nuovamente i writer al termine delle operazioni di copia shadow e backup.

In risposta a queste notifiche, il writer fornisce informazioni sui file di cui eseguire il backup, ad esempio specificando i gruppi di file da coordinare ([*componenti*](vssgloss-c.md)), sospendendo le operazioni di i/O prima di una copia shadow e quindi torna al normale funzionamento dopo il completamento di una copia shadow o alla fine del backup.

Nel corso dell'elaborazione del backup, un writer specifica i file di cui è responsabile tramite i metadati di sola lettura, ovvero il documento di metadati del writer (vedere [metadati VSS: utilizzo del documento di metadati del writer](working-with-the-writer-metadata-document.md)). Il richiedente interpreta quindi questi metadati, sceglie gli elementi di cui eseguire il backup e archivia tali decisioni nel relativo oggetto metadati, il documento componenti di backup (vedere [metadati VSS: utilizzo del documento componenti di backup](working-with-the-backup-components-document.md)). Questo documento dei componenti di backup è disponibile per l'ispezione e la modifica del writer durante le operazioni di backup e ripristino.

Questo diagramma illustra le interazioni tra il richiedente, il servizio VSS, il supporto del kernel VSS, gli eventuali writer VSS interessati ed eventuali provider hardware VSS.

![interazioni tra richiedente, componenti di backup, writer e provider](images/vssimpl.png)

Per comprendere appieno le attività di base necessarie per l'esecuzione di un backup, è utile suddividere questa panoramica negli argomenti seguenti:

-   [Panoramica dell'inizializzazione del backup](overview-of-backup-initialization.md)
-   [Panoramica della fase di individuazione del backup](overview-of-the-backup-discovery-phase.md)
-   [Panoramica delle attività di pre-backup](overview-of-pre-backup-tasks.md)
-   [Panoramica del backup effettivo dei file](overview-of-actual-backup-of-files.md)
-   [Panoramica della terminazione del backup](overview-of-backup-termination.md)

 

 



