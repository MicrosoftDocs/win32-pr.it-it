---
description: Un gestore eccezioni basato su frame consente di gestire la possibilità che si verifichi un'eccezione in una determinata sequenza di codice. Un gestore di eccezioni basato su frame è costituito dai seguenti elementi.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Gestione delle eccezioni basata su frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb72118aca7653e9bc15e7f4ff4b75e46b1abad5bab7dee4a3397ae5f98e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573121"
---
# <a name="frame-based-exception-handling"></a>Gestione delle eccezioni basata su frame

Un *gestore eccezioni basato su* frame consente di gestire la possibilità che si verifichi un'eccezione in una determinata sequenza di codice. Un gestore di eccezioni basato su frame è costituito dai seguenti elementi.

-   Corpo di codice sorvegliato
-   Espressione di filtro
-   Blocco del gestore eccezioni

I gestori eccezioni basati su frame vengono dichiarati nella sintassi specifica del linguaggio. Ad esempio, nel compilatore microsoft C/C++ Optimizing vengono implementati usando **\_ \_ try** e **\_ \_ tranne**. Per altre informazioni, vedere [Sintassi del gestore](handler-syntax.md).

Il *corpo sorvegliato del* codice è un set di una o più istruzioni per le quali l'espressione di filtro e il blocco del gestore eccezioni forniscono la protezione della gestione delle eccezioni. Il corpo sorvegliato può essere un blocco di codice, un set di blocchi annidati o un'intera routine o funzione. Usando il compilatore microsoft C/C++ Optimizing, un corpo sorvegliato è racchiuso tra parentesi graffe ( {} ) dopo la parola chiave **\_ \_ try.**

*L'espressione di* filtro di un gestore eccezioni basato su frame è un'espressione valutata dal sistema quando si verifica un'eccezione all'interno del corpo sorvegliato. Questa valutazione comporta una delle azioni seguenti da parte del sistema.

-   Il sistema arresta la ricerca di un gestore eccezioni, ripristina lo stato del computer e continua l'esecuzione del thread nel punto in cui si è verificata l'eccezione.
-   Il sistema continua la ricerca di un gestore eccezioni.
-   Il sistema trasferisce il controllo al gestore eccezioni e l'esecuzione del thread continua in sequenza nel stack frame in cui viene trovato il gestore eccezioni. Se il gestore non si trova nel stack frame in cui si è verificata l'eccezione, il sistema annulla lo stack, lasciando il stack frame corrente e qualsiasi altro stack frame fino a quando non torna al stack frame del gestore di eccezioni. Prima dell'esecuzione di un gestore di eccezioni, i gestori di terminazione vengono eseguiti per tutti i corpi sorvegliati di codice terminati in seguito al trasferimento del controllo al gestore eccezioni. Per altre informazioni sui gestori di terminazione, vedere [Gestione delle terminazioni](termination-handling.md).

L'espressione di filtro può essere un'espressione semplice oppure può richiamare una *funzione di filtro* che tenta di gestire l'eccezione. È possibile chiamare le [**funzioni GetExceptionCode**](getexceptioncode.md) e [**GetExceptionInformation**](getexceptioninformation.md) dall'interno di un'espressione di filtro per ottenere informazioni sull'eccezione filtrata. **GetExceptionCode** restituisce un codice che identifica il tipo di eccezione e **GetExceptionInformation** restituisce un puntatore a una struttura [**EXCEPTION \_ POINTERS**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) che contiene puntatori alle strutture [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) e [**EXCEPTION \_ RECORD.**](/windows/desktop/api/WinNT/ns-winnt-exception_record)

Queste funzioni non possono essere chiamate dall'interno di una funzione di filtro, ma i relativi valori restituiti possono essere passati come parametri a una funzione di filtro. [**GetExceptionCode**](getexceptioncode.md) può essere usato all'interno del blocco del gestore eccezioni, ma Non è possibile usare [**GetExceptionInformation**](getexceptioninformation.md) perché le informazioni a cui punta si trovano in genere nello stack e vengono distrutte quando il controllo viene trasferito a un gestore eccezioni. Tuttavia, un'applicazione può copiare le informazioni nell'archiviazione sicura per renderle disponibili al gestore delle eccezioni.

Il vantaggio di una funzione di filtro è che può gestire un'eccezione e restituire un valore che fa sì che il sistema continui l'esecuzione dal punto in cui si è verificata l'eccezione. Con un blocco del gestore eccezioni, invece, l'esecuzione continua in sequenza dal gestore delle eccezioni anziché dal punto dell'eccezione.

La gestione di un'eccezione può essere semplice come la notazione di un errore e l'impostazione di un flag che verrà esaminato in un secondo momento, la stampa di un avviso o un messaggio di errore o l'esecuzione di altre azioni limitate. Se è possibile continuare l'esecuzione, potrebbe essere necessario modificare anche lo stato del computer modificando il record di contesto. Per un esempio di funzione di filtro che gestisce un'eccezione di errore di pagina, vedere [Uso delle funzioni di memoria virtuale](../memory/using-the-memory-management-functions.md).

La [**funzione UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) può essere usata come funzione di filtro in un'espressione di filtro. Restituisce EXCEPTION EXECUTE HANDLER a meno che il processo non sia in fase di debug, nel qual \_ caso restituisce EXCEPTION CONTINUE \_ \_ \_ SEARCH.

 

 
