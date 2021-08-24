---
description: Durante l'elaborazione di un backup, il richiedente e i writer si coordinano per fornire un'immagine di sistema stabile da cui eseguire il backup dei dati (volume shadow copiato), raggruppare i file in base al relativo utilizzo e archiviare le informazioni sui dati salvati.
ms.assetid: d7acb2a2-bb58-47e3-a950-d32f663ae36d
title: Panoramica dell'elaborazione di un backup in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60874b1c66bcc75788912f54e5b3ffc8314f1bc0d0ad6d92b815725af727936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510011"
---
# <a name="overview-of-processing-a-backup-under-vss"></a>Panoramica dell'elaborazione di un backup in VSS

Durante l'elaborazione di un backup, il richiedente e i writer si coordinano per fornire un'immagine di sistema stabile da cui eseguire il backup dei dati (volume shadow copiato), raggruppare i file in base al relativo utilizzo e archiviare le informazioni sui dati salvati. Questa operazione deve essere eseguita durante la creazione di un'interruzione minima del normale flusso di lavoro del writer.

Un richiedente esegue una query sui writer per i relativi metadati, elabora questi dati, invia una notifica ai writer prima dell'inizio della copia shadow e delle operazioni di backup e quindi invia di nuovo una notifica ai writer al termine delle operazioni di copia shadow e backup.

In risposta a queste notifiche, il writer fornisce informazioni sui file di cui eseguire il backup, inclusa la specifica di gruppi di file da coordinare [*(componenti*](vssgloss-c.md)), sospende le operazioni di I/O prima di una copia shadow e quindi torna al normale funzionamento dopo il completamento di una copia shadow o alla fine del backup.

Durante l'elaborazione del backup, un writer specifica i file di cui è responsabile tramite i metadati di sola lettura, ovvero il documento di metadati del writer(vedere [VsS Metadata: Working with the Writer Metadata Document](working-with-the-writer-metadata-document.md)). Il richiedente interpreta quindi questi metadati, sceglie gli elementi di cui eseguire il backup e archivia queste decisioni nel proprio oggetto metadati, il documento dei componenti di backup (vedere [VsS Metadata: Working with the Backup Components Document](working-with-the-backup-components-document.md)). Questo documento sui componenti di backup è disponibile per l'ispezione e la modifica del writer durante le operazioni di backup e ripristino.

Questo diagramma mostra le interazioni tra il richiedente, il servizio VSS, il supporto del kernel VSS, tutti i VSS writer coinvolti ed eventuali provider di hardware vss.

![interazioni tra richiedente, componenti di backup, writer e provider](images/vssimpl.png)

Per comprendere meglio le attività di base necessarie per eseguire un backup, è utile suddividere questa panoramica negli argomenti seguenti:

-   [Panoramica dell'inizializzazione del backup](overview-of-backup-initialization.md)
-   [Panoramica della fase di individuazione dei backup](overview-of-the-backup-discovery-phase.md)
-   [Panoramica delle attività di pre-backup](overview-of-pre-backup-tasks.md)
-   [Panoramica del backup effettivo dei file](overview-of-actual-backup-of-files.md)
-   [Panoramica della terminazione del backup](overview-of-backup-termination.md)

 

 



