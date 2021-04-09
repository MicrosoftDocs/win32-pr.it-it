---
description: COM+ tenta di evitare situazioni in cui tali percorsi di errore devono essere eseguiti in un server.
ms.assetid: 0de125a2-2e91-49b9-a903-6c2e173e22a2
title: Concetti di COM+ Low-Memory Activation Gates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d844a0492301ef067f5b3cd0e0749ec3a21779
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "103968807"
---
# <a name="com-low-memory-activation-gates-concepts"></a>Concetti di COM+ Low-Memory Activation Gates

In genere, la sincronizzazione non è necessaria quando si ha un Apartment a thread singolo (STA) perché l'Apartment fornisce la sincronizzazione. La sincronizzazione diventa importante quando si dispone di un Apartment a thread multipli (MTA) e di un oggetto a thread libero. In passato, gli oggetti a thread libero hanno dovuto gestire il blocco. È possibile eliminare la necessità di utilizzare il blocco impostando l'attributo di sincronizzazione per un componente.

I problemi di affidabilità si verificano spesso quando le risorse di un server non possono rispondere in modo efficiente ai picchi di carico Quando un server non dispone di risorse fisiche sufficienti per soddisfare i picchi della domanda, può esaurire la memoria virtuale. Questo diventa un problema se il codice utente o il codice di sistema non gestisce correttamente gli errori di allocazione della memoria. Il server inizia a rallentare e, quando la memoria viene esaurita, le allocazioni di memoria hanno esito negativo. Il server esegue i percorsi degli errori per gestire gli errori di allocazione. Se un percorso di errore contiene un bug nel sistema o nel codice utente in esecuzione nel server, è molto difficile da intercettare e gestire in modo sicuro.

COM+ tenta di evitare situazioni in cui tali percorsi di errore devono essere eseguiti in un server. Grazie alla funzionalità di controllo di attivazione a memoria insufficiente, COM+ monitora in modo proattivo il carico di memoria nel sistema e garantisce la disponibilità di una quantità di memoria ragionevole prima di eseguire il codice utente. Se la percentuale di memoria virtuale disponibile per l'applicazione scende al di sotto di una soglia fissa, l'attivazione avrà esito negativo prima della creazione di un'applicazione o di un oggetto server COM+, come illustrato nella figura seguente. Se queste attivazioni non vengono eseguite correttamente, la funzionalità relativa ai cancelli di attivazione a memoria ridotta riduce al minimo i problemi associati alle allocazioni di memoria nel codice utente, migliorando significativamente l'affidabilità del sistema.

![Diagramma che mostra la relazione tra un'applicazione COM+ e un gate di attivazione a memoria insufficiente.](images/ada5ef02-f2b1-46bb-b0fc-fe7d65f31b43.png)

La funzionalità di controllo di attivazione a memoria insufficiente si applica solo ai componenti COM configurati installati in un'applicazione COM+.

## <a name="how-the-low-memory-activation-gates-feature-works"></a>Funzionamento della funzionalità dei controlli di attivazione Low-Memory

La funzionalità di controllo di attivazione a memoria insufficiente utilizza un livello di soglia fisso diverso a seconda del tipo di attivazione. Quando si crea un'applicazione server COM+, COM+ consente l'attivazione se è disponibile più del 10% della memoria virtuale. Se è disponibile meno del 10%, COM+ esegue un'allocazione di test per verificare se il file di paging può espandersi per adattarsi al nuovo carico di memoria. Se il file di paging viene espanso, viene creata l'applicazione server. Se non è possibile espandere il file di paging, l'attivazione ha esito negativo e la memoria non viene allocata.

Il processo è simile quando si crea un oggetto. In questo caso, COM+ consente l'attivazione se è disponibile più del 5% di memoria virtuale. Se è disponibile meno del 5%, COM+ procede con un'allocazione di test. Anche in questo caso, se l'allocazione di test espande il file di paging, viene creato l'oggetto. In caso contrario, l'attivazione avrà esito negativo.

Attualmente non è possibile configurare i livelli di soglia fissa per i controlli di attivazione a memoria insufficiente. Per questo motivo, non sono presenti attività associate a questa funzionalità.

 

 



