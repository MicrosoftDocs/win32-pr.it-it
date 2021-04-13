---
title: Regole per la gestione dei conteggi dei riferimenti
description: L'utilizzo di un conteggio dei riferimenti per gestire la durata di un oggetto consente a più client di ottenere e rilasciare l'accesso a un singolo oggetto senza dover coordinarsi tra loro per gestire la durata dell'oggetto.
ms.assetid: bbe7d16c-fcb7-474d-a22d-5a3b33dd800e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9520cbbc88cb73c6e2abbd7908bed3754bb3945
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399754"
---
# <a name="rules-for-managing-reference-counts"></a>Regole per la gestione dei conteggi dei riferimenti

L'utilizzo di un conteggio dei riferimenti per gestire la durata di un oggetto consente a più client di ottenere e rilasciare l'accesso a un singolo oggetto senza dover coordinarsi tra loro per gestire la durata dell'oggetto. Finché l'oggetto client è conforme a determinate regole d'uso, l'oggetto, in effetti, fornisce tale gestione. Queste regole specificano come gestire i riferimenti tra oggetti. (COM non specifica implementazioni interne di oggetti, anche se queste regole rappresentano un punto di partenza ragionevole per un criterio all'interno di un oggetto).

Concettualmente, i puntatori all'interfaccia possono essere considerati come risiedono all'interno di variabili puntatore che includono tutto lo stato di calcolo interno che contiene un puntatore a interfaccia. Sono incluse le variabili in posizioni di memoria, i registri interni del processore e le variabili generate dal programmatore e generate dal compilatore. L'assegnazione o l'inizializzazione di una variabile puntatore implica la creazione di una nuova copia di un puntatore già esistente. Dove era presente una copia del puntatore in una variabile (il valore usato nell'assegnazione/inizializzazione), ora sono due. Un'assegnazione a una variabile puntatore Elimina la copia del puntatore attualmente nella variabile, così come la distruzione della variabile stessa. Ovvero, l'ambito in cui viene trovata la variabile, ad esempio il stack frame, viene eliminato definitivamente.

Dal punto di vista del client COM, il conteggio dei riferimenti viene sempre eseguito per ogni interfaccia. I client non devono mai presupporre che un oggetto usi lo stesso contatore per tutte le interfacce.

Il caso predefinito è che [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) deve essere chiamato per ogni nuova copia di un puntatore a interfaccia e la [**versione**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) deve essere chiamata per ogni eliminazione di un puntatore a interfaccia, tranne nel caso in cui le regole seguenti consentano altrimenti:

-   **Parametri in uscita per le funzioni.** Il chiamante deve chiamare [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sul parametro perché verrà rilasciato (con una chiamata a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)) nel codice di implementazione quando il valore out viene archiviato al suo interno.
-   **Recupero di una variabile globale.** Quando si crea una copia locale di un puntatore a interfaccia da una copia esistente del puntatore in una variabile globale, è necessario chiamare [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sulla copia locale perché un'altra funzione potrebbe eliminare la copia nella variabile globale mentre la copia locale è ancora valida.
-   **I nuovi puntatori sintetizzano una "aria sottile".** Una funzione che sintetizza un puntatore di interfaccia usando una conoscenza interna speciale anziché ottenerla da un'altra origine deve chiamare [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) inizialmente sul puntatore appena sintetizzato. Esempi importanti di tali routine includono routine di creazione di istanze, implementazioni di [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))e così via.
-   **Recupero di una copia di un puntatore archiviato internamente.** Quando una funzione recupera una copia di un puntatore archiviato internamente dall'oggetto chiamato, il codice dell'oggetto deve chiamare [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) sul puntatore prima che la funzione restituisca. Una volta recuperato il puntatore, l'oggetto di origine non è in grado di determinare il modo in cui la sua durata è correlata a quella della copia interna del puntatore.

Per le uniche eccezioni al caso predefinito è necessario che il codice di gestione conosca le relazioni delle durate di due o più copie di un puntatore alla stessa interfaccia di un oggetto e assicuri semplicemente che l'oggetto non venga eliminato definitivamente consentendo al conteggio dei riferimenti di andare a zero. Esistono in genere due casi, come indicato di seguito:

-   Quando una copia di un puntatore esiste già e un secondo viene creato successivamente e viene eliminato definitivamente mentre la prima copia esiste ancora, le chiamate a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)per la seconda copia possono essere omesse.
-   Quando una copia di un puntatore esiste e viene creato un secondo e il primo viene eliminato definitivamente prima del secondo, le chiamate a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)per la seconda copia e al [**rilascio**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) per la prima copia possono essere omesse.

Di seguito sono riportati alcuni esempi specifici di queste situazioni, le prime due sono particolarmente comuni:

-   **In parametri per le funzioni.** Il ciclo di vita della copia di un puntatore a interfaccia passato come parametro a una funzione è annidato in quello del puntatore utilizzato per inizializzare il valore, pertanto non è necessario un conteggio dei riferimenti separato sul parametro.
-   **Parametri out da funzioni, inclusi i valori restituiti.** Per impostare il parametro out, è necessario che la funzione disponga di una copia stabile del puntatore a interfaccia. Al ritorno, il chiamante è responsabile del rilascio del puntatore. Il parametro out non necessita pertanto di un conteggio dei riferimenti separato.
-   **Variabili locali.** Un'implementazione del metodo ha il controllo delle durate di ogni variabile del puntatore allocata nel stack frame e può usarla per determinare come omettere le coppie di versioni [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)ridondanti / [](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .
-   **Puntatori.** Alcune strutture di dati contengono due oggetti, ognuno con un puntatore all'altro. Se la durata del primo oggetto è nota per contenere la durata del secondo, non è necessario disporre di un conteggio dei riferimenti sul puntatore del secondo oggetto al primo oggetto. Spesso, evitando questo ciclo è importante mantenere il comportamento di deallocazione appropriato. Tuttavia, i puntatori non conteggiati devono essere usati con estrema cautela perché la parte del sistema operativo che gestisce l'elaborazione remota non è in grado di conoscere questa relazione. Pertanto, in quasi tutti i casi, la soluzione preferita è rappresentata dal fatto che il backpointer Visualizza un secondo oggetto "Friend" del primo puntatore (evitando così la circolare). L'architettura degli oggetti collegabili di COM, ad esempio, usa questo approccio.

Quando si implementano o si usano oggetti con conteggio dei riferimenti, può essere utile applicare *conteggi dei riferimenti artificiali*, che garantiscono la stabilità degli oggetti durante l'elaborazione di una funzione. Quando si implementa un metodo di un'interfaccia, è possibile chiamare le funzioni che hanno la possibilità di decrementare il conteggio dei riferimenti a un oggetto, causando una versione prematura dell'oggetto e l'errore dell'implementazione. Un modo efficace per evitare questo problema consiste nell'inserire una chiamata a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) all'inizio dell'implementazione del metodo e associarla a una chiamata a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) immediatamente prima della restituzione del metodo.

In alcune situazioni, i valori restituiti di [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) possono risultare instabili e non devono essere basati su di essi. devono essere utilizzati solo a scopo di debug o di diagnostica.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della durata degli oggetti tramite il conteggio dei riferimenti](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 