---
description: Ogni processo fornisce le risorse necessarie per l'esecuzione di un programma.
ms.assetid: 055458cf-9fc7-4a16-be14-1122b3cf0251
title: Informazioni su processi e thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 650eab4421971bdc08e71c031aec433ed84471bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231525"
---
# <a name="about-processes-and-threads"></a>Informazioni su processi e thread

Ogni *processo* fornisce le risorse necessarie per l'esecuzione di un programma. Un processo ha uno spazio di indirizzi virtuale, un codice eseguibile, handle aperti per gli oggetti di sistema, un contesto di sicurezza, un identificatore di processo univoco, variabili di ambiente, una classe di priorità, dimensioni minime e massime working set e almeno un thread di esecuzione. Ogni processo viene avviato con un singolo thread, spesso denominato *thread primario*, ma può creare thread aggiuntivi da uno qualsiasi dei relativi thread.

Un *thread* è l'entità all'interno di un processo che può essere pianificata per l'esecuzione. Tutti i thread di un processo condividono lo spazio degli indirizzi virtuale e le risorse di sistema. Ogni thread gestisce inoltre gestori di eccezioni, una priorità di pianificazione, l'archiviazione locale di thread, un identificatore univoco del thread e un set di strutture che verrà utilizzato dal sistema per salvare il contesto del thread fino a quando non viene pianificato. Il *contesto del thread* include il set di registri computer del thread, lo stack del kernel, un blocco di ambiente del thread e uno stack utente nello spazio degli indirizzi del processo del thread. I thread possono anche avere un proprio contesto di sicurezza, che può essere usato per la rappresentazione dei client.

Microsoft Windows supporta il *multitasking preemptive*, che crea l'effetto dell'esecuzione simultanea di più thread da più processi. In un computer multiprocessore, il sistema può eseguire simultaneamente tutti i thread quanti sono i processori presenti nel computer.

Un *oggetto processo* consente la gestione di gruppi di processi come unità. Gli oggetti processo sono oggetti namable, a protezione diretta e condivisibili che controllano gli attributi dei processi ad essi associati. Le operazioni eseguite sull'oggetto processo hanno effetto su tutti i processi associati all'oggetto processo.

Un'applicazione può utilizzare il *pool di thread* per ridurre il numero di thread dell'applicazione e fornire la gestione dei thread di lavoro. Le applicazioni possono accodare gli elementi di lavoro, associare il lavoro con handle waitable, accodarsi automaticamente in base a un timer e associarli all'I/O.

La *pianificazione in modalità utente* è un meccanismo leggero che le applicazioni possono utilizzare per pianificare i propri thread. Un'applicazione può passare tra i thread UMS in modalità utente senza coinvolgere l' [utilità di pianificazione del sistema](scheduling.md) e riacquisire il controllo del processore se un thread UMS si blocca nel kernel. Ogni thread UMS dispone di un proprio contesto di thread invece di condividere il contesto del thread di un singolo thread. La possibilità di passare da un thread all'altro in modalità utente rende il UMS più efficiente dei pool di thread per gli elementi di lavoro di breve durata che richiedono poche chiamate di sistema.

Un *Fiber* è un'unità di esecuzione che deve essere pianificata manualmente dall'applicazione. I fiber vengono eseguiti nel contesto dei thread che li pianificano. Ogni thread può pianificare più Fiber. In generale, i fiber non offrono vantaggi in un'applicazione multithreading progettata correttamente. Tuttavia, l'uso di fiber può semplificare la portabilità delle applicazioni progettate per pianificare i propri thread.

Per altre informazioni, vedere i seguenti argomenti:

-   [Multitasking](multitasking.md)
-   [Pianificazione](scheduling.md)
-   [Più thread](multiple-threads.md)
-   [Processi figlio](child-processes.md)
-   [Pool di thread](thread-pools.md)
-   [Oggetti processo](job-objects.md)
-   [Pianificazione in modalità utente](user-mode-scheduling.md)
-   [Fiber](fibers.md)

 

 



