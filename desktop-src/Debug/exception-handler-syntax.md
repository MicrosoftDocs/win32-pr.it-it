---
description: Le \_ \_ \_ \_ parole chiave try e except vengono usate per costruire un gestore di eccezioni basato su frame. Nell'esempio seguente viene illustrata la struttura di un gestore di eccezioni.
ms.assetid: 1ea2c7f7-f920-4c72-bc62-4eb5e8d70790
title: Sintassi Exception-Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eff9e6ca5d16a71b416f79a09f46795592a696
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522874"
---
# <a name="exception-handler-syntax"></a><span data-ttu-id="e02e5-104">Sintassi Exception-Handler</span><span class="sxs-lookup"><span data-stu-id="e02e5-104">Exception-Handler Syntax</span></span>

<span data-ttu-id="e02e5-105">Le parole chiave **\_ \_ try** e **\_ \_ except** vengono usate per costruire un gestore di eccezioni basato su frame.</span><span class="sxs-lookup"><span data-stu-id="e02e5-105">The **\_\_try** and **\_\_except** keywords are used to construct a frame-based exception handler.</span></span> <span data-ttu-id="e02e5-106">Nell'esempio seguente viene illustrata la struttura di un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="e02e5-106">The following example shows the structure of an exception handler.</span></span>


```C++
__try 
{
    // guarded body of code 
 
} 
__except (filter-expression) 
{ 
    // exception-handler block 
 
}
```



<span data-ttu-id="e02e5-107">Si noti che il blocco **\_ \_ try** e il blocco del gestore di eccezioni richiedono le parentesi graffe ( {} ).</span><span class="sxs-lookup"><span data-stu-id="e02e5-107">Note that the **\_\_try** block and the exception-handler block require braces ({}).</span></span> <span data-ttu-id="e02e5-108">Non è consentito usare un'istruzione **goto** per passare al corpo di un blocco **\_ \_ try** o in un blocco del gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="e02e5-108">Using a **goto** statement to jump into the body of a **\_\_try** block or into an exception-handler block is not permitted.</span></span> <span data-ttu-id="e02e5-109">Questa regola si applica sia ai gestori di eccezioni che ai gestori di terminazione.</span><span class="sxs-lookup"><span data-stu-id="e02e5-109">This rule applies to both exception handlers and termination handlers.</span></span>

<span data-ttu-id="e02e5-110">Il blocco **\_ \_ try** contiene il corpo sorvegliato del codice protetto dal gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="e02e5-110">The **\_\_try** block contains the guarded body of code that the exception handler protects.</span></span> <span data-ttu-id="e02e5-111">Una funzione può avere un numero qualsiasi di gestori di eccezioni e queste istruzioni di gestione delle eccezioni possono essere annidate all'interno della stessa funzione o in funzioni diverse.</span><span class="sxs-lookup"><span data-stu-id="e02e5-111">A function can have any number of exception handlers, and these exception-handling statements can be nested within the same function or in different functions.</span></span> <span data-ttu-id="e02e5-112">Se si verifica un'eccezione all'interno del blocco **\_ \_ try** , il sistema acquisisce il controllo e inizia la ricerca di un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="e02e5-112">If an exception occurs within the **\_\_try** block, the system takes control and begins the search for an exception handler.</span></span> <span data-ttu-id="e02e5-113">Per una descrizione dettagliata di questa ricerca, vedere [gestione delle eccezioni](exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e02e5-113">For a detailed description of this search, see [Exception Handling](exception-handling.md).</span></span>

