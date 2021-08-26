---
description: La linea guida consigliata è usare il numero più ridotto possibile di thread, riducendo al minimo l'uso delle risorse di sistema.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Considerazioni sul multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd11b0015db8f3fd3606b74a5bce695aed135f79265b3f1d6ba410002b74a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032241"
---
# <a name="multitasking-considerations"></a>Considerazioni sul multitasking

La linea guida consigliata è usare il numero più ridotto possibile di thread, riducendo al minimo l'uso delle risorse di sistema. In questo modo le prestazioni risultano migliorate. Il multitasking presenta requisiti di risorse e potenziali conflitti da considerare durante la progettazione dell'applicazione. Di seguito sono elencati i requisiti in termini di risorse:

-   Il sistema utilizza memoria per le informazioni sul contesto richieste dai processi e dai thread. Di conseguenza, il numero di processi e thread che è possibile creare è limitato dalla memoria disponibile.
-   Tenere traccia di un numero elevato di thread determina un consumo significativo di tempo del processore. Se sono presenti troppi thread, la maggior parte di essi non sarà in grado di eseguire progressi significativi. Se la maggior parte dei thread correnti si trova in un processo, quelli contenuti in altri processi vengono pianificati meno frequentemente.

L'accesso condiviso alle risorse può creare conflitti. Per evitarli, è necessario sincronizzare l'accesso alle risorse condivise. Ciò vale per le risorse di sistema (ad esempio le porte di comunicazione), le risorse condivise da più processi (ad esempio gli handle di file) o le risorse di un singolo processo (ad esempio variabili globali) a cui a cui a loro volta aerino più thread. La mancata sincronizzazione corretta dell'accesso (nello stesso processo o in processi diversi) può causare problemi quali deadlock e race conditions. Oggetti e funzioni di sincronizzazione che è possibile usare per coordinare la condivisione delle risorse tra più thread. Per altre informazioni sulla sincronizzazione, vedere [Sincronizzazione dell'esecuzione di più thread.](synchronizing-execution-of-multiple-threads.md) La riduzione del numero di thread rende più semplice ed efficace la sincronizzazione delle risorse.

Una buona progettazione per un'applicazione multithreading è il server di pipeline. In questa progettazione si crea un thread per processore e si creano code di richieste per le quali l'applicazione gestisce le informazioni sul contesto. Un thread elabora tutte le richieste in una coda prima di elaborare le richieste nella coda successiva.

 

 



