---
description: L'I/O Alertable è il metodo mediante il quale i thread dell'applicazione elaborano le richieste I/O asincrone solo quando sono in uno stato di avviso.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: I/O Alertable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308913"
---
# <a name="alertable-io"></a>I/O Alertable

L'I/O Alertable è il metodo mediante il quale i thread dell'applicazione elaborano le richieste I/O asincrone solo quando sono in uno stato di avviso.

Per comprendere quando un thread è in uno stato di avviso, si consideri lo scenario seguente:

1.  Un thread avvia una richiesta di lettura asincrona chiamando [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) con un puntatore a una funzione di callback.
2.  Il thread avvia una richiesta di scrittura asincrona chiamando [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) con un puntatore a una funzione di callback.
3.  Il thread chiama una funzione che recupera una riga di dati da un server di database remoto.

In questo scenario, le chiamate a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) torneranno probabilmente prima della chiamata di funzione nel passaggio 3. In tal caso, il kernel inserisce i puntatori alle funzioni di callback nella coda di chiamata di procedura asincrona (APC) del thread. Il kernel mantiene questa coda in modo specifico per contenere i dati della richiesta I/O restituiti fino a quando non può essere elaborata dal thread corrispondente.

Quando il recupero delle righe viene completato e il thread viene restituito dalla funzione, la priorità più elevata consiste nell'elaborare le richieste di I/O restituite nella coda chiamando le funzioni di callback. A tale scopo, deve immettere uno stato di avviso. Un thread può eseguire questa operazione solo chiamando una delle funzioni seguenti con i flag appropriati:

-   [**SleepEx**](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

Quando il thread entra in uno stato di avviso, si verificano gli eventi seguenti:

1.  Il kernel controlla la coda APC del thread. Se la coda contiene puntatori a funzioni di callback, il kernel rimuove il puntatore dalla coda e lo invia al thread.
2.  Il thread esegue la funzione di callback.
3.  I passaggi 1 e 2 vengono ripetuti per ogni puntatore rimanente nella coda.
4.  Quando la coda è vuota, il thread viene restituito dalla funzione che lo ha inserito in uno stato di avviso.

In questo scenario, quando il thread entra in uno stato di avviso, chiamerà le funzioni di callback inviate a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), quindi restituirà dalla funzione che lo ha inserito in uno stato di avviso.

Se un thread entra in uno stato di avviso mentre la coda APC è vuota, l'esecuzione del thread verrà sospesa dal kernel fino a quando non si verifica una delle condizioni seguenti:

-   L'oggetto kernel in attesa di diventa segnalato.
-   Un puntatore alla funzione di callback viene inserito nella coda APC.

Un thread che usa l'I/O con avvisi elabora le richieste di I/o asincrone in modo più efficiente rispetto a quando attendono semplicemente il flag di evento nella struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) e il meccanismo di i/o di avviso è meno complesso delle [porte di completamento i/o](i-o-completion-ports.md) da usare. Tuttavia, l'I/O con avvisi restituisce il risultato della richiesta di I/O solo al thread che lo ha avviato. Le porte di completamento I/O non presentano questa limitazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Chiamate di procedure asincrone](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
