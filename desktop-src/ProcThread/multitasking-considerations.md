---
description: Le linee guida consigliate sono l'uso del minor numero possibile di thread, riducendo così al minimo l'uso delle risorse di sistema.
ms.assetid: ed9bd3cf-b10c-49f9-bf62-7332517350b7
title: Considerazioni sul multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec64bf1b7d59a42a1aec3511a72328f18bfaa88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131670"
---
# <a name="multitasking-considerations"></a>Considerazioni sul multitasking

Le linee guida consigliate sono l'uso del minor numero possibile di thread, riducendo così al minimo l'uso delle risorse di sistema. In questo modo le prestazioni risultano migliorate. Il multitasking presenta requisiti di risorse e potenziali conflitti da considerare durante la progettazione dell'applicazione. Di seguito sono elencati i requisiti in termini di risorse:

-   Il sistema utilizza memoria per le informazioni di contesto richieste da processi e thread. Pertanto, il numero di processi e thread che è possibile creare è limitato dalla memoria disponibile.
-   Tenere traccia di un numero elevato di thread determina un consumo significativo di tempo del processore. Se sono presenti troppi thread, la maggior parte di essi non sarà in grado di eseguire progressi significativi. Se la maggior parte dei thread correnti si trova in un processo, quelli contenuti in altri processi vengono pianificati meno frequentemente.

L'accesso condiviso alle risorse può creare conflitti. Per evitarli, è necessario sincronizzare l'accesso alle risorse condivise. Questo vale per le risorse di sistema, ad esempio le porte di comunicazione, le risorse condivise da più processi, ad esempio gli handle di file, o le risorse di un singolo processo, ad esempio le variabili globali, a cui si accede da più thread. La mancata sincronizzazione dell'accesso correttamente (nello stesso o in processi diversi) può causare problemi quali deadlock e race condition. Oggetti e funzioni di sincronizzazione che è possibile usare per coordinare la condivisione delle risorse tra più thread. Per ulteriori informazioni sulla sincronizzazione, vedere [sincronizzazione dell'esecuzione di più thread](synchronizing-execution-of-multiple-threads.md). La riduzione del numero di thread rende più semplice ed efficace la sincronizzazione delle risorse.

Un progetto valido per un'applicazione multithreading è il server pipeline. In questa progettazione viene creato un thread per processore e vengono compilate le code di richieste per le quali l'applicazione mantiene le informazioni sul contesto. Un thread elabora tutte le richieste in una coda prima di elaborare le richieste nella coda successiva.

 

 



