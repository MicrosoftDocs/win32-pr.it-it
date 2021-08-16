---
description: Un oggetto semaforo è un oggetto di sincronizzazione che mantiene un conteggio compreso tra zero e un valore massimo specificato.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Oggetti semaforo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c814be0ab2fafe7fbabfdeca5b640cfb550172a09e465dddc71629dfa5b0068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886260"
---
# <a name="semaphore-objects"></a>Oggetti semaforo

Un *oggetto semaforo* è un oggetto di sincronizzazione che mantiene un conteggio compreso tra zero e un valore massimo specificato. Il conteggio viene decrementato ogni volta che un thread completa un'attesa per l'oggetto semaforo e incrementato ogni volta che un thread rilascia il semaforo. Quando il conteggio raggiunge lo zero, nessun altro thread può attendere correttamente che lo stato dell'oggetto semaforo diventi segnalato. Lo stato di un semaforo denominato è impostato come segnalato quando il relativo conteggio è maggiore di zero e come non segnalato quando il relativo conteggio è zero.

L'oggetto semaforo è utile per controllare una risorsa condivisa in grado di supportare un numero limitato di utenti. Funge da gate che limita il numero di thread che condividono la risorsa a un numero massimo specificato. Ad esempio, un'applicazione potrebbe limitare il numero di finestre create. Usa un semaforo con un conteggio massimo uguale al limite della finestra, decrementando il conteggio ogni volta che viene creata una finestra e incrementarlo ogni volta che una finestra viene chiusa. L'applicazione specifica l'oggetto semaforo nella chiamata a una delle funzioni [di attesa](wait-functions.md) prima della creazione di ogni finestra. Quando il conteggio è zero, a indicare che è stato raggiunto il limite della finestra, la funzione di attesa blocca l'esecuzione del codice di creazione della finestra.

Un thread usa la [**funzione CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) o [**CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) per creare un oggetto semaforo. Il thread di creazione specifica il conteggio iniziale e il valore massimo del conteggio per l'oggetto . Il conteggio iniziale non deve essere minore di zero né maggiore del valore massimo. Il thread di creazione può anche specificare un nome per l'oggetto semaforo. I thread in altri processi possono aprire un handle a un oggetto semaforo esistente specificandone il nome in una chiamata alla [**funzione OpenSemaphore.**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) Per altre informazioni sui nomi per gli oggetti mutex, event, semaphore e timer, vedere [Sincronizzazione interprocesso.](interprocess-synchronization.md)

Se più thread sono in attesa in un semaforo, viene selezionato un thread in attesa. Non presupporre un ordine FIFO (First-In, First-Out). Gli eventi esterni, ad esempio le API in modalità kernel, possono modificare l'ordine di attesa.

Ogni volta che [](wait-functions.md) una delle funzioni di attesa viene restituita perché lo stato di un semaforo è stato impostato su segnalato, il conteggio del semaforo viene ridotto di uno. La [**funzione ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) aumenta il conteggio di un semaforo di una quantità specificata. Il conteggio non può mai essere minore di zero o maggiore del valore massimo.

Il conteggio iniziale di un semaforo viene in genere impostato sul valore massimo. Il conteggio viene quindi decrementato da tale livello quando viene utilizzata la risorsa protetta. In alternativa, è possibile creare un semaforo con un conteggio iniziale pari a zero per bloccare l'accesso alla risorsa protetta durante l'inizializzazione dell'applicazione. Dopo l'inizializzazione, è [**possibile usare ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) per incrementare il conteggio al valore massimo.

Un thread proprietario di un oggetto mutex può attendere ripetutamente che lo stesso oggetto mutex diventi segnalato senza che l'esecuzione diventi bloccata. Un thread che attende ripetutamente lo stesso oggetto semaforo, tuttavia, decrementa il conteggio del semaforo ogni volta che viene completata un'operazione di attesa. il thread viene bloccato quando il conteggio arriva a zero. Analogamente, solo il thread proprietario di un mutex può chiamare correttamente la funzione [**ReleaseMutex,**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) anche se qualsiasi thread può usare [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) per aumentare il conteggio di un oggetto semaforo.

Un thread può decrementare il conteggio di un semaforo più di una volta specificando ripetutamente lo stesso oggetto semaforo nelle chiamate a una delle funzioni [di attesa](wait-functions.md). Tuttavia, la chiamata di una delle funzioni di attesa a più oggetti con una matrice che contiene più handle dello stesso semaforo non comporta più decrementi.

Dopo aver terminato di usare l'oggetto semaforo, chiamare la [**funzione CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) per chiudere l'handle. L'oggetto semaforo viene eliminato quando l'ultimo handle è stato chiuso. La chiusura dell'handle non influisce sul conteggio dei semafori. Assicurarsi quindi di chiamare [**ReleaseSemaphore prima**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) di chiudere l'handle o prima che il processo termini. In caso contrario, le operazioni di attesa in sospeso avranno un timeout o continueranno per un periodo illimitato, a seconda che sia stato specificato o meno un valore di timeout.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di oggetti Semaphore](using-semaphore-objects.md)
</dt> </dl>

 

 
