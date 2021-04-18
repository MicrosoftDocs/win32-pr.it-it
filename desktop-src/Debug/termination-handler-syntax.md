---
description: "\\_ \\_ \\_ \\_ Per costruire un gestore di terminazione vengono usate le parole chiave try e finally. Nell'esempio seguente viene illustrata la struttura di un gestore di terminazione."
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Sintassi Termination-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcbf2656636490738a292c274a3e3184a34c0f94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304864"
---
# <a name="termination-handler-syntax"></a>Sintassi Termination-Handler

Per costruire un gestore di terminazione vengono usate le parole chiave **\_ \_ try** e **\_ \_ finally** . Nell'esempio seguente viene illustrata la struttura di un gestore di terminazione.


```C++
__try 
{ 
    // guarded body of code 
 
} 
__finally 
{ 
    // __finally block 
 
}
```



Per esempi, vedere [uso di un gestore di terminazione](using-a-termination-handler.md).

Come per il gestore di eccezioni, il blocco **\_ \_ try** e il blocco **\_ \_ finally** richiedono parentesi graffe ( {} ) e l'utilizzo di un'istruzione **goto** per passare a uno dei blocchi non è consentito.

Il blocco **\_ \_ try** contiene il corpo sorvegliato del codice protetto dal gestore di terminazione. Una funzione può avere un numero qualsiasi di gestori di terminazione e questi blocchi di gestione delle terminazioni possono essere annidati all'interno della stessa funzione o in funzioni diverse.

Il blocco **\_ \_ finally** viene eseguito ogni volta che il flusso di controllo lascia il blocco **\_ \_ try** . Tuttavia, il blocco **\_ \_ finally** non viene eseguito se si chiama una delle funzioni seguenti all'interno del blocco **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)o **Abort**.

Il blocco **\_ \_ finally** viene eseguito nel contesto della funzione in cui si trova il gestore di terminazione. Questo significa che il blocco **\_ \_ finally** può accedere alle variabili locali della funzione. L'esecuzione del blocco **\_ \_ finally** può terminare con uno dei metodi seguenti.

-   Esecuzione dell'ultima istruzione nel blocco e della continuazione all'istruzione successiva
-   Uso di un'istruzione di controllo (**return**, **break**, **continue** o **goto**)
-   Uso di **longjmp** o di un salto a un gestore di eccezioni

Se l'esecuzione del blocco **\_ \_ try** viene terminata a causa di un'eccezione che richiama il blocco di gestione delle eccezioni di un gestore di eccezioni basato su frame, il blocco **\_ \_ finally** viene eseguito prima dell'esecuzione del blocco di gestione delle eccezioni. Analogamente, una chiamata alla funzione della libreria di runtime C **longjmp** dal blocco **\_ \_ try** causa l'esecuzione del blocco **\_ \_ finally** prima che l'esecuzione venga ripresa alla destinazione dell'operazione **longjmp** . Se l'esecuzione del blocco **\_ \_ try** viene terminata a causa di un'istruzione di controllo (**return**, **break**, **continue** o **goto**), viene eseguito il blocco **\_ \_ finally** .

La funzione [**AbnormalTermination**](abnormaltermination.md) può essere usata all'interno del blocco **\_ \_ finally** per determinare se il blocco **\_ \_ try** è stato terminato in sequenza, ovvero se ha raggiunto la parentesi graffa di chiusura (}). Quando si lascia il blocco **\_ \_ try** a causa di una chiamata a **longjmp**, un passaggio a un gestore di eccezioni o un'istruzione **return**, **break**, **continue** o **goto** viene considerata una terminazione anomala. Si noti che l'errore di terminazione sequenziale induce il sistema a cercare tutti gli stack frame in ordine inverso per determinare se devono essere chiamati gestori di terminazione. Questo può comportare un peggioramento delle prestazioni a causa dell'esecuzione di centinaia di istruzioni.

Per evitare la chiusura anomala del gestore di terminazione, l'esecuzione deve proseguire fino alla fine del blocco. È anche possibile eseguire l'istruzione **\_ \_ Leave** . L'istruzione **\_ \_ Leave** consente la chiusura immediata del blocco **\_ \_ try** senza causare la terminazione anomala e la riduzione delle prestazioni. Controllare la documentazione del compilatore per determinare se l'istruzione **\_ \_ Leave** è supportata.

Se l'esecuzione del blocco **\_ \_ finally** termina a causa dell'istruzione **return** Control, è equivalente a un **goto** alla parentesi graffa di chiusura nella funzione contenitore. La funzione contenitore restituirà pertanto.

 

 
