---
description: Per evitare race conditions e deadlock, è necessario sincronizzare l'accesso di più thread alle risorse condivise. La sincronizzazione è necessaria anche per garantire che il codice interdipendente sia eseguito nella sequenza corretta.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Sincronizzazione dell'esecuzione di più thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04a7e80f3c1d4ffdd874d9627a8212e26ee4923a5f2349bdebc4ff09299936c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793094"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Sincronizzazione dell'esecuzione di più thread

Per evitare race conditions e deadlock, è necessario sincronizzare l'accesso di più thread alle risorse condivise. La sincronizzazione è necessaria anche per garantire che il codice interdipendente sia eseguito nella sequenza corretta.

Esistono diversi oggetti i cui handle possono essere usati per sincronizzare più thread. Questi oggetti includono:

-   Buffer di input della console
-   Eventi
-   Mutex
-   Processi
-   Semafori
-   Thread
-   Timer

Lo stato di ognuno di questi oggetti è segnalato o non segnalato. Quando si specifica un handle per uno di questi oggetti in una chiamata a una delle funzioni di attesa [,](../sync/wait-functions.md)l'esecuzione del thread chiamante viene bloccata finché non viene segnalato lo stato dell'oggetto specificato.

Alcuni di questi oggetti sono utili per bloccare un thread fino a quando non si verifica un evento. Ad esempio, un handle del buffer di input della console viene segnalato quando è presente un input non letto, ad esempio una pressione di tasti o un clic del pulsante del mouse. Gli handle di processo e thread vengono segnalati al termine del processo o del thread. In questo modo, ad esempio, un processo può creare un processo figlio e quindi bloccarne l'esecuzione fino al termine del nuovo processo.

Altri oggetti sono utili per proteggere le risorse condivise dall'accesso simultaneo. Ad esempio, più thread possono avere ognuno un handle per un oggetto mutex. Prima di accedere a una risorsa condivisa, [](../sync/wait-functions.md) i thread devono chiamare una delle funzioni di attesa per attendere che lo stato del mutex venga segnalato. Quando il mutex viene segnalato, viene rilasciato un solo thread in attesa per accedere alla risorsa. Lo stato del mutex viene reimpostato immediatamente in modo che non sia segnalato in modo che tutti gli altri thread in attesa rimangano bloccati. Quando il thread termina con la risorsa, deve impostare lo stato del mutex su segnalato per consentire ad altri thread di accedere alla risorsa.

Per i thread di un singolo processo, gli oggetti sezione critica offrono un mezzo di sincronizzazione più efficiente rispetto ai mutex. Una sezione critica viene usata come un mutex per consentire a un thread alla volta di usare la risorsa protetta. Un thread può usare la [**funzione EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) per richiedere la proprietà di una sezione critica. Se è già di proprietà di un altro thread, il thread richiedente viene bloccato. Un thread può usare la [**funzione TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) per richiedere la proprietà di una sezione critica, senza bloccarsi in caso di errore di recupero della sezione critica. Dopo aver ricevuto la proprietà, il thread è libero di usare la risorsa protetta. L'esecuzione degli altri thread del processo non è interessata a meno che non tentino di accedere alla stessa sezione critica.

La [**funzione WaitForInputIdle fa**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) in modo che un thread attenda l'inizializzazione di un processo specificato e attenda l'input dell'utente senza input in sospeso. La **chiamata di WaitForInputIdle** può essere utile per sincronizzare i processi padre e figlio, perché [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) restituisce un risultato senza attendere che il processo figlio completi l'inizializzazione.

Per altre informazioni, vedere [Sincronizzazione.](../sync/synchronization.md)

 

 
