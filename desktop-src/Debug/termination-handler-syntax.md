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
# <a name="termination-handler-syntax"></a><span data-ttu-id="f2794-104">Sintassi Termination-Handler</span><span class="sxs-lookup"><span data-stu-id="f2794-104">Termination-Handler Syntax</span></span>

<span data-ttu-id="f2794-105">Per costruire un gestore di terminazione vengono usate le parole chiave **\_ \_ try** e **\_ \_ finally** .</span><span class="sxs-lookup"><span data-stu-id="f2794-105">The **\_\_try** and **\_\_finally** keywords are used to construct a termination handler.</span></span> <span data-ttu-id="f2794-106">Nell'esempio seguente viene illustrata la struttura di un gestore di terminazione.</span><span class="sxs-lookup"><span data-stu-id="f2794-106">The following example shows the structure of a termination handler.</span></span>


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



<span data-ttu-id="f2794-107">Per esempi, vedere [uso di un gestore di terminazione](using-a-termination-handler.md).</span><span class="sxs-lookup"><span data-stu-id="f2794-107">For examples, see [Using a Termination Handler](using-a-termination-handler.md).</span></span>

<span data-ttu-id="f2794-108">Come per il gestore di eccezioni, il blocco **\_ \_ try** e il blocco **\_ \_ finally** richiedono parentesi graffe ( {} ) e l'utilizzo di un'istruzione **goto** per passare a uno dei blocchi non è consentito.</span><span class="sxs-lookup"><span data-stu-id="f2794-108">As with the exception handler, both the **\_\_try** block and the **\_\_finally** block require braces ({}), and using a **goto** statement to jump into either block is not permitted.</span></span>

<span data-ttu-id="f2794-109">Il blocco **\_ \_ try** contiene il corpo sorvegliato del codice protetto dal gestore di terminazione.</span><span class="sxs-lookup"><span data-stu-id="f2794-109">The **\_\_try** block contains the guarded body of code that is protected by the termination handler.</span></span> <span data-ttu-id="f2794-110">Una funzione può avere un numero qualsiasi di gestori di terminazione e questi blocchi di gestione delle terminazioni possono essere annidati all'interno della stessa funzione o in funzioni diverse.</span><span class="sxs-lookup"><span data-stu-id="f2794-110">A function can have any number of termination handlers, and these termination-handling blocks can be nested within the same function or in different functions.</span></span>

<span data-ttu-id="f2794-111">Il blocco **\_ \_ finally** viene eseguito ogni volta che il flusso di controllo lascia il blocco **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="f2794-111">The **\_\_finally** block is executed whenever the flow of control leaves the **\_\_try** block.</span></span> <span data-ttu-id="f2794-112">Tuttavia, il blocco **\_ \_ finally** non viene eseguito se si chiama una delle funzioni seguenti all'interno del blocco **\_ \_ try** : [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)o **Abort**.</span><span class="sxs-lookup"><span data-stu-id="f2794-112">However, the **\_\_finally** block is not executed if you call any of the following functions within the **\_\_try** block: [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), or **abort**.</span></span>

<span data-ttu-id="f2794-113">Il blocco **\_ \_ finally** viene eseguito nel contesto della funzione in cui si trova il gestore di terminazione.</span><span class="sxs-lookup"><span data-stu-id="f2794-113">The **\_\_finally** block is executed in the context of the function in which the termination handler is located.</span></span> <span data-ttu-id="f2794-114">Questo significa che il blocco **\_ \_ finally** può accedere alle variabili locali della funzione.</span><span class="sxs-lookup"><span data-stu-id="f2794-114">This means that the **\_\_finally** block can access that function's local variables.</span></span> <span data-ttu-id="f2794-115">L'esecuzione del blocco **\_ \_ finally** può terminare con uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f2794-115">Execution of the **\_\_finally** block can terminate by any of the following means.</span></span>

-   <span data-ttu-id="f2794-116">Esecuzione dell'ultima istruzione nel blocco e della continuazione all'istruzione successiva</span><span class="sxs-lookup"><span data-stu-id="f2794-116">Execution of the last statement in the block and continuation to the next instruction</span></span>
-   <span data-ttu-id="f2794-117">Uso di un'istruzione di controllo (**return**, **break**, **continue** o **goto**)</span><span class="sxs-lookup"><span data-stu-id="f2794-117">Use of a control statement (**return**, **break**, **continue**, or **goto**)</span></span>
-   <span data-ttu-id="f2794-118">Uso di **longjmp** o di un salto a un gestore di eccezioni</span><span class="sxs-lookup"><span data-stu-id="f2794-118">Use of **longjmp** or a jump to an exception handler</span></span>

