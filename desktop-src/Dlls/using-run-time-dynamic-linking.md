---
description: È possibile usare la stessa DLL sia nel collegamento dinamico in fase di caricamento che in quello di esecuzione.
ms.assetid: 0ffce2b1-ce50-4550-aa68-6628fdcac01a
title: Uso Run-Time collegamento dinamico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c13cc66a34f0fd5938fcdada027b30223ebff0abe6e9ce459d60f93a6546f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119255981"
---
# <a name="using-run-time-dynamic-linking"></a>Uso Run-Time collegamento dinamico

È possibile usare la stessa DLL sia nel collegamento dinamico in fase di caricamento che in quello di esecuzione. L'esempio seguente usa [**la funzione LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per ottenere un handle per la DLL Myputs (vedere [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)). Se **LoadLibrary** ha esito positivo, il programma usa l'handle restituito nella [**funzione GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per ottenere l'indirizzo della funzione myPuts della DLL. Dopo aver chiamato la funzione DLL, il programma chiama la [**funzione FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per scaricare la DLL.

Poiché il programma usa il collegamento dinamico in fase di esecuzione, non è necessario collegare il modulo a una libreria di importazione per la DLL.

Questo esempio illustra una differenza importante tra il collegamento dinamico in fase di esecuzione e quello in fase di caricamento. Se la DLL non è disponibile, l'applicazione che usa il collegamento dinamico in fase di caricamento deve semplicemente terminare. L'esempio di collegamento dinamico in fase di esecuzione, tuttavia, può rispondere all'errore.


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

 

 
