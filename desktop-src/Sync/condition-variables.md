---
description: Le variabili di condizione sono primitive di sincronizzazione che consentono ai thread di attendere fino a quando non si verifica una determinata condizione. Le variabili di condizione sono oggetti in modalità utente che non possono essere condivisi tra processi.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variabili di condizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d7ee98b4f5c5a65e633f7d1647b6c624840f9740efb639959c1500bec591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886361"
---
# <a name="condition-variables"></a>Variabili di condizione

Le variabili di condizione sono primitive di sincronizzazione che consentono ai thread di attendere fino a quando non si verifica una determinata condizione. Le variabili di condizione sono oggetti in modalità utente che non possono essere condivisi tra processi.

Le variabili di condizione consentono ai thread di rilasciare un blocco in modo atomico e di entrare nello stato di sospensione. Possono essere usati con sezioni critiche o blocchi SRW (Slim Reader/Writer). Le variabili di condizione supportano operazioni che "riattivano uno" o "riattivano tutti" i thread in attesa. Dopo che un thread è stato rimesso in stato di sospensione, acquisisce nuovamente il blocco rilasciato quando il thread entra nello stato di sospensione.

Si noti che il chiamante deve allocare una struttura **CONDITION \_ VARIABLE** e inizializzarla chiamando [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (per inizializzare la struttura in modo dinamico) o assegnando la costante **CONDITION VARIABLE \_ \_ INIT** alla variabile di struttura (per inizializzare la struttura in modo statico).

**Windows Server 2003 e Windows XP:** Le variabili di condizione non sono supportate.

Di seguito sono riportate le funzioni delle variabili di condizione.



| Funzione di variabile di condizione                                        | Descrizione                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Inizializza una variabile di condizione.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Sospensione sulla variabile di condizione specificata e rilascio della sezione critica specificata come operazione atomica. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Sospensione sulla variabile di condizione specificata e rilascio del blocco SRW specificato come operazione atomica.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Riattiva tutti i thread in attesa della variabile di condizione specificata.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Riattiva un singolo thread in attesa della variabile di condizione specificata.                                             |



 

Lo pseudocodice seguente illustra il modello di utilizzo tipico delle variabili di condizione.

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

Ad esempio, in un'implementazione di un blocco reader/writer, la funzione verifica che la richiesta di blocco corrente sia `TestPredicate` compatibile con i proprietari esistenti. In caso contrario, acquisire il blocco. in caso contrario, sospensione. Per un esempio più dettagliato, vedere Uso [delle variabili di condizione](using-condition-variables.md).

Le variabili di condizione sono soggette a riattivazioni spurie (quelle non associate a una riattivazione esplicita) e riattivazioni rubate (un altro thread riesce a essere eseguito prima del thread riattivato). Pertanto, è necessario controllare nuovamente un predicato (in genere in un **ciclo while)** dopo la fine di un'operazione di sospensione.

È possibile riattivare altri thread usando [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) o [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) all'interno o all'esterno del blocco associato alla variabile della condizione. In genere è meglio rilasciare il blocco prima di svegliare altri thread per ridurre il numero di commutatori di contesto.

Spesso è utile usare più variabili di condizione con lo stesso blocco. Ad esempio, un'implementazione di un blocco reader/writer potrebbe usare una singola sezione critica, ma variabili di condizione separate per lettori e writer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso delle variabili di condizione](using-condition-variables.md)
</dt> </dl>

 

 
