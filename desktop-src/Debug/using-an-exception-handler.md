---
description: Negli esempi seguenti viene illustrato l'utilizzo di un gestore di eccezioni.
ms.assetid: c3b4e696-9f45-4616-ac6b-07ba29750bb2
title: Uso di un gestore di eccezioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dbe7ec23ddd5372cecfe85ae8348092d91cfff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304861"
---
# <a name="using-an-exception-handler"></a><span data-ttu-id="975d9-103">Uso di un gestore di eccezioni</span><span class="sxs-lookup"><span data-stu-id="975d9-103">Using an Exception Handler</span></span>

<span data-ttu-id="975d9-104">Negli esempi seguenti viene illustrato l'utilizzo di un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="975d9-104">The following examples demonstrate the use of an exception handler.</span></span>

## <a name="example-1"></a><span data-ttu-id="975d9-105">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="975d9-105">Example 1</span></span>

<span data-ttu-id="975d9-106">Il frammento di codice seguente usa la gestione delle eccezioni strutturata per verificare se un'operazione di divisione su interi a 2 32 bit provocherà un errore di divisione per zero.</span><span class="sxs-lookup"><span data-stu-id="975d9-106">The following code fragment uses structured exception handling to check whether a division operation on two 32-bit integers will result in an division-by-zero error.</span></span> <span data-ttu-id="975d9-107">In tal caso, la funzione restituisce **false**, in caso contrario restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="975d9-107">If this occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>


```C++
BOOL SafeDiv(INT32 dividend, INT32 divisor, INT32 *pResult)
{
    __try 
    { 
        *pResult = dividend / divisor; 
    } 
    __except(GetExceptionCode() == EXCEPTION_INT_DIVIDE_BY_ZERO ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
    { 
        return FALSE;
    }
    return TRUE;
} 
```



## <a name="example-2"></a><span data-ttu-id="975d9-108">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="975d9-108">Example 2</span></span>

<span data-ttu-id="975d9-109">La funzione di esempio seguente chiama la funzione [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) e usa la gestione strutturata delle eccezioni per verificare la presenza di un'eccezione del punto di interruzione.</span><span class="sxs-lookup"><span data-stu-id="975d9-109">The following example function calls the [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function and uses structured exception handling to check for a breakpoint exception.</span></span> <span data-ttu-id="975d9-110">Se si verifica un errore, la funzione restituisce **false**, in caso contrario restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="975d9-110">If one occurs, the function returns **FALSE**— otherwise it returns **TRUE**.</span></span>

<span data-ttu-id="975d9-111">L'espressione di filtro nell'esempio usa la funzione [**GetExceptionCode**](getexceptioncode.md) per controllare il tipo di eccezione prima di eseguire il gestore.</span><span class="sxs-lookup"><span data-stu-id="975d9-111">The filter expression in the example uses the [**GetExceptionCode**](getexceptioncode.md) function to check the exception type before executing the handler.</span></span> <span data-ttu-id="975d9-112">Ciò consente al sistema di continuare la ricerca di un gestore appropriato se si verifica un altro tipo di eccezione.</span><span class="sxs-lookup"><span data-stu-id="975d9-112">This enables the system to continue its search for an appropriate handler if some other type of exception occurs.</span></span>

<span data-ttu-id="975d9-113">Inoltre, l'utilizzo dell'istruzione **return** nel blocco **\_ \_ try** di un gestore di eccezioni è diverso dall'utilizzo di **return** nel blocco **\_ \_ try** di un gestore di terminazione, causando una chiusura anomala del blocco **\_ \_ try** .</span><span class="sxs-lookup"><span data-stu-id="975d9-113">Also, use of the **return** statement in the **\_\_try** block of an exception handler differs from the use of **return** in the **\_\_try** block of a termination handler, which causes an abnormal termination of the **\_\_try** block.</span></span> <span data-ttu-id="975d9-114">Si tratta di un utilizzo valido dell'istruzione return in un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="975d9-114">This is an valid use of the return statement in an exception handler.</span></span>


```C++
BOOL CheckForDebugger()
{
    __try 
    {
        DebugBreak();
    }
    __except(GetExceptionCode() == EXCEPTION_BREAKPOINT ? 
             EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH) 
    {
        // No debugger is attached, so return FALSE 
        // and continue.
        return FALSE;
    }
    return TRUE;
}
```



<span data-ttu-id="975d9-115">Restituisce solo il \_ \_ gestore di esecuzione eccezioni da un filtro eccezioni quando è previsto il tipo di eccezione e l'indirizzo di errore è noto.</span><span class="sxs-lookup"><span data-stu-id="975d9-115">Only return EXCEPTION\_EXECUTE\_HANDLER from an exception filter when the exception type is expected and the faulting address is known.</span></span> <span data-ttu-id="975d9-116">È necessario consentire al gestore di eccezioni predefinito di elaborare tipi di eccezione e indirizzi di errore imprevisti.</span><span class="sxs-lookup"><span data-stu-id="975d9-116">You should allow the default exception handler to process unexpected exception types and faulting addresses.</span></span>

## <a name="example-3"></a><span data-ttu-id="975d9-117">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="975d9-117">Example 3</span></span>

<span data-ttu-id="975d9-118">Nell'esempio seguente viene illustrata l'interazione dei gestori annidati.</span><span class="sxs-lookup"><span data-stu-id="975d9-118">The following example shows the interaction of nested handlers.</span></span> <span data-ttu-id="975d9-119">La funzione [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) genera un'eccezione nel corpo sorvegliato di un gestore di terminazione che si trova all'interno del corpo sorvegliato di un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="975d9-119">The [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) function causes an exception in the guarded body of a termination handler that is inside the guarded body of an exception handler.</span></span> <span data-ttu-id="975d9-120">L'eccezione fa in modo che il sistema valuti la funzione FilterFunction, il cui valore restituito a sua volta causa la chiamata del gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="975d9-120">The exception causes the system to evaluate the FilterFunction function, whose return value in turn causes the exception handler to be invoked.</span></span> <span data-ttu-id="975d9-121">Tuttavia, prima dell'esecuzione del blocco del gestore di eccezioni, viene eseguito il blocco **\_ \_ finally** del gestore di terminazione, perché il flusso di controllo ha lasciato il blocco **\_ \_ try** del gestore di terminazione.</span><span class="sxs-lookup"><span data-stu-id="975d9-121">However, before the exception-handler block is executed, the **\_\_finally** block of the termination handler is executed because the flow of control has left the **\_\_try** block of the termination handler.</span></span>


```C++
DWORD FilterFunction() 
{ 
    printf("1 ");                     // printed first 
    return EXCEPTION_EXECUTE_HANDLER; 
} 
 
VOID main(VOID) 
{ 
    __try 
    { 
        __try 
        { 
            RaiseException( 
                1,                    // exception code 
                0,                    // continuable exception 
                0, NULL);             // no arguments 
        } 
        __finally 
        { 
            printf("2 ");             // this is printed second 
        } 
    } 
    __except ( FilterFunction() ) 
    { 
        printf("3\n");                // this is printed last 
    } 
}
```



 

 
