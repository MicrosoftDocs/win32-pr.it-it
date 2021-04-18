---
description: Per evitare race condition e deadlock, è necessario sincronizzare l'accesso da più thread a risorse condivise. La sincronizzazione è necessaria anche per garantire che il codice interdipendente venga eseguito nella sequenza corretta.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Sincronizzazione dell'esecuzione di più thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a1b3dd51d666d507771476792e679f7980fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311955"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Sincronizzazione dell'esecuzione di più thread

Per evitare race condition e deadlock, è necessario sincronizzare l'accesso da più thread a risorse condivise. La sincronizzazione è necessaria anche per garantire che il codice interdipendente venga eseguito nella sequenza corretta.

Sono disponibili diversi oggetti i cui handle possono essere utilizzati per sincronizzare più thread. Questi oggetti includono:

-   Buffer di input della console
-   Eventi
-   Mutex
-   Processi
-   Semafori
-   Thread
-   Timer

Lo stato di ognuno di questi oggetti è segnalato o non segnalato. Quando si specifica un handle per uno di questi oggetti in una chiamata a una delle [funzioni Wait](../sync/wait-functions.md), l'esecuzione del thread chiamante viene bloccata fino a quando non viene segnalato lo stato dell'oggetto specificato.

Alcuni di questi oggetti sono utili per bloccare un thread fino a quando non si verifica un evento. Ad esempio, un handle del buffer di input della console viene segnalato quando è presente un input non letto, ad esempio una sequenza di tasti o un clic del pulsante del mouse. Gli handle di processo e di thread vengono segnalati al termine del processo o del thread. Questo consente a un processo, ad esempio, di creare un processo figlio e quindi di bloccare la propria esecuzione fino a quando il nuovo processo non viene terminato.

Altri oggetti sono utili per proteggere le risorse condivise dall'accesso simultaneo. Ad esempio, più thread possono avere un handle per un oggetto mutex. Prima di accedere a una risorsa condivisa, i thread devono chiamare una delle [funzioni di attesa](../sync/wait-functions.md) per attendere che lo stato del mutex venga segnalato. Quando il mutex viene segnalato, viene rilasciato un solo thread in attesa per accedere alla risorsa. Lo stato del mutex viene immediatamente reimpostato su non segnalato, in modo che tutti gli altri thread in attesa rimangano bloccati. Quando il thread è terminato con la risorsa, deve impostare lo stato del mutex su segnalato per consentire ad altri thread di accedere alla risorsa.

Per i thread di un singolo processo, gli oggetti della sezione critica forniscono un mezzo di sincronizzazione più efficiente rispetto a mutex. Una sezione critica viene utilizzata come un mutex per abilitare un thread alla volta per l'utilizzo della risorsa protetta. Un thread può usare la funzione [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) per richiedere la proprietà di una sezione critica. Se è già di proprietà di un altro thread, il thread richiedente è bloccato. Un thread può usare la funzione [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) per richiedere la proprietà di una sezione critica, senza bloccarsi in caso di errore per ottenere la sezione critica. Dopo la ricezione della proprietà, il thread è libero di usare la risorsa protetta. L'esecuzione degli altri thread del processo non è interessata, a meno che non tenti di entrare nella stessa sezione critica.

La funzione [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) rende un thread in attesa finché un processo specificato non viene inizializzato e in attesa dell'input dell'utente senza input in sospeso. La chiamata di **WaitForInputIdle** può essere utile per la sincronizzazione dei processi padre e figlio, perché [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) restituisce senza attendere il completamento dell'inizializzazione da parte del processo figlio.

Per ulteriori informazioni, vedere [sincronizzazione](../sync/synchronization.md).

 

 
