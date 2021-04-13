---
description: Un gestore di eccezioni basato su frame consente di gestire la possibilità che un'eccezione possa verificarsi in una determinata sequenza di codice. Un gestore di eccezioni basato su frame è costituito dagli elementi seguenti.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Gestione delle eccezioni basata su frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b268b5d02de83bca22a1d3311905b05be1f748
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483508"
---
# <a name="frame-based-exception-handling"></a>Gestione delle eccezioni basata su frame

Un *gestore di eccezioni basato su frame* consente di gestire la possibilità che un'eccezione possa verificarsi in una determinata sequenza di codice. Un gestore di eccezioni basato su frame è costituito dagli elementi seguenti.

-   Corpo sorvegliato del codice
-   Espressione di filtro
-   Un blocco del gestore di eccezioni

I gestori di eccezioni basati su frame sono dichiarati nella sintassi specifica del linguaggio. Nel compilatore Microsoft C/C++ Optimizing, ad esempio, vengono implementate usando **\_ \_ try** e **\_ \_ except**. Per ulteriori informazioni, vedere [sintassi del gestore](handler-syntax.md).

Il *corpo sorvegliato del codice* è un set di una o più istruzioni per le quali l'espressione di filtro e il blocco del gestore di eccezioni forniscono la protezione per la gestione delle eccezioni. Il corpo sorvegliato può essere un blocco di codice, un set di blocchi annidati o un'intera routine o funzione. Utilizzando il compilatore di ottimizzazione Microsoft C/C++, un corpo sorvegliato è racchiuso tra parentesi graffe ( {} ) che seguono la parola chiave **\_ \_ try** .

L' *espressione di filtro* di un gestore di eccezioni basato su frame è un'espressione valutata dal sistema quando si verifica un'eccezione all'interno del corpo sorvegliato. Questa valutazione comporta una delle azioni seguenti da parte del sistema.

-   Il sistema arresta la ricerca di un gestore di eccezioni, ripristina lo stato del computer e continua l'esecuzione del thread nel momento in cui si è verificata l'eccezione.
-   Il sistema continua la ricerca di un gestore di eccezioni.
-   Il sistema trasferisce il controllo al gestore di eccezioni e l'esecuzione del thread continua in sequenza nei stack frame in cui viene trovato il gestore di eccezioni. Se il gestore non si trova nel stack frame in cui si è verificata l'eccezione, il sistema rimuove lo stack, lasciando l'stack frame corrente e gli altri stack frame fino a quando non torna al stack frame del gestore di eccezioni. Prima dell'esecuzione di un gestore di eccezioni, i gestori di terminazione vengono eseguiti per tutti i corpi di codice sorvegliati che terminano come risultato del trasferimento del controllo al gestore di eccezioni. Per ulteriori informazioni sui gestori di terminazione, vedere la sezione relativa alla [gestione della terminazione](termination-handling.md).

L'espressione di filtro può essere un'espressione semplice oppure può richiamare una *funzione di filtro* che tenta di gestire l'eccezione. È possibile chiamare le funzioni [**GetExceptionCode**](getexceptioncode.md) e [**GetExceptionInformation**](getexceptioninformation.md) dall'interno di un'espressione di filtro per ottenere informazioni sull'eccezione da filtrare. **GetExceptionCode** restituisce un codice che identifica il tipo di eccezione e **GetExceptionInformation** restituisce un puntatore a una struttura [**di \_ puntatori di eccezione**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) che contiene i puntatori alle strutture di [**\_ record**](/windows/desktop/api/WinNT/ns-winnt-exception_record) di [**contesto**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) e di eccezione.

Queste funzioni non possono essere chiamate dall'interno di una funzione di filtro, ma i valori restituiti possono essere passati come parametri a una funzione di filtro. [**GetExceptionCode**](getexceptioncode.md) può essere usato all'interno del blocco del gestore di eccezioni, ma [**GetExceptionInformation**](getexceptioninformation.md) non può perché le informazioni a cui fa riferimento sono in genere nello stack e vengono distrutte quando il controllo viene trasferito a un gestore di eccezioni. Tuttavia, un'applicazione può copiare le informazioni nell'archiviazione sicura per renderla disponibile al gestore di eccezioni.

Il vantaggio di una funzione di filtro è che può gestire un'eccezione e restituire un valore che determina la continuazione dell'esecuzione del sistema dal punto in cui si è verificata l'eccezione. Con un blocco del gestore di eccezioni, l'esecuzione continua in sequenza dal gestore di eccezioni anziché dal punto dell'eccezione.

La gestione di un'eccezione può essere semplice quanto si noti un errore e impostare un flag che verrà esaminato in seguito, stampando un messaggio di avviso o di errore o eseguendo un'altra azione limitata. Se è possibile continuare l'esecuzione, potrebbe essere necessario modificare lo stato del computer modificando il record di contesto. Per un esempio di funzione di filtro che gestisce un'eccezione di errore di pagina, vedere [utilizzo delle funzioni di memoria virtuale](../memory/using-the-memory-management-functions.md).

La funzione [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) può essere utilizzata come funzione di filtro in un'espressione di filtro. Restituisce \_ \_ il gestore di esecuzione dell'eccezione, a meno che non sia in corso il debug del processo. in tal caso, viene restituita l'eccezione \_ \_ ricerca continua.

 

 
