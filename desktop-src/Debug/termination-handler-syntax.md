---
description: Le \_ \_ parole chiave try e finally vengono \_ \_ usate per costruire un gestore di terminazione. Nell'esempio seguente viene illustrata la struttura di un gestore di terminazione.
ms.assetid: fbaf8890-2516-4b60-be57-464f91f2a38a
title: Termination-Handler sintassi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3a6322bbcf86f56a75c62eaba03d50827edcd71a57addf48ef3777c7687796
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984461"
---
# <a name="termination-handler-syntax"></a>Termination-Handler sintassi

Le **\_ \_ parole chiave try** e **\_ \_ finally** vengono usate per costruire un gestore di terminazione. Nell'esempio seguente viene illustrata la struttura di un gestore di terminazione.


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



Per esempi, vedere [Uso di un gestore di terminazione](using-a-termination-handler.md).

Come per il gestore eccezioni, sia il blocco **\_ \_ try** che il blocco **\_ \_ finally** richiedono parentesi graffe ( ) e l'uso di un'istruzione goto per passare a uno dei due blocchi {} non è consentito. 

Il **\_ \_ blocco try** contiene il corpo sorvegliato del codice protetto dal gestore di terminazione. Una funzione può avere un numero qualsiasi di gestori di terminazione e questi blocchi di gestione della terminazione possono essere annidati all'interno della stessa funzione o in funzioni diverse.

Il **\_ \_ blocco finally** viene eseguito ogni volta che il flusso di controllo lascia il blocco **\_ \_ try.** Tuttavia, il **\_ \_ blocco finally** non viene eseguito se si chiama una delle funzioni seguenti all'interno del blocco **\_ \_ try:** [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)o **abort**.

Il **\_ \_ blocco finally** viene eseguito nel contesto della funzione in cui si trova il gestore di terminazione. Ciò significa che il **\_ \_ blocco finally** può accedere alle variabili locali della funzione. L'esecuzione **\_ \_ del blocco finally** può terminare in uno dei modi seguenti.

-   Esecuzione dell'ultima istruzione nel blocco e continuazione dell'istruzione successiva
-   Uso di un'istruzione di controllo (**return**, **break**, **continue** o **goto**)
-   Uso di **longjmp o** di un passaggio a un gestore di eccezioni

Se l'esecuzione del blocco **\_ \_ try** termina a causa di un'eccezione che richiama il blocco di gestione delle eccezioni di un gestore di eccezioni basato su frame, il **\_ \_ blocco finally** viene eseguito prima dell'esecuzione del blocco di gestione delle eccezioni. Analogamente, una chiamata alla funzione della libreria di runtime C **longjmp** dal blocco **\_ \_ try** causa l'esecuzione del blocco **\_ \_ finally** prima della ripresa dell'esecuzione nella destinazione dell'operazione **longjmp.** Se **\_ \_ l'esecuzione** del blocco try termina a causa di un'istruzione di controllo (**return**, **break**, **continue** o **goto**), viene eseguito **\_ \_ il blocco finally.**

La [**funzione AbnormalTermination**](abnormaltermination.md) può essere usata all'interno del blocco **\_ \_ finally** per determinare se il blocco **\_ \_ try** è terminato in sequenza, ovvero se ha raggiunto la parentesi graffa di chiusura (}). L'uscita dal blocco **\_ \_ try** a causa di una chiamata a **longjmp**, un passaggio a un gestore di eccezioni o un'istruzione **return**, **break**, **continue** **o goto** viene considerata una terminazione anomala. Si noti che la mancata terminazione in sequenza determina la ricerca di tutti gli stack frame in ordine inverso per determinare se è necessario chiamare i gestori di terminazione. Ciò può comportare una riduzione delle prestazioni a causa dell'esecuzione di centinaia di istruzioni.

Per evitare la terminazione anomala del gestore di terminazione, l'esecuzione deve continuare fino alla fine del blocco. È anche possibile eseguire **\_ \_ l'istruzione leave.** **\_ \_ L'istruzione leave** consente la terminazione immediata del blocco **\_ \_ try** senza causare interruzioni anomale e la relativa penalità per le prestazioni. Controllare la documentazione del compilatore per determinare se **\_ \_ l'istruzione leave** è supportata.

Se l'esecuzione del **\_ \_ blocco finally** termina a causa dell'istruzione **di** controllo return, equivale a **goto** alla parentesi graffa di chiusura nella funzione di inclusione. Di conseguenza, la funzione di inclusione restituirà .

 

 
