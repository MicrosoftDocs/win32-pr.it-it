---
description: Durante l'elaborazione di un backup nel Servizio Copia Shadow del volume, i richiedenti e i writer hanno lavorato insieme per produrre un'immagine di sistema stabile da cui eseguire il backup dei dati, che richiedeva il coordinamento e la creazione di una copia shadow del sistema corrente.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Panoramica dell'elaborazione di un ripristino in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b01094a02b823f372271f14c04801820407573b9351bfe7e2fc2ad9dc74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937959"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Panoramica dell'elaborazione di un ripristino in VSS

Durante l'elaborazione di un backup nel Servizio Copia Shadow del volume, i richiedenti e i writer hanno lavorato insieme per produrre un'immagine di sistema stabile da cui eseguire il backup dei dati, che richiedeva il coordinamento e la creazione di una copia shadow del sistema corrente.

A differenza di un backup vss, in cui lo scopo del coordinamento di richiedenti e writer è produrre un'immagine di sistema stabile da cui copiare i dati, l'obiettivo di un ripristino basato su VSS è restituire i file su disco nel modo più utile per le applicazioni (writer) attualmente in esecuzione nel sistema. Questa operazione non richiede un'immagine di sistema stabile, quindi non è necessaria alcuna copia shadow.

Al contrario, l'attenzione è incentrata su come evitare l'interruzione dell'attività del writer, impedire la creazione di set di dati incoerenti su disco e consentire ai writer l'ambito necessario per valutare e unire i dati quando necessario.

Analogamente a un'operazione di backup, un ripristino vss richiede l'accesso sia a un documento di componenti di backup che a documenti di metadati del writer. Questi documenti non vengono in genere ottenuti eseguendo query sulle applicazioni in esecuzione, ma vengono recuperati dalle versioni archiviate come documenti XML nei supporti di backup.

Come nel caso delle operazioni di backup, i documenti di metadati del writer rimangono oggetti di sola lettura e, una volta recuperati, il documento dei componenti di backup può comunque essere modificato. Le modifiche del documento dei componenti di backup consentono a writer e richiedenti di comunicare quanto segue:

-   Override dei [*metodi di ripristino con*](vssgloss-r.md) destinazioni di [*ripristino*](vssgloss-r.md)
-   Uso [ *di mapping di percorsi alternativi*](vssgloss-a.md)
-   Ripristino dei file in nuovi percorsi su disco
-   Uso di regole di selezione diverse da quelle usate durante il backup

Per comprendere appieno le attività di base dell'esecuzione di un ripristino, è utile suddividere questa panoramica negli argomenti seguenti:

-   [Panoramica dell'inizializzazione del ripristino](overview-of-restore-initialization.md)
-   [Panoramica della preparazione per il ripristino](overview-of-preparing-for-restore.md)
-   [Panoramica del ripristino effettivo dei file](overview-of-actual-file-restoration.md)
-   [Panoramica della pulizia e della chiusura del ripristino](overview-of-restore-clean-up-and-termination.md)

 

 



