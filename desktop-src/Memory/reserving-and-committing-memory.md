---
description: Nell'esempio seguente viene illustrato l'utilizzo delle funzioni VirtualAlloc e VirtualFree per la conservazione e il commit della memoria in base alle esigenze di una matrice dinamica.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Riserva e commit della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ff5853d01561454265e1ee2102fbf6ebd9bb04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319443"
---
# <a name="reserving-and-committing-memory"></a>Riserva e commit della memoria

Nell'esempio seguente viene illustrato l'utilizzo delle funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) per la conservazione e il commit della memoria in base alle esigenze di una matrice dinamica. Per prima cosa, viene chiamato **VirtualAlloc** per riservare un blocco di pagine con **null** specificato come parametro dell'indirizzo di base, forzando il sistema a determinare il percorso del blocco. Successivamente, **VirtualAlloc** viene chiamato ogni volta che è necessario eseguire il commit di una pagina da questa area riservata e viene specificato l'indirizzo di base della pagina successiva di cui è stato eseguito il commit.

Nell'esempio viene usata la sintassi strutturata di gestione delle eccezioni per eseguire il commit di pagine dall'area riservata. Ogni volta che si verifica un'eccezione di errore di pagina durante l'esecuzione del blocco **\_ \_ try** , viene eseguita la funzione di filtro nell'espressione che precede il blocco **\_ \_ except** . Se la funzione di filtro può allocare un'altra pagina, l'esecuzione continua nel blocco **\_ \_ try** nel punto in cui si è verificata l'eccezione. In caso contrario, viene eseguito il gestore di eccezioni nel blocco **\_ \_ except** . Per altre informazioni, vedere [gestione delle eccezioni strutturata](../debug/structured-exception-handling.md).

In alternativa all'allocazione dinamica, il processo può semplicemente eseguire il commit dell'intera area anziché riservarlo. Entrambi i metodi generano lo stesso utilizzo di memoria fisica, perché le pagine di cui è stato eseguito il commit non utilizzano alcuna risorsa di archiviazione fisica fino a quando non vengono prima Il vantaggio dell'allocazione dinamica è che riduce al minimo il numero totale di pagine di cui è stato eseguito il commit nel sistema. Per le allocazioni di grandi dimensioni, il precommit di un'intera allocazione può causare l'esaurimento delle pagine di cui è possibile eseguire il commit, causando errori di allocazione della memoria virtuale.

La funzione [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) nel blocco **\_ \_ except** rilascia automaticamente le allocazioni di memoria virtuale, pertanto non è necessario liberare in modo esplicito le pagine quando il programma termina attraverso questo percorso di esecuzione. La funzione [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libera le pagine riservate e di cui è stato eseguito il commit se il programma viene compilato con la gestione delle eccezioni disabilitata. Questa funzione usa **la \_ versione di MEM** per eseguire il commit e rilasciare l'intera area di pagine riservate e di cui è stato eseguito il commit

Nell'esempio C++ riportato di seguito viene illustrata l'allocazione di memoria dinamica utilizzando un gestore di eccezioni strutturato


```C++
// A short program to demonstrate dynamic memory allocation
// using a structured exception handler.

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>             // For exit

#define PAGELIMIT 80            // Number of pages to ask for

LPTSTR lpNxtPage;               // Address of the next page to ask for
DWORD dwPages = 0;              // Count of pages gotten so far
DWORD dwPageSize;               // Page size on this computer

INT PageFaultExceptionFilter(DWORD dwCode)
{
    LPVOID lpvResult;

    // If the exception is not a page fault, exit.

    if (dwCode != EXCEPTION_ACCESS_VIOLATION)
    {
        _tprintf(TEXT("Exception code = %d.\n"), dwCode);
        return EXCEPTION_EXECUTE_HANDLER;
    }

    _tprintf(TEXT("Exception is a page fault.\n"));

    // If the reserved pages are used up, exit.

    if (dwPages >= PAGELIMIT)
    {
        _tprintf(TEXT("Exception: out of pages.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }

    // Otherwise, commit another page.

    lpvResult = VirtualAlloc(
                     (LPVOID) lpNxtPage, // Next page to commit
                     dwPageSize,         // Page size, in bytes
                     MEM_COMMIT,         // Allocate a committed page
                     PAGE_READWRITE);    // Read/write access
    if (lpvResult == NULL )
    {
        _tprintf(TEXT("VirtualAlloc failed.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }
    else
    {
        _tprintf(TEXT("Allocating another page.\n"));
    }

    // Increment the page count, and advance lpNxtPage to the next page.

    dwPages++;
    lpNxtPage = (LPTSTR) ((PCHAR) lpNxtPage + dwPageSize);

    // Continue execution where the page fault occurred.

    return EXCEPTION_CONTINUE_EXECUTION;
}

VOID ErrorExit(LPTSTR lpMsg)
{
    _tprintf(TEXT("Error! %s with error code of %ld.\n"),
             lpMsg, GetLastError ());
    exit (0);
}

VOID _tmain(VOID)
{
    LPVOID lpvBase;               // Base address of the test memory
    LPTSTR lpPtr;                 // Generic character pointer
    BOOL bSuccess;                // Flag
    DWORD i;                      // Generic counter
    SYSTEM_INFO sSysInfo;         // Useful information about the system

    GetSystemInfo(&sSysInfo);     // Initialize the structure.

    _tprintf (TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

    dwPageSize = sSysInfo.dwPageSize;

    // Reserve pages in the virtual address space of the process.

    lpvBase = VirtualAlloc(
                     NULL,                 // System selects address
                     PAGELIMIT*dwPageSize, // Size of allocation
                     MEM_RESERVE,          // Allocate reserved pages
                     PAGE_NOACCESS);       // Protection = no access
    if (lpvBase == NULL )
        ErrorExit(TEXT("VirtualAlloc reserve failed."));

    lpPtr = lpNxtPage = (LPTSTR) lpvBase;

    // Use structured exception handling when accessing the pages.
    // If a page fault occurs, the exception filter is executed to
    // commit another page from the reserved block of pages.

    for (i=0; i < PAGELIMIT*dwPageSize; i++)
    {
        __try
        {
            // Write to memory.

            lpPtr[i] = 'a';
        }

        // If there's a page fault, commit another page and try again.

        __except ( PageFaultExceptionFilter( GetExceptionCode() ) )
        {

            // This code is executed only if the filter function
            // is unsuccessful in committing the next page.

            _tprintf (TEXT("Exiting process.\n"));

            ExitProcess( GetLastError() );

        }

    }

    // Release the block of pages when you are finished using them.

    bSuccess = VirtualFree(
                       lpvBase,       // Base address of block
                       0,             // Bytes of committed pages
                       MEM_RELEASE);  // Decommit the pages

    _tprintf (TEXT("Release %s.\n"), bSuccess ? TEXT("succeeded") : TEXT("failed") );

}
```



 

 
