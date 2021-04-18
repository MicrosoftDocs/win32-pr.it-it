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
# <a name="reserving-and-committing-memory"></a><span data-ttu-id="4a863-103">Riserva e commit della memoria</span><span class="sxs-lookup"><span data-stu-id="4a863-103">Reserving and Committing Memory</span></span>

<span data-ttu-id="4a863-104">Nell'esempio seguente viene illustrato l'utilizzo delle funzioni [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) e [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) per la conservazione e il commit della memoria in base alle esigenze di una matrice dinamica.</span><span class="sxs-lookup"><span data-stu-id="4a863-104">The following example illustrates the use of the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) and [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) functions in reserving and committing memory as needed for a dynamic array.</span></span> <span data-ttu-id="4a863-105">Per prima cosa, viene chiamato **VirtualAlloc** per riservare un blocco di pagine con **null** specificato come parametro dell'indirizzo di base, forzando il sistema a determinare il percorso del blocco.</span><span class="sxs-lookup"><span data-stu-id="4a863-105">First, **VirtualAlloc** is called to reserve a block of pages with **NULL** specified as the base address parameter, forcing the system to determine the location of the block.</span></span> <span data-ttu-id="4a863-106">Successivamente, **VirtualAlloc** viene chiamato ogni volta che è necessario eseguire il commit di una pagina da questa area riservata e viene specificato l'indirizzo di base della pagina successiva di cui è stato eseguito il commit.</span><span class="sxs-lookup"><span data-stu-id="4a863-106">Later, **VirtualAlloc** is called whenever it is necessary to commit a page from this reserved region, and the base address of the next page to be committed is specified.</span></span>

<span data-ttu-id="4a863-107">Nell'esempio viene usata la sintassi strutturata di gestione delle eccezioni per eseguire il commit di pagine dall'area riservata.</span><span class="sxs-lookup"><span data-stu-id="4a863-107">The example uses structured exception-handling syntax to commit pages from the reserved region.</span></span> <span data-ttu-id="4a863-108">Ogni volta che si verifica un'eccezione di errore di pagina durante l'esecuzione del blocco **\_ \_ try** , viene eseguita la funzione di filtro nell'espressione che precede il blocco **\_ \_ except** .</span><span class="sxs-lookup"><span data-stu-id="4a863-108">Whenever a page fault exception occurs during the execution of the **\_\_try** block, the filter function in the expression preceding the **\_\_except** block is executed.</span></span> <span data-ttu-id="4a863-109">Se la funzione di filtro può allocare un'altra pagina, l'esecuzione continua nel blocco **\_ \_ try** nel punto in cui si è verificata l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="4a863-109">If the filter function can allocate another page, execution continues in the **\_\_try** block at the point where the exception occurred.</span></span> <span data-ttu-id="4a863-110">In caso contrario, viene eseguito il gestore di eccezioni nel blocco **\_ \_ except** .</span><span class="sxs-lookup"><span data-stu-id="4a863-110">Otherwise, the exception handler in the **\_\_except** block is executed.</span></span> <span data-ttu-id="4a863-111">Per altre informazioni, vedere [gestione delle eccezioni strutturata](../debug/structured-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="4a863-111">For more information, see [Structured Exception Handling](../debug/structured-exception-handling.md).</span></span>

<span data-ttu-id="4a863-112">In alternativa all'allocazione dinamica, il processo può semplicemente eseguire il commit dell'intera area anziché riservarlo.</span><span class="sxs-lookup"><span data-stu-id="4a863-112">As an alternative to dynamic allocation, the process can simply commit the entire region instead of only reserving it.</span></span> <span data-ttu-id="4a863-113">Entrambi i metodi generano lo stesso utilizzo di memoria fisica, perché le pagine di cui è stato eseguito il commit non utilizzano alcuna risorsa di archiviazione fisica fino a quando non vengono prima</span><span class="sxs-lookup"><span data-stu-id="4a863-113">Both methods result in the same physical memory usage because committed pages do not consume any physical storage until they are first accessed.</span></span> <span data-ttu-id="4a863-114">Il vantaggio dell'allocazione dinamica è che riduce al minimo il numero totale di pagine di cui è stato eseguito il commit nel sistema.</span><span class="sxs-lookup"><span data-stu-id="4a863-114">The advantage of dynamic allocation is that it minimizes the total number of committed pages on the system.</span></span> <span data-ttu-id="4a863-115">Per le allocazioni di grandi dimensioni, il precommit di un'intera allocazione può causare l'esaurimento delle pagine di cui è possibile eseguire il commit, causando errori di allocazione della memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a863-115">For very large allocations, pre-committing an entire allocation can cause the system to run out of committable pages, resulting in virtual memory allocation failures.</span></span>

<span data-ttu-id="4a863-116">La funzione [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) nel blocco **\_ \_ except** rilascia automaticamente le allocazioni di memoria virtuale, pertanto non è necessario liberare in modo esplicito le pagine quando il programma termina attraverso questo percorso di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4a863-116">The [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function in the **\_\_except** block automatically releases virtual memory allocations, so it is not necessary to explicitly free the pages when the program terminates through this execution path.</span></span> <span data-ttu-id="4a863-117">La funzione [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) libera le pagine riservate e di cui è stato eseguito il commit se il programma viene compilato con la gestione delle eccezioni disabilitata.</span><span class="sxs-lookup"><span data-stu-id="4a863-117">The [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) function frees the reserved and committed pages if the program is built with exception handling disabled.</span></span> <span data-ttu-id="4a863-118">Questa funzione usa **la \_ versione di MEM** per eseguire il commit e rilasciare l'intera area di pagine riservate e di cui è stato eseguito il commit</span><span class="sxs-lookup"><span data-stu-id="4a863-118">This function uses **MEM\_RELEASE** to decommit and release the entire region of reserved and committed pages.</span></span>

<span data-ttu-id="4a863-119">Nell'esempio C++ riportato di seguito viene illustrata l'allocazione di memoria dinamica utilizzando un gestore di eccezioni strutturato</span><span class="sxs-lookup"><span data-stu-id="4a863-119">The following C++ example demonstrates dynamic memory allocation using a structured exception handler.</span></span>


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



 

 
