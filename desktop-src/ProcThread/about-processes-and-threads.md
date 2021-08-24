---
description: Ogni processo fornisce le risorse necessarie per eseguire un programma.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: Informazioni su processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cbce9375d3c27fd58d6bab48c11fe2bdb825dfc729c2176dd2f14eba0a958e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032621"
---
# <a name="about-processes-and-threads"></a>Informazioni su processi e thread

Ogni *processo* fornisce le risorse necessarie per eseguire un programma. Un processo ha uno spazio indirizzi virtuali, codice eseguibile, handle aperti per gli oggetti di sistema, un contesto di sicurezza, un identificatore di processo univoco, variabili di ambiente, una classe di priorità, dimensioni di working set minime e massime e almeno un thread di esecuzione. Ogni processo viene avviato con un singolo thread, spesso denominato *thread primario,* ma può creare thread aggiuntivi da uno qualsiasi dei relativi thread.

Un *thread è* l'entità all'interno di un processo che può essere pianificato per l'esecuzione. Tutti i thread di un processo condividono lo spazio degli indirizzi virtuali e le risorse di sistema. Inoltre, ogni thread gestisce gestori di eccezioni, una priorità di pianificazione, l'archiviazione locale del thread, un identificatore di thread univoco e un set di strutture che il sistema userà per salvare il contesto del thread fino a quando non viene pianificato. Il *contesto del thread* include il set di registri del computer del thread, lo stack del kernel, un blocco di ambiente del thread e uno stack utente nello spazio degli indirizzi del processo del thread. I thread possono anche avere un proprio contesto di sicurezza, che può essere usato per la rappresentazione dei client.

Microsoft Windows supporta *il multitasking preemptive,* che crea l'effetto dell'esecuzione simultanea di più thread da più processi. In un computer multiprocessore, il sistema può eseguire simultaneamente tutti i thread presenti nel computer.

Un *oggetto processo* consente di gestire gruppi di processi come unità. Gli oggetti processo sono oggetti rinominabili, a protezione diretta e con condivisione che controllano gli attributi dei processi associati. Le operazioni eseguite sull'oggetto processo influiscono su tutti i processi associati all'oggetto processo.

Un'applicazione può usare il *pool di thread* per ridurre il numero di thread dell'applicazione e fornire la gestione dei thread di lavoro. Le applicazioni possono accoda gli elementi di lavoro, associare il lavoro agli handle in attesa, accodarsi automaticamente in base a un timer e associare all'I/O.

*La pianificazione in modalità utente* è un meccanismo leggero che le applicazioni possono usare per pianificare i propri thread. Un'applicazione può passare da un thread [](scheduling.md) UMS all'altro in modalità utente senza coinvolgere l'utilità di pianificazione di sistema e ottenere nuovamente il controllo del processore se un thread UMS si blocca nel kernel. Ogni thread UMS ha un proprio contesto di thread anziché condividere il contesto di thread di un singolo thread. La possibilità di passare da un thread all'altro in modalità utente rende UMS più efficiente rispetto ai pool di thread per gli elementi di lavoro di breve durata che richiedono poche chiamate di sistema.

Un *fiber* è un'unità di esecuzione che deve essere pianificata manualmente dall'applicazione. I fiber vengono eseguiti nel contesto dei thread che li pianificano. Ogni thread può pianificare più fiber. In generale, i fiber non offrono vantaggi rispetto a un'applicazione multithreading ben progettata. Tuttavia, l'uso di fiber può semplificare la portabilità delle applicazioni progettate per pianificare i propri thread.

Per altre informazioni, vedere i seguenti argomenti:

-   [Multitasking](multitasking.md)
-   [Pianificazione](scheduling.md)
-   [Più thread](multiple-threads.md)
-   [Processi figlio](child-processes.md)
-   [Pool di thread](thread-pools.md)
-   [Oggetti processo](job-objects.md)
-   [Pianificazione in modalità utente](user-mode-scheduling.md)
-   [Fibre](fibers.md)

 

 



