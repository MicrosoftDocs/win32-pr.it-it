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
# <a name="using-named-objects"></a>Uso di oggetti denominati

Nell'esempio seguente viene illustrato l'utilizzo dei [nomi di oggetto](object-names.md) tramite la creazione e l'apertura di un mutex denominato.

## <a name="first-process"></a>Primo processo

Il primo processo utilizza la funzione [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) per creare l'oggetto mutex. Si noti che questa funzione ha esito positivo anche se è presente un oggetto esistente con lo stesso nome.


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

Il secondo processo usa la funzione [**errore in OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) per aprire un handle per il mutex esistente. Questa funzione ha esito negativo se non esiste un oggetto mutex con il nome specificato. Il parametro di accesso richiede l'accesso completo all'oggetto mutex, che è necessario per l'utilizzo dell'handle in una qualsiasi delle funzioni di attesa.


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

[Utilizzo di oggetti mutex](using-mutex-objects.md)
</dt> </dl>

 

 
