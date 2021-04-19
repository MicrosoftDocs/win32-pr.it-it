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
# <a name="condition-variables"></a><span data-ttu-id="3fe45-104">Variabili di condizione</span><span class="sxs-lookup"><span data-stu-id="3fe45-104">Condition Variables</span></span>

<span data-ttu-id="3fe45-105">Le variabili di condizione sono primitive di sincronizzazione che consentono ai thread di attendere fino a quando si verifica una condizione specifica.</span><span class="sxs-lookup"><span data-stu-id="3fe45-105">Condition variables are synchronization primitives that enable threads to wait until a particular condition occurs.</span></span> <span data-ttu-id="3fe45-106">Le variabili di condizione sono oggetti in modalità utente che non possono essere condivisi tra più processi.</span><span class="sxs-lookup"><span data-stu-id="3fe45-106">Condition variables are user-mode objects that cannot be shared across processes.</span></span>

<span data-ttu-id="3fe45-107">Le variabili di condizione consentono ai thread di rilasciare atomicamente un blocco e di passare allo stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-107">Condition variables enable threads to atomically release a lock and enter the sleeping state.</span></span> <span data-ttu-id="3fe45-108">Possono essere usati con sezioni critiche o blocchi di lettura/scrittura (SRW).</span><span class="sxs-lookup"><span data-stu-id="3fe45-108">They can be used with critical sections or slim reader/writer (SRW) locks.</span></span> <span data-ttu-id="3fe45-109">Le variabili di condizione supportano le operazioni che "riattivano uno" o "riattivano tutti" i thread in attesa.</span><span class="sxs-lookup"><span data-stu-id="3fe45-109">Condition variables support operations that "wake one" or "wake all" waiting threads.</span></span> <span data-ttu-id="3fe45-110">Dopo la riattivazione, un thread riacquisisce il blocco rilasciato quando il thread entra nello stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-110">After a thread is woken, it re-acquires the lock it released when the thread entered the sleeping state.</span></span>

