---
description: Nell'esempio seguente viene illustrato l'utilizzo dei nomi di oggetto tramite la creazione e l'apertura di un mutex denominato.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Uso di oggetti denominati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a349e3e26f661ca988bc5c5ebbc7b3c6ea622956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312738"
---
# <a name="using-named-objects"></a><span data-ttu-id="554f2-103">Uso di oggetti denominati</span><span class="sxs-lookup"><span data-stu-id="554f2-103">Using Named Objects</span></span>

<span data-ttu-id="554f2-104">Nell'esempio seguente viene illustrato l'utilizzo dei [nomi di oggetto](object-names.md) tramite la creazione e l'apertura di un mutex denominato.</span><span class="sxs-lookup"><span data-stu-id="554f2-104">The following example illustrates the use of [object names](object-names.md) by creating and opening a named mutex.</span></span>

## <a name="first-process"></a><span data-ttu-id="554f2-105">Primo processo</span><span class="sxs-lookup"><span data-stu-id="554f2-105">First Process</span></span>

<span data-ttu-id="554f2-106">Il primo processo utilizza la funzione [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) per creare l'oggetto mutex.</span><span class="sxs-lookup"><span data-stu-id="554f2-106">The first process uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create the mutex object.</span></span> <span data-ttu-id="554f2-107">Si noti che questa funzione ha esito positivo anche se è presente un oggetto esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="554f2-107">Note that this function succeeds even if there is an existing object with the same name.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <conio.h>

// This process creates the mutex object.

int main(void)
{
    HANDLE hMutex; 

    hMutex = CreateMutex( 
        NULL,                        // default security descriptor
        FALSE,                       // mutex not owned
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("CreateMutex error: %d\n", GetLastError() ); 
    else 
        if ( GetLastError() == ERROR_ALREADY_EXISTS ) 
            printf("CreateMutex opened an existing mutex\n"); 
        else printf("CreateMutex created a new mutex.\n");

    // Keep this process around until the second process is run
    _getch();

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="second-process"></a><span data-ttu-id="554f2-108">Secondo processo</span><span class="sxs-lookup"><span data-stu-id="554f2-108">Second Process</span></span>

<span data-ttu-id="554f2-109">Il secondo processo usa la funzione [**errore in OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) per aprire un handle per il mutex esistente.</span><span class="sxs-lookup"><span data-stu-id="554f2-109">The second process uses the [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) function to open a handle to the existing mutex.</span></span> <span data-ttu-id="554f2-110">Questa funzione ha esito negativo se non esiste un oggetto mutex con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="554f2-110">This function fails if a mutex object with the specified name does not exist.</span></span> <span data-ttu-id="554f2-111">Il parametro di accesso richiede l'accesso completo all'oggetto mutex, che è necessario per l'utilizzo dell'handle in una qualsiasi delle funzioni di attesa.</span><span class="sxs-lookup"><span data-stu-id="554f2-111">The access parameter requests full access to the mutex object, which is necessary for the handle to be used in any of the wait functions.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

// This process opens a handle to a mutex created by another process.

int main(void)
{
    HANDLE hMutex; 

    hMutex = OpenMutex( 
        MUTEX_ALL_ACCESS,            // request full access
        FALSE,                       // handle not inheritable
        TEXT("NameOfMutexObject"));  // object name

    if (hMutex == NULL) 
        printf("OpenMutex error: %d\n", GetLastError() );
    else printf("OpenMutex successfully opened the mutex.\n");

    CloseHandle(hMutex);

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="554f2-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="554f2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="554f2-113">Nomi degli oggetti</span><span class="sxs-lookup"><span data-stu-id="554f2-113">Object Names</span></span>](object-names.md)
</dt> <dt>

[<span data-ttu-id="554f2-114">Utilizzo di oggetti mutex</span><span class="sxs-lookup"><span data-stu-id="554f2-114">Using Mutex Objects</span></span>](using-mutex-objects.md)
</dt> </dl>

 

 
