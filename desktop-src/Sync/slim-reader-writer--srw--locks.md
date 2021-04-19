---
description: I blocchi di lettura/scrittura (SRW) Slim consentono ai thread di un singolo processo di accedere alle risorse condivise; sono ottimizzate per la velocità e occupano molto poca memoria.
ms.assetid: 2d439b21-291f-4ff0-910a-c1c27e800019
title: Blocchi di lettura/scrittura (SRW) Slim
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d76d956e1425531eae43b0daa6817002a92bc
ms.sourcegitcommit: 663239b4560bfd5314e86901c65805c9bbcab07d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/15/2021
ms.locfileid: "106320064"
---
# <a name="slim-readerwriter-srw-locks"></a>Blocchi di lettura/scrittura (SRW) Slim

I blocchi di lettura/scrittura (SRW) Slim consentono ai thread di un singolo processo di accedere alle risorse condivise; sono ottimizzate per la velocità e occupano molto poca memoria. I blocchi di lettura/scrittura Slim non possono essere condivisi tra i processi.

I thread di lettura leggono i dati da una risorsa condivisa, mentre i thread del writer scrivono i dati in una risorsa condivisa. Quando più thread leggono e scrivono usando una risorsa condivisa, i blocchi esclusivi come una sezione critica o un mutex possono diventare un collo di bottiglia se i thread di lettura vengono eseguiti in modo continuo, ma le operazioni di scrittura sono rare.

I blocchi SRW forniscono due modalità in cui i thread possono accedere a una risorsa condivisa:

-   **Modalità condivisa**, che concede l'accesso condiviso di sola lettura a più thread di lettura, che consente di leggere i dati dalla risorsa condivisa simultaneamente. Se le operazioni di lettura superano le operazioni di scrittura, la concorrenza aumenta le prestazioni e la velocità effettiva rispetto alle sezioni critiche.
    > [!NOTE]
    > I blocchi SRW in modalità condivisa non devono essere acquisiti in modo ricorsivo perché questo può causare deadlock in caso di combinazione con acquisizione esclusiva.

-   **Modalità esclusiva**, che concede l'accesso in lettura/scrittura a un thread del writer alla volta. Quando il blocco è stato acquisito in modalità esclusiva, nessun altro thread può accedere alla risorsa condivisa finché il writer non rilascia il blocco.
    > [!NOTE]
    > Impossibile acquisire in modo ricorsivo i blocchi SRW in modalità esclusiva. Se un thread tenta di acquisire un blocco che possiede già, il tentativo avrà esito negativo (per [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)) o un deadlock (per [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive))

In entrambe le modalità è possibile acquisire un singolo blocco SRW; i thread Reader possono acquisirlo in modalità condivisa, mentre i thread di scrittura possono acquisirlo in modalità esclusiva. Non esiste alcuna garanzia sull'ordine in cui i thread a cui viene richiesta la proprietà verranno concessi la proprietà; I blocchi SRW non sono corretti né FIFO.

Un blocco SRW è la dimensione di un puntatore. Il vantaggio è che è veloce aggiornare lo stato di blocco. Lo svantaggio è che è possibile archiviare pochissime informazioni sullo stato, quindi i blocchi SRW non rilevano l'utilizzo ricorsivo errato in modalità condivisa. Inoltre, un thread proprietario di un blocco SRW in modalità condivisa non può aggiornare la propria proprietà del blocco alla modalità esclusiva.

Il chiamante deve allocare una struttura SRWLOCK e inizializzarla chiamando [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock) (per inizializzare la struttura in modo dinamico) o assegnare la costante **SRWLock \_ init** alla variabile della struttura (per inizializzare la struttura in modo statico).

È possibile usare [Application Verifier](/windows-hardware/drivers/devtest/application-verifier) per trovare l'uso ricorsivo (rientrante) dei blocchi SRW.

Di seguito sono riportate le funzioni di blocco SRW.

| Funzione Lock SRW                                                | Descrizione                                                                                                                                       |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockexclusive)       | Acquisisce un blocco SRW in modalità esclusiva.                                                                                                           |
| [**AcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-acquiresrwlockshared)             | Acquisisce un blocco SRW in modalità condivisa.                                                                                                              |
| [**InitializeSRWLock**](/windows/win32/api/synchapi/nf-synchapi-initializesrwlock)                   | Inizializzare un blocco SRW.                                                                                                                           |
| [**ComplementareReleaseSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockexclusive)       | Rilascia un blocco SRW aperto in modalità esclusiva.                                                                                           |
| [**ReleaseSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-releasesrwlockshared)             | Rilascia un blocco SRW aperto in modalità condivisa.                                                                                              |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)   | Dorme sulla variabile di condizione specificata e rilascia il blocco specificato come operazione atomica.                                                |
| [**TryAcquireSRWLockExclusive**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive) | Tenta di acquisire un blocco di lettura/scrittura (SRW) Slim in modalità esclusiva. Se la chiamata ha esito positivo, il thread chiamante acquisisce la proprietà del blocco. |
| [**TryAcquireSRWLockShared**](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)       | Tenta di acquisire un blocco di lettura/scrittura (SRW) Slim in modalità condivisa. Se la chiamata ha esito positivo, il thread chiamante acquisisce la proprietà del blocco.    |

 
