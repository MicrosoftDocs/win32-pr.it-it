---
description: 'Esistono due modi per implementare il multitasking: come un singolo processo con più thread o come più processi, ognuno con uno o più thread.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Quando usare il multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17e52f39a08120d3038663a95307ad72f228cfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313312"
---
# <a name="when-to-use-multitasking"></a>Quando usare il multitasking

Esistono due modi per implementare il multitasking: come un singolo processo con più thread o come più processi, ognuno con uno o più thread. Un'applicazione può inserire ogni thread che richiede uno spazio di indirizzi privato e risorse private nel proprio processo, per proteggerlo dalle attività di altri thread di processo.

Un processo multithread può gestire attività che si escludono a vicenda con i thread, ad esempio fornire un'interfaccia utente ed eseguire calcoli in background. La creazione di un processo multithread può anche essere un modo pratico per strutturare un programma che esegue diverse attività simili o identiche simultaneamente. Ad esempio, un server di named pipe può creare un thread per ogni processo client che si connette alla pipe. Questo thread gestisce la comunicazione tra il server e il client. Il processo può usare più thread per eseguire le attività seguenti:

-   Gestire l'input per più finestre.
-   Gestire l'input da più dispositivi di comunicazione.
-   Operare una distinzione tra attività con diversa priorità. Un thread ad alta priorità, ad esempio, gestisce attività in cui il tempo riveste molta importanza mentre un'attività a bassa priorità ne esegue altre.
-   Consentire all'interfaccia utente di continuare ad essere veloce, allocando più tempo alle attività in background.

È in genere più efficiente per un'applicazione implementare il multitasking creando un singolo processo multithread, anziché creare più processi, per i motivi seguenti:

-   Il sistema può eseguire più rapidamente un cambio di contesto per i thread rispetto ai processi, poiché un processo ha un sovraccarico maggiore rispetto a un thread (il contesto del processo è più grande del contesto del thread).
-   Tutti i thread di un processo condividono lo stesso spazio di indirizzi e possono accedere alle variabili globali del processo, che possono semplificare la comunicazione tra thread.
-   Tutti i thread di un processo possono condividere handle aperti per le risorse, ad esempio file e pipe.

Esistono altre tecniche che è possibile usare al posto del multithreading. I più significativi sono i seguenti: input e output asincroni (I/O), porte di completamento I/O, chiamate di procedure asincrone (APC) e la possibilità di attendere più eventi.

Un singolo thread può avviare più richieste di I/O che richiedono molto tempo che possono essere eseguite simultaneamente utilizzando l'I/O asincrono. Le operazioni di I/O asincrone possono essere eseguite su file, pipe e dispositivi di comunicazione seriale. Per altre informazioni, vedere [sincronizzazione e input e output sovrapposti](../sync/synchronization-and-overlapped-input-and-output.md).

Un thread singolo può bloccare la propria esecuzione mentre è in attesa che si verifichino tutti i diversi eventi. Questa operazione è più efficiente rispetto all'uso di più thread, ognuno in attesa di un singolo evento e più efficiente rispetto all'uso di un singolo thread che utilizza il tempo del processore controllando costantemente la presenza di eventi. Per altre informazioni, vedere [funzioni di attesa](../sync/wait-functions.md).

 

 
