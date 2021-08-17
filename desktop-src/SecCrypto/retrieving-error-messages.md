---
description: Quando una chiamata al metodo genera un errore, molte funzioni restituiscono un codice di errore.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Recupero di messaggi di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d96ffb6627dac4f8612a80c68b1a227516ec645440c56dd7c58672cd8222c23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900509"
---
# <a name="retrieving-error-messages"></a>Recupero di messaggi di errore

Quando una chiamata al metodo genera un errore, molte funzioni restituiscono un codice di errore. Per la maggior parte delle interfacce di Servizi certificati e degli elementi API che restituiscono un codice di errore, il testo del messaggio di errore può essere recuperato chiamando [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con un handle di modulo **NULL.** Se **FormatMessage non** riesce, è probabile che il codice di errore sia stato generato da un elemento API di backup o da un errore correlato al database. Chiamando **FormatMessage con** un handle di modulo corrispondente alla libreria Ntdsbmsg.dll deve recuperare il testo del messaggio di errore. Nell'esempio seguente viene illustrato come recuperare il testo del messaggio di errore in un'applicazione di Servizi certificati.


```C++
#include <windows.h>
#include <stdio.h>
// Display error message text, given an error code.
// Typically, the parameter passed to this function is retrieved
// from GetLastError().
void PrintCSBackupAPIErrorMessage(DWORD dwErr)
{

    WCHAR   wszMsgBuff[512];  // Buffer for text.

    DWORD   dwChars;  // Number of chars returned.

    // Try to get the message from the system errors.
    dwChars = FormatMessage( FORMAT_MESSAGE_FROM_SYSTEM |
                             FORMAT_MESSAGE_IGNORE_INSERTS,
                             NULL,
                             dwErr,
                             0,
                             wszMsgBuff,
                             512,
                             NULL );

    if (0 == dwChars)
    {
        // The error code did not exist in the system errors.
        // Try Ntdsbmsg.dll for the error code.

        HINSTANCE hInst;

        // Load the library.
        hInst = LoadLibrary(L"Ntdsbmsg.dll");
        if ( NULL == hInst )
        {
            printf("cannot load Ntdsbmsg.dll\n");
            exit(1);  // Could 'return' instead of 'exit'.
        }

        // Try getting message text from ntdsbmsg.
        dwChars = FormatMessage( FORMAT_MESSAGE_FROM_HMODULE |
                                 FORMAT_MESSAGE_IGNORE_INSERTS,
                                 hInst,
                                 dwErr,
                                 0,
                                 wszMsgBuff,
                                 512,
                                 NULL );

        // Free the library.
        FreeLibrary( hInst );

    }

    // Display the error message, or generic text if not found.
    printf("Error value: %d Message: %ws\n",
            dwErr,
            dwChars ? wszMsgBuff : L"Error message not found." );

}
```



 

 
