---
description: Le variabili di condizione sono primitive di sincronizzazione che consentono ai thread di attendere fino a quando si verifica una condizione specifica. Le variabili di condizione sono oggetti in modalità utente che non possono essere condivisi tra più processi.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variabili di condizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711fad7d80c1c5e06fc6e496198cd298b190daba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315308"
---
# <a name="condition-variables"></a>Variabili di condizione

Le variabili di condizione sono primitive di sincronizzazione che consentono ai thread di attendere fino a quando si verifica una condizione specifica. Le variabili di condizione sono oggetti in modalità utente che non possono essere condivisi tra più processi.

Le variabili di condizione consentono ai thread di rilasciare atomicamente un blocco e di passare allo stato di sospensione. Possono essere usati con sezioni critiche o blocchi di lettura/scrittura (SRW). Le variabili di condizione supportano le operazioni che "riattivano uno" o "riattivano tutti" i thread in attesa. Dopo la riattivazione, un thread riacquisisce il blocco rilasciato quando il thread entra nello stato di sospensione.

Si noti che il chiamante deve allocare una struttura di **\_ variabili di condizione** e inizializzarla chiamando [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (per inizializzare la struttura in modo dinamico) o assegnare la **variabile di condizione costante \_ \_ init** alla variabile di struttura (per inizializzare la struttura in modo statico).

**Windows Server 2003 e Windows XP:** Le variabili di condizione non sono supportate.

Di seguito sono riportate le funzioni delle variabili di condizione.



| Funzione della variabile Condition                                        | Descrizione                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Inizializza una variabile di condizione.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Dorme sulla variabile di condizione specificata e rilascia la sezione critica specificata come operazione atomica. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Dorme sulla variabile di condizione specificata e rilascia il blocco SRW specificato come operazione atomica.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Attiva tutti i thread in attesa della variabile di condizione specificata.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Attiva un singolo thread in attesa della variabile di condizione specificata.                                             |



 

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

Ad esempio, in un'implementazione di un blocco in lettura/scrittura, la `TestPredicate` funzione verificherebbe che la richiesta di blocco corrente sia compatibile con i proprietari esistenti. In caso contrario, acquisire il blocco; in caso contrario, sospensione. Per un esempio più dettagliato, vedere [utilizzo delle variabili di condizione](using-condition-variables.md).

Le variabili di condizione sono soggette a riattivazioni non corrette (quelle non associate a una riattivazione esplicita) e Riattivazioni rubate (un altro thread riesce a eseguire prima del thread riattivato). È pertanto necessario ricontrollare un predicato, in genere in un ciclo **while** , dopo la restituzione di un'operazione di sospensione.

È possibile riattivare gli altri thread utilizzando [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) o [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) all'interno o all'esterno del blocco associato alla variabile di condizione. È in genere preferibile rilasciare il blocco prima di riattivare altri thread per ridurre il numero di cambi di contesto.

Spesso è consigliabile usare più di una variabile di condizione con lo stesso blocco. Ad esempio, un'implementazione di un blocco reader/writer può utilizzare una sola sezione critica ma separare le variabili di condizione per Reader e writer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di variabili di condizione](using-condition-variables.md)
</dt> </dl>

 

 