<span data-ttu-id="f2794-119">Se l'esecuzione del blocco **\_ \_ try** viene terminata a causa di un'eccezione che richiama il blocco di gestione delle eccezioni di un gestore di eccezioni basato su frame, il blocco **\_ \_ finally** viene eseguito prima dell'esecuzione del blocco di gestione delle eccezioni.</span><span class="sxs-lookup"><span data-stu-id="f2794-119">If execution of the **\_\_try** block terminates because of an exception that invokes the exception-handling block of a frame-based exception handler, the **\_\_finally** block is executed before the exception-handling block is executed.</span></span> <span data-ttu-id="f2794-120">Analogamente, una chiamata alla funzione della libreria di runtime C **longjmp** dal blocco **\_ \_ try** causa l'esecuzione del blocco **\_ \_ finally** prima che l'esecuzione venga ripresa alla destinazione dell'operazione **longjmp** .</span><span class="sxs-lookup"><span data-stu-id="f2794-120">Similarly, a call to the **longjmp** C run-time library function from the **\_\_try** block causes execution of the **\_\_finally** block before execution resumes at the target of the **longjmp** operation.</span></span> <span data-ttu-id="f2794-121">Se l'esecuzione del blocco **\_ \_ try** viene terminata a causa di un'istruzione di controllo (**return**, **break**, **continue** o **goto**), viene eseguito il blocco **\_ \_ finally** .</span><span class="sxs-lookup"><span data-stu-id="f2794-121">If **\_\_try** block execution terminates due to a control statement (**return**, **break**, **continue**, or **goto**), the **\_\_finally** block is executed.</span></span>

<span data-ttu-id="f2794-122">La funzione [**AbnormalTermination**](abnormaltermination.md) può essere usata all'interno del blocco **\_ \_ finally** per determinare se il blocco **\_ \_ try** è stato terminato in sequenza, ovvero se ha raggiunto la parentesi graffa di chiusura (}).</span><span class="sxs-lookup"><span data-stu-id="f2794-122">The [**AbnormalTermination**](abnormaltermination.md) function can be used within the **\_\_finally** block to determine whether the **\_\_try** block terminated sequentially — that is, whether it reached the closing brace (}).</span></span> <span data-ttu-id="f2794-123">Quando si lascia il blocco **\_ \_ try** a causa di una chiamata a **longjmp**, un passaggio a un gestore di eccezioni o un'istruzione **return**, **break**, **continue** o **goto** viene considerata una terminazione anomala.</span><span class="sxs-lookup"><span data-stu-id="f2794-123">Leaving the **\_\_try** block because of a call to **longjmp**, a jump to an exception handler, or a **return**, **break**, **continue**, or **goto** statement, is considered an abnormal termination.</span></span> <span data-ttu-id="f2794-124">Si noti che l'errore di terminazione sequenziale induce il sistema a cercare tutti gli stack frame in ordine inverso per determinare se devono essere chiamati gestori di terminazione.</span><span class="sxs-lookup"><span data-stu-id="f2794-124">Note that failure to terminate sequentially causes the system to search through all stack frames in reverse order to determine whether any termination handlers must be called.</span></span> <span data-ttu-id="f2794-125">Questo può comportare un peggioramento delle prestazioni a causa dell'esecuzione di centinaia di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="f2794-125">This can result in performance degradation due to the execution of hundreds of instructions.</span></span>

<span data-ttu-id="f2794-126">Per evitare la chiusura anomala del gestore di terminazione, l'esecuzione deve proseguire fino alla fine del blocco.</span><span class="sxs-lookup"><span data-stu-id="f2794-126">To avoid abnormal termination of the termination handler, execution should continue to the end of the block.</span></span> <span data-ttu-id="f2794-127">È anche possibile eseguire l'istruzione **\_ \_ Leave** .</span><span class="sxs-lookup"><span data-stu-id="f2794-127">You can also execute the **\_\_leave** statement.</span></span> <span data-ttu-id="f2794-128">L'istruzione **\_ \_ Leave** consente la chiusura immediata del blocco **\_ \_ try** senza causare la terminazione anomala e la riduzione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="f2794-128">The **\_\_leave** statement allows for immediate termination of the **\_\_try** block without causing abnormal termination and its performance penalty.</span></span> <span data-ttu-id="f2794-129">Controllare la documentazione del compilatore per determinare se l'istruzione **\_ \_ Leave** è supportata.</span><span class="sxs-lookup"><span data-stu-id="f2794-129">Check your compiler documentation to determine if the **\_\_leave** statement is supported.</span></span>

<span data-ttu-id="f2794-130">Se l'esecuzione del blocco **\_ \_ finally** termina a causa dell'istruzione **return** Control, è equivalente a un **goto** alla parentesi graffa di chiusura nella funzione contenitore.</span><span class="sxs-lookup"><span data-stu-id="f2794-130">If execution of the **\_\_finally** block terminates because of the **return** control statement, it is equivalent to a **goto** to the closing brace in the enclosing function.</span></span> <span data-ttu-id="f2794-131">La funzione contenitore restituirà pertanto.</span><span class="sxs-lookup"><span data-stu-id="f2794-131">Therefore, the enclosing function will return.</span></span>

 

 
