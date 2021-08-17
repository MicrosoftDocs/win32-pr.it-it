---
description: COM+ tenta di evitare situazioni in cui questi percorsi di errore devono essere eseguiti in un server.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Concetti relativi ai Low-Memory di attivazione di COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b4c34e10dcb18a88566d1bc45bb6751e500767c34a2e17cf8cdf12f0f1930c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129179"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Concetti relativi ai Low-Memory di attivazione di COM+

In genere, la sincronizzazione non è necessaria quando si dispone di un apartment a thread singolo (STA), perché l'apartment fornisce la sincronizzazione automaticamente. La sincronizzazione diventa importante quando si dispone di un apartment multithreading (MTA) e di un oggetto a thread libero. In passato, gli oggetti a thread libero dovevano gestire il blocco. È possibile eliminare la necessità di usare il blocco impostando l'attributo di sincronizzazione per un componente.

I problemi di affidabilità si verificano spesso quando le risorse di un server non possono reagire in modo efficiente ai carichi di picco. Quando un server non ha risorse fisiche sufficienti per soddisfare i picchi di richiesta, può esaurire la memoria virtuale. Questo diventa un problema se il codice utente o il codice di sistema non gestisce correttamente gli errori di allocazione della memoria. Il server inizia a rallentare e, quando la memoria è esaurita, le allocazioni di memoria hanno esito negativo. Il server esegue percorsi di errore per gestire gli errori di allocazione. Se un percorso di errore contiene un bug nel sistema o nel codice utente in esecuzione nel server, è estremamente difficile intercettare e gestire in modo sicuro.

COM+ tenta di evitare situazioni in cui questi percorsi di errore devono essere eseguiti in un server. Tramite la funzionalità porte di attivazione a memoria bassa, COM+ monitora in modo proattivo il carico di memoria nel sistema e garantisce che sia disponibile una quantità ragionevole di memoria prima di eseguire il codice utente. Se la percentuale di memoria virtuale disponibile per l'applicazione scende al di sotto di una soglia fissa, l'attivazione ha esito negativo prima della creazione di un oggetto o di un'applicazione server COM+, come illustrato nella figura seguente. In caso di errore di queste attivazioni che normalmente verrebbero eseguite, la funzionalità dei gate di attivazione con memoria insufficiente riduce al minimo i problemi associati alle allocazioni di memoria nel codice utente, con un miglioramento significativo dell'affidabilità del sistema.

![Diagramma che illustra la relazione tra un'applicazione COM+ e un gate di attivazione con memoria insufficiente.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

La funzionalità dei gate di attivazione con memoria insufficiente si applica solo ai componenti COM configurati installati in un'applicazione COM+.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Funzionamento della Low-Memory dei gate di attivazione

La funzionalità dei gate di attivazione a memoria bassa usa un livello di soglia fisso diverso a seconda del tipo di attivazione. Quando si crea un'applicazione server COM+, COM+ consente l'attivazione se è disponibile più del 10% della memoria virtuale. Se è disponibile un valore inferiore al 10%, COM+ esegue un'allocazione di test per determinare se il file di paging può espandersi per supportare il nuovo carico di memoria. Se il file di paging si espande, viene creata l'applicazione server. Se non è possibile espandere il file di paging, l'attivazione ha esito negativo e la memoria non viene allocata.

Il processo è simile quando si crea un oggetto . In questo caso, COM+ consente l'attivazione se è disponibile più del 5% della memoria virtuale. Se è disponibile meno del 5%, COM+ procede con un'allocazione di test. Anche in questo caso, se l'allocazione di test espande il file di paging, viene creato l'oggetto . In caso contrario, l'attivazione non riesce.

I livelli di soglia fissi per i gate di attivazione con memoria insufficiente non sono attualmente configurabili. Per questo motivo, non sono presenti attività associate a questa funzionalità.

 

 



