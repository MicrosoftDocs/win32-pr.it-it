---
description: Dopo aver creato un file INF, in genere si scriverà il codice sorgente per l'applicazione di installazione. Le funzioni di installazione vengono chiamate dall'applicazione di installazione per eseguire molte operazioni di installazione.
ms.assetid: 9f444564-d3a4-4b3c-8849-b56cd610356c
title: Creazione di applicazioni di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77f920a024a4414690baad7684af90a30ee4ca3c9f96a2c6f61b1b84430c072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887439"
---
# <a name="creating-setup-applications"></a>Creazione di applicazioni di installazione

Dopo aver creato un file INF, in genere si scriverà il codice sorgente per l'applicazione di installazione. Le funzioni di installazione vengono chiamate dall'applicazione di installazione per eseguire molte operazioni di installazione.

I passaggi seguenti illustrano un modo per usare le funzioni di installazione per creare un'applicazione di installazione. È possibile usare questo esempio come punto di partenza o sviluppare un algoritmo di installazione personalizzato.

**Inizializzazione**

-   [Aprire il file INF e, se appropriato, aggiungere altri file INF.](opening-the-inf-file.md)
-   [Estrarre le informazioni sul file dal file INF.](extracting-file-information-from-the-inf-file.md)
-   [Raccogliere le informazioni di configurazione dall'utente.](gathering-setup-information-from-the-user.md)
-   [Creare una coda.](creating-a-queue-and-queuing-file-operations.md)

**Installare i file**

-   [Eseguire il commit della coda, specificando una routine di callback.](committing-the-queue.md)
-   [Aggiornare le informazioni del Registro di sistema.](updating-registry-information.md)

**Eseguire la pulizia**

-   [Chiudere la coda di file e INF.](closing-the-file-queue-and-inf-file.md)
-   [Rilasciare eventuali altre risorse di sistema e terminare il programma.](releasing-other-system-resources.md)

 

 