<span data-ttu-id="e02e5-114">Il gestore di eccezioni riceve solo le eccezioni che si verificano all'interno di un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="e02e5-114">The exception handler receives only exceptions that occur within a single thread.</span></span> <span data-ttu-id="e02e5-115">Ciò significa che se un blocco **\_ \_ try** contiene una chiamata alla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , le eccezioni che si verificano all'interno del nuovo processo o del nuovo thread non vengono inviate a questo gestore.</span><span class="sxs-lookup"><span data-stu-id="e02e5-115">This means that if a **\_\_try** block contains a call to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) or [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function, exceptions that occur within the new process or thread are not dispatched to this handler.</span></span>

<span data-ttu-id="e02e5-116">Il sistema valuta l'espressione di filtro di ogni gestore di eccezioni che protegge il codice in cui si è verificata l'eccezione fino a quando l'eccezione non viene gestita o non sono presenti altri gestori.</span><span class="sxs-lookup"><span data-stu-id="e02e5-116">The system evaluates the filter expression of each exception handler guarding the code in which the exception occurred until either the exception is handled or there are no more handlers.</span></span> <span data-ttu-id="e02e5-117">Un'espressione di filtro deve essere valutata come uno dei tre valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e02e5-117">A filter expression must be evaluated as one of the three following values.</span></span>



| <span data-ttu-id="e02e5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e02e5-118">Value</span></span>                              | <span data-ttu-id="e02e5-119">Significato</span><span class="sxs-lookup"><span data-stu-id="e02e5-119">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e02e5-120">**\_gestore di esecuzione eccezioni \_**</span><span class="sxs-lookup"><span data-stu-id="e02e5-120">**EXCEPTION\_EXECUTE\_HANDLER**</span></span>    | <span data-ttu-id="e02e5-121">Il sistema trasferisce il controllo al gestore di eccezioni e l'esecuzione continua nel stack frame in cui viene individuato il gestore.</span><span class="sxs-lookup"><span data-stu-id="e02e5-121">The system transfers control to the exception handler, and execution continues in the stack frame in which the handler is found.</span></span>                                                                                       |
| <span data-ttu-id="e02e5-122">**\_continua \_ ricerca eccezione**</span><span class="sxs-lookup"><span data-stu-id="e02e5-122">**EXCEPTION\_CONTINUE\_SEARCH**</span></span>    | <span data-ttu-id="e02e5-123">Il sistema continua la ricerca di un gestore.</span><span class="sxs-lookup"><span data-stu-id="e02e5-123">The system continues to search for a handler.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="e02e5-124">**esecuzione dell'eccezione \_ continua \_**</span><span class="sxs-lookup"><span data-stu-id="e02e5-124">**EXCEPTION\_CONTINUE\_EXECUTION**</span></span> | <span data-ttu-id="e02e5-125">Il sistema arresta la ricerca di un gestore e restituisce il controllo al punto in cui si è verificata l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="e02e5-125">The system stops its search for a handler and returns control to the point at which the exception occurred.</span></span> <span data-ttu-id="e02e5-126">Se l'eccezione è non continuabile, viene generata un'eccezione di eccezione non **\_ continuabile \_** .</span><span class="sxs-lookup"><span data-stu-id="e02e5-126">If the exception is noncontinuable, this results in an **EXCEPTION\_NONCONTINUABLE\_EXCEPTION** exception.</span></span> |



 

<span data-ttu-id="e02e5-127">L'espressione di filtro viene valutata nel contesto della funzione in cui si trova il gestore eccezioni, anche se l'eccezione potrebbe essersi verificata in una funzione diversa.</span><span class="sxs-lookup"><span data-stu-id="e02e5-127">The filter expression is evaluated in the context of the function in which the exception handler is located, even though the exception may have occurred in a different function.</span></span> <span data-ttu-id="e02e5-128">Ciò significa che l'espressione di filtro può accedere alle variabili locali della funzione.</span><span class="sxs-lookup"><span data-stu-id="e02e5-128">This means that the filter expression can access the function's local variables.</span></span> <span data-ttu-id="e02e5-129">Analogamente, il blocco del gestore di eccezioni può accedere alle variabili locali della funzione in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="e02e5-129">Similarly, the exception-handler block can access the local variables of the function in which it is located.</span></span>

<span data-ttu-id="e02e5-130">Per altri esempi, vedere [uso di un gestore di eccezioni](using-an-exception-handler.md).</span><span class="sxs-lookup"><span data-stu-id="e02e5-130">For more examples, see [Using an Exception Handler](using-an-exception-handler.md).</span></span>

<span data-ttu-id="e02e5-131">Per ulteriori informazioni sulle espressioni di filtro e sulle funzioni di filtro, vedere [gestione delle eccezioni basata su frame](frame-based-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="e02e5-131">For more information about filter expressions and filter functions, see [Frame-based Exception Handling](frame-based-exception-handling.md).</span></span>

 

 
