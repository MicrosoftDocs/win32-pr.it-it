---
description: Quando una chiamata al metodo genera un errore, molte funzioni restituiscono un codice di errore.
ms.assetid: 9d60277a-5ee8-471e-bfcd-d104064030a8
title: Recupero dei messaggi di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cefeab75e4419bc1e36785236962069a6913e84d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881657"
---
# <a name="retrieving-error-messages"></a>Recupero dei messaggi di errore

Quando una chiamata al metodo genera un errore, molte funzioni restituiscono un codice di errore. Per la maggior parte delle interfacce di Servizi certificati e degli elementi API che restituiscono un codice di errore, è possibile recuperare il testo del messaggio di errore chiamando [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con un handle di modulo **null** . Se **FormatMessage** ha esito negativo, il codice di errore probabilmente è risultato da un errore relativo al database o all'elemento API di backup; la chiamata di **FormatMessage** con un handle di modulo corrispondente alla libreria Ntdsbmsg.dll deve recuperare il testo del messaggio di errore. Nell'esempio seguente viene illustrato come recuperare il testo del messaggio di errore in un'applicazione di Servizi certificati.


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



 

 
