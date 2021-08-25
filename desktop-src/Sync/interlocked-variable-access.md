---
description: Le applicazioni devono sincronizzare l'accesso alle variabili condivise da più thread.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Accesso a variabili interlocked
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b298dffe45d1a0de655e225c8a240dd72be15a0fff7e4d6eac25ebb0a1130ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126321"
---
# <a name="interlocked-variable-access"></a>Accesso a variabili interlocked

Le applicazioni devono sincronizzare l'accesso alle variabili condivise da più thread. Le applicazioni devono anche garantire che le operazioni su queste variabili siano eseguite in modo atomico (eseguite nella loro interezza o non vengono eseguite affatto).

Le operazioni di lettura e scrittura semplici in variabili a 32 bit allineate correttamente sono operazioni atomiche. In altre parole, non verrà aggiornata solo una parte della variabile. tutti i bit vengono aggiornati in modo atomico. Tuttavia, non è garantita la sincronizzazione dell'accesso. Se due thread leggono e scrivono dalla stessa variabile, non è possibile determinare se un thread eseguirà l'operazione di lettura prima che l'altro esegua l'operazione di scrittura.

Le operazioni di lettura e scrittura semplici in variabili a 64 bit correttamente allineate sono atomiche in operazioni di Windows a 64 bit. Non è garantito che le operazioni di lettura e scrittura in valori a 64 bit siano atomiche nei valori a 32 bit Windows. Non è garantito che le operazioni di lettura e scrittura in variabili di altre dimensioni siano atomiche in alcuna piattaforma.

## <a name="the-interlocked-api"></a>The Interlocked API

Le funzioni interlocked forniscono un meccanismo semplice per sincronizzare l'accesso a una variabile condivisa da più thread. Eseguono anche operazioni sulle variabili in modo atomico. I thread di processi diversi possono usare queste funzioni se la variabile è in memoria condivisa.

Le [**funzioni InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) e [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) combinano i passaggi necessari per incrementare o decrementare una variabile in un'operazione atomica. Questa funzionalità è utile in un sistema operativo multitasking, in cui il sistema può interrompere l'esecuzione di un thread per concedere una sezione di tempo del processore a un altro thread. Senza tale sincronizzazione, due thread potrebbero leggere lo stesso valore, incrementarlo di 1 e archiviare il nuovo valore per un aumento totale di 1 anziché 2. Le funzioni di accesso alle variabili interlocked proteggono da questo tipo di errore.

Le [**funzioni InterlockedExchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) e [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) scambiano atomicamente i valori delle variabili specificate. La [**funzione InterlockedExchangeAdd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) combina due operazioni: l'aggiunta di due variabili e l'archiviazione del risultato in una delle variabili.

Le funzioni [**InterlockedCompareExchange**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange), [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))e [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) combinano due operazioni: il confronto di due valori e l'archiviazione di un terzo valore in una delle variabili, in base al risultato del confronto.

Le [**funzioni InterlockedAnd**](/windows/win32/api/winnt/nf-winnt-interlockedand), [**InterlockedOr**](/windows/win32/api/winnt/nf-winnt-interlockedor)e [**InterlockedXor**](/windows/win32/api/winnt/nf-winnt-interlockedxor) eseguono rispettivamente operazioni AND, OR e XOR in modo atomico.

Esistono funzioni appositamente progettate per eseguire l'accesso a variabili interlocked su indirizzi e valori di memoria a 64 bit e sono ottimizzate per l'uso in Windows a 64 bit. Ognuna di queste funzioni contiene "64" nel nome. ad esempio [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) e [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

La maggior parte delle funzioni interlocked offre barriere di memoria complete in tutte Windows piattaforme. Sono inoltre disponibili funzioni che combinano le operazioni di accesso alle variabili interlocked di base con la semantica di acquisizione e rilascio dell'ordinamento della memoria supportata da determinati processori. Ognuna di queste funzioni contiene la parola "Acquire" o "Release" nei nomi; ad esempio [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) e [**InterlockedDecrementRelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)). La semantica di acquisizione della memoria specifica che l'operazione di memoria eseguita dal thread corrente sarà visibile prima di qualsiasi altra operazione di memoria. La semantica di memoria di rilascio specifica che l'operazione di memoria eseguita dal thread corrente sarà visibile dopo il completamento di tutte le altre operazioni sulla memoria. Questa semantica consente di forzare l'esecuzione delle operazioni di memoria in un ordine specifico. Usare la semantica di acquisizione quando si entra in un'area protetta e la semantica di rilascio all'uscita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Intrinseci del compilatore](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Problemi di sincronizzazione e multiprocessore](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
