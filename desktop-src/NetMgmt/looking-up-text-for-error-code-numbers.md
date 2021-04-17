---
title: Ricerca di testo per i numeri di codice di errore
description: A volte è necessario visualizzare il testo dell'errore associato ai codici di errore restituiti dalle funzioni correlate alla rete. Potrebbe essere necessario eseguire questa attività con le funzioni di gestione della rete fornite dal sistema.
ms.assetid: 90ed87ca-7a08-4a66-b06a-e1bf668fb81a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0811c2b2da283a9cd5eb776cdb33a175c63491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299914"
---
# <a name="looking-up-text-for-error-code-numbers"></a>Ricerca di testo per i numeri di codice di errore

A volte è necessario visualizzare il testo dell'errore associato ai codici di errore restituiti dalle funzioni correlate alla rete. Potrebbe essere necessario eseguire questa attività con le funzioni di gestione della rete fornite dal sistema.

Il testo dell'errore per questi messaggi è disponibile nel file della tabella dei messaggi denominato Netmsg.dll, disponibile in% SystemRoot% \\ system32. Questo file contiene messaggi di errore compresi nell'intervallo NERR \_ base (2100) fino al numero massimo di \_ NERR (Nerr \_ base + 899). Questi codici di errore sono definiti nel file di intestazione SDK Lmerr. h.

Le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) possono caricare Netmsg.dll. La funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) esegue il mapping di un codice di errore al testo del messaggio, dato un handle del modulo al file Netmsg.dll.

Nell'esempio seguente viene illustrato come visualizzare il testo dell'errore associato alle funzioni di gestione della rete, oltre a visualizzare il testo dell'errore associato ai codici di errore relativi al sistema. Se il numero di errore specificato è compreso in un intervallo specifico, il modulo del messaggio netmsg.dll viene caricato e utilizzato per cercare il numero di errore specificato con la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .


```C++
#include <windows.h>
#include <stdio.h>

#include <lmerr.h>

void
DisplayErrorText(
    DWORD dwLastError
    );

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

int
__cdecl
main(
    int argc,
    char *argv[]
    )
{
    if(argc != 2) {
        fprintf(stderr,"Usage: %s <error number>\n", argv[0]);
        return RTN_USAGE;
    }

    DisplayErrorText( atoi(argv[1]) );

    return RTN_OK;
}

void
DisplayErrorText(
    DWORD dwLastError
    )
{
    HMODULE hModule = NULL; // default to system source
    LPSTR MessageBuffer;
    DWORD dwBufferLength;

    DWORD dwFormatFlags = FORMAT_MESSAGE_ALLOCATE_BUFFER |
        FORMAT_MESSAGE_IGNORE_INSERTS |
        FORMAT_MESSAGE_FROM_SYSTEM ;

    //
    // If dwLastError is in the network range, 
    //  load the message source.
    //

    if(dwLastError >= NERR_BASE && dwLastError <= MAX_NERR) {
        hModule = LoadLibraryEx(
            TEXT("netmsg.dll"),
            NULL,
            LOAD_LIBRARY_AS_DATAFILE
            );

        if(hModule != NULL)
            dwFormatFlags |= FORMAT_MESSAGE_FROM_HMODULE;
    }

    //
    // Call FormatMessage() to allow for message 
    //  text to be acquired from the system 
    //  or from the supplied module handle.
    //

    if(dwBufferLength = FormatMessageA(
        dwFormatFlags,
        hModule, // module to get message from (NULL == system)
        dwLastError,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // default language
        (LPSTR) &MessageBuffer,
        0,
        NULL
        ))
    {
        DWORD dwBytesWritten;

        //
        // Output message string on stderr.
        //
        WriteFile(
            GetStdHandle(STD_ERROR_HANDLE),
            MessageBuffer,
            dwBufferLength,
            &dwBytesWritten,
            NULL
            );

        //
        // Free the buffer allocated by the system.
        //
        LocalFree(MessageBuffer);
    }

    //
    // If we loaded a message source, unload it.
    //
    if(hModule != NULL)
        FreeLibrary(hModule);
}
```



Dopo aver compilato il programma, è possibile inserire il numero di codice dell'errore come argomento e il programma visualizzerà il testo. Ad esempio:

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 