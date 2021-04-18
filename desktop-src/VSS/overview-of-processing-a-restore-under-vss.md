---
description: Durante l'elaborazione di un backup in VSS, i richiedenti e i writer collaborano per produrre un'immagine di sistema stabile dalla quale eseguire il backup dei dati, il che richiede il coordinamento e la creazione di una copia shadow del sistema corrente.
ms.assetid: 1cefb6ac-f2bb-464b-a62f-05be91ae56f7
title: Panoramica dell'elaborazione di un ripristino in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0279888b28af82eb1b4b51093b421b9db5e15d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310684"
---
# <a name="overview-of-processing-a-restore-under-vss"></a>Panoramica dell'elaborazione di un ripristino in VSS

Durante l'elaborazione di un backup in VSS, i richiedenti e i writer collaborano per produrre un'immagine di sistema stabile dalla quale eseguire il backup dei dati, il che richiede il coordinamento e la creazione di una copia shadow del sistema corrente.

A differenza di un backup VSS, in cui lo scopo del richiedente e il coordinamento dei writer è quello di produrre un'immagine di sistema stabile da cui copiare i dati, l'obiettivo di un ripristino basato su VSS consiste nel restituire i file su disco in modo più utile per le applicazioni (writer) attualmente in esecuzione nel sistema. Questa operazione non richiede un'immagine di sistema stabile, quindi non è necessaria alcuna copia shadow.

Al contrario, l'attenzione è incentrata sulla prevenzione dell'attività del writer, sulla prevenzione della creazione di set di dati incoerenti sul disco e sulla possibilità per gli autori di valutare e unire i dati quando necessario.

Analogamente a un'operazione di backup, un ripristino VSS richiede l'accesso sia a un documento dei componenti di backup che ai documenti di metadati del writer. Questi documenti non vengono in genere ottenuti eseguendo una query sulle applicazioni in esecuzione, ma vengono recuperate da versioni archiviate come documenti XML nei supporti di backup.

Come nel caso delle operazioni di backup, i documenti dei metadati del writer rimangono oggetti di sola lettura e, una volta recuperati, il documento componenti di backup può comunque essere modificato. Le modifiche del documento componenti di backup consentono a writer e richiedente di comunicare nei modi seguenti:

-   Override dei [*metodi di ripristino*](vssgloss-r.md) con [*destinazioni Restore*](vssgloss-r.md)
-   Uso di [ *mapping di percorsi alternativi*](vssgloss-a.md)
-   Ripristino dei file nei nuovi percorsi sul disco
-   Uso di regole di selezione diverse da quelle usate durante il backup

Per comprendere appieno le attività di base dell'esecuzione di un ripristino, è utile suddividere questa panoramica negli argomenti seguenti:

-   [Panoramica dell'inizializzazione del ripristino](overview-of-restore-initialization.md)
-   [Panoramica della preparazione per il ripristino](overview-of-preparing-for-restore.md)
-   [Panoramica del ripristino dei file effettivi](overview-of-actual-file-restoration.md)
-   [Panoramica della pulizia e della chiusura del ripristino](overview-of-restore-clean-up-and-termination.md)

 

 



