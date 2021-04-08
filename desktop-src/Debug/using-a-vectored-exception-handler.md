---
description: Nell'esempio di codice riportato di seguito viene illustrato come utilizzare la gestione delle eccezioni vettoriale. Usa la funzione AddVectoredExceptionHandler per aggiungere diversi gestori, verifica i gestori, quindi usa la funzione RemoveVectoredExceptionHandler per rimuovere i gestori.
ms.assetid: dbf7016b-09ac-4ca7-9b47-38b0dd763462
title: Uso di un gestore di eccezioni con vettori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c766d6695ebebdcb65f2895356866233117d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877778"
---
# <a name="using-a-vectored-exception-handler"></a>Uso di un gestore di eccezioni con vettori

Nell'esempio di codice riportato di seguito viene illustrato come utilizzare la gestione delle eccezioni vettoriale. Usa la funzione [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) per aggiungere diversi gestori, verifica i gestori, quindi usa la funzione [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) per rimuovere i gestori.

**Windows a 64 bit:** Questo codice non è adatto per Windows a 64 bit.


```C++
#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>

// NOTE: The CONTEXT structure contains processor-specific 
// information. This sample was designed for X86 processors.

//addVectoredExceptionHandler constants:
//CALL_FIRST means call this exception handler first;
//CALL_LAST means call this exception handler last
#define CALL_FIRST 1  
#define CALL_LAST 0

LONG Sequence=1;
LONG Actual[3];

LONG WINAPI
VectoredHandler1(
    struct _EXCEPTION_POINTERS *ExceptionInfo
    )
{
    UNREFERENCED_PARAMETER(ExceptionInfo);
    
    Actual[0] = Sequence++;
    return EXCEPTION_CONTINUE_SEARCH;
}

LONG WINAPI
VectoredHandler2(
    struct _EXCEPTION_POINTERS *ExceptionInfo
    )
{
    UNREFERENCED_PARAMETER(ExceptionInfo);

    Actual[1] = Sequence++;
    return EXCEPTION_CONTINUE_SEARCH;
}

LONG WINAPI
VectoredHandler3(
    struct _EXCEPTION_POINTERS *ExceptionInfo
    )
{
    UNREFERENCED_PARAMETER(ExceptionInfo);

    Actual[2] = Sequence++;
    return EXCEPTION_CONTINUE_SEARCH;
}

LONG WINAPI
VectoredHandlerSkip1(
    struct _EXCEPTION_POINTERS *ExceptionInfo
    )
{
    PCONTEXT Context;
    
    Sequence++;
    Context = ExceptionInfo->ContextRecord;
    Actual[0] = 0xcc;
#ifdef _AMD64_
    Context->Rip++;
#else
    Context->Eip++;
#endif    
    return EXCEPTION_CONTINUE_EXECUTION;
}

LONG WINAPI
VectoredHandlerSkip2(
    struct _EXCEPTION_POINTERS *ExceptionInfo
    )
{
    PCONTEXT Context;
    
    Sequence++;
    Context = ExceptionInfo->ContextRecord;
    Actual[1] = 0xcc;
#ifdef _AMD64_
    Context->Rip++;
#else
    Context->Eip++;
#endif    
    return EXCEPTION_CONTINUE_EXECUTION;
}

LONG WINAPI
VectoredHandlerSkip3(
    struct _EXCEPTION_POINTERS *ExceptionInfo
    )
{
    PCONTEXT Context;
    
    Sequence++;
    Context = ExceptionInfo->ContextRecord;
    Actual[2] = 0xcc;
#ifdef _AMD64_
    Context->Rip++;
#else
    Context->Eip++;
#endif    
    return EXCEPTION_CONTINUE_EXECUTION;
}

BOOL CheckTest(
    char *Variation,
    PLONG e,
    PLONG a
    )
{
    int i;
    BOOL Pass = TRUE;

    for(i=0;i<3;i++) 
    {
        if (e[i] != a[i]) 
        {
            if (Variation) 
            {
                printf("%s Failed at %d Expected %d vs Actual %d\n", 
                        Variation, i, e[i], a[i]);
            }
            Pass = FALSE;
        }

        // Clear actual for next pass.
        a[i] = 0;
    }

    // Get ready for next pass.
    Sequence = 1;

    if (Variation) 
    {
        printf("Variation %s %s\n", Variation, 
                Pass ? "Passed" : "Failed");
    }
    return Pass;
}

void
CheckAllClear()
{
    LONG e[3];
    BOOL b = 0;

    e[0]=0;e[1]=0;e[2]=0;
    __try 
    {
        RaiseException(1,0,0,NULL);
    }
    __except(EXCEPTION_EXECUTE_HANDLER)
    {
        b = CheckTest(NULL,e,Actual);
    }
    if (!b) 
    {
        printf("Fatal error, handlers still registered.\n");
    }
}

void IllegalInst()
{
    char *ptr = 0;
    *ptr = 0;
}

void Test1()
{
    
    PVOID h1,h2,h3;
    LONG e[3];
     
    e[0]=1;e[1]=2;e[2]=3;
    h2 = AddVectoredExceptionHandler(CALL_FIRST,VectoredHandler2);
    h3 = AddVectoredExceptionHandler(CALL_LAST,VectoredHandler3);
    h1 = AddVectoredExceptionHandler(CALL_FIRST,VectoredHandler1);

    __try 
    {
        RaiseException(1,0,0,NULL);
    }
    __except(EXCEPTION_EXECUTE_HANDLER)
    {
        CheckTest("Test1a",e,Actual);
    }

    RemoveVectoredExceptionHandler(h1);
    RemoveVectoredExceptionHandler(h3);
    RemoveVectoredExceptionHandler(h2);
    CheckAllClear();
}

void Test2()
{
    
    PVOID h1,h2,h3;
    LONG e[3];
     
    e[0]=0xcc;e[1]=0;e[2]=0;
    h1 = AddVectoredExceptionHandler(1,VectoredHandlerSkip1);
    IllegalInst();
    CheckTest("Test2a",e,Actual);
    RemoveVectoredExceptionHandler(h1);
    CheckAllClear();

    e[0]=1;e[1]=2;e[2]=0xcc;
    h2 = AddVectoredExceptionHandler(CALL_FIRST,VectoredHandler2);
    h3 = AddVectoredExceptionHandler(CALL_LAST,VectoredHandlerSkip3);
    h1 = AddVectoredExceptionHandler(CALL_FIRST,VectoredHandler1);
    IllegalInst();
    CheckTest("Test2b",e,Actual);
    RemoveVectoredExceptionHandler(h1);
    RemoveVectoredExceptionHandler(h2);
    RemoveVectoredExceptionHandler(h3);
    CheckAllClear();

    e[0]=1;e[1]=0xcc;e[2]=0;
    h1 = AddVectoredExceptionHandler(CALL_LAST,VectoredHandler1);
    h2 = AddVectoredExceptionHandler(CALL_LAST,VectoredHandlerSkip2);
    h3 = AddVectoredExceptionHandler(CALL_LAST,VectoredHandler3);
    IllegalInst();
    CheckTest("Test2c",e,Actual);
    RemoveVectoredExceptionHandler(h1);
    RemoveVectoredExceptionHandler(h2);
    RemoveVectoredExceptionHandler(h3);
    CheckAllClear();

    e[0]=2;e[1]=0xcc;e[2]=1;
    h1 = AddVectoredExceptionHandler(CALL_LAST,VectoredHandler1);
    h3 = AddVectoredExceptionHandler(CALL_FIRST,VectoredHandler3);
    h2 = AddVectoredExceptionHandler(CALL_LAST,VectoredHandlerSkip2);
    __try 
    {
        IllegalInst();
    }
    __except(EXCEPTION_EXECUTE_HANDLER)
    {
        // Should not make it to here.
        e[0]=0;e[1]=0;e[2]=0;
        CheckTest("Test2d-1",e,Actual);
    }
    CheckTest("Test2d-2",e,Actual);
    RemoveVectoredExceptionHandler(h1);
    RemoveVectoredExceptionHandler(h2);
    RemoveVectoredExceptionHandler(h3);
    CheckAllClear();
}

void main( )
{
    Test1();
    Test2();
}
```



 

 
