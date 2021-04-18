---
description: Nell'esempio seguente viene riportato il codice sorgente necessario per creare una DLL semplice, Myputs.dll.
ms.assetid: 3b11a83b-9943-4b66-8d0d-4a236ad5ffb8
title: Creazione di una semplice libreria di Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572c25c87a3130739a55fcccfc9d8f9c6514d812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308923"
---
# <a name="creating-a-simple-dynamic-link-library"></a>Creazione di una semplice libreria di Dynamic-Link

Nell'esempio seguente viene riportato il codice sorgente necessario per creare una DLL semplice, Myputs.dll. Definisce una semplice funzione di stampa stringa denominata put. La DLL put non definisce una funzione del punto di ingresso, perché è collegata alla libreria di runtime del linguaggio C e non dispone di funzioni di inizializzazione o pulitura proprie da eseguire.

Per compilare la DLL, seguire le istruzioni riportate nella documentazione inclusa con gli strumenti di sviluppo.

Per un esempio in cui viene usato il valore di, vedere [uso di Load-Time collegamento dinamico](using-load-time-dynamic-linking.md) o [uso di Run-Time collegamento dinamico](using-run-time-dynamic-linking.md).


```C++
// The myPuts function writes a null-terminated string to
// the standard output device.
 
// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.
 
 
#include <windows.h>
 
#define EOF (-1)
 
#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif
 
__declspec(dllexport) int __cdecl myPuts(LPWSTR lpszMsg)
{
    DWORD cchWritten;
    HANDLE hConout;
    BOOL fRet;
 
    // Get a handle to the console output device.

    hConout = CreateFileW(L"CONOUT$",
                         GENERIC_WRITE,
                         FILE_SHARE_WRITE,
                         NULL,
                         OPEN_EXISTING,
                         FILE_ATTRIBUTE_NORMAL,
                         NULL);

    if (INVALID_HANDLE_VALUE == hConout)
        return EOF;
 
    // Write a null-terminated string to the console output device.
 
    while (*lpszMsg != L'\0')
    {
        fRet = WriteConsole(hConout, lpszMsg, 1, &cchWritten, NULL);
        if( (FALSE == fRet) || (1 != cchWritten) )
            return EOF;
        lpszMsg++;
    }
    return 1;
}
 
#ifdef __cplusplus
}
#endif
```



 

 



