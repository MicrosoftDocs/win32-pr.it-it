---
description: Un oggetto semaforo è un oggetto di sincronizzazione che mantiene un conteggio compreso tra zero e un valore massimo specificato.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Oggetti semaforo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f36313d76c5d98c786a76f10ad8439965f180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317663"
---
# <a name="semaphore-objects"></a>Oggetti semaforo

Un *oggetto semaforo* è un oggetto di sincronizzazione che mantiene un conteggio compreso tra zero e un valore massimo specificato. Il conteggio viene decrementato ogni volta che un thread completa un'attesa per l'oggetto semaforo e viene incrementato ogni volta che un thread rilascia il semaforo. Quando il conteggio raggiunge lo zero, nessun altro thread può attendere che lo stato dell'oggetto semaforo venga segnalato. Lo stato di un semaforo denominato è impostato come segnalato quando il relativo conteggio è maggiore di zero e come non segnalato quando il relativo conteggio è zero.

L'oggetto semaforo è utile per il controllo di una risorsa condivisa in grado di supportare un numero limitato di utenti. Funge da Gate che limita il numero di thread che condividono la risorsa a un numero massimo specificato. Ad esempio, un'applicazione può inserire un limite per il numero di finestre che crea. Usa un semaforo con un conteggio massimo uguale al limite della finestra, decrementa il conteggio ogni volta che viene creata una finestra e la incrementa a ogni chiusura di una finestra. L'applicazione specifica l'oggetto semaforo nella chiamata a una delle [funzioni di attesa](wait-functions.md) prima della creazione di ogni finestra. Quando il conteggio è zero, a indicare che è stato raggiunto il limite della finestra, la funzione wait blocca l'esecuzione del codice di creazione della finestra.

Un thread usa la funzione [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) o [**CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) per creare un oggetto semaforo. Il thread di creazione specifica il numero iniziale e il valore massimo del conteggio per l'oggetto. Il numero iniziale deve essere minore di zero o maggiore del valore massimo. Il thread di creazione può inoltre specificare un nome per l'oggetto semaforo. I thread di altri processi possono aprire un handle per un oggetto semaforo esistente specificandone il nome in una chiamata alla funzione [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) . Per ulteriori informazioni sui nomi per gli oggetti mutex, Event, Semaphore e timer, vedere [sincronizzazione interprocesso](interprocess-synchronization.md).

Se più di un thread è in attesa su un semaforo, viene selezionato un thread in attesa. Non presupporre un ordine FIFO (First-in, First-out). Gli eventi esterni, ad esempio APC in modalità kernel, possono modificare l'ordine di attesa.

Ogni volta che una delle [funzioni di attesa](wait-functions.md) restituisce perché lo stato di un semaforo è stato impostato su segnalato, il conteggio del semaforo viene ridotto di uno. La funzione [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) aumenta il conteggio di un semaforo in base a un importo specificato. Il conteggio non può mai essere minore di zero o maggiore del valore massimo.

Il numero iniziale di un semaforo viene in genere impostato sul valore massimo. Il conteggio viene quindi decrementato da tale livello man mano che la risorsa protetta viene utilizzata. In alternativa, è possibile creare un semaforo con un conteggio iniziale pari a zero per bloccare l'accesso alla risorsa protetta mentre è in corso l'inizializzazione dell'applicazione. Dopo l'inizializzazione, è possibile usare [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) per incrementare il conteggio fino al valore massimo.

Un thread proprietario di un oggetto mutex può attendere ripetutamente che lo stesso oggetto mutex venga segnalato senza che l'esecuzione venga bloccata. Un thread che attende ripetutamente lo stesso oggetto semaforo, tuttavia, decrementa il conteggio del semaforo ogni volta che viene completata un'operazione di attesa. il thread viene bloccato quando il conteggio raggiunge lo zero. Analogamente, solo il thread proprietario di un mutex può chiamare correttamente la funzione [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) , anche se qualsiasi thread può utilizzare [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) per aumentare il numero di un oggetto semaforo.

Un thread può decrementare il conteggio di un semaforo più di una volta, specificando ripetutamente lo stesso oggetto semaforo nelle chiamate a una qualsiasi delle [funzioni di attesa](wait-functions.md). Tuttavia, la chiamata di una delle funzioni di attesa di più oggetti con una matrice che contiene più handle dello stesso semaforo non comporta decrementi multipli.

Al termine dell'utilizzo dell'oggetto semaforo, chiamare la funzione [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) per chiudere l'handle. L'oggetto semaforo viene eliminato definitivamente quando l'ultimo handle è stato chiuso. La chiusura dell'handle non influisce sul conteggio dei semafori; Assicurarsi pertanto di chiamare [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) prima di chiudere l'handle o prima che il processo venga terminato. In caso contrario, le operazioni di attesa in sospeso verranno interrotte o continueranno a tempo indefinito, a seconda che sia stato specificato un valore di timeout.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di oggetti semaforo](using-semaphore-objects.md)
</dt> </dl>

 

 
