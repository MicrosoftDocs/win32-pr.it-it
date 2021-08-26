---
description: 'Esistono due modi per implementare il multitasking: come singolo processo con più thread o come più processi, ognuno con uno o più thread.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Quando usare il multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3e37f63ada4aa1a17355ac3bc5b7361d498a1a20ec87b490965b53c4811ebb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031341"
---
# <a name="when-to-use-multitasking"></a>Quando usare il multitasking

Esistono due modi per implementare il multitasking: come singolo processo con più thread o come più processi, ognuno con uno o più thread. Un'applicazione può inserire ogni thread che richiede uno spazio indirizzi privato e risorse private nel proprio processo, per proteggerlo dalle attività di altri thread di processo.

Un processo multithreading può gestire attività che si escludono a vicenda con i thread, ad esempio fornire un'interfaccia utente ed eseguire calcoli in background. La creazione di un processo multithreading può anche essere un modo pratico per strutturare un programma che esegue contemporaneamente diverse attività simili o identiche. Ad esempio, un named pipe può creare un thread per ogni processo client collegato alla pipe. Questo thread gestisce la comunicazione tra il server e il client. Il processo può usare più thread per eseguire le attività seguenti:

-   Gestire l'input per più finestre.
-   Gestire l'input da diversi dispositivi di comunicazione.
-   Operare una distinzione tra attività con diversa priorità. Un thread ad alta priorità, ad esempio, gestisce attività in cui il tempo riveste molta importanza mentre un'attività a bassa priorità ne esegue altre.
-   Consentire all'interfaccia utente di continuare ad essere veloce, allocando più tempo alle attività in background.

In genere è più efficiente per un'applicazione implementare il multitasking creando un singolo processo multithreading, anziché creare più processi, per i motivi seguenti:

-   Il sistema può eseguire un cambio di contesto più rapidamente per i thread rispetto ai processi, perché un processo ha un sovraccarico maggiore rispetto a un thread (il contesto del processo è più grande del contesto del thread).
-   Tutti i thread di un processo condividono lo stesso spazio di indirizzi e possono accedere alle variabili globali del processo, semplificando la comunicazione tra i thread.
-   Tutti i thread di un processo possono condividere handle aperti per le risorse, ad esempio file e pipe.

Esistono altre tecniche che è possibile usare al posto del multithreading. I più significativi sono i seguenti: input e output asincrono (I/O), porte di completamento I/O, chiamate di procedura asincrone (APC) e possibilità di attendere più eventi.

Un singolo thread può avviare più richieste di I/O dispendiose in termini di tempo che possono essere eseguite contemporaneamente usando operazioni di I/O asincrone. L'I/O asincrono può essere eseguito su file, pipe e dispositivi di comunicazione seriale. Per altre informazioni, vedere [Sincronizzazione e input e output sovrapposti.](../sync/synchronization-and-overlapped-input-and-output.md)

Un singolo thread può bloccare la propria esecuzione durante l'attesa che si verifichi uno o tutti gli eventi. Ciò è più efficiente rispetto all'uso di più thread, ognuno in attesa di un singolo evento, e più efficiente rispetto all'uso di un singolo thread che utilizza il tempo del processore controllando continuamente la presenza di eventi. Per altre informazioni, vedere [Funzioni di attesa](../sync/wait-functions.md).

 

 
