---
description: Dopo aver creato un file INF, in genere si scriverà il codice sorgente per l'applicazione di installazione. È possibile chiamare le funzioni di installazione dell'applicazione di installazione per eseguire numerose operazioni di installazione.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Creazione di applicazioni di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3aaca2b1d509795f625e67c18c13131d7e502b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314661"
---
# <a name="creating-setup-applications"></a>Creazione di applicazioni di installazione

Dopo aver creato un file INF, in genere si scriverà il codice sorgente per l'applicazione di installazione. È possibile chiamare le funzioni di installazione dell'applicazione di installazione per eseguire numerose operazioni di installazione.

I passaggi seguenti illustrano come usare le funzioni di installazione per creare un'applicazione di installazione. È possibile usare questo esempio come punto di partenza o sviluppare un algoritmo di installazione personalizzato.

**Inizializzazione**

-   [Aprire il file INF e, se necessario, aggiungere altri file INF.](opening-the-inf-file.md)
-   [Estrarre le informazioni sul file dal file INF.](extracting-file-information-from-the-inf-file.md)
-   [Raccogliere le informazioni di installazione dall'utente.](gathering-setup-information-from-the-user.md)
-   [Creare una coda.](creating-a-queue-and-queuing-file-operations.md)

**Installa file**

-   [Eseguire il commit della coda, specificando una routine di callback.](committing-the-queue.md)
-   [Aggiornare le informazioni del registro di sistema.](updating-registry-information.md)

**Eseguire la pulizia**

-   [Chiudere la coda di file e il file INF.](closing-the-file-queue-and-inf-file.md)
-   [Rilasciare tutte le altre risorse di sistema e terminare il programma.](releasing-other-system-resources.md)

 

 



