---
description: L'esempio seguente illustra l'uso dei nomi di oggetto creando e aprendo un mutex denominato.
ms.assetid: 06199f83-8fe0-42b9-9db1-58fe1443db4e
title: Uso di oggetti denominati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e31d21af713a28d5bee501349e818327750cba15a961ebd0f6a5295be91e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765130"
---
# <a name="using-named-objects"></a>Uso di oggetti denominati

L'esempio seguente illustra l'uso dei nomi [di oggetto](object-names.md) creando e aprendo un mutex denominato.

## <a name="first-process"></a>Primo processo

Il primo processo usa la [**funzione CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) per creare l'oggetto mutex. Si noti che questa funzione ha esito positivo anche se è presente un oggetto esistente con lo stesso nome.


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



## <a name="second-process"></a>Secondo processo

Il secondo processo usa la [**funzione OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) per aprire un handle per il mutex esistente. Questa funzione ha esito negativo se non esiste un oggetto mutex con il nome specificato. Il parametro di accesso richiede l'accesso completo all'oggetto mutex, necessario per l'uso dell'handle in una delle funzioni di attesa.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Nomi degli oggetti](object-names.md)
</dt> <dt>

[Uso di oggetti Mutex](using-mutex-objects.md)
</dt> </dl>

 

 
