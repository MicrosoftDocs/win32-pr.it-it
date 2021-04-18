---
description: Le applicazioni devono sincronizzare l'accesso a variabili condivise da più thread.
ms.assetid: 729c0e68-ef52-4d6c-b771-a89043a937e6
title: Accesso a variabili Interlocked
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2e083d3e3420e870ad9781b0d262df3d0786f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315304"
---
# <a name="interlocked-variable-access"></a>Accesso a variabili Interlocked

Le applicazioni devono sincronizzare l'accesso a variabili condivise da più thread. Le applicazioni devono inoltre garantire che le operazioni su queste variabili vengano eseguite in modo atomico (eseguite interamente o in modo non completo).

Semplici letture e scritture per variabili a 32 bit allineate correttamente sono operazioni atomiche. In altre parole, non si concluderà con una sola parte della variabile aggiornata; tutti i bit vengono aggiornati in modo atomico. Tuttavia, non è garantita la sincronizzazione dell'accesso. Se due thread leggono e scrivono dalla stessa variabile, non è possibile determinare se un thread eseguirà l'operazione di lettura prima che l'altra esegua l'operazione di scrittura.

Semplici letture e scritture per variabili a 64 bit correttamente allineate sono atomiche in Windows a 64 bit. Le letture e le scritture nei valori a 64 bit non sono necessariamente atomiche nelle finestre a 32 bit. Non è garantito che le letture e le Scritture in variabili di altre dimensioni siano atomiche su qualsiasi piattaforma.

## <a name="the-interlocked-api"></a>API Interlocked

Le funzioni Interlocked forniscono un meccanismo semplice per la sincronizzazione dell'accesso a una variabile condivisa da più thread. Eseguono anche operazioni sulle variabili in modo atomico. I thread di processi diversi possono usare queste funzioni se la variabile si trova nella memoria condivisa.

Le funzioni [**InterlockedIncrement**](/windows/win32/api/winnt/nf-winnt-interlockedincrement) e [**InterlockedDecrement**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement) combinano i passaggi necessari per incrementare o decrementare una variabile in un'operazione atomica. Questa funzionalità è utile in un sistema operativo multitasking, in cui il sistema può interrompere l'esecuzione di un thread per concedere una sezione del tempo del processore a un altro thread. Senza tale sincronizzazione, due thread potrebbero leggere lo stesso valore, incrementarlo di 1 e archiviare il nuovo valore per un incremento totale di 1 anziché 2. Le funzioni di accesso a variabili interlocked proteggono da questo tipo di errore.

Le funzioni [**InterlockedExchange**](/windows/win32/api/winnt/nf-winnt-interlockedexchange) e [**InterlockedExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedexchangepointer) scambiano in modo atomico i valori delle variabili specificate. La funzione [**InterlockedExchangeAdd**](/windows/win32/api/winnt/nf-winnt-interlockedexchangeadd) combina due operazioni: aggiungendo due variabili insieme e archiviando il risultato in una delle variabili.

Le funzioni [**InterlockedCompareExchange**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchange), [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85))e [**InterlockedCompareExchangePointer**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) combinano due operazioni: il confronto di due valori e l'archiviazione di un terzo valore in una delle variabili, in base al risultato del confronto.

Le funzioni [**InterlockedAnd**](/windows/win32/api/winnt/nf-winnt-interlockedand), [**interlockedr**](/windows/win32/api/winnt/nf-winnt-interlockedor)e [**InterlockedXor**](/windows/win32/api/winnt/nf-winnt-interlockedxor) eseguono atomicamente rispettivamente le operazioni and, or e XOR.

Sono disponibili funzioni progettate in modo specifico per eseguire l'accesso con variabile Interlocked in valori di memoria e indirizzi a 64 bit e sono ottimizzate per l'utilizzo in Windows a 64 bit. Ognuna di queste funzioni contiene "64" nel nome; ad esempio, [**InterlockedDecrement64**](/windows/win32/api/winnt/nf-winnt-interlockeddecrement64) e [**InterlockedCompareExchangeAcquire64**](/previous-versions/windows/desktop/legacy/ms683566(v=vs.85)).

La maggior parte delle funzioni Interlocked offre barriere di memoria complete su tutte le piattaforme Windows. Sono inoltre disponibili funzioni che combinano le operazioni di accesso alle variabili di base Interlocked con la semantica di ordinamento della memoria di acquisizione e rilascio supportata da determinati processori. Ognuna di queste funzioni contiene la parola "Acquire" o "release" nei rispettivi nomi; ad esempio, [**InterlockedDecrementAcquire**](/previous-versions/windows/desktop/legacy/ms683583(v=vs.85)) e [**InterlockedDecrementRelease**](/previous-versions/windows/desktop/legacy/ms683586(v=vs.85)). Acquisisci semantica di memoria consente di specificare che l'operazione di memoria eseguita dal thread corrente sarà visibile prima che vengano tentate altre operazioni di memoria. Semantica versione memoria specifica che l'operazione di memoria eseguita dal thread corrente sarà visibile dopo il completamento di tutte le altre operazioni di memoria. Queste semantiche consentono di forzare l'esecuzione delle operazioni di memoria in un ordine specifico. Usare la semantica di acquisizione quando si immette un'area protetta e una semantica di rilascio quando viene lasciata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Intrinseci del compilatore](/cpp/intrinsics/compiler-intrinsics?view=vs-2019)
</dt> <dt>

[Problemi di sincronizzazione e multiprocessore](synchronization-and-multiprocessor-issues.md)
</dt> </dl>

 

 