<span data-ttu-id="3fe45-111">Si noti che il chiamante deve allocare una struttura di **\_ variabili di condizione** e inizializzarla chiamando [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (per inizializzare la struttura in modo dinamico) o assegnare la **variabile di condizione costante \_ \_ init** alla variabile di struttura (per inizializzare la struttura in modo statico).</span><span class="sxs-lookup"><span data-stu-id="3fe45-111">Note that the caller must allocate a **CONDITION\_VARIABLE** structure and initialize it by either calling [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (to initialize the structure dynamically) or assign the constant **CONDITION\_VARIABLE\_INIT** to the structure variable (to initialize the structure statically).</span></span>

<span data-ttu-id="3fe45-112">**Windows Server 2003 e Windows XP:** Le variabili di condizione non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="3fe45-112">**Windows Server 2003 and Windows XP:** Condition variables are not supported.</span></span>

<span data-ttu-id="3fe45-113">Di seguito sono riportate le funzioni delle variabili di condizione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-113">The following are the condition variable functions.</span></span>



| <span data-ttu-id="3fe45-114">Funzione della variabile Condition</span><span class="sxs-lookup"><span data-stu-id="3fe45-114">Condition variable function</span></span>                                        | <span data-ttu-id="3fe45-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fe45-115">Description</span></span>                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fe45-116">**InitializeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="3fe45-116">**InitializeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | <span data-ttu-id="3fe45-117">Inizializza una variabile di condizione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-117">Initializes a condition variable.</span></span>                                                                              |
| [<span data-ttu-id="3fe45-118">**SleepConditionVariableCS**</span><span class="sxs-lookup"><span data-stu-id="3fe45-118">**SleepConditionVariableCS**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | <span data-ttu-id="3fe45-119">Dorme sulla variabile di condizione specificata e rilascia la sezione critica specificata come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="3fe45-119">Sleeps on the specified condition variable and releases the specified critical section as an atomic operation.</span></span> |
| [<span data-ttu-id="3fe45-120">**SleepConditionVariableSRW**</span><span class="sxs-lookup"><span data-stu-id="3fe45-120">**SleepConditionVariableSRW**</span></span>](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | <span data-ttu-id="3fe45-121">Dorme sulla variabile di condizione specificata e rilascia il blocco SRW specificato come operazione atomica.</span><span class="sxs-lookup"><span data-stu-id="3fe45-121">Sleeps on the specified condition variable and releases the specified SRW lock as an atomic operation.</span></span>         |
| [<span data-ttu-id="3fe45-122">**WakeAllConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="3fe45-122">**WakeAllConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | <span data-ttu-id="3fe45-123">Attiva tutti i thread in attesa della variabile di condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3fe45-123">Wakes all threads waiting on the specified condition variable.</span></span>                                                 |
| [<span data-ttu-id="3fe45-124">**WakeConditionVariable**</span><span class="sxs-lookup"><span data-stu-id="3fe45-124">**WakeConditionVariable**</span></span>](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | <span data-ttu-id="3fe45-125">Attiva un singolo thread in attesa della variabile di condizione specificata.</span><span class="sxs-lookup"><span data-stu-id="3fe45-125">Wakes a single thread waiting on the specified condition variable.</span></span>                                             |



 

<span data-ttu-id="3fe45-126">Lo pseudocodice seguente illustra il modello di utilizzo tipico delle variabili di condizione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-126">The following pseudocode demonstrates the typical usage pattern of condition variables.</span></span>

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

<span data-ttu-id="3fe45-127">Ad esempio, in un'implementazione di un blocco in lettura/scrittura, la `TestPredicate` funzione verificherebbe che la richiesta di blocco corrente sia compatibile con i proprietari esistenti.</span><span class="sxs-lookup"><span data-stu-id="3fe45-127">For example, in an implementation of a reader/writer lock, the `TestPredicate` function would verify that the current lock request is compatible with the existing owners.</span></span> <span data-ttu-id="3fe45-128">In caso contrario, acquisire il blocco; in caso contrario, sospensione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-128">If it is, acquire the lock; otherwise, sleep.</span></span> <span data-ttu-id="3fe45-129">Per un esempio più dettagliato, vedere [utilizzo delle variabili di condizione](using-condition-variables.md).</span><span class="sxs-lookup"><span data-stu-id="3fe45-129">For a more detailed example, see [Using Condition Variables](using-condition-variables.md).</span></span>

<span data-ttu-id="3fe45-130">Le variabili di condizione sono soggette a riattivazioni non corrette (quelle non associate a una riattivazione esplicita) e Riattivazioni rubate (un altro thread riesce a eseguire prima del thread riattivato).</span><span class="sxs-lookup"><span data-stu-id="3fe45-130">Condition variables are subject to spurious wakeups (those not associated with an explicit wake) and stolen wakeups (another thread manages to run before the woken thread).</span></span> <span data-ttu-id="3fe45-131">È pertanto necessario ricontrollare un predicato, in genere in un ciclo **while** , dopo la restituzione di un'operazione di sospensione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-131">Therefore, you should recheck a predicate (typically in a **while** loop) after a sleep operation returns.</span></span>

<span data-ttu-id="3fe45-132">È possibile riattivare gli altri thread utilizzando [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) o [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) all'interno o all'esterno del blocco associato alla variabile di condizione.</span><span class="sxs-lookup"><span data-stu-id="3fe45-132">You can wake other threads using [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) or [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) either inside or outside the lock associated with the condition variable.</span></span> <span data-ttu-id="3fe45-133">È in genere preferibile rilasciare il blocco prima di riattivare altri thread per ridurre il numero di cambi di contesto.</span><span class="sxs-lookup"><span data-stu-id="3fe45-133">It is usually better to release the lock before waking other threads to reduce the number of context switches.</span></span>

<span data-ttu-id="3fe45-134">Spesso è consigliabile usare più di una variabile di condizione con lo stesso blocco.</span><span class="sxs-lookup"><span data-stu-id="3fe45-134">It is often convenient to use more than one condition variable with the same lock.</span></span> <span data-ttu-id="3fe45-135">Ad esempio, un'implementazione di un blocco reader/writer può utilizzare una sola sezione critica ma separare le variabili di condizione per Reader e writer.</span><span class="sxs-lookup"><span data-stu-id="3fe45-135">For example, an implementation of a reader/writer lock might use a single critical section but separate condition variables for readers and writers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fe45-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3fe45-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe45-137">Utilizzo di variabili di condizione</span><span class="sxs-lookup"><span data-stu-id="3fe45-137">Using Condition Variables</span></span>](using-condition-variables.md)
</dt> </dl>

 

 
