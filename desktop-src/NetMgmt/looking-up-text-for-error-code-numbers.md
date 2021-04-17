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
# <a name="looking-up-text-for-error-code-numbers"></a><span data-ttu-id="480fa-104">Ricerca di testo per i numeri di codice di errore</span><span class="sxs-lookup"><span data-stu-id="480fa-104">Looking Up Text for Error Code Numbers</span></span>

<span data-ttu-id="480fa-105">A volte è necessario visualizzare il testo dell'errore associato ai codici di errore restituiti dalle funzioni correlate alla rete.</span><span class="sxs-lookup"><span data-stu-id="480fa-105">It is sometimes necessary to display error text associated with error codes returned from networking-related functions.</span></span> <span data-ttu-id="480fa-106">Potrebbe essere necessario eseguire questa attività con le funzioni di gestione della rete fornite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="480fa-106">You may need to perform this task with the network management functions provided by the system.</span></span>

<span data-ttu-id="480fa-107">Il testo dell'errore per questi messaggi è disponibile nel file della tabella dei messaggi denominato Netmsg.dll, disponibile in% SystemRoot% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="480fa-107">The error text for these messages is found in the message table file named Netmsg.dll, which is found in %systemroot%\\system32.</span></span> <span data-ttu-id="480fa-108">Questo file contiene messaggi di errore compresi nell'intervallo NERR \_ base (2100) fino al numero massimo di \_ NERR (Nerr \_ base + 899).</span><span class="sxs-lookup"><span data-stu-id="480fa-108">This file contains error messages in the range NERR\_BASE (2100) through MAX\_NERR(NERR\_BASE+899).</span></span> <span data-ttu-id="480fa-109">Questi codici di errore sono definiti nel file di intestazione SDK Lmerr. h.</span><span class="sxs-lookup"><span data-stu-id="480fa-109">These error codes are defined in the SDK header file lmerr.h.</span></span>

<span data-ttu-id="480fa-110">Le funzioni [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) possono caricare Netmsg.dll.</span><span class="sxs-lookup"><span data-stu-id="480fa-110">The [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) functions can load Netmsg.dll.</span></span> <span data-ttu-id="480fa-111">La funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) esegue il mapping di un codice di errore al testo del messaggio, dato un handle del modulo al file Netmsg.dll.</span><span class="sxs-lookup"><span data-stu-id="480fa-111">The [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function maps an error code to message text, given a module handle to the Netmsg.dll file.</span></span>

<span data-ttu-id="480fa-112">Nell'esempio seguente viene illustrato come visualizzare il testo dell'errore associato alle funzioni di gestione della rete, oltre a visualizzare il testo dell'errore associato ai codici di errore relativi al sistema.</span><span class="sxs-lookup"><span data-stu-id="480fa-112">The following sample illustrates how to display error text associated with network management functions, in addition to displaying error text associated with system-related error codes.</span></span> <span data-ttu-id="480fa-113">Se il numero di errore specificato è compreso in un intervallo specifico, il modulo del messaggio netmsg.dll viene caricato e utilizzato per cercare il numero di errore specificato con la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) .</span><span class="sxs-lookup"><span data-stu-id="480fa-113">If the supplied error number is in a specific range, the netmsg.dll message module is loaded and used to look up the specified error number with the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function.</span></span>


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



<span data-ttu-id="480fa-114">Dopo aver compilato il programma, è possibile inserire il numero di codice dell'errore come argomento e il programma visualizzerà il testo.</span><span class="sxs-lookup"><span data-stu-id="480fa-114">After you compile this program, you can insert the error code number as an argument and the program will display the text.</span></span> <span data-ttu-id="480fa-115">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="480fa-115">For example:</span></span>

``` syntax
C:\> netmsg 2453
Could not find domain controller for this domain
```

 

 