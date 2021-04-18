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
# <a name="using-an-exception-handler"></a>Uso di un gestore di eccezioni

Negli esempi seguenti viene illustrato l'utilizzo di un gestore di eccezioni.

## <a name="example-1"></a>Esempio 1

Il frammento di codice seguente usa la gestione delle eccezioni strutturata per verificare se un'operazione di divisione su interi a 2 32 bit provocherà un errore di divisione per zero. In tal caso, la funzione restituisce **false**, in caso contrario restituisce **true**.


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



## <a name="example-2"></a>Esempio 2

La funzione di esempio seguente chiama la funzione [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) e usa la gestione strutturata delle eccezioni per verificare la presenza di un'eccezione del punto di interruzione. Se si verifica un errore, la funzione restituisce **false**, in caso contrario restituisce **true**.

L'espressione di filtro nell'esempio usa la funzione [**GetExceptionCode**](getexceptioncode.md) per controllare il tipo di eccezione prima di eseguire il gestore. Ciò consente al sistema di continuare la ricerca di un gestore appropriato se si verifica un altro tipo di eccezione.

Inoltre, l'utilizzo dell'istruzione **return** nel blocco **\_ \_ try** di un gestore di eccezioni è diverso dall'utilizzo di **return** nel blocco **\_ \_ try** di un gestore di terminazione, causando una chiusura anomala del blocco **\_ \_ try** . Si tratta di un utilizzo valido dell'istruzione return in un gestore di eccezioni.


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



Restituisce solo il \_ \_ gestore di esecuzione eccezioni da un filtro eccezioni quando è previsto il tipo di eccezione e l'indirizzo di errore è noto. È necessario consentire al gestore di eccezioni predefinito di elaborare tipi di eccezione e indirizzi di errore imprevisti.

## <a name="example-3"></a>Esempio 3

Nell'esempio seguente viene illustrata l'interazione dei gestori annidati. La funzione [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) genera un'eccezione nel corpo sorvegliato di un gestore di terminazione che si trova all'interno del corpo sorvegliato di un gestore di eccezioni. L'eccezione fa in modo che il sistema valuti la funzione FilterFunction, il cui valore restituito a sua volta causa la chiamata del gestore di eccezioni. Tuttavia, prima dell'esecuzione del blocco del gestore di eccezioni, viene eseguito il blocco **\_ \_ finally** del gestore di terminazione, perché il flusso di controllo ha lasciato il blocco **\_ \_ try** del gestore di terminazione.


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



 

 
