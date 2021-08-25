---
description: I blocchi SRW (Slim Reader/Writer) consentono ai thread di un singolo processo di accedere alle risorse condivise. sono ottimizzati per la velocità e occupano pochissima memoria.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: Blocchi SRW (Slim Reader/Writer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc478d5f9bbfec1268f65b3e4a7f562b9bdca3d2df21f4570a52782eec9f028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959981"
---
# <a name="slim-readerwriter-srw-locks"></a>Blocchi SRW (Slim Reader/Writer)

I blocchi SRW (Slim Reader/Writer) consentono ai thread di un singolo processo di accedere alle risorse condivise. sono ottimizzati per la velocità e occupano pochissima memoria. I blocchi reader-writer non possono essere condivisi tra processi.

I thread di lettura leggono i dati da una risorsa condivisa, mentre i thread del writer scrivono dati in una risorsa condivisa. Quando più thread eseguono operazioni di lettura e scrittura usando una risorsa condivisa, i blocchi esclusivi, ad esempio una sezione critica o un mutex, possono diventare un collo di bottiglia se i thread di lettura vengono eseguiti in modo continuo, ma le operazioni di scrittura sono rare.

I blocchi SRW offrono due modalità in cui i thread possono accedere a una risorsa condivisa:

-   **Modalità condivisa**, che concede l'accesso condiviso in sola lettura a più thread di lettura, che consente loro di leggere contemporaneamente i dati dalla risorsa condivisa. Se le operazioni di lettura superano le operazioni di scrittura, questa concorrenza aumenta le prestazioni e la velocità effettiva rispetto alle sezioni critiche.
    > [!NOTE]
    > I blocchi SRW in modalità condivisa non devono essere acquisiti in modo ricorsivo, perché ciò può causare deadlock se combinati con l'acquisizione esclusiva.

-   **Modalità esclusiva**, che concede l'accesso in lettura/scrittura a un thread di scrittura alla volta. Quando il blocco è stato acquisito in modalità esclusiva, nessun altro thread può accedere alla risorsa condivisa fino a quando il writer non rilascia il blocco.
    > [!NOTE]
    > I blocchi SRW in modalità esclusiva non possono essere acquisiti in modo ricorsivo. Se un thread tenta di acquisire un blocco già incluso, tale tentativo avrà esito negativo (per [**TryAcquireSRWLockExclusive)**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)o deadlock (per [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive))

Un singolo blocco SRW può essere acquisito in entrambe le modalità. I thread di lettura possono acquisirlo in modalità condivisa, mentre i thread del writer possono acquisirlo in modalità esclusiva. Non esiste alcuna garanzia sull'ordine in cui ai thread che richiedono la proprietà verrà concessa la proprietà. I blocchi SRW non sono equi né FIFO.

Un blocco SRW è la dimensione di un puntatore. Il vantaggio è che è veloce aggiornare lo stato di blocco. Lo svantaggio è che è possibile archiviare pochissime informazioni sullo stato, quindi i blocchi SRW non rilevano un uso ricorsivo non corretto in modalità condivisa. Inoltre, un thread proprietario di un blocco SRW in modalità condivisa non può aggiornare la proprietà del blocco alla modalità esclusiva.

Il chiamante deve allocare una struttura SRWLOCK e inizializzarla chiamando [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) (per inizializzare la struttura in modo dinamico) o assegnare la costante **SRWLOCK \_ INIT** alla variabile di struttura (per inizializzare la struttura in modo statico).

È possibile usare [Application Verifier](/windows-hardware/drivers/devtest/application-verifier) per trovare l'uso ricorsivo (rientrante) dei blocchi SRW.

Di seguito sono riportate le funzioni di blocco SRW.

| Funzione di blocco SRW                                                | Descrizione                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Acquisisce un blocco SRW in modalità esclusiva.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Acquisisce un blocco SRW in modalità condivisa.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Inizializzare un blocco SRW.                                                                                                                           |
| [**ReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Rilascia un blocco SRW aperto in modalità esclusiva.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Rilascia un blocco SRW aperto in modalità condivisa.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Sospensione della variabile di condizione specificata e rilascio del blocco specificato come operazione atomica.                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Tenta di acquisire un blocco SRW (Slim Reader/Writer) in modalità esclusiva. Se la chiamata ha esito positivo, il thread chiamante diventa proprietario del blocco. |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Tenta di acquisire un blocco SRW (Slim Reader/Writer) in modalità condivisa. Se la chiamata ha esito positivo, il thread chiamante diventa proprietario del blocco.    |

 
