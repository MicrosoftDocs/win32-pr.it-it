---
description: È possibile utilizzare la stessa DLL in entrambi i tempi di caricamento e il collegamento dinamico in fase di esecuzione.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Uso di Run-Time collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d6ca65c510433350b81a282d8bf7a3a3825ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310040"
---
# <a name="using-run-time-dynamic-linking"></a>Uso di Run-Time collegamento dinamico

È possibile utilizzare la stessa DLL in entrambi i tempi di caricamento e il collegamento dinamico in fase di esecuzione. Nell'esempio seguente viene usata la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per ottenere un handle per la dll put (vedere [creazione di una semplice libreria di Dynamic-Link](creating-a-simple-dynamic-link-library.md)). Se **LoadLibrary** ha esito positivo, il programma usa l'handle restituito nella funzione [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere l'indirizzo della funzione My put della dll. Dopo aver chiamato la funzione DLL, il programma chiama la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per scaricare la dll.

Poiché il programma utilizza il collegamento dinamico in fase di esecuzione, non è necessario collegare il modulo a una libreria di importazione per la DLL.

In questo esempio viene illustrata una differenza importante tra il collegamento dinamico in fase di esecuzione e in fase di caricamento. Se la DLL non è disponibile, l'applicazione che utilizza il collegamento dinamico in fase di caricamento deve semplicemente terminare. Tuttavia, l'esempio di collegamento dinamico in fase di esecuzione può rispondere all'errore.


```C++
// A simple program that uses LoadLibrary and 
// GetProcAddress to access myPuts from Myputs.dll. 
 
#include <windows.h> 
#include <stdio.h> 
 
typedef int (__cdecl *MYPROC)(LPWSTR); 
 
int main( void ) 
{ 
    HINSTANCE hinstLib; 
    MYPROC ProcAdd; 
    BOOL fFreeResult, fRunTimeLinkSuccess = FALSE; 
 
    // Get a handle to the DLL module.
 
    hinstLib = LoadLibrary(TEXT("MyPuts.dll")); 
 
    // If the handle is valid, try to get the function address.
 
    if (hinstLib != NULL) 
    { 
        ProcAdd = (MYPROC) GetProcAddress(hinstLib, "myPuts"); 
 
        // If the function address is valid, call the function.
 
        if (NULL != ProcAdd) 
        {
            fRunTimeLinkSuccess = TRUE;
            (ProcAdd) (L"Message sent to the DLL function\n"); 
        }
        // Free the DLL module.
 
        fFreeResult = FreeLibrary(hinstLib); 
    } 

    // If unable to call the DLL function, use an alternative.
    if (! fRunTimeLinkSuccess) 
        printf("Message printed from executable\n"); 

    return 0;

}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Collegamento dinamico in fase di esecuzione](run-time-dynamic-linking.md)
</dt> </dl>

 

 
